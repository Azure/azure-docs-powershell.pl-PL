---
title: Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell
description: Dowiedz się, jak utworzyć jednostkę usługi dla swojej aplikacji lub usługi za pomocą programu Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 3e1c5ad280bdb29ce479dd0a478d0ed58237f969
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594959"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="1f244-104">Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1f244-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="1f244-105">Jeśli planujesz zarządzanie swoją aplikacją lub usługą za pomocą programu Azure PowerShell, musisz uruchomić go w ramach jednostki usługi Azure Active Directory (AAD), a nie przy użyciu własnych poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="1f244-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="1f244-106">W tym artykule przedstawiono kroki umożliwiające utworzenie podmiotu zabezpieczeń za pomocą programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1f244-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="1f244-107">Co to jest jednostka usługi?</span><span class="sxs-lookup"><span data-stu-id="1f244-107">What is a service principal?</span></span>

<span data-ttu-id="1f244-108">Jednostka usługi platformy Azure to tożsamość zabezpieczeń używana przez aplikacje, usługi i narzędzia automatyzacji utworzone przez użytkownika w celu uzyskania dostępu do określonych zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1f244-108">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="1f244-109">Jednostkom usług są przypisywane określone uprawnienia związane z ich zadaniami, co daje lepszą kontrolę nad bezpieczeństwem.</span><span class="sxs-lookup"><span data-stu-id="1f244-109">Service principals are assigned specific permissions related to their tasks, giving you better security control.</span></span> <span data-ttu-id="1f244-110">Różni się to od ogólnej tożsamości użytkownika, która zazwyczaj ma autoryzację do wprowadzania dowolnych zmian.</span><span class="sxs-lookup"><span data-stu-id="1f244-110">This is unlike a general user identity, which is usually authorized to make any changes.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="1f244-111">Sprawdzenie własnego poziomu uprawnień</span><span class="sxs-lookup"><span data-stu-id="1f244-111">Verify your own permission level</span></span>

<span data-ttu-id="1f244-112">Po pierwsze, musisz mieć wystarczające uprawnienia zarówno w usłudze Azure Active Directory, jak i subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1f244-112">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="1f244-113">Musisz mieć możliwość tworzenia aplikacji w usłudze Active Directory i przypisywania roli do jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="1f244-113">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="1f244-114">Najłatwiejszym sposobem sprawdzenia, czy Twoje konto ma odpowiednie uprawnienia, jest skorzystanie z portalu.</span><span class="sxs-lookup"><span data-stu-id="1f244-114">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="1f244-115">Zobacz [Sprawdzanie wymaganego uprawnienia w portalu](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="1f244-115">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="1f244-116">Tworzenie jednostki usługi dla aplikacji</span><span class="sxs-lookup"><span data-stu-id="1f244-116">Create a service principal for your app</span></span>

<span data-ttu-id="1f244-117">Po zalogowaniu się na koncie platformy Azure można utworzyć jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="1f244-117">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="1f244-118">Aby zidentyfikować wdrożoną aplikację, musisz użyć jednej z następujących metod:</span><span class="sxs-lookup"><span data-stu-id="1f244-118">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="1f244-119">Unikatowa nazwa wdrożonej aplikacji, na przykład „MyDemoWebApp” w poniższych przykładach</span><span class="sxs-lookup"><span data-stu-id="1f244-119">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples</span></span>
* <span data-ttu-id="1f244-120">Identyfikator aplikacji, unikatowy identyfikator GUID skojarzony z wdrożoną aplikacją, usługą lub obiektem</span><span class="sxs-lookup"><span data-stu-id="1f244-120">The Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="1f244-121">Pobieranie informacji o aplikacji</span><span class="sxs-lookup"><span data-stu-id="1f244-121">Get information about your application</span></span>

<span data-ttu-id="1f244-122">Aby uzyskać informacje o aplikacji, można użyć polecenia cmdlet `Get-AzADApplication`.</span><span class="sxs-lookup"><span data-stu-id="1f244-122">The `Get-AzADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
$app = Get-AzADApplication -DisplayNameStartWith MyDemoWebApp
$app
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="1f244-123">Tworzenie jednostki usługi dla aplikacji</span><span class="sxs-lookup"><span data-stu-id="1f244-123">Create a service principal for your application</span></span>

<span data-ttu-id="1f244-124">Do utworzenia jednostki usługi służy polecenie cmdlet `New-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="1f244-124">The `New-AzADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
$servicePrincipal = New-AzADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

<span data-ttu-id="1f244-125">Na tym etapie możesz bezpośrednio użyć właściwości `$servicePrincipal.Secret` jako argumentu polecenia `Connect-AzAccount` (zobacz „Logowanie za pomocą jednostki usługi”) lub przekonwertować ciąg `SecureString` na ciąg w postaci zwykłego tekstu:</span><span class="sxs-lookup"><span data-stu-id="1f244-125">From here, you can either directly use the `$servicePrincipal.Secret` property as an argument to `Connect-AzAccount` (see "Sign in using the service principal"), or you can convert this `SecureString` to a plain text string:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="1f244-126">Logowanie za pomocą jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="1f244-126">Sign in using the service principal</span></span>

<span data-ttu-id="1f244-127">Teraz możesz zalogować się w ramach nowej jednostki usługi dla aplikacji przy użyciu podanego identyfikatora `appId` i wartości `password`, którą</span><span class="sxs-lookup"><span data-stu-id="1f244-127">You can now sign in as the new service principal for your app using the `appId` you provided and `password` that was</span></span>  
<span data-ttu-id="1f244-128">wygenerowano.</span><span class="sxs-lookup"><span data-stu-id="1f244-128">generated.</span></span> <span data-ttu-id="1f244-129">Potrzebujesz także identyfikatora dzierżawy dla jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="1f244-129">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="1f244-130">Identyfikator dzierżawy jest wyświetlany po zalogowaniu się do platformy Azure przy użyciu osobistych poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="1f244-130">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="1f244-131">Aby zalogować się przy użyciu jednostki usługi, użyj tych poleceń:</span><span class="sxs-lookup"><span data-stu-id="1f244-131">To sign in with a service principal, use the commands:</span></span>

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="1f244-132">Po pomyślnym zalogowaniu się zostaną wyświetlone dane wyjściowe, takie jak:</span><span class="sxs-lookup"><span data-stu-id="1f244-132">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="1f244-133">Gratulacje!</span><span class="sxs-lookup"><span data-stu-id="1f244-133">Congratulations!</span></span> <span data-ttu-id="1f244-134">Możesz użyć tych poświadczeń do uruchomienia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f244-134">You can use these credentials to run your app.</span></span> <span data-ttu-id="1f244-135">Następnie musisz dostosować uprawnienia jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="1f244-135">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="1f244-136">Zarządzanie rolami</span><span class="sxs-lookup"><span data-stu-id="1f244-136">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="1f244-137">Kontrola dostępu oparta na rolach (RBAC) platformy Azure to model definiowania ról użytkowników i jednostek usługi oraz zarządzania nimi.</span><span class="sxs-lookup"><span data-stu-id="1f244-137">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="1f244-138">Role mają skojarzone ze sobą zestawy uprawnień umożliwiające wskazanie zasobów, które nazwa główna może odczytywać, zapisywać, do których może uzyskać dostęp lub którymi może zarządzać.</span><span class="sxs-lookup"><span data-stu-id="1f244-138">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="1f244-139">Aby uzyskać więcej informacji o rolach i kontroli dostępu opartej na rolach, zobacz [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles) (Kontrola dostępu oparta na rolach: role wbudowane).</span><span class="sxs-lookup"><span data-stu-id="1f244-139">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="1f244-140">Program Azure PowerShell udostępnia następujące polecenia cmdlet do zarządzania przypisaniami ról:</span><span class="sxs-lookup"><span data-stu-id="1f244-140">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="1f244-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1f244-141">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="1f244-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1f244-142">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="1f244-143">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1f244-143">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="1f244-144">Rolą domyślną dla jednostki usługi jest **Współautor**.</span><span class="sxs-lookup"><span data-stu-id="1f244-144">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="1f244-145">Biorąc pod uwagę szerokie uprawnienia tej roli, jej użycie może nie być najlepszą opcją, w zależności od zakresu interakcji aplikacji z usługami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1f244-145">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="1f244-146">Rola **Czytelnik** jest bardziej restrykcyjna i jest dobrym wyborem dla aplikacji potrzebujących dostępu tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="1f244-146">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="1f244-147">Za pomocą witryny Azure Portal możesz wyświetlić szczegóły uprawnień specyficznych dla ról lub utworzyć niestandardowe uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="1f244-147">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="1f244-148">Zmienimy teraz poprzedni przykład — dodamy rolę **Czytelnik** i usuniemy rolę **Współautor**:</span><span class="sxs-lookup"><span data-stu-id="1f244-148">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="1f244-149">Aby wyświetlić obecnie przypisane role:</span><span class="sxs-lookup"><span data-stu-id="1f244-149">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="1f244-150">Inne polecenia cmdlet programu Azure PowerShell umożliwiające zarządzania rolami:</span><span class="sxs-lookup"><span data-stu-id="1f244-150">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="1f244-151">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1f244-151">Get-AzRoleDefinition</span></span>](/powershell/module/az.resources/Get-azRoleDefinition)
* [<span data-ttu-id="1f244-152">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1f244-152">New-AzRoleDefinition</span></span>](/powershell/module/az.resources/New-azRoleDefinition)
* [<span data-ttu-id="1f244-153">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1f244-153">Remove-AzRoleDefinition</span></span>](/powershell/module/az.resources/Remove-azRoleDefinition)
* [<span data-ttu-id="1f244-154">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1f244-154">Set-AzRoleDefinition</span></span>](/powershell/module/az.resources/Set-azRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="1f244-155">Zmienianie poświadczeń podmiotu zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="1f244-155">Change the credentials of the security principal</span></span>

<span data-ttu-id="1f244-156">Dobrą praktyką w zakresie zabezpieczeń jest regularne sprawdzanie uprawnień i aktualizowanie haseł.</span><span class="sxs-lookup"><span data-stu-id="1f244-156">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="1f244-157">Warto też zarządzać poświadczeniami zabezpieczeń i modyfikować je w miarę wprowadzania zmian w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f244-157">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="1f244-158">Można na przykład zmienić hasło jednostki usługi, tworząc nowe hasło i usuwając stare.</span><span class="sxs-lookup"><span data-stu-id="1f244-158">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="1f244-159">Dodawanie nowego hasła dla jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="1f244-159">Add a new password for the service principal</span></span>

```azurepowershell-interactive
New-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="1f244-160">Pobieranie listy poświadczeń dla jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="1f244-160">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="1f244-161">Usuwanie starego hasła dla jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="1f244-161">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="1f244-162">Sprawdzanie listy poświadczeń dla jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="1f244-162">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="1f244-163">Pobieranie informacji o jednostce usługi</span><span class="sxs-lookup"><span data-stu-id="1f244-163">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
