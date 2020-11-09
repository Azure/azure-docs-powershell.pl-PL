---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 039ae434a28da0b8f320925c4e84c57571a74273
ms.sourcegitcommit: e30c11217b1ac93493fdd509fa71ac33510a98b5
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/29/2020
ms.locfileid: "94319464"
---
# <span data-ttu-id="7acca-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="7acca-101">Connect-AzAccount</span></span>

## <span data-ttu-id="7acca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7acca-102">SYNOPSIS</span></span>
<span data-ttu-id="7acca-103">Połącz się z platformą Azure za pomocą konta uwierzytelnionego do użycia z poleceniami cmdlet z poziomu AZ modułów programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7acca-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="7acca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7acca-104">SYNTAX</span></span>

### <span data-ttu-id="7acca-105">UserWithSubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7acca-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7acca-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7acca-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7acca-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="7acca-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7acca-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7acca-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7acca-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7acca-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7acca-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="7acca-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7acca-111">Opis</span><span class="sxs-lookup"><span data-stu-id="7acca-111">DESCRIPTION</span></span>

<span data-ttu-id="7acca-112">`Connect-AzAccount`Polecenie cmdlet umożliwia nawiązanie połączenia z platformą Azure za pomocą konta uwierzytelnionego do użycia z poleceniami cmdlet z modułów AZ programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7acca-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="7acca-113">Możesz używać tego konta uwierzytelnionego tylko w przypadku żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="7acca-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="7acca-114">Aby dodać uwierzytelnione konto do użytku z zarządzaniem usługami, użyj `Add-AzureAccount` polecenia cmdlet z modułu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7acca-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="7acca-115">Jeśli nie odnaleziono kontekstu dla bieżącego użytkownika, lista kontekstowa użytkownika zostanie uzupełniona kontekstem dla każdego z nich pierwszych 25 abonamentów.</span><span class="sxs-lookup"><span data-stu-id="7acca-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="7acca-116">Lista kontekstów utworzonych dla użytkownika można znaleźć, uruchamiając `Get-AzContext -ListAvailable` .</span><span class="sxs-lookup"><span data-stu-id="7acca-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="7acca-117">Aby pominąć tę populację kontekstu, określ parametr przełącznika **SkipContextPopulation** .</span><span class="sxs-lookup"><span data-stu-id="7acca-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="7acca-118">Po wykonaniu tego polecenia cmdlet możesz rozłączyć konto platformy Azure przy użyciu `Disconnect-AzAccount` .</span><span class="sxs-lookup"><span data-stu-id="7acca-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="7acca-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7acca-119">EXAMPLES</span></span>

### <span data-ttu-id="7acca-120">Przykład 1: Nawiązywanie połączenia z kontem na platformie Azure</span><span class="sxs-lookup"><span data-stu-id="7acca-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="7acca-121">W tym przykładzie nawiążesz połączenie z kontem na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="7acca-121">This example connects to an Azure account.</span></span> <span data-ttu-id="7acca-122">Musisz podać poświadczenia konta Microsoft lub identyfikatora organizacji.</span><span class="sxs-lookup"><span data-stu-id="7acca-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="7acca-123">Jeśli dla poświadczeń włączono uwierzytelnianie wieloskładnikowe, należy zalogować się przy użyciu opcji interakcyjnej lub użyć uwierzytelniania głównego usługi.</span><span class="sxs-lookup"><span data-stu-id="7acca-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="7acca-124">Przykład 2: (tylko program Windows PowerShell 5,1) Nawiązywanie połączenia z usługą Azure przy użyciu poświadczeń identyfikatora organizacji</span><span class="sxs-lookup"><span data-stu-id="7acca-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="7acca-125">Ten scenariusz działa tylko w programie Windows PowerShell 5,1.</span><span class="sxs-lookup"><span data-stu-id="7acca-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="7acca-126">Pierwsze polecenie monituje o podanie poświadczeń użytkownika i przechowuje je w `$Credential` zmiennej.</span><span class="sxs-lookup"><span data-stu-id="7acca-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="7acca-127">Drugie polecenie nawiązuje połączenie z kontem na platformie Azure przy użyciu poświadczeń przechowywanych w programie `$Credential` .</span><span class="sxs-lookup"><span data-stu-id="7acca-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="7acca-128">To konto jest uwierzytelniane na platformie Azure przy użyciu poświadczeń identyfikatora organizacji.</span><span class="sxs-lookup"><span data-stu-id="7acca-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="7acca-129">Przykład 3: Nawiązywanie połączenia z platformą Azure przy użyciu głównego konta usługi</span><span class="sxs-lookup"><span data-stu-id="7acca-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="7acca-130">Pierwsze polecenie monituje o podanie poświadczeń głównych usług i zapisuje je w `$Credential` zmiennej.</span><span class="sxs-lookup"><span data-stu-id="7acca-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="7acca-131">Jeśli zostanie wyświetlony monit, wprowadź identyfikator aplikacji dla nazwy użytkownika i hasła głównego usługi.</span><span class="sxs-lookup"><span data-stu-id="7acca-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="7acca-132">Drugie polecenie łączy określoną dzierżawę platformy Azure przy użyciu głównych poświadczeń usługi przechowywanych w `$Credential` zmiennej.</span><span class="sxs-lookup"><span data-stu-id="7acca-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="7acca-133">Parametr **serviceprincipal** Switch wskazuje, że konto jest uwierzytelniane jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="7acca-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="7acca-134">Przykład 4: używanie interakcyjnego logowania do nawiązywania połączenia z określonym dzierżawcą i abonamentem</span><span class="sxs-lookup"><span data-stu-id="7acca-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="7acca-135">W tym przykładzie nawiążesz połączenie z kontem platformy Azure z określonym dzierżawcą i abonamentem.</span><span class="sxs-lookup"><span data-stu-id="7acca-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="7acca-136">Przykład 5: Nawiązywanie połączenia przy użyciu tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="7acca-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="7acca-137">W tym przykładzie nawiąże połączenie przy użyciu tożsamości usługi zarządzanej (MSI) środowiska hosta.</span><span class="sxs-lookup"><span data-stu-id="7acca-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="7acca-138">Na przykład użytkownik loguje się do platformy Azure z maszyny wirtualnej z przypisanym instalatorem MSI.</span><span class="sxs-lookup"><span data-stu-id="7acca-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="7acca-139">Przykład 6: Nawiązywanie połączenia przy użyciu identyfikatora logowania i ClientId tożsamości zarządzanych usług</span><span class="sxs-lookup"><span data-stu-id="7acca-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="7acca-140">W tym przykładzie nawiąże połączenie przy użyciu tożsamości usługi zarządzanej **myUserAssignedIdentity**.</span><span class="sxs-lookup"><span data-stu-id="7acca-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="7acca-141">Do maszyny wirtualnej zostanie dodana tożsamość użytkownika, a następnie nawiążesz połączenie przy użyciu ClientIda tożsamości przypisanej do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7acca-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="7acca-142">Aby uzyskać więcej informacji, zobacz [Konfigurowanie tożsamości zarządzanych dla zasobów platformy Azure na maszynie wirtualnej Azure](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span><span class="sxs-lookup"><span data-stu-id="7acca-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

```powershell
$identity = Get-AzUserAssignedIdentity -ResourceGroupName 'myResourceGroup' -Name 'myUserAssignedIdentity'
Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the virtual machine
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="7acca-143">Przykład 7: Nawiązywanie połączenia przy użyciu certyfikatów</span><span class="sxs-lookup"><span data-stu-id="7acca-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="7acca-144">W tym przykładzie nawiążesz połączenie z kontem na platformie Azure przy użyciu uwierzytelniania głównego usług opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="7acca-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="7acca-145">Podmiot zabezpieczeń usługi służący do uwierzytelniania musi zostać utworzony przy użyciu określonego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="7acca-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="7acca-146">Aby uzyskać więcej informacji na temat tworzenia certyfikatów z podpisem własnym i przypisywania im uprawnień, zobacz [Używanie platformy Azure PowerShell do tworzenia podmiotu usługi z certyfikatem](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span><span class="sxs-lookup"><span data-stu-id="7acca-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

```powershell
$Thumbprint = '0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV'
$TenantId = '4cd76576-b611-43d0-8f2b-adcb139531bf'
$ApplicationId = '3794a65a-e4e4-493d-ac1d-f04308d712dd'
Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal
```

```Output
Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

## <span data-ttu-id="7acca-147">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7acca-147">PARAMETERS</span></span>

### <span data-ttu-id="7acca-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="7acca-148">-AccessToken</span></span>

<span data-ttu-id="7acca-149">Określa token dostępu.</span><span class="sxs-lookup"><span data-stu-id="7acca-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="7acca-150">Tokeny dostępu są typu poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="7acca-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="7acca-151">Należy podjąć odpowiednie środki ostrożności, aby zachować ich poufność.</span><span class="sxs-lookup"><span data-stu-id="7acca-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="7acca-152">Tokeny dostępu również przekroczą limit czasu i mogą uniemożliwiać wykonywanie długotrwałych zadań.</span><span class="sxs-lookup"><span data-stu-id="7acca-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="7acca-153">-AccountId</span></span>

<span data-ttu-id="7acca-154">Identyfikator konta dla tokenu dostępu w zestawie parametrów **AccessToken** .</span><span class="sxs-lookup"><span data-stu-id="7acca-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="7acca-155">Identyfikator konta dla usługi zarządzanej w zestawie parametrów **ManagedService** .</span><span class="sxs-lookup"><span data-stu-id="7acca-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="7acca-156">Może to być zarządzany identyfikator zasobu usługi lub skojarzony identyfikator klienta.</span><span class="sxs-lookup"><span data-stu-id="7acca-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="7acca-157">Aby użyć tożsamości przypisanej do systemu, pozostaw to pole puste.</span><span class="sxs-lookup"><span data-stu-id="7acca-157">To use the system assigned identity, leave this field blank.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-158">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="7acca-158">-ApplicationId</span></span>

<span data-ttu-id="7acca-159">Identyfikator aplikacji głównej usługi.</span><span class="sxs-lookup"><span data-stu-id="7acca-159">Application ID of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="7acca-160">-CertificateThumbprint</span></span>

<span data-ttu-id="7acca-161">Skrót certyfikatu lub odcisk palca.</span><span class="sxs-lookup"><span data-stu-id="7acca-161">Certificate Hash or Thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-162">-Ontextname</span><span class="sxs-lookup"><span data-stu-id="7acca-162">-ContextName</span></span>

<span data-ttu-id="7acca-163">Nazwa domyślnego kontekstu platformy Azure dla tego logowania.</span><span class="sxs-lookup"><span data-stu-id="7acca-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="7acca-164">Aby uzyskać więcej informacji na temat kontekstów platformy Azure, zobacz [obiekty kontekstu usługi Azure PowerShell](/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="7acca-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-165">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="7acca-165">-Credential</span></span>

<span data-ttu-id="7acca-166">Określa obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="7acca-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="7acca-167">Aby uzyskać więcej informacji na temat obiektu **PSCredential** , wpisz `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="7acca-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="7acca-168">Obiekt **PSCredential** zapewnia identyfikator użytkownika i hasło dla poświadczeń identyfikatora organizacji lub identyfikator aplikacji oraz klucz tajny dla poświadczeń głównych usługi.</span><span class="sxs-lookup"><span data-stu-id="7acca-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, UserWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7acca-169">-DefaultProfile</span></span>

<span data-ttu-id="7acca-170">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7acca-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-171">-Środowisko</span><span class="sxs-lookup"><span data-stu-id="7acca-171">-Environment</span></span>

<span data-ttu-id="7acca-172">Środowisko zawierające konto platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7acca-172">Environment containing the Azure account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-173">-Force</span><span class="sxs-lookup"><span data-stu-id="7acca-173">-Force</span></span>

<span data-ttu-id="7acca-174">Zastąp istniejący kontekst o tej samej nazwie bez monitowania.</span><span class="sxs-lookup"><span data-stu-id="7acca-174">Overwrite the existing context with the same name without prompting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="7acca-175">-GraphAccessToken</span></span>

<span data-ttu-id="7acca-176">AccessToken dla usługi Graph.</span><span class="sxs-lookup"><span data-stu-id="7acca-176">AccessToken for Graph Service.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-177">-Identity (tożsamość)</span><span class="sxs-lookup"><span data-stu-id="7acca-177">-Identity</span></span>

<span data-ttu-id="7acca-178">Logowanie przy użyciu tożsamości usługi zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="7acca-178">Login using a Managed Service Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="7acca-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="7acca-180">AccessToken dla usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="7acca-180">AccessToken for KeyVault Service.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="7acca-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="7acca-182">Nazwa hosta usługi zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="7acca-182">Host name for the managed service.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-183">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="7acca-183">-ManagedServicePort</span></span>

<span data-ttu-id="7acca-184">Numer portu zarządzanej usługi.</span><span class="sxs-lookup"><span data-stu-id="7acca-184">Port number for the managed service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-185">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="7acca-185">-ManagedServiceSecret</span></span>

<span data-ttu-id="7acca-186">Token służący do logowania zarządzanych usług.</span><span class="sxs-lookup"><span data-stu-id="7acca-186">Token for the managed service login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-187">-MaxContextPopulation</span><span class="sxs-lookup"><span data-stu-id="7acca-187">-MaxContextPopulation</span></span>

<span data-ttu-id="7acca-188">Maksymalny numer abonamentu, aby wypełnić konteksty po zalogowaniu.</span><span class="sxs-lookup"><span data-stu-id="7acca-188">Max subscription number to populate contexts after login.</span></span> <span data-ttu-id="7acca-189">Wartość domyślna to 25.</span><span class="sxs-lookup"><span data-stu-id="7acca-189">Default is 25.</span></span> <span data-ttu-id="7acca-190">Aby wypełnić wszystkie abonamenty kontekstowe, ustaw wartość-1.</span><span class="sxs-lookup"><span data-stu-id="7acca-190">To populate all subscriptions to contexts, set to -1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-191">-Zakres</span><span class="sxs-lookup"><span data-stu-id="7acca-191">-Scope</span></span>

<span data-ttu-id="7acca-192">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7acca-192">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-193">-Serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="7acca-193">-ServicePrincipal</span></span>

<span data-ttu-id="7acca-194">Wskazuje, że to konto uwierzytelnia się, dostarczając poświadczenia podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="7acca-194">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-195">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="7acca-195">-SkipContextPopulation</span></span>

<span data-ttu-id="7acca-196">Pomija populację kontekstu, jeśli nie zostaną znalezione żadne konteksty.</span><span class="sxs-lookup"><span data-stu-id="7acca-196">Skips context population if no contexts are found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-197">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="7acca-197">-SkipValidation</span></span>

<span data-ttu-id="7acca-198">Pomijanie sprawdzania poprawności tokenu dostępu.</span><span class="sxs-lookup"><span data-stu-id="7acca-198">Skip validation for access token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-199">-Subscription</span><span class="sxs-lookup"><span data-stu-id="7acca-199">-Subscription</span></span>

<span data-ttu-id="7acca-200">Nazwa lub Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7acca-200">Subscription Name or ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-201">-Dzierżawca</span><span class="sxs-lookup"><span data-stu-id="7acca-201">-Tenant</span></span>

<span data-ttu-id="7acca-202">Opcjonalna nazwa lub identyfikator dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="7acca-202">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="7acca-203">Ze względu na ograniczenia bieżącego interfejsu API podczas łączenia się z kontem firmowym (B2B) należy użyć identyfikatora dzierżawy zamiast nazwy dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="7acca-203">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, UserWithCredential, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-204">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="7acca-204">-UseDeviceAuthentication</span></span>

<span data-ttu-id="7acca-205">Użyj uwierzytelniania kodu urządzenia zamiast kontrolki przeglądarki.</span><span class="sxs-lookup"><span data-stu-id="7acca-205">Use device code authentication instead of a browser control.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UserWithSubscriptionId
Aliases: DeviceCode, DeviceAuth, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-206">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7acca-206">-Confirm</span></span>

<span data-ttu-id="7acca-207">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7acca-207">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-208">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7acca-208">-WhatIf</span></span>

<span data-ttu-id="7acca-209">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7acca-209">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7acca-210">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7acca-210">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acca-211">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7acca-211">CommonParameters</span></span>
<span data-ttu-id="7acca-212">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7acca-212">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7acca-213">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7acca-213">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7acca-214">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7acca-214">INPUTS</span></span>

### <span data-ttu-id="7acca-215">System. String</span><span class="sxs-lookup"><span data-stu-id="7acca-215">System.String</span></span>

## <span data-ttu-id="7acca-216">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7acca-216">OUTPUTS</span></span>

### <span data-ttu-id="7acca-217">Microsoft. Azure. Commands. profile. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="7acca-217">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="7acca-218">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7acca-218">NOTES</span></span>

## <span data-ttu-id="7acca-219">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7acca-219">RELATED LINKS</span></span>
