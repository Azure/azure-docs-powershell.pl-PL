---
title: Używanie jednostek usługi platformy Azure w programie Azure PowerShell
description: Dowiedz się, jak utworzyć jednostkę usługi i używać jej za pomocą programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.openlocfilehash: 9d1f0e3be894a592bdf105c2070e9db0cf882921
ms.sourcegitcommit: e324ad44921c9d8228ec7b91f3f8b333d2c520d4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/08/2020
ms.locfileid: "86127760"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="c2240-103">Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c2240-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="c2240-104">Zautomatyzowane narzędzia, które korzystają z usług platformy Azure, powinny zawsze mieć ograniczone uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="c2240-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="c2240-105">Zamiast wymagać, aby aplikacje logowały się jako użytkownik z pełnymi uprawnieniami, platforma Azure oferuje jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="c2240-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="c2240-106">Jednostka usługi platformy Azure to tożsamość przeznaczona do użycia z aplikacjami, usługami hostowanymi i zautomatyzowanymi narzędziami w celu uzyskiwania dostępu do zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2240-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="c2240-107">Ten dostęp jest ograniczony przez role przypisane do jednostki usługi, dzięki czemu możesz kontrolować, do których zasobów jest uzyskiwany dostęp i na jakim poziomie.</span><span class="sxs-lookup"><span data-stu-id="c2240-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="c2240-108">Ze względów bezpieczeństwa zawsze zaleca się używanie jednostek usługi ze zautomatyzowanymi narzędziami, zamiast zezwalać im na logowanie za pomocą tożsamości użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c2240-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="c2240-109">W tym artykule przedstawiono kroki tworzenia i resetowania jednostki usługi oraz uzyskiwania informacji o niej przy użyciu programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c2240-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="c2240-110">Tworzenie nazwy głównej usługi</span><span class="sxs-lookup"><span data-stu-id="c2240-110">Create a service principal</span></span>

<span data-ttu-id="c2240-111">Utwórz jednostkę usługi za pomocą polecenia cmdlet [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="c2240-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="c2240-112">Podczas tworzenia jednostki usługi wybierz używany przez nią typ uwierzytelniania logowania.</span><span class="sxs-lookup"><span data-stu-id="c2240-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
> <span data-ttu-id="c2240-113">Jeśli konto nie ma wystarczających uprawnień do utworzenia jednostki usługi, polecenie `New-AzADServicePrincipal` zwróci komunikat „Uprawnienia niewystarczające do ukończenia operacji”.</span><span class="sxs-lookup"><span data-stu-id="c2240-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation".</span></span>
> <span data-ttu-id="c2240-114">Skontaktuj się z administratorem usługi Azure Active Directory w celu utworzenia jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="c2240-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="c2240-115">Istnieją dwa typy uwierzytelniania dostępne dla jednostek usługi: Uwierzytelnianie oparte na hasłach i uwierzytelnianie oparte na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="c2240-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="c2240-116">Uwierzytelnianie oparte na hasłach</span><span class="sxs-lookup"><span data-stu-id="c2240-116">Password-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2240-117">Domyślna rola jednostki usługi uwierzytelniania opartego na hasłach to **Współautor**.</span><span class="sxs-lookup"><span data-stu-id="c2240-117">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="c2240-118">Ta rola ma pełne uprawnienia do odczytu i zapisu dla konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2240-118">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="c2240-119">Aby uzyskać informacje na temat zarządzania przypisaniami ról, zobacz [Zarządzanie rolami jednostki usługi](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="c2240-119">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="c2240-120">Jeśli żadne inne parametry uwierzytelniania nie istnieją, jest używane uwierzytelnianie oparte na hasłach i otrzymujesz hasło utworzone losowo.</span><span class="sxs-lookup"><span data-stu-id="c2240-120">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="c2240-121">Jeśli chcesz używać uwierzytelniania opartego na hasłach, ta metoda jest zalecana.</span><span class="sxs-lookup"><span data-stu-id="c2240-121">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="c2240-122">Zwrócony obiekt zawiera element członkowski `Secret`, który jest elementem `SecureString` zawierającym wygenerowane hasło.</span><span class="sxs-lookup"><span data-stu-id="c2240-122">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="c2240-123">Upewnij się, że ta wartość jest przechowywana w bezpiecznym miejscu, aby przeprowadzać uwierzytelnianie za pomocą jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="c2240-123">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="c2240-124">Wartość _nie_ będzie wyświetlana w danych wyjściowych konsoli.</span><span class="sxs-lookup"><span data-stu-id="c2240-124">Its value _won't_ be displayed in the console output.</span></span> <span data-ttu-id="c2240-125">W przypadku utraty hasła [zresetuj poświadczenia jednostki usługi](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="c2240-125">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="c2240-126">Następujący kod pozwala wyeksportować wpis tajny:</span><span class="sxs-lookup"><span data-stu-id="c2240-126">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="c2240-127">W przypadku haseł podawanych przez użytkowników argument `-PasswordCredential` przyjmuje obiekty `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`.</span><span class="sxs-lookup"><span data-stu-id="c2240-127">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="c2240-128">Te obiekty muszą mieć prawidłowe daty `StartDate` i `EndDate` oraz zawierać zwykły tekst typu `Password`.</span><span class="sxs-lookup"><span data-stu-id="c2240-128">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="c2240-129">Podczas tworzenia hasła upewnij się, że przestrzegasz [reguł i ograniczeń dotyczących haseł usługi Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="c2240-129">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span>
<span data-ttu-id="c2240-130">Nie używaj słabych haseł ani nie stosuj ponownie tych samych haseł.</span><span class="sxs-lookup"><span data-stu-id="c2240-130">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="c2240-131">Obiekt zwrócony przez polecenie `New-AzADServicePrincipal` zawiera elementy członkowskie `Id` i `DisplayName`. Każdego z nich można użyć do logowania przy użyciu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="c2240-131">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2240-132">Logowanie za pomocą jednostki usługi wymaga identyfikatora dzierżawy, w ramach którego utworzono jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="c2240-132">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="c2240-133">Aby pobrać dzierżawę aktywną w trakcie tworzenia jednostki usługi, uruchom następujące polecenie _natychmiast po_ utworzeniu jednostki usługi:</span><span class="sxs-lookup"><span data-stu-id="c2240-133">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a><span data-ttu-id="c2240-134">Uwierzytelnianie oparte na certyfikacie</span><span class="sxs-lookup"><span data-stu-id="c2240-134">Certificate-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2240-135">Podczas tworzenia jednostki usługi uwierzytelniania opartego na certyfikacie nie jest przypisywana rola domyślna.</span><span class="sxs-lookup"><span data-stu-id="c2240-135">There is no default role assigned when creating a certificate-based authentication service principal.</span></span> <span data-ttu-id="c2240-136">Aby uzyskać informacje na temat zarządzania przypisaniami ról, zobacz [Zarządzanie rolami jednostki usługi](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="c2240-136">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="c2240-137">Jednostki usługi używające uwierzytelniania opartego na certyfikatach są tworzone za pomocą parametru `-CertValue`.</span><span class="sxs-lookup"><span data-stu-id="c2240-137">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="c2240-138">Ten parametr przyjmuje ciąg ASCII szyfrowany przy użyciu algorytmu base64 z certyfikatu publicznego.</span><span class="sxs-lookup"><span data-stu-id="c2240-138">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="c2240-139">Jest on reprezentowany przez plik PEM lub plik CRT lub CER zakodowany jako tekst.</span><span class="sxs-lookup"><span data-stu-id="c2240-139">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="c2240-140">Kodowania plików binarnych certyfikatu publicznego nie są obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="c2240-140">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="c2240-141">W instrukcjach założono, że masz już dostępny certyfikat.</span><span class="sxs-lookup"><span data-stu-id="c2240-141">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="c2240-142">Możesz również użyć parametru `-KeyCredential`, który przyjmuje obiekty `PSADKeyCredential`.</span><span class="sxs-lookup"><span data-stu-id="c2240-142">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="c2240-143">Te obiekty muszą mieć prawidłowe daty `StartDate` i `EndDate` oraz element członkowski `CertValue` ustawiony na ciąg ASCII kodowany przy użyciu algorytmu base64 z certyfikatu publicznego.</span><span class="sxs-lookup"><span data-stu-id="c2240-143">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="c2240-144">Obiekt zwrócony przez polecenie `New-AzADServicePrincipal` zawiera elementy członkowskie `Id` i `DisplayName`. Każdego z nich można użyć do logowania przy użyciu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="c2240-144">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="c2240-145">Klienci logujący się przy użyciu jednostki usługi potrzebują również dostępu do klucza prywatnego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="c2240-145">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2240-146">Logowanie za pomocą jednostki usługi wymaga identyfikatora dzierżawy, w ramach którego utworzono jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="c2240-146">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="c2240-147">Aby pobrać dzierżawę aktywną w trakcie tworzenia jednostki usługi, uruchom następujące polecenie _natychmiast po_ utworzeniu jednostki usługi:</span><span class="sxs-lookup"><span data-stu-id="c2240-147">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="c2240-148">Uzyskiwanie istniejącej jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="c2240-148">Get an existing service principal</span></span>

<span data-ttu-id="c2240-149">Listę jednostek usługi dla aktywnej dzierżawy można pobrać przy użyciu polecenia [Get AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="c2240-149">A list of service principals for the active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="c2240-150">Domyślnie to polecenie zwraca _wszystkie_ jednostki usługi w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="c2240-150">By default this command returns _all_ service principals in a tenant.</span></span> <span data-ttu-id="c2240-151">Zwrócenie wyników w przypadku dużych organizacji może zająć dużo czasu.</span><span class="sxs-lookup"><span data-stu-id="c2240-151">For large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="c2240-152">Zamiast tego zaleca się użycie jednego z opcjonalnych argumentów filtrowania po stronie serwera:</span><span class="sxs-lookup"><span data-stu-id="c2240-152">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

- <span data-ttu-id="c2240-153">`-DisplayNameBeginsWith` żąda jednostek usługi, które mają _prefiks_ odpowiadający podanej wartości.</span><span class="sxs-lookup"><span data-stu-id="c2240-153">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="c2240-154">Nazwa wyświetlana jednostki usługi jest wartością ustawioną przy użyciu opcji `-DisplayName` podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="c2240-154">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
- <span data-ttu-id="c2240-155">`-DisplayName` żąda _dokładnego dopasowania_ nazwy jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="c2240-155">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="c2240-156">Zarządzanie rolami jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="c2240-156">Manage service principal roles</span></span>

<span data-ttu-id="c2240-157">Program Azure PowerShell oferuje następujące polecenia cmdlet do zarządzania przypisaniami ról:</span><span class="sxs-lookup"><span data-stu-id="c2240-157">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

- [<span data-ttu-id="c2240-158">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c2240-158">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
- [<span data-ttu-id="c2240-159">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c2240-159">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
- [<span data-ttu-id="c2240-160">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c2240-160">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="c2240-161">Domyślna rola jednostki usługi uwierzytelniania opartego na hasłach to **Współautor**.</span><span class="sxs-lookup"><span data-stu-id="c2240-161">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="c2240-162">Ta rola ma pełne uprawnienia do odczytu i zapisu dla konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2240-162">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="c2240-163">Rola **Czytelnik** jest bardziej restrykcyjna i zapewnia dostęp tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="c2240-163">The **Reader** role is more restrictive, with read-only access.</span></span> <span data-ttu-id="c2240-164">Aby uzyskać więcej informacji o rolach i kontroli dostępu opartej na rolach (RBAC), zobacz [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles) (Kontrola dostępu oparta na rolach: role wbudowane).</span><span class="sxs-lookup"><span data-stu-id="c2240-164">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="c2240-165">W tym przykładzie jest dodawana rola **Czytelnik** i usuwana rola **Współautor**:</span><span class="sxs-lookup"><span data-stu-id="c2240-165">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> <span data-ttu-id="c2240-166">Polecenia cmdlet przypisania roli nie przyjmują identyfikatora obiektu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="c2240-166">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="c2240-167">Przyjmują one identyfikator skojarzonej aplikacji, który jest generowany podczas tworzenia.</span><span class="sxs-lookup"><span data-stu-id="c2240-167">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="c2240-168">Aby uzyskać identyfikator aplikacji dla jednostki usługi, użyj polecenia `Get-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="c2240-168">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="c2240-169">Jeśli konto nie ma uprawnienia do przypisywania roli, zobaczysz komunikat o błędzie informujący, że Twoje konto „nie ma autoryzacji do wykonania akcji Microsoft.Authorization/roleAssignments/write”.</span><span class="sxs-lookup"><span data-stu-id="c2240-169">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'".</span></span> <span data-ttu-id="c2240-170">Skontaktuj się z administratorem usługi Azure Active Directory w celu zarządzania rolami.</span><span class="sxs-lookup"><span data-stu-id="c2240-170">Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="c2240-171">Dodanie roli _nie_ ogranicza wcześniej przypisanych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="c2240-171">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="c2240-172">Po ograniczeniu uprawnień jednostki usługi rola **Współautor** powinna zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="c2240-172">When restricting a service principal's permissions, the **Contributor** role should be removed.</span></span>

<span data-ttu-id="c2240-173">Zmiany można zweryfikować przez wyświetlenie listy przypisanych ról:</span><span class="sxs-lookup"><span data-stu-id="c2240-173">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="c2240-174">Logowanie za pomocą jednostki usługi</span><span class="sxs-lookup"><span data-stu-id="c2240-174">Sign in using a service principal</span></span>

<span data-ttu-id="c2240-175">Przetestuj poświadczenia i uprawnienia nowej jednostki usługi przez zalogowanie.</span><span class="sxs-lookup"><span data-stu-id="c2240-175">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="c2240-176">Do zalogowania się przy użyciu jednostki usługi potrzebujesz skojarzonej z nią wartości `applicationId`, a także dzierżawy, w ramach której została utworzona.</span><span class="sxs-lookup"><span data-stu-id="c2240-176">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="c2240-177">Aby zalogować się przy użyciu jednostki usługi używającej hasła:</span><span class="sxs-lookup"><span data-stu-id="c2240-177">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

<span data-ttu-id="c2240-178">Uwierzytelnianie oparte na certyfikatach wymaga, aby program Azure PowerShell mógł pobierać informacje z lokalnego magazynu certyfikatów na podstawie na odcisku palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="c2240-178">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <TenantId> -CertificateThumbprint <Thumbprint> -ApplicationId <ApplicationId>
```

<span data-ttu-id="c2240-179">Aby uzyskać instrukcje dotyczące importowania certyfikatu do magazynu poświadczeń dostępnego z programu PowerShell, zobacz [Logowanie się w programie Azure PowerShell](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="c2240-179">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="c2240-180">Resetowanie poświadczeń</span><span class="sxs-lookup"><span data-stu-id="c2240-180">Reset credentials</span></span>

<span data-ttu-id="c2240-181">Jeśli nie pamiętasz poświadczeń dla jednostki usługi, użyj polecenia [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential), aby dodać nowe poświadczenie z losowym hasłem.</span><span class="sxs-lookup"><span data-stu-id="c2240-181">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential with a random password.</span></span> <span data-ttu-id="c2240-182">To polecenie cmdlet nie obsługuje poświadczeń zdefiniowanych przez użytkownika podczas resetowania hasła.</span><span class="sxs-lookup"><span data-stu-id="c2240-182">This cmdlet does not support user-defined credentials when resetting the password.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2240-183">Przed przypisaniem nowych poświadczeń możesz usunąć istniejące poświadczenia, aby zapobiec logowaniu przy ich użyciu.</span><span class="sxs-lookup"><span data-stu-id="c2240-183">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="c2240-184">W tym celu użyj polecenia cmdlet [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="c2240-184">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a><span data-ttu-id="c2240-185">Rozwiązywanie problemów</span><span class="sxs-lookup"><span data-stu-id="c2240-185">Troubleshooting</span></span>

<span data-ttu-id="c2240-186">Jeśli zostanie wyświetlony błąd: _„New-AzADServicePrincipal: Istnieje już inny obiekt o tej samej wartości właściwości identifierUris”_ , upewnij się, że nie istnieje jednostka usługi o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="c2240-186">If you receive the error: _"New-AzADServicePrincipal: Another object with the same value for property identifierUris already exists."_, verify that a service principal with the same name doesn't already exist.</span></span>

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="c2240-187">Jeśli istniejąca jednostka usługi nie jest już potrzebna, możesz ją usunąć przy użyciu poniższego przykładu.</span><span class="sxs-lookup"><span data-stu-id="c2240-187">If the existing service principal is no longer needed, you can remove it using the following example.</span></span>

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="c2240-188">Ten błąd może wystąpić również wtedy, gdy wcześniej utworzono jednostkę usługi dla aplikacji usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c2240-188">This error can also occur when you've previously created a service principal for an Azure Active Directory application.</span></span> <span data-ttu-id="c2240-189">Po usunięciu jednostki usługi aplikacja będzie nadal dostępna.</span><span class="sxs-lookup"><span data-stu-id="c2240-189">If you remove the service principal, the application is still available.</span></span> <span data-ttu-id="c2240-190">Ta aplikacja uniemożliwia utworzenie innej jednostki usługi o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="c2240-190">This application prevents you from creating another service principal with the same name.</span></span>

<span data-ttu-id="c2240-191">Za pomocą następującego przykładu możesz się upewnić, że aplikacja usługi Azure Active Directory o tej samej nazwie nie istnieje:</span><span class="sxs-lookup"><span data-stu-id="c2240-191">You can use the following example to verify that an Azure Active Directory application with the same name doesn't exist:</span></span>

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="c2240-192">Jeśli aplikacja o tej samej nazwie istnieje i nie jest już potrzebna, możesz ją usunąć przy użyciu poniższego przykładu.</span><span class="sxs-lookup"><span data-stu-id="c2240-192">If an application with the same name does exist and is no longer needed, it can be removed using the following example.</span></span>

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="c2240-193">W przeciwnym razie wybierz alternatywną nazwę nowej jednostki usługi, którą próbujesz utworzyć.</span><span class="sxs-lookup"><span data-stu-id="c2240-193">Otherwise, choose an alternate name for the new service principal that you're attempting to create.</span></span>
