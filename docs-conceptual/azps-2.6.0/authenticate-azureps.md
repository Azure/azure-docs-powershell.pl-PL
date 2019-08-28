---
title: Logowanie się w programie Azure PowerShell
description: Jak zalogować się w programie Azure PowerShell jako użytkownik albo za pomocą jednostki usługi lub tożsamości zarządzanych dla zasobów platformy Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/20/2019
ms.openlocfilehash: 0b7a6fa4278d95a69b21f570ac6fb22b70f073f6
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052485"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="0981f-103">Logowanie się w programie Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0981f-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="0981f-104">Program Azure PowerShell obsługuje kilka metod uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="0981f-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="0981f-105">Najprostszym sposobem na rozpoczęcie pracy jest usługa [Azure Cloud Shell](/azure/cloud-shell/overview), która loguje Cię automatycznie.</span><span class="sxs-lookup"><span data-stu-id="0981f-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="0981f-106">W przypadku instalacji lokalnej możesz logować się interaktywnie za pośrednictwem przeglądarki.</span><span class="sxs-lookup"><span data-stu-id="0981f-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="0981f-107">Podczas pisania skryptów automatyzacji zalecanym rozwiązaniem jest użycie [jednostki usługi](create-azure-service-principal-azureps.md) z odpowiednimi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="0981f-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="0981f-108">Możliwie największe ograniczenie uprawnień logowania w danym przypadku użycia pomaga w zabezpieczeniu zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0981f-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="0981f-109">Po zalogowaniu się polecenia są uruchamiane względem subskrypcji domyślnej.</span><span class="sxs-lookup"><span data-stu-id="0981f-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="0981f-110">Aby zmienić aktywną subskrypcję dla sesji, użyj polecenia cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="0981f-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="0981f-111">Aby zmienić domyślną subskrypcję używaną podczas logowania się przy użyciu programu Azure PowerShell, użyj polecenia [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span><span class="sxs-lookup"><span data-stu-id="0981f-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="0981f-112">Poświadczenia są współdzielone w ramach wielu sesji programu PowerShell, dopóki użytkownik pozostanie zalogowany.</span><span class="sxs-lookup"><span data-stu-id="0981f-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="0981f-113">Aby uzyskać więcej informacji, zobacz artykuł dotyczący [poświadczeń trwałych](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="0981f-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="0981f-114">Logowanie interakcyjne</span><span class="sxs-lookup"><span data-stu-id="0981f-114">Sign in interactively</span></span>

<span data-ttu-id="0981f-115">Aby zalogować się interakcyjnie, skorzystaj z polecenia cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="0981f-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="0981f-116">Po uruchomieniu to polecenie cmdlet spowoduje wyświetlenie ciągu tokenu.</span><span class="sxs-lookup"><span data-stu-id="0981f-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="0981f-117">Aby się zalogować, skopiuj ten ciąg i wklej go w witrynie https://microsoft.com/devicelogin w przeglądarce.</span><span class="sxs-lookup"><span data-stu-id="0981f-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="0981f-118">Sesja programu PowerShell zostanie uwierzytelniona na potrzeby połączenia z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0981f-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="0981f-119">Autoryzacja poświadczenia nazwy użytkownika/hasła została usunięta z programu Azure PowerShell z powodu zmian implementacji autoryzacji usługi Active Directory i zagadnień związanych z bezpieczeństwem.</span><span class="sxs-lookup"><span data-stu-id="0981f-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span>
> <span data-ttu-id="0981f-120">Jeśli używasz autoryzacji poświadczeń do celów automatyzacji, w zamian [utwórz jednostkę usługi](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="0981f-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a><span data-ttu-id="0981f-121">Logowanie za pomocą jednostki usługi <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="0981f-121">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="0981f-122">Jednostki usługi to nieinterakcyjne konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0981f-122">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="0981f-123">Podobnie jak w przypadku innych kont użytkownika, ich uprawnieniami zarządza się za pomocą usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0981f-123">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="0981f-124">Udzielając jednostce usługi tylko potrzebnych uprawnień, możesz zapewnić bezpieczeństwo skryptom automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="0981f-124">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="0981f-125">Aby dowiedzieć się, jak utworzyć jednostkę usługi do użycia z programem Azure PowerShell, zobacz [Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="0981f-125">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="0981f-126">Aby zalogować się przy użyciu jednostki usługi, podaj argument `-ServicePrincipal` w poleceniu cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="0981f-126">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="0981f-127">Z jednostką usługi trzeba będzie również skojarzyć jej identyfikator aplikacji, poświadczenia logowania oraz identyfikator dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="0981f-127">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="0981f-128">Sposób logowania przy użyciu jednostki usługi będzie zależeć od tego, czy została ona skonfigurowana do uwierzytelniania opartego na hasłach, czy opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="0981f-128">How you sign in with a service principal will depend on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="0981f-129">Uwierzytelnianie oparte na hasłach</span><span class="sxs-lookup"><span data-stu-id="0981f-129">Password-based authentication</span></span>

<span data-ttu-id="0981f-130">Aby pobrać poświadczenia jednostki usługi jako odpowiedni obiekt, użyj polecenia cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="0981f-130">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="0981f-131">To polecenie cmdlet wyświetli monit o podanie nazwy użytkownika i hasła.</span><span class="sxs-lookup"><span data-stu-id="0981f-131">This cmdlet will present a prompt for a username and password.</span></span> <span data-ttu-id="0981f-132">Użyj identyfikatora jednostki usługi w przypadku nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0981f-132">Use the service principal ID for the username.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="0981f-133">Dla scenariuszy automatyzacji musisz utworzyć poświadczenia na podstawie nazwy użytkownika i bezpiecznego ciągu:</span><span class="sxs-lookup"><span data-stu-id="0981f-133">For automation scenarios, you need to create credentials from a user name and secure string:</span></span>

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="0981f-134">Upewnij się, że podczas automatyzowania połączeń jednostki usługi używasz najlepszych rozwiązań dotyczących magazynu haseł.</span><span class="sxs-lookup"><span data-stu-id="0981f-134">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="0981f-135">Uwierzytelnianie oparte na certyfikacie</span><span class="sxs-lookup"><span data-stu-id="0981f-135">Certificate-based authentication</span></span>

<span data-ttu-id="0981f-136">Uwierzytelnianie oparte na certyfikatach wymaga, aby program Azure PowerShell mógł pobierać informacje z lokalnego magazynu certyfikatów na podstawie na odcisku palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0981f-136">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>
```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="0981f-137">W programie PowerShell 5.1 zarządzanie magazynem certyfikatów i jego badanie może odbywać się za pomocą modułu infrastruktury [PKI](/powershell/module/pkiclient).</span><span class="sxs-lookup"><span data-stu-id="0981f-137">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="0981f-138">Dla programu PowerShell Core w wersji 6.x i późniejszych proces jest bardziej skomplikowany.</span><span class="sxs-lookup"><span data-stu-id="0981f-138">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="0981f-139">Poniższe skrypty pokazują, jak zaimportować istniejący certyfikat do magazynu certyfikatów dostępnego w programie PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0981f-139">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="0981f-140">Importowanie certyfikatu w programie PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0981f-140">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="0981f-141">Importowanie certyfikatu w programie PowerShell Core w wersji 6.x lub nowszej</span><span class="sxs-lookup"><span data-stu-id="0981f-141">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="0981f-142">Logowanie się przy użyciu tożsamości zarządzanej</span><span class="sxs-lookup"><span data-stu-id="0981f-142">Sign in using a managed identity</span></span> 

<span data-ttu-id="0981f-143">Tożsamości zarządzane to funkcja w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0981f-143">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="0981f-144">Tożsamości zarządzane to jednostki usługi przypisane do zasobów, które działają na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="0981f-144">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="0981f-145">Jednostki usługi tożsamości zarządzanej można używać do logowania się i uzyskiwania aplikacyjnego tokenu dostępu do uzyskania dostępu do innych zasobów.</span><span class="sxs-lookup"><span data-stu-id="0981f-145">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="0981f-146">Tożsamości zarządzane są dostępne tylko w przypadku zasobów działających w chmurze platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0981f-146">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="0981f-147">Aby uzyskać więcej informacji na temat tożsamości zarządzanych dla zasobów platformy Azure, zobacz [Jak używać tożsamości zarządzanych dla zasobów platformy Azure na maszynie wirtualnej platformy Azure w celu uzyskania tokenu dostępu](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="0981f-147">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="0981f-148">Logowanie się przy użyciu innej niż domyślnej dzierżawy lub jako dostawca rozwiązań w chmurze (CSP, Cloud Solution Provider)</span><span class="sxs-lookup"><span data-stu-id="0981f-148">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="0981f-149">Jeśli konto jest skojarzone z więcej niż jedną dzierżawą, logowanie wymaga użycia parametru `-TenantId` podczas nawiązywania połączenia.</span><span class="sxs-lookup"><span data-stu-id="0981f-149">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="0981f-150">Ten parametr będzie współdziałać z każdą inną metodą logowania.</span><span class="sxs-lookup"><span data-stu-id="0981f-150">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="0981f-151">Podczas logowania się wartość tego parametru może być identyfikatorem obiektu platformy Azure dzierżawy (identyfikatorem dzierżawy) lub w pełni kwalifikowaną nazwą domeny dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="0981f-151">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="0981f-152">Jeśli jesteś [dostawcą rozwiązań w chmurze (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), wartość `-TenantId` **musi** być identyfikatorem dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="0981f-152">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="0981f-153">Logowanie się do innej chmury</span><span class="sxs-lookup"><span data-stu-id="0981f-153">Sign in to another Cloud</span></span>

<span data-ttu-id="0981f-154">Usługi w chmurze platformy Azure oferują środowiska zgodne z regionalnymi przepisami dotyczącymi obsługi danych.</span><span class="sxs-lookup"><span data-stu-id="0981f-154">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="0981f-155">W przypadku kont w chmurze regionalnej określ środowisko po zalogowaniu się, używając argumentu `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="0981f-155">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="0981f-156">Na przykład jeśli Twoje konto znajduje się w chmurze w Chinach:</span><span class="sxs-lookup"><span data-stu-id="0981f-156">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="0981f-157">Następujące polecenie pozwala uzyskać listę dostępnych środowisk:</span><span class="sxs-lookup"><span data-stu-id="0981f-157">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
