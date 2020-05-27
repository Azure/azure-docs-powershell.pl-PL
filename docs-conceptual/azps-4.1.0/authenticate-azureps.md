---
title: Logowanie się w programie Azure PowerShell
description: Jak zalogować się w programie Azure PowerShell jako użytkownik albo za pomocą jednostki usługi lub tożsamości zarządzanych dla zasobów platformy Azure.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/04/2019
ms.openlocfilehash: f0354c67295b425b03c9780bf76ffef11d477951
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/19/2020
ms.locfileid: "83631119"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="ef44c-103">Logowanie się w programie Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ef44c-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="ef44c-104">Program Azure PowerShell obsługuje kilka metod uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="ef44c-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="ef44c-105">Najprostszym sposobem na rozpoczęcie pracy jest usługa [Azure Cloud Shell](/azure/cloud-shell/overview), która loguje Cię automatycznie.</span><span class="sxs-lookup"><span data-stu-id="ef44c-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="ef44c-106">W przypadku instalacji lokalnej możesz logować się interaktywnie za pośrednictwem przeglądarki.</span><span class="sxs-lookup"><span data-stu-id="ef44c-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="ef44c-107">Podczas pisania skryptów automatyzacji zalecanym rozwiązaniem jest użycie [jednostki usługi](create-azure-service-principal-azureps.md) z odpowiednimi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="ef44c-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="ef44c-108">Możliwie największe ograniczenie uprawnień logowania w danym przypadku użycia pomaga w zabezpieczeniu zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ef44c-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="ef44c-109">Po zalogowaniu się polecenia są uruchamiane względem subskrypcji domyślnej.</span><span class="sxs-lookup"><span data-stu-id="ef44c-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="ef44c-110">Aby zmienić aktywną subskrypcję dla sesji, użyj polecenia cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="ef44c-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="ef44c-111">Aby zmienić domyślną subskrypcję używaną podczas logowania się przy użyciu programu Azure PowerShell, użyj polecenia [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span><span class="sxs-lookup"><span data-stu-id="ef44c-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ef44c-112">Poświadczenia są współdzielone w ramach wielu sesji programu PowerShell, dopóki użytkownik pozostanie zalogowany.</span><span class="sxs-lookup"><span data-stu-id="ef44c-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="ef44c-113">Aby uzyskać więcej informacji, zobacz artykuł dotyczący [poświadczeń trwałych](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="ef44c-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="ef44c-114">Logowanie interakcyjne</span><span class="sxs-lookup"><span data-stu-id="ef44c-114">Sign in interactively</span></span>

<span data-ttu-id="ef44c-115">Aby zalogować się interakcyjnie, skorzystaj z polecenia cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="ef44c-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="ef44c-116">Po uruchomieniu to polecenie cmdlet spowoduje wyświetlenie ciągu tokenu.</span><span class="sxs-lookup"><span data-stu-id="ef44c-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="ef44c-117">Aby się zalogować, skopiuj ten ciąg i wklej go w witrynie https://microsoft.com/devicelogin w przeglądarce.</span><span class="sxs-lookup"><span data-stu-id="ef44c-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="ef44c-118">Sesja programu PowerShell zostanie uwierzytelniona na potrzeby połączenia z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef44c-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ef44c-119">Autoryzacja poświadczenia nazwy użytkownika/hasła została usunięta z programu Azure PowerShell z powodu zmian implementacji autoryzacji usługi Active Directory i zagadnień związanych z bezpieczeństwem.</span><span class="sxs-lookup"><span data-stu-id="ef44c-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span>
> <span data-ttu-id="ef44c-120">Jeśli używasz autoryzacji poświadczeń do celów automatyzacji, w zamian [utwórz jednostkę usługi](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="ef44c-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="ef44c-121">Logowanie za pomocą jednostki usługi <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="ef44c-121">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="ef44c-122">Jednostki usługi to nieinterakcyjne konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ef44c-122">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="ef44c-123">Podobnie jak w przypadku innych kont użytkownika, ich uprawnieniami zarządza się za pomocą usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ef44c-123">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="ef44c-124">Udzielając jednostce usługi tylko potrzebnych uprawnień, możesz zapewnić bezpieczeństwo skryptom automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="ef44c-124">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="ef44c-125">Aby dowiedzieć się, jak utworzyć jednostkę usługi do użycia z programem Azure PowerShell, zobacz [Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="ef44c-125">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="ef44c-126">Aby zalogować się przy użyciu jednostki usługi, podaj argument `-ServicePrincipal` w poleceniu cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="ef44c-126">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="ef44c-127">Z jednostką usługi trzeba będzie również skojarzyć jej identyfikator aplikacji, poświadczenia logowania oraz identyfikator dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ef44c-127">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="ef44c-128">Sposób logowania przy użyciu jednostki usługi będzie zależeć od tego, czy została ona skonfigurowana do uwierzytelniania opartego na hasłach, czy opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="ef44c-128">How you sign in with a service principal will depend on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="ef44c-129">Uwierzytelnianie oparte na hasłach</span><span class="sxs-lookup"><span data-stu-id="ef44c-129">Password-based authentication</span></span>

<span data-ttu-id="ef44c-130">Aby pobrać poświadczenia jednostki usługi jako odpowiedni obiekt, użyj polecenia cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="ef44c-130">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="ef44c-131">To polecenie cmdlet wyświetli monit o podanie nazwy użytkownika i hasła.</span><span class="sxs-lookup"><span data-stu-id="ef44c-131">This cmdlet will present a prompt for a username and password.</span></span> <span data-ttu-id="ef44c-132">Użyj identyfikatora jednostki usługi w przypadku nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ef44c-132">Use the service principal ID for the username.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="ef44c-133">Dla scenariuszy automatyzacji musisz utworzyć poświadczenia na podstawie nazwy użytkownika i bezpiecznego ciągu:</span><span class="sxs-lookup"><span data-stu-id="ef44c-133">For automation scenarios, you need to create credentials from a user name and secure string:</span></span>

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="ef44c-134">Upewnij się, że podczas automatyzowania połączeń jednostki usługi używasz najlepszych rozwiązań dotyczących magazynu haseł.</span><span class="sxs-lookup"><span data-stu-id="ef44c-134">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="ef44c-135">Uwierzytelnianie oparte na certyfikacie</span><span class="sxs-lookup"><span data-stu-id="ef44c-135">Certificate-based authentication</span></span>

<span data-ttu-id="ef44c-136">Uwierzytelnianie oparte na certyfikatach wymaga, aby program Azure PowerShell mógł pobierać informacje z lokalnego magazynu certyfikatów na podstawie na odcisku palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="ef44c-136">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="ef44c-137">Jeśli zamiast zarejestrowanej aplikacji używasz jednostki usługi, dodaj argument `-ServicePrincipal` i podaj identyfikator aplikacji jednostki usługi jako wartość parametru `-ApplicationId`.</span><span class="sxs-lookup"><span data-stu-id="ef44c-137">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="ef44c-138">W programie PowerShell 5.1 zarządzanie magazynem certyfikatów i jego badanie może odbywać się za pomocą modułu infrastruktury [PKI](/powershell/module/pkiclient).</span><span class="sxs-lookup"><span data-stu-id="ef44c-138">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="ef44c-139">Dla programu PowerShell Core w wersji 6.x i późniejszych proces jest bardziej skomplikowany.</span><span class="sxs-lookup"><span data-stu-id="ef44c-139">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="ef44c-140">Poniższe skrypty pokazują, jak zaimportować istniejący certyfikat do magazynu certyfikatów dostępnego w programie PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ef44c-140">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="ef44c-141">Importowanie certyfikatu w programie PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ef44c-141">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="ef44c-142">Importowanie certyfikatu w programie PowerShell Core w wersji 6.x lub nowszej</span><span class="sxs-lookup"><span data-stu-id="ef44c-142">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="ef44c-143">Logowanie się przy użyciu tożsamości zarządzanej</span><span class="sxs-lookup"><span data-stu-id="ef44c-143">Sign in using a managed identity</span></span>

<span data-ttu-id="ef44c-144">Tożsamości zarządzane to funkcja w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ef44c-144">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="ef44c-145">Tożsamości zarządzane to jednostki usługi przypisane do zasobów, które działają na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ef44c-145">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="ef44c-146">Jednostki usługi tożsamości zarządzanej można używać do logowania się i uzyskiwania aplikacyjnego tokenu dostępu do uzyskania dostępu do innych zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef44c-146">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="ef44c-147">Tożsamości zarządzane są dostępne tylko w przypadku zasobów działających w chmurze platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ef44c-147">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="ef44c-148">To polecenie nawiązuje połączenie przy użyciu tożsamości zarządzanej środowiska hosta.</span><span class="sxs-lookup"><span data-stu-id="ef44c-148">This command connects using the managed identity of the host environment.</span></span> <span data-ttu-id="ef44c-149">Na przykład w przypadku wykonania na maszynie wirtualnej z przypisaną tożsamością usługi zarządzanej umożliwia kodowi logowanie się przy użyciu tej przypisanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ef44c-149">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity 
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="ef44c-150">Logowanie się przy użyciu innej niż domyślnej dzierżawy lub jako dostawca rozwiązań w chmurze (CSP, Cloud Solution Provider)</span><span class="sxs-lookup"><span data-stu-id="ef44c-150">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="ef44c-151">Jeśli konto jest skojarzone z więcej niż jedną dzierżawą, logowanie wymaga użycia parametru `-Tenant` podczas nawiązywania połączenia.</span><span class="sxs-lookup"><span data-stu-id="ef44c-151">If your account is associated with more than one tenant, sign-in requires the use of the `-Tenant` parameter when connecting.</span></span> <span data-ttu-id="ef44c-152">Ten parametr będzie współdziałać z każdą metodą logowania.</span><span class="sxs-lookup"><span data-stu-id="ef44c-152">This parameter will work with any sign-in method.</span></span> <span data-ttu-id="ef44c-153">Podczas logowania się wartość tego parametru może być identyfikatorem obiektu platformy Azure dzierżawy (identyfikatorem dzierżawy) lub w pełni kwalifikowaną nazwą domeny dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ef44c-153">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="ef44c-154">Jeśli jesteś [dostawcą rozwiązań w chmurze (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), wartość `-Tenant`**musi** być identyfikatorem dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ef44c-154">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="ef44c-155">Logowanie się do innej chmury</span><span class="sxs-lookup"><span data-stu-id="ef44c-155">Sign in to another Cloud</span></span>

<span data-ttu-id="ef44c-156">Usługi w chmurze platformy Azure oferują środowiska zgodne z regionalnymi przepisami dotyczącymi obsługi danych.</span><span class="sxs-lookup"><span data-stu-id="ef44c-156">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="ef44c-157">W przypadku kont w chmurze regionalnej określ środowisko po zalogowaniu się, używając argumentu `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="ef44c-157">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="ef44c-158">Ten parametr będzie współdziałać z każdą metodą logowania.</span><span class="sxs-lookup"><span data-stu-id="ef44c-158">This parameter will work with any sign-in method.</span></span> <span data-ttu-id="ef44c-159">Na przykład jeśli Twoje konto znajduje się w chmurze w Chinach:</span><span class="sxs-lookup"><span data-stu-id="ef44c-159">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="ef44c-160">Następujące polecenie pozwala uzyskać listę dostępnych środowisk:</span><span class="sxs-lookup"><span data-stu-id="ef44c-160">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```