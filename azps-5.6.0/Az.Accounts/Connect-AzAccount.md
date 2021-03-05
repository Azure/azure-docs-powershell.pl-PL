---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: dcf4e78e9b6e467961eb05dd141396e426dfe5e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999118"
---
# <span data-ttu-id="b26f4-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="b26f4-101">Connect-AzAccount</span></span>

## <span data-ttu-id="b26f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b26f4-102">SYNOPSIS</span></span>
<span data-ttu-id="b26f4-103">Połącz się z platformą Azure przy użyciu uwierzytelnionego konta w celu używania z poleceniami cmdlet z modułów programu Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b26f4-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="b26f4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b26f4-104">SYNTAX</span></span>

### <span data-ttu-id="b26f4-105">UserWithSubscriptionId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b26f4-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b26f4-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b26f4-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b26f4-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="b26f4-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b26f4-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b26f4-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b26f4-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b26f4-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b26f4-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="b26f4-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b26f4-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="b26f4-111">DESCRIPTION</span></span>

<span data-ttu-id="b26f4-112">Polecenie cmdlet łączy się z platformą Azure przy użyciu uwierzytelnionego konta w celu używania z `Connect-AzAccount` poleceniami cmdlet z modułów programu Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b26f4-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="b26f4-113">Tego uwierzytelnionego konta można używać tylko w przypadku żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b26f4-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="b26f4-114">Aby dodać uwierzytelnione konto do użycia z zarządzaniem usługami, użyj `Add-AzureAccount` polecenia cmdlet z modułu programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b26f4-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="b26f4-115">Jeśli dla bieżącego użytkownika nie zostanie znaleziony kontekst, lista kontekstowa użytkownika zostanie wypełniona kontekstem dla każdej z pierwszych 25 subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b26f4-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="b26f4-116">Listę kontekstów utworzonych dla użytkownika można znaleźć, uruchamiając `Get-AzContext -ListAvailable` program.</span><span class="sxs-lookup"><span data-stu-id="b26f4-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="b26f4-117">Aby pominąć tę populację kontekstu, określ **parametr przełącznika SkipContextPopulation.**</span><span class="sxs-lookup"><span data-stu-id="b26f4-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="b26f4-118">Po wykonaniu tego polecenia cmdlet możesz rozłączyć się z kontem platformy Azure przy `Disconnect-AzAccount` użyciu.</span><span class="sxs-lookup"><span data-stu-id="b26f4-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="b26f4-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b26f4-119">EXAMPLES</span></span>

### <span data-ttu-id="b26f4-120">Przykład 1. Nawiązywanie połączenia z kontem platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b26f4-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="b26f4-121">W tym przykładzie jest nawiąże połączenie z kontem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b26f4-121">This example connects to an Azure account.</span></span> <span data-ttu-id="b26f4-122">Musisz podać poświadczenia konta Microsoft lub identyfikatora organizacyjnego.</span><span class="sxs-lookup"><span data-stu-id="b26f4-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="b26f4-123">Jeśli dla twoich poświadczeń włączono uwierzytelnianie wieloskładnikowe, musisz zalogować się przy użyciu opcji interakcyjnej lub użyć uwierzytelniania podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b26f4-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="b26f4-124">Przykład 2. (tylko program Windows PowerShell 5.1) Łączenie się z platformą Azure przy użyciu poświadczeń identyfikatora organizacyjnego</span><span class="sxs-lookup"><span data-stu-id="b26f4-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="b26f4-125">Ten scenariusz działa tylko w programie Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="b26f4-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="b26f4-126">Pierwsze polecenie wyświetla monit o poświadczenia użytkownika i zapisuje je w `$Credential` zmiennej.</span><span class="sxs-lookup"><span data-stu-id="b26f4-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="b26f4-127">Drugie polecenie łączy się z kontem platformy Azure przy użyciu poświadczeń przechowywanych w `$Credential` usłudze.</span><span class="sxs-lookup"><span data-stu-id="b26f4-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="b26f4-128">To konto jest uwierzytelniane na platformie Azure przy użyciu poświadczeń identyfikatora organizacyjnego.</span><span class="sxs-lookup"><span data-stu-id="b26f4-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="b26f4-129">Przykład 3. Nawiązywanie połączenia z platformą Azure przy użyciu konta podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="b26f4-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="b26f4-130">Pierwsze polecenie monituje o poświadczenia podmiotu zabezpieczeń usługi i przechowuje je w `$Credential` zmiennej.</span><span class="sxs-lookup"><span data-stu-id="b26f4-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="b26f4-131">Po wyświetleniu monitu wprowadź identyfikator aplikacji dla nazwy użytkownika i podmiotu zabezpieczeń usługi jako hasło.</span><span class="sxs-lookup"><span data-stu-id="b26f4-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="b26f4-132">Drugie polecenie łączy określoną dzierżawę platformy Azure przy użyciu przechowywanych w zmiennej poświadczeń podmiotu zabezpieczeń `$Credential` usługi.</span><span class="sxs-lookup"><span data-stu-id="b26f4-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="b26f4-133">Parametr **przełącznika ServicePrincipal** wskazuje, że konto uwierzytelnia się jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b26f4-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="b26f4-134">Przykład 4. Używanie interakcyjnego logowania w celu nawiązania połączenia z konkretną dzierżawą i subskrypcją</span><span class="sxs-lookup"><span data-stu-id="b26f4-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="b26f4-135">W tym przykładzie powiążesz się z kontem platformy Azure z określoną dzierżawą i subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="b26f4-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="b26f4-136">Przykład 5. Nawiązywanie połączenia przy użyciu tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="b26f4-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="b26f4-137">W tym przykładzie jest nawiązuje połączenie przy użyciu tożsamości usługi zarządzanej (MSI) środowiska hosta.</span><span class="sxs-lookup"><span data-stu-id="b26f4-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="b26f4-138">Na przykład możesz zalogować się do platformy Azure z maszyny wirtualnej z przypisanym msi.</span><span class="sxs-lookup"><span data-stu-id="b26f4-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="b26f4-139">Przykład 6. Łączenie przy użyciu logowania tożsamości usługi zarządzanej i identyfikatora klienta</span><span class="sxs-lookup"><span data-stu-id="b26f4-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="b26f4-140">W tym przykładzie jest nawiązuje połączenie przy użyciu tożsamości usługi zarządzanej **myUserAssignedIdentity.**</span><span class="sxs-lookup"><span data-stu-id="b26f4-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="b26f4-141">Dodaje tożsamość przypisaną do użytkownika do maszyny wirtualnej, a następnie łączy się przy użyciu wartości ClientId przypisanej tożsamości użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b26f4-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="b26f4-142">Aby uzyskać więcej informacji, zobacz Konfigurowanie tożsamości [zarządzanych dla zasobów platformy Azure w maszyny wirtualnej platformy Azure.](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)</span><span class="sxs-lookup"><span data-stu-id="b26f4-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

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

### <span data-ttu-id="b26f4-143">Przykład 7. Nawiązywanie połączenia przy użyciu certyfikatów</span><span class="sxs-lookup"><span data-stu-id="b26f4-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="b26f4-144">W tym przykładzie powiążesz się z kontem platformy Azure przy użyciu uwierzytelniania głównego usługi opartej na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="b26f4-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="b26f4-145">Podmiot zabezpieczeń usługi używany do uwierzytelniania musi zostać utworzony przy użyciu określonego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b26f4-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="b26f4-146">Aby uzyskać więcej informacji na temat tworzenia certyfikatów z podpisem własnym i przypisywania do nich uprawnień, zobacz Używanie programu Azure PowerShell do tworzenia podmiotu zabezpieczeń usługi [z certyfikatem.](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span><span class="sxs-lookup"><span data-stu-id="b26f4-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

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

## <span data-ttu-id="b26f4-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b26f4-147">PARAMETERS</span></span>

### <span data-ttu-id="b26f4-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="b26f4-148">-AccessToken</span></span>

<span data-ttu-id="b26f4-149">Określa token dostępu.</span><span class="sxs-lookup"><span data-stu-id="b26f4-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="b26f4-150">Tokeny dostępu są typem poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="b26f4-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="b26f4-151">Należy podjąć odpowiednie środki ostrożności, aby zachować ich poufność.</span><span class="sxs-lookup"><span data-stu-id="b26f4-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="b26f4-152">Limit czasu tokenów programu Access może również uniemożliwiać ukończenie długo wykonywanych zadań.</span><span class="sxs-lookup"><span data-stu-id="b26f4-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

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

### <span data-ttu-id="b26f4-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="b26f4-153">-AccountId</span></span>

<span data-ttu-id="b26f4-154">Identyfikator konta tokenu dostępu w zestawie parametrów **AccessToken.**</span><span class="sxs-lookup"><span data-stu-id="b26f4-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="b26f4-155">Identyfikator konta dla usługi zarządzanej w zestawie **parametrów ManagedService.**</span><span class="sxs-lookup"><span data-stu-id="b26f4-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="b26f4-156">Może być identyfikatorem zarządzanego zasobu usługi lub skojarzonym identyfikatorem klienta.</span><span class="sxs-lookup"><span data-stu-id="b26f4-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="b26f4-157">Aby użyć tożsamości przypisanej przez system, pozostaw to pole puste.</span><span class="sxs-lookup"><span data-stu-id="b26f4-157">To use the system assigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="b26f4-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b26f4-158">-ApplicationId</span></span>

<span data-ttu-id="b26f4-159">Identyfikator aplikacji podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b26f4-159">Application ID of the service principal.</span></span>

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

### <span data-ttu-id="b26f4-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b26f4-160">-CertificateThumbprint</span></span>

<span data-ttu-id="b26f4-161">Certificate Hash lub Thumbprint.</span><span class="sxs-lookup"><span data-stu-id="b26f4-161">Certificate Hash or Thumbprint.</span></span>

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

### <span data-ttu-id="b26f4-162">-ContextName</span><span class="sxs-lookup"><span data-stu-id="b26f4-162">-ContextName</span></span>

<span data-ttu-id="b26f4-163">Nazwa domyślnego kontekstu platformy Azure dla tego logowania.</span><span class="sxs-lookup"><span data-stu-id="b26f4-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="b26f4-164">Aby uzyskać więcej informacji o kontekstach platformy Azure, zobacz obiekty kontekstowe [programu Azure PowerShell.](/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="b26f4-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

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

### <span data-ttu-id="b26f4-165">- Credential</span><span class="sxs-lookup"><span data-stu-id="b26f4-165">-Credential</span></span>

<span data-ttu-id="b26f4-166">Określa obiekt **PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="b26f4-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="b26f4-167">Aby uzyskać więcej informacji na **temat obiektu PSCredential,** wpisz `Get-Help Get-Credential` tekst .</span><span class="sxs-lookup"><span data-stu-id="b26f4-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="b26f4-168">Obiekt **PSCredential** udostępnia identyfikator użytkownika i hasło dla poświadczeń identyfikatora organizacyjnego lub identyfikator aplikacji i klucz tajny dla poświadczeń podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b26f4-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="b26f4-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b26f4-169">-DefaultProfile</span></span>

<span data-ttu-id="b26f4-170">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b26f4-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b26f4-171">— Środowisko</span><span class="sxs-lookup"><span data-stu-id="b26f4-171">-Environment</span></span>

<span data-ttu-id="b26f4-172">Środowisko zawierające konto platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b26f4-172">Environment containing the Azure account.</span></span>

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

### <span data-ttu-id="b26f4-173">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b26f4-173">-Force</span></span>

<span data-ttu-id="b26f4-174">Zastąp istniejący kontekst taką samą nazwą bez monitowania.</span><span class="sxs-lookup"><span data-stu-id="b26f4-174">Overwrite the existing context with the same name without prompting.</span></span>

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

### <span data-ttu-id="b26f4-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="b26f4-175">-GraphAccessToken</span></span>

<span data-ttu-id="b26f4-176">AccessToken for Graph Service.</span><span class="sxs-lookup"><span data-stu-id="b26f4-176">AccessToken for Graph Service.</span></span>

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

### <span data-ttu-id="b26f4-177">— Tożsamość</span><span class="sxs-lookup"><span data-stu-id="b26f4-177">-Identity</span></span>

<span data-ttu-id="b26f4-178">Zaloguj się przy użyciu tożsamości usługi zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="b26f4-178">Login using a Managed Service Identity.</span></span>

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

### <span data-ttu-id="b26f4-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="b26f4-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="b26f4-180">AccessToken for KeyVault Service.</span><span class="sxs-lookup"><span data-stu-id="b26f4-180">AccessToken for KeyVault Service.</span></span>

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

### <span data-ttu-id="b26f4-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="b26f4-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="b26f4-182">Przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b26f4-182">Obsolete.</span></span> <span data-ttu-id="b26f4-183">Aby użyć dostosowanego punktu końcowego MSI, ustaw wartość zmiennej MSI_ENDPOINT, na przykład " http://localhost:50342/oauth2/token ".</span><span class="sxs-lookup"><span data-stu-id="b26f4-183">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".</span></span> <span data-ttu-id="b26f4-184">Nazwa hosta usługi zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="b26f4-184">Host name for the managed service.</span></span>

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

### <span data-ttu-id="b26f4-185">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="b26f4-185">-ManagedServicePort</span></span>

<span data-ttu-id="b26f4-186">Przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b26f4-186">Obsolete.</span></span> <span data-ttu-id="b26f4-187">Aby użyć dostosowanego punktu końcowego MSI, ustaw wartość zmiennej MSI_ENDPOINT, na przykład " http://localhost:50342/oauth2/token ". Numer portu usługi zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="b26f4-187">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".Port number for the managed service.</span></span>

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

### <span data-ttu-id="b26f4-188">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="b26f4-188">-ManagedServiceSecret</span></span>

<span data-ttu-id="b26f4-189">Przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b26f4-189">Obsolete.</span></span> <span data-ttu-id="b26f4-190">Aby użyć niestandardowego msi tajnego, ustaw zmienną środowiskową MSI_SECRET.</span><span class="sxs-lookup"><span data-stu-id="b26f4-190">To use customized MSI secret, please set environment variable MSI_SECRET.</span></span> <span data-ttu-id="b26f4-191">Token dla logowania usługi zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="b26f4-191">Token for the managed service login.</span></span>

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

### <span data-ttu-id="b26f4-192">-MaxContextPopulation</span><span class="sxs-lookup"><span data-stu-id="b26f4-192">-MaxContextPopulation</span></span>

<span data-ttu-id="b26f4-193">Maksymalny numer subskrypcji, aby wypełnić konteksty po zalogowaniu się.</span><span class="sxs-lookup"><span data-stu-id="b26f4-193">Max subscription number to populate contexts after login.</span></span> <span data-ttu-id="b26f4-194">Wartość domyślna to 25.</span><span class="sxs-lookup"><span data-stu-id="b26f4-194">Default is 25.</span></span> <span data-ttu-id="b26f4-195">Aby wypełnić wszystkie subskrypcje kontekstami, ustaw wartość -1.</span><span class="sxs-lookup"><span data-stu-id="b26f4-195">To populate all subscriptions to contexts, set to -1.</span></span>

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

### <span data-ttu-id="b26f4-196">— Zakres</span><span class="sxs-lookup"><span data-stu-id="b26f4-196">-Scope</span></span>

<span data-ttu-id="b26f4-197">Określa zakres zmian kontekstu, na przykład tego, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b26f4-197">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="b26f4-198">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b26f4-198">-ServicePrincipal</span></span>

<span data-ttu-id="b26f4-199">Wskazuje, że to konto uwierzytelnia się, podając poświadczenia podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b26f4-199">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="b26f4-200">- SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="b26f4-200">-SkipContextPopulation</span></span>

<span data-ttu-id="b26f4-201">Pomija populację kontekstu w przypadku, gdy nie zostaną znalezione żadne konteksty.</span><span class="sxs-lookup"><span data-stu-id="b26f4-201">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="b26f4-202">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="b26f4-202">-SkipValidation</span></span>

<span data-ttu-id="b26f4-203">Pomiń sprawdzanie poprawności tokenu dostępu.</span><span class="sxs-lookup"><span data-stu-id="b26f4-203">Skip validation for access token.</span></span>

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

### <span data-ttu-id="b26f4-204">— Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="b26f4-204">-Subscription</span></span>

<span data-ttu-id="b26f4-205">Nazwa lub identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b26f4-205">Subscription Name or ID.</span></span>

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

### <span data-ttu-id="b26f4-206">— Dzierżawa</span><span class="sxs-lookup"><span data-stu-id="b26f4-206">-Tenant</span></span>

<span data-ttu-id="b26f4-207">Opcjonalna nazwa dzierżawy lub identyfikator.</span><span class="sxs-lookup"><span data-stu-id="b26f4-207">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="b26f4-208">Ze względu na ograniczenia bieżącego interfejsu API podczas łączenia się z kontem między firmami (B2B) należy użyć identyfikatora dzierżawy zamiast nazwy dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="b26f4-208">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

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

### <span data-ttu-id="b26f4-209">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="b26f4-209">-UseDeviceAuthentication</span></span>

<span data-ttu-id="b26f4-210">Użyj uwierzytelniania kodu urządzenia zamiast kontrolki przeglądarki.</span><span class="sxs-lookup"><span data-stu-id="b26f4-210">Use device code authentication instead of a browser control.</span></span>

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

### <span data-ttu-id="b26f4-211">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b26f4-211">-Confirm</span></span>

<span data-ttu-id="b26f4-212">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b26f4-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b26f4-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b26f4-213">-WhatIf</span></span>

<span data-ttu-id="b26f4-214">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b26f4-214">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b26f4-215">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b26f4-215">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b26f4-216">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b26f4-216">CommonParameters</span></span>
<span data-ttu-id="b26f4-217">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b26f4-217">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b26f4-218">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b26f4-218">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b26f4-219">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b26f4-219">INPUTS</span></span>

### <span data-ttu-id="b26f4-220">System.String</span><span class="sxs-lookup"><span data-stu-id="b26f4-220">System.String</span></span>

## <span data-ttu-id="b26f4-221">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b26f4-221">OUTPUTS</span></span>

### <span data-ttu-id="b26f4-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="b26f4-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="b26f4-223">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b26f4-223">NOTES</span></span>

## <span data-ttu-id="b26f4-224">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b26f4-224">RELATED LINKS</span></span>
