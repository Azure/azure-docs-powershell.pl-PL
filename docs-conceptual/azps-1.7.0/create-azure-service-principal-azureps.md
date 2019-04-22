---
title: Używanie jednostek usługi platformy Azure w programie Azure PowerShell
description: Dowiedz się, jak utworzyć jednostkę usługi i używać jej za pomocą programu Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/20/2019
ms.openlocfilehash: 06116c7eb6ed848c9f369a3dd16f5e901e02afbe
ms.sourcegitcommit: ae4540a90508db73335a54408dfd6cdf3712a1e9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/18/2019
ms.locfileid: "59430622"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="51f1f-103">Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="51f1f-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="51f1f-104">Zautomatyzowane narzędzia, które korzystają z usług platformy Azure, powinny zawsze mieć ograniczone uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="51f1f-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="51f1f-105">Zamiast wymagać, aby aplikacje logowały się jako użytkownik z pełnymi uprawnieniami, platforma Azure oferuje jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="51f1f-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="51f1f-106">Jednostka usługi platformy Azure to tożsamość przeznaczona do użycia z aplikacjami, usługami hostowanymi i zautomatyzowanymi narzędziami w celu uzyskiwania dostępu do zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="51f1f-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="51f1f-107">Ten dostęp jest ograniczony przez role przypisane do jednostki usługi, dzięki czemu możesz kontrolować, do których zasobów jest uzyskiwany dostęp i na jakim poziomie.</span><span class="sxs-lookup"><span data-stu-id="51f1f-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="51f1f-108">Ze względów bezpieczeństwa zawsze zaleca się używanie jednostek usługi ze zautomatyzowanymi narzędziami, zamiast zezwalać im na logowanie za pomocą tożsamości użytkownika.</span><span class="sxs-lookup"><span data-stu-id="51f1f-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="51f1f-109">W tym artykule przedstawiono kroki tworzenia i resetowania jednostki usługi oraz uzyskiwania informacji o niej przy użyciu programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="51f1f-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="51f1f-110">Tworzenie nazwy głównej usługi</span><span class="sxs-lookup"><span data-stu-id="51f1f-110">Create a service principal</span></span>

<span data-ttu-id="51f1f-111">Utwórz jednostkę usługi za pomocą polecenia cmdlet [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="51f1f-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="51f1f-112">Podczas tworzenia jednostki usługi wybierz używany przez nią typ uwierzytelniania logowania.</span><span class="sxs-lookup"><span data-stu-id="51f1f-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="51f1f-113">Jeśli konto nie ma wystarczających uprawnień do utworzenia jednostki usługi, polecenie `New-AzADServicePrincipal` zwróci komunikat „Uprawnienia niewystarczające do ukończenia operacji”.</span><span class="sxs-lookup"><span data-stu-id="51f1f-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="51f1f-114">Skontaktuj się z administratorem usługi Azure Active Directory w celu utworzenia jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="51f1f-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="51f1f-115">Istnieją dwa typy uwierzytelniania dostępne dla jednostek usługi: Uwierzytelnianie oparte na hasłach i uwierzytelnianie oparte na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="51f1f-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="51f1f-116">Uwierzytelnianie oparte na hasłach</span><span class="sxs-lookup"><span data-stu-id="51f1f-116">Password-based authentication</span></span>

<span data-ttu-id="51f1f-117">Jeśli żadne inne parametry uwierzytelniania nie istnieją, jest używane uwierzytelnianie oparte na hasłach i otrzymujesz hasło utworzone losowo.</span><span class="sxs-lookup"><span data-stu-id="51f1f-117">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="51f1f-118">Jeśli chcesz używać uwierzytelniania opartego na hasłach, ta metoda jest zalecana.</span><span class="sxs-lookup"><span data-stu-id="51f1f-118">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="51f1f-119">Zwrócony obiekt zawiera element członkowski `Secret`, który jest elementem `SecureString` zawierającym wygenerowane hasło.</span><span class="sxs-lookup"><span data-stu-id="51f1f-119">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="51f1f-120">Upewnij się, że ta wartość jest przechowywana w bezpiecznym miejscu, aby przeprowadzać uwierzytelnianie za pomocą jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="51f1f-120">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="51f1f-121">Wartość __nie__ będzie wyświetlana w danych wyjściowych konsoli.</span><span class="sxs-lookup"><span data-stu-id="51f1f-121">Its value __won't__ be displayed in the console output.</span></span> <span data-ttu-id="51f1f-122">W przypadku utraty hasła [zresetuj poświadczenia jednostki usługi](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="51f1f-122">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span> 

<span data-ttu-id="51f1f-123">W przypadku haseł podawanych przez użytkowników argument `-PasswordCredential` przyjmuje obiekty `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`.</span><span class="sxs-lookup"><span data-stu-id="51f1f-123">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="51f1f-124">Te obiekty muszą mieć prawidłowe daty `StartDate` i `EndDate` oraz zawierać zwykły tekst typu `Password`.</span><span class="sxs-lookup"><span data-stu-id="51f1f-124">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="51f1f-125">Podczas tworzenia hasła upewnij się, że przestrzegasz [reguł i ograniczeń dotyczących haseł usługi Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="51f1f-125">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="51f1f-126">Nie używaj słabych haseł ani nie stosuj ponownie tych samych haseł.</span><span class="sxs-lookup"><span data-stu-id="51f1f-126">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="51f1f-127">Obiekt zwrócony przez polecenie `New-AzADServicePrincipal` zawiera elementy członkowskie `Id` i `DisplayName`. Każdego z nich można użyć do logowania przy użyciu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="51f1f-127">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="51f1f-128">Logowanie za pomocą jednostki usługi wymaga identyfikatora dzierżawy, w ramach którego utworzono jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="51f1f-128">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="51f1f-129">Aby pobrać dzierżawę aktywną w trakcie tworzenia jednostki usługi, uruchom następujące polecenie __natychmiast po__ utworzeniu jednostki usługi:</span><span class="sxs-lookup"><span data-stu-id="51f1f-129">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a><span data-ttu-id="51f1f-130">Uwierzytelnianie oparte na certyfikacie</span><span class="sxs-lookup"><span data-stu-id="51f1f-130">Certificate-based authentication</span></span>

<span data-ttu-id="51f1f-131">Jednostki usługi używające uwierzytelniania opartego na certyfikatach są tworzone za pomocą parametru `-CertValue`.</span><span class="sxs-lookup"><span data-stu-id="51f1f-131">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="51f1f-132">Ten parametr przyjmuje ciąg ASCII szyfrowany przy użyciu algorytmu base64 z certyfikatu publicznego.</span><span class="sxs-lookup"><span data-stu-id="51f1f-132">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="51f1f-133">Jest on reprezentowany przez plik PEM lub plik CRT lub CER zakodowany jako tekst.</span><span class="sxs-lookup"><span data-stu-id="51f1f-133">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="51f1f-134">Kodowania plików binarnych certyfikatu publicznego nie są obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="51f1f-134">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="51f1f-135">W instrukcjach założono, że masz już dostępny certyfikat.</span><span class="sxs-lookup"><span data-stu-id="51f1f-135">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="51f1f-136">Możesz również użyć parametru `-KeyCredential`, który przyjmuje obiekty `PSADKeyCredential`.</span><span class="sxs-lookup"><span data-stu-id="51f1f-136">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="51f1f-137">Te obiekty muszą mieć prawidłowe daty `StartDate` i `EndDate` oraz element członkowski `CertValue` ustawiony na ciąg ASCII kodowany przy użyciu algorytmu base64 z certyfikatu publicznego.</span><span class="sxs-lookup"><span data-stu-id="51f1f-137">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="51f1f-138">Obiekt zwrócony przez polecenie `New-AzADServicePrincipal` zawiera elementy członkowskie `Id` i `DisplayName`. Każdego z nich można użyć do logowania przy użyciu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="51f1f-138">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="51f1f-139">Klienci logujący się przy użyciu jednostki usługi potrzebują również dostępu do klucza prywatnego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="51f1f-139">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="51f1f-140">Logowanie za pomocą jednostki usługi wymaga identyfikatora dzierżawy, w ramach którego utworzono jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="51f1f-140">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="51f1f-141">Aby pobrać dzierżawę aktywną w trakcie tworzenia jednostki usługi, uruchom następujące polecenie __natychmiast po__ utworzeniu jednostki usługi:</span><span class="sxs-lookup"><span data-stu-id="51f1f-141">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="51f1f-142">Uzyskiwanie istniejącej jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="51f1f-142">Get an existing service principal</span></span>

<span data-ttu-id="51f1f-143">Listę jednostek usługi dla aktualnie aktywnej dzierżawy można pobrać przy użyciu polecenia [Get AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="51f1f-143">A list of service principals for the currently active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="51f1f-144">Domyślnie to polecenie zwraca __wszystkie__ jednostki usługi w dzierżawie, dlatego w przypadku dużych organizacji zwracanie wyników może potrwać dłużej.</span><span class="sxs-lookup"><span data-stu-id="51f1f-144">By default this command returns __all__ service principals in a tenant, so for large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="51f1f-145">Zamiast tego zaleca się użycie jednego z opcjonalnych argumentów filtrowania po stronie serwera:</span><span class="sxs-lookup"><span data-stu-id="51f1f-145">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

* <span data-ttu-id="51f1f-146">`-DisplayNameBeginsWith` żąda jednostek usługi, które mają _prefiks_ odpowiadający podanej wartości.</span><span class="sxs-lookup"><span data-stu-id="51f1f-146">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="51f1f-147">Nazwa wyświetlana jednostki usługi jest wartością ustawioną przy użyciu opcji `-DisplayName` podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="51f1f-147">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
* <span data-ttu-id="51f1f-148">`-DisplayName` żąda _dokładnego dopasowania_ nazwy jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="51f1f-148">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="51f1f-149">Zarządzanie rolami jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="51f1f-149">Manage service principal roles</span></span>

<span data-ttu-id="51f1f-150">Program Azure PowerShell oferuje następujące polecenia cmdlet do zarządzania przypisaniami ról:</span><span class="sxs-lookup"><span data-stu-id="51f1f-150">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="51f1f-151">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="51f1f-151">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="51f1f-152">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="51f1f-152">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="51f1f-153">Delete-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="51f1f-153">Delete-AzRoleAssignment</span></span>](/powershell/module/az.resources/delete-azroleassignment)

<span data-ttu-id="51f1f-154">Rolą domyślną dla jednostki usługi jest **Współautor**.</span><span class="sxs-lookup"><span data-stu-id="51f1f-154">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="51f1f-155">Ta rola ma pełne uprawnienia do odczytu i zapisu dla konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="51f1f-155">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="51f1f-156">Rola **Czytelnik** jest bardziej restrykcyjna i zapewnia dostęp tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="51f1f-156">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="51f1f-157">Aby uzyskać więcej informacji o rolach i kontroli dostępu opartej na rolach (RBAC), zobacz [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles) (Kontrola dostępu oparta na rolach: role wbudowane).</span><span class="sxs-lookup"><span data-stu-id="51f1f-157">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="51f1f-158">W tym przykładzie jest dodawana rola **Czytelnik** i usuwana rola **Współautor**:</span><span class="sxs-lookup"><span data-stu-id="51f1f-158">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Delete-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> <span data-ttu-id="51f1f-159">Polecenia cmdlet przypisania roli nie przyjmują identyfikatora obiektu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="51f1f-159">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="51f1f-160">Przyjmują one identyfikator skojarzonej aplikacji, który jest generowany podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="51f1f-160">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="51f1f-161">Aby uzyskać identyfikator aplikacji dla jednostki usługi, użyj polecenia `Get-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="51f1f-161">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="51f1f-162">Jeśli konto nie ma uprawnienia do przypisywania roli, zobaczysz komunikat o błędzie informujący, że Twoje konto „nie ma autoryzacji do wykonania akcji Microsoft.Authorization/roleAssignments/write”. Skontaktuj się z administratorem usługi Azure Active Directory w celu zarządzania rolami.</span><span class="sxs-lookup"><span data-stu-id="51f1f-162">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="51f1f-163">Dodanie roli _nie_ ogranicza wcześniej przypisanych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="51f1f-163">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="51f1f-164">Po ograniczeniu uprawnień jednostki usługi rola __Współautor__ powinna zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="51f1f-164">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="51f1f-165">Zmiany można zweryfikować przez wyświetlenie listy przypisanych ról:</span><span class="sxs-lookup"><span data-stu-id="51f1f-165">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="51f1f-166">Logowanie za pomocą jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="51f1f-166">Sign in using a service principal</span></span>

<span data-ttu-id="51f1f-167">Przetestuj poświadczenia i uprawnienia nowej jednostki usługi przez zalogowanie.</span><span class="sxs-lookup"><span data-stu-id="51f1f-167">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="51f1f-168">Do zalogowania się przy użyciu jednostki usługi potrzebujesz skojarzonej z nią wartości `applicationId`, a także dzierżawy, w ramach której została utworzona.</span><span class="sxs-lookup"><span data-stu-id="51f1f-168">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="51f1f-169">Aby zalogować się przy użyciu jednostki usługi używającej hasła:</span><span class="sxs-lookup"><span data-stu-id="51f1f-169">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

<span data-ttu-id="51f1f-170">Uwierzytelnianie oparte na certyfikatach wymaga, aby program Azure PowerShell mógł pobierać informacje z lokalnego magazynu certyfikatów na podstawie na odcisku palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="51f1f-170">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="51f1f-171">Aby uzyskać instrukcje dotyczące importowania certyfikatu do magazynu poświadczeń dostępnego z programu PowerShell, zobacz [Logowanie się w programie Azure PowerShell](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="51f1f-171">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="51f1f-172">Resetowanie poświadczeń</span><span class="sxs-lookup"><span data-stu-id="51f1f-172">Reset credentials</span></span>

<span data-ttu-id="51f1f-173">Jeśli nie pamiętasz poświadczeń dla jednostki usługi, użyj polecenia [New-AzADSpCredential](/module/az.resources/new-azadspcredential), aby dodać nowe poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="51f1f-173">If you forget the credentials for a service principal, use [New-AzADSpCredential](/module/az.resources/new-azadspcredential) to add a new credential.</span></span> <span data-ttu-id="51f1f-174">To polecenie cmdlet przyjmuje te same typy i argumenty poświadczeń i typy co polecenie `New-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="51f1f-174">This cmdlet takes the same credential arguments and types as `New-AzADServicePrincipal`.</span></span> <span data-ttu-id="51f1f-175">Jeśli nie ma argumentów poświadczeń, jest tworzony nowy element `PasswordCredential` z losowym hasłem.</span><span class="sxs-lookup"><span data-stu-id="51f1f-175">Without any credential arguments, a new `PasswordCredential` with a random password is created.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51f1f-176">Przed przypisaniem nowych poświadczeń możesz usunąć istniejące poświadczenia, aby zapobiec logowaniu przy ich użyciu.</span><span class="sxs-lookup"><span data-stu-id="51f1f-176">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="51f1f-177">W tym celu użyj polecenia cmdlet [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="51f1f-177">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -DisplayName ServicePrincipalName
```
