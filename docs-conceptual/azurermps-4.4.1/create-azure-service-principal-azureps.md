---
title: Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell
description: Dowiedz się, jak utworzyć jednostkę usługi dla swojej aplikacji lub usługi za pomocą programu Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 6eda2d2a729331b212938aa2681d0188a25b734a
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/08/2018
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="9f000-104">Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9f000-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="9f000-105">Jeśli planujesz zarządzanie swoją aplikacją lub usługą za pomocą programu Azure PowerShell, musisz uruchomić go w ramach jednostki usługi Azure Active Directory (AAD), a nie przy użyciu własnych poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="9f000-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="9f000-106">W tym temacie przedstawiono kroki umożliwiające utworzenie podmiotu zabezpieczeń za pomocą programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9f000-106">This topic steps you through creating a security principal with Azure PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="9f000-107">Za pośrednictwem witryny Azure Portal możesz również utworzyć jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="9f000-107">You can also create a service principal through the Azure portal.</span></span> <span data-ttu-id="9f000-108">Aby uzyskać więcej szczegółów, przeczytaj artykuł [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) (Używanie portalu do tworzenia aplikacji usługi Active Directory i jednostki usługi używanej do uzyskiwania dostępu do zasobów).</span><span class="sxs-lookup"><span data-stu-id="9f000-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="9f000-109">Co to jest „jednostka usługi”?</span><span class="sxs-lookup"><span data-stu-id="9f000-109">What is a 'service principal'?</span></span>

<span data-ttu-id="9f000-110">Jednostka usługi platformy Azure to tożsamość zabezpieczeń używana przez aplikacje, usługi i narzędzia automatyzacji utworzone przez użytkownika w celu uzyskania dostępu do określonych zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9f000-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="9f000-111">Można ją traktować jako „tożsamość użytkownika” (nazwa logowania i hasło lub certyfikat) z określoną rolą i ściśle kontrolowanymi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="9f000-111">Think of it as a 'user identity' (username and password or certificate) with a specific role, and tightly controlled permissions.</span></span> <span data-ttu-id="9f000-112">Musi ona mieć możliwość wykonywania tylko konkretnych czynności w odróżnieniu od ogólnej tożsamości użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9f000-112">It only needs to be able to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="9f000-113">Nazwa główna usługi pozwala poprawić bezpieczeństwo, jeśli przyznasz jej tylko minimalny poziom uprawnień potrzebny do wykonywania zadań zarządzania.</span><span class="sxs-lookup"><span data-stu-id="9f000-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="9f000-114">Sprawdzenie własnego poziomu uprawnień</span><span class="sxs-lookup"><span data-stu-id="9f000-114">Verify your own permission level</span></span>

<span data-ttu-id="9f000-115">Po pierwsze, musisz mieć wystarczające uprawnienia zarówno w usłudze Azure Active Directory, jak i subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9f000-115">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="9f000-116">W szczególności musisz mieć możliwość tworzenia aplikacji w usłudze Active Directory i przypisywania roli do jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="9f000-116">Specifically, you must be able to create an app in the Active Directory, and assign a role to the service principal.</span></span>

<span data-ttu-id="9f000-117">Najłatwiejszym sposobem sprawdzenia, czy Twoje konto ma odpowiednie uprawnienia, jest skorzystanie z portalu.</span><span class="sxs-lookup"><span data-stu-id="9f000-117">The easiest way to check whether your account has adequate permissions is through the portal.</span></span> <span data-ttu-id="9f000-118">Zobacz [Sprawdzanie wymaganego uprawnienia w portalu](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="9f000-118">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="9f000-119">Tworzenie jednostki usługi dla aplikacji</span><span class="sxs-lookup"><span data-stu-id="9f000-119">Create a service principal for your app</span></span>

<span data-ttu-id="9f000-120">Po zalogowaniu się na koncie platformy Azure można utworzyć jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="9f000-120">Once you are signed into your Azure account, you can create the service principal.</span></span> <span data-ttu-id="9f000-121">Aby zidentyfikować wdrożoną aplikację, musisz użyć jednej z następujących metod:</span><span class="sxs-lookup"><span data-stu-id="9f000-121">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="9f000-122">Unikatowa nazwa wdrożonej aplikacji, na przykład „MyDemoWebApp” w poniższych przykładach, lub</span><span class="sxs-lookup"><span data-stu-id="9f000-122">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples, or</span></span>
* <span data-ttu-id="9f000-123">Identyfikator aplikacji, unikatowy identyfikator GUID skojarzony z wdrożoną aplikacją, usługą lub obiektem</span><span class="sxs-lookup"><span data-stu-id="9f000-123">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="9f000-124">Pobieranie informacji o aplikacji</span><span class="sxs-lookup"><span data-stu-id="9f000-124">Get information about your application</span></span>

<span data-ttu-id="9f000-125">Aby znaleźć informacje o aplikacji, można użyć polecenia cmdlet `Get-AzureRmADApplication`.</span><span class="sxs-lookup"><span data-stu-id="9f000-125">The `Get-AzureRmADApplication` cmdlet can be used to discover information about your application.</span></span>

```powershell
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```
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

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="9f000-126">Tworzenie jednostki usługi dla aplikacji</span><span class="sxs-lookup"><span data-stu-id="9f000-126">Create a service principal for your application</span></span>

<span data-ttu-id="9f000-127">Do utworzenia jednostki usługi służy polecenie cmdlet `New-AzureRmADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="9f000-127">The `New-AzureRmADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```powershell
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $password
```

```
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="9f000-128">Pobieranie informacji o jednostce usługi</span><span class="sxs-lookup"><span data-stu-id="9f000-128">Get information about the service principal</span></span>

```powershell
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="9f000-129">Logowanie za pomocą jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="9f000-129">Sign in using the service principal</span></span>

<span data-ttu-id="9f000-130">Możesz teraz zalogować się w ramach nowej jednostki usługi dla aplikacji przy użyciu podanych opcji *appId* i *password*.</span><span class="sxs-lookup"><span data-stu-id="9f000-130">You can now sign in as the new service principal for your app using the *appId* and *password* you provided.</span></span> <span data-ttu-id="9f000-131">Musisz podać identyfikator dzierżawy dla swojego konta.</span><span class="sxs-lookup"><span data-stu-id="9f000-131">You need to supply the Tenant Id for your account.</span></span> <span data-ttu-id="9f000-132">Identyfikator dzierżawy jest wyświetlany po zalogowaniu się do platformy Azure przy użyciu osobistych poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="9f000-132">Your Tenant Id is displayed when you sign into Azure with your personal credentials.</span></span>

```powershell
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Login-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="9f000-133">Uruchom to polecenie w nowej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9f000-133">Run this command from a new PowerShell session.</span></span> <span data-ttu-id="9f000-134">Po pomyślnym zalogowaniu zostaną wyświetlone dane wyjściowe, wyglądające mniej więcej tak:</span><span class="sxs-lookup"><span data-stu-id="9f000-134">After a successfully signing on you see output something like this:</span></span>

```
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="9f000-135">Gratulacje!</span><span class="sxs-lookup"><span data-stu-id="9f000-135">Congratulations!</span></span> <span data-ttu-id="9f000-136">Możesz użyć tych poświadczeń do uruchomienia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9f000-136">You can use these credentials to run your app.</span></span> <span data-ttu-id="9f000-137">Następnie musisz dostosować uprawnienia jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="9f000-137">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="9f000-138">Zarządzanie rolami</span><span class="sxs-lookup"><span data-stu-id="9f000-138">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="9f000-139">Kontrola dostępu oparta na rolach (RBAC) platformy Azure to model definiowania ról użytkowników i jednostek usługi oraz zarządzania nimi.</span><span class="sxs-lookup"><span data-stu-id="9f000-139">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="9f000-140">Role mają skojarzone ze sobą zestawy uprawnień umożliwiające wskazanie zasobów, które nazwa główna może odczytywać, zapisywać, do których może uzyskać dostęp lub którymi może zarządzać.</span><span class="sxs-lookup"><span data-stu-id="9f000-140">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="9f000-141">Aby uzyskać więcej informacji o rolach i kontroli dostępu opartej na rolach, zobacz [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles) (Kontrola dostępu oparta na rolach (RBAC): role wbudowane).</span><span class="sxs-lookup"><span data-stu-id="9f000-141">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="9f000-142">Program Azure PowerShell udostępnia następujące polecenia cmdlet do zarządzania przypisaniami ról:</span><span class="sxs-lookup"><span data-stu-id="9f000-142">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="9f000-143">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9f000-143">Get-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [<span data-ttu-id="9f000-144">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9f000-144">New-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [<span data-ttu-id="9f000-145">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9f000-145">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/remove-azurermroleassignment)

<span data-ttu-id="9f000-146">Rolą domyślną dla jednostki usługi jest **Współautor**.</span><span class="sxs-lookup"><span data-stu-id="9f000-146">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="9f000-147">Biorąc pod uwagę szerokie uprawnienia tej roli, jej użycie może nie być najlepszą opcją, w zależności od zakresu interakcji aplikacji z usługami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9f000-147">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="9f000-148">Rola **Czytelnik** jest bardziej restrykcyjna i jest dobrym wyborem dla aplikacji potrzebujących dostępu tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="9f000-148">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="9f000-149">Za pomocą witryny Azure Portal możesz wyświetlić szczegóły uprawnień specyficznych dla ról lub utworzyć niestandardowe uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="9f000-149">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="9f000-150">Zmienimy teraz poprzedni przykład — dodamy rolę **Czytelnik** i usuniemy rolę **Współautor**:</span><span class="sxs-lookup"><span data-stu-id="9f000-150">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```powershell
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```powershell
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="9f000-151">Aby wyświetlić obecnie przypisane role:</span><span class="sxs-lookup"><span data-stu-id="9f000-151">To view the current roles assigned:</span></span>

```powershell
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="9f000-152">Inne polecenia cmdlet programu Azure PowerShell umożliwiające zarządzania rolami:</span><span class="sxs-lookup"><span data-stu-id="9f000-152">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="9f000-153">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9f000-153">Get-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="9f000-154">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9f000-154">New-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="9f000-155">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9f000-155">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="9f000-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9f000-156">Set-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="9f000-157">Zmienianie poświadczeń podmiotu zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="9f000-157">Change the credentials of the security principal</span></span>

<span data-ttu-id="9f000-158">Dobrą praktyką w zakresie zabezpieczeń jest regularne sprawdzanie uprawnień i aktualizowanie haseł.</span><span class="sxs-lookup"><span data-stu-id="9f000-158">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="9f000-159">Warto też zarządzać poświadczeniami zabezpieczeń i modyfikować je w miarę wprowadzania zmian w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9f000-159">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="9f000-160">Można na przykład zmienić hasło jednostki usługi, tworząc nowe hasło i usuwając stare.</span><span class="sxs-lookup"><span data-stu-id="9f000-160">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="9f000-161">Dodawanie nowego hasła dla jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="9f000-161">Add a new password for the service principal</span></span>

```powershell
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="9f000-162">Pobieranie listy poświadczeń dla jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="9f000-162">Get a list of credentials for the service principal</span></span>

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="9f000-163">Usuwanie starego hasła dla jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="9f000-163">Remove the old password from the service principal</span></span>

```powershell
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="9f000-164">Sprawdzanie listy poświadczeń dla jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="9f000-164">Verify the list of credentials for the service principal</span></span>

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
