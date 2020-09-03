---
title: Logowanie się w programie Azure PowerShell
description: Jak zalogować się w programie Azure PowerShell jako użytkownik albo za pomocą jednostki usługi lub tożsamości zarządzanych dla zasobów platformy Azure.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/18/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 10deb367456574a29b5b9c301e0e1a6b10d95c14
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241478"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="f013c-103">Logowanie się w programie Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f013c-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="f013c-104">Program Azure PowerShell obsługuje kilka metod uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="f013c-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="f013c-105">Najprostszym sposobem na rozpoczęcie pracy jest usługa [Azure Cloud Shell](/azure/cloud-shell/overview), która loguje Cię automatycznie.</span><span class="sxs-lookup"><span data-stu-id="f013c-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="f013c-106">W przypadku instalacji lokalnej możesz logować się interaktywnie za pośrednictwem przeglądarki.</span><span class="sxs-lookup"><span data-stu-id="f013c-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="f013c-107">Podczas pisania skryptów automatyzacji zalecanym rozwiązaniem jest użycie [jednostki usługi](create-azure-service-principal-azureps.md) z odpowiednimi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="f013c-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="f013c-108">Możliwie największe ograniczenie uprawnień logowania w danym przypadku użycia pomaga w zabezpieczeniu zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f013c-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="f013c-109">Po zalogowaniu się polecenia są uruchamiane względem subskrypcji domyślnej.</span><span class="sxs-lookup"><span data-stu-id="f013c-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="f013c-110">Aby zmienić aktywną subskrypcję dla sesji, użyj polecenia cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="f013c-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="f013c-111">Aby zmienić domyślną subskrypcję używaną podczas logowania się przy użyciu programu Azure PowerShell, użyj polecenia [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span><span class="sxs-lookup"><span data-stu-id="f013c-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f013c-112">Poświadczenia są współdzielone w ramach wielu sesji programu PowerShell, dopóki użytkownik pozostanie zalogowany.</span><span class="sxs-lookup"><span data-stu-id="f013c-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="f013c-113">Aby uzyskać więcej informacji, zobacz artykuł dotyczący [poświadczeń trwałych](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="f013c-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="f013c-114">Logowanie interakcyjne</span><span class="sxs-lookup"><span data-stu-id="f013c-114">Sign in interactively</span></span>

<span data-ttu-id="f013c-115">Aby zalogować się interakcyjnie, skorzystaj z polecenia cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="f013c-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="f013c-116">W przypadku uruchomienia w programie PowerShell w wersji 6 lub nowszej to polecenie cmdlet przedstawia ciąg tokenu.</span><span class="sxs-lookup"><span data-stu-id="f013c-116">When run from PowerShell version 6 and higher, this cmdlet presents a token string.</span></span> <span data-ttu-id="f013c-117">Aby się zalogować, skopiuj ten ciąg i wklej go w witrynie [microsoft.com/devicelogin](https://microsoft.com/devicelogin) otwartej w przeglądarce internetowej.</span><span class="sxs-lookup"><span data-stu-id="f013c-117">To sign in, copy this string and paste it into [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in a web browser.</span></span> <span data-ttu-id="f013c-118">Sesja programu PowerShell zostanie uwierzytelniona na potrzeby połączenia z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f013c-118">Your PowerShell session will be authenticated to connect to Azure.</span></span> <span data-ttu-id="f013c-119">Możesz podać parametr `UseDeviceAuthentication`, aby otrzymać ciąg tokenu w programie Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f013c-119">You can specify the `UseDeviceAuthentication` parameter to receive a token string on Windows PowerShell.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f013c-120">Autoryzacja poświadczenia nazwy użytkownika/hasła została usunięta z programu Azure PowerShell z powodu zmian implementacji autoryzacji usługi Active Directory i zagadnień związanych z bezpieczeństwem.</span><span class="sxs-lookup"><span data-stu-id="f013c-120">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span> <span data-ttu-id="f013c-121">Jeśli używasz autoryzacji poświadczeń do celów automatyzacji, w zamian [utwórz jednostkę usługi](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="f013c-121">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="f013c-122">Za pomocą polecenia cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext) zapisz identyfikator dzierżawy w zmiennej na potrzeby użycia w następnych dwóch sekcjach tego artykułu.</span><span class="sxs-lookup"><span data-stu-id="f013c-122">Use the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet to store your tenant ID in a variable to be used in the next two sections of this article.</span></span>

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="f013c-123">Logowanie za pomocą jednostki usługi <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="f013c-123">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="f013c-124">Jednostki usługi to nieinterakcyjne konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f013c-124">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="f013c-125">Podobnie jak w przypadku innych kont użytkownika, ich uprawnieniami zarządza się za pomocą usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f013c-125">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="f013c-126">Udzielając jednostce usługi tylko potrzebnych uprawnień, możesz zapewnić bezpieczeństwo skryptom automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f013c-126">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="f013c-127">Aby dowiedzieć się, jak utworzyć jednostkę usługi do użycia z programem Azure PowerShell, zobacz [Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="f013c-127">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="f013c-128">Aby zalogować się przy użyciu jednostki usługi, podaj argument `-ServicePrincipal` w poleceniu cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="f013c-128">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="f013c-129">Z jednostką usługi trzeba będzie również skojarzyć jej identyfikator aplikacji, poświadczenia logowania oraz identyfikator dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="f013c-129">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="f013c-130">Sposób logowania przy użyciu jednostki usługi zależy od tego, czy została ona skonfigurowana do uwierzytelniania opartego na hasłach, czy opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="f013c-130">How you sign in with a service principal depends on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="f013c-131">Uwierzytelnianie oparte na hasłach</span><span class="sxs-lookup"><span data-stu-id="f013c-131">Password-based authentication</span></span>

<span data-ttu-id="f013c-132">Utwórz jednostkę usługi na potrzeby użycia w przykładach w tej sekcji.</span><span class="sxs-lookup"><span data-stu-id="f013c-132">Create a service principal to be used in the examples in this section.</span></span> <span data-ttu-id="f013c-133">Aby uzyskać więcej informacji na temat tworzenia jednostek usługi, zobacz [Tworzenie jednostki usługi platformy Azure przy użyciu programu Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span><span class="sxs-lookup"><span data-stu-id="f013c-133">For more information on creating service principals, see [Create an Azure service principal with Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="f013c-134">Aby pobrać poświadczenia jednostki usługi jako odpowiedni obiekt, użyj polecenia cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="f013c-134">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="f013c-135">To polecenie cmdlet wyświetla monit o podanie nazwy użytkownika i hasła.</span><span class="sxs-lookup"><span data-stu-id="f013c-135">This cmdlet presents a prompt for a username and password.</span></span> <span data-ttu-id="f013c-136">Podaj wartość `applicationID` jednostki usługi jako nazwę użytkownika i przekonwertuj jej wartość `secret` na zwykły tekst w celu uzyskania hasła.</span><span class="sxs-lookup"><span data-stu-id="f013c-136">Use the service principal's `applicationID` for the username and convert its `secret` to plain text for the password.</span></span>

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="f013c-137">Dla scenariuszy automatyzacji musisz utworzyć poświadczenia na podstawie wartości `applicationId` i `secret` jednostki usługi:</span><span class="sxs-lookup"><span data-stu-id="f013c-137">For automation scenarios, you need to create credentials from a service principal's `applicationId` and `secret`:</span></span>

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="f013c-138">Upewnij się, że podczas automatyzowania połączeń jednostki usługi używasz najlepszych rozwiązań dotyczących magazynu haseł.</span><span class="sxs-lookup"><span data-stu-id="f013c-138">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="f013c-139">Uwierzytelnianie oparte na certyfikacie</span><span class="sxs-lookup"><span data-stu-id="f013c-139">Certificate-based authentication</span></span>

<span data-ttu-id="f013c-140">Uwierzytelnianie oparte na certyfikatach wymaga, aby program Azure PowerShell mógł pobierać informacje z lokalnego magazynu certyfikatów na podstawie na odcisku palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f013c-140">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="f013c-141">Jeśli zamiast zarejestrowanej aplikacji używasz jednostki usługi, dodaj argument `-ServicePrincipal` i podaj identyfikator aplikacji jednostki usługi jako wartość parametru `-ApplicationId`.</span><span class="sxs-lookup"><span data-stu-id="f013c-141">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="f013c-142">W programie PowerShell 5.1 zarządzanie magazynem certyfikatów i jego badanie może odbywać się za pomocą modułu infrastruktury [PKI](/powershell/module/pkiclient).</span><span class="sxs-lookup"><span data-stu-id="f013c-142">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="f013c-143">Dla programu PowerShell Core w wersji 6.x i późniejszych proces jest bardziej skomplikowany.</span><span class="sxs-lookup"><span data-stu-id="f013c-143">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="f013c-144">Poniższe skrypty pokazują, jak zaimportować istniejący certyfikat do magazynu certyfikatów dostępnego w programie PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f013c-144">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="f013c-145">Importowanie certyfikatu w programie PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f013c-145">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="f013c-146">Importowanie certyfikatu w programie PowerShell Core w wersji 6.x lub nowszej</span><span class="sxs-lookup"><span data-stu-id="f013c-146">Import a certificate in PowerShell Core 6.x and later</span></span>

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation)
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag)
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite)
$store.Add($Certificate)
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="f013c-147">Logowanie się przy użyciu tożsamości zarządzanej</span><span class="sxs-lookup"><span data-stu-id="f013c-147">Sign in using a managed identity</span></span>

<span data-ttu-id="f013c-148">Tożsamości zarządzane to funkcja w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f013c-148">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="f013c-149">Tożsamości zarządzane to jednostki usługi przypisane do zasobów, które działają na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f013c-149">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="f013c-150">Jednostki usługi tożsamości zarządzanej można używać do logowania się i uzyskiwania aplikacyjnego tokenu dostępu do uzyskania dostępu do innych zasobów.</span><span class="sxs-lookup"><span data-stu-id="f013c-150">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="f013c-151">Tożsamości zarządzane są dostępne tylko w przypadku zasobów działających w chmurze platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f013c-151">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="f013c-152">Ten przykład nawiązuje połączenie przy użyciu tożsamości zarządzanej środowiska hosta.</span><span class="sxs-lookup"><span data-stu-id="f013c-152">This example connects using the managed identity of the host environment.</span></span> <span data-ttu-id="f013c-153">Na przykład w przypadku wykonania na maszynie wirtualnej z przypisaną tożsamością usługi zarządzanej umożliwia kodowi logowanie się przy użyciu tej przypisanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="f013c-153">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="f013c-154">Logowanie się przy użyciu innej niż domyślnej dzierżawy lub jako dostawca rozwiązań w chmurze (CSP, Cloud Solution Provider)</span><span class="sxs-lookup"><span data-stu-id="f013c-154">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="f013c-155">Jeśli konto jest skojarzone z więcej niż jedną dzierżawą, logowanie wymaga podania parametru `-Tenant` podczas nawiązywania połączenia.</span><span class="sxs-lookup"><span data-stu-id="f013c-155">If your account is associated with more than one tenant, sign-in requires the `-Tenant` parameter to be specified when connecting.</span></span> <span data-ttu-id="f013c-156">Ten parametr działa z każdą metodą logowania.</span><span class="sxs-lookup"><span data-stu-id="f013c-156">This parameter works with any sign-in method.</span></span> <span data-ttu-id="f013c-157">Podczas logowania się wartość tego parametru może być identyfikatorem obiektu platformy Azure dzierżawy (identyfikatorem dzierżawy) lub w pełni kwalifikowaną nazwą domeny dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="f013c-157">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="f013c-158">Jeśli jesteś [dostawcą rozwiązań w chmurze (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), wartość `-Tenant`**musi** być identyfikatorem dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="f013c-158">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="f013c-159">Logowanie się do innej chmury</span><span class="sxs-lookup"><span data-stu-id="f013c-159">Sign in to another Cloud</span></span>

<span data-ttu-id="f013c-160">Usługi w chmurze platformy Azure oferują środowiska zgodne z regionalnymi przepisami dotyczącymi obsługi danych.</span><span class="sxs-lookup"><span data-stu-id="f013c-160">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="f013c-161">W przypadku kont w chmurze regionalnej określ środowisko po zalogowaniu się, używając argumentu `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="f013c-161">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span> <span data-ttu-id="f013c-162">Ten parametr działa z każdą metodą logowania.</span><span class="sxs-lookup"><span data-stu-id="f013c-162">This parameter works with any sign-in method.</span></span> <span data-ttu-id="f013c-163">Na przykład jeśli Twoje konto znajduje się w chmurze w Chinach:</span><span class="sxs-lookup"><span data-stu-id="f013c-163">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="f013c-164">Następujące polecenie pozwala uzyskać listę dostępnych środowisk:</span><span class="sxs-lookup"><span data-stu-id="f013c-164">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
