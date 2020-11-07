---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 87e8615e7862e8b3314c9dace4849621a8ed4c78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890257"
---
# <span data-ttu-id="f2d84-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f2d84-101">Connect-AzAccount</span></span>

## <span data-ttu-id="f2d84-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2d84-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d84-103">Połącz się z usługą Azure za pomocą konta uwierzytelnionego do użycia z żądaniami polecenia cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f2d84-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="f2d84-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2d84-104">SYNTAX</span></span>

### <span data-ttu-id="f2d84-105">UserWithSubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f2d84-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2d84-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2d84-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2d84-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="f2d84-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2d84-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2d84-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2d84-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2d84-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2d84-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="f2d84-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2d84-111">Opis</span><span class="sxs-lookup"><span data-stu-id="f2d84-111">DESCRIPTION</span></span>
<span data-ttu-id="f2d84-112">Polecenie cmdlet Connect-AzAccount łączy się z usługą Azure za pomocą konta uwierzytelnionego do użycia z żądaniami polecenia cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f2d84-112">The Connect-AzAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="f2d84-113">Tego konta można używać tylko z poleceniami cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f2d84-113">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="f2d84-114">Aby dodać uwierzytelnione konto do użycia z poleceniami cmdlet zarządzania usługami, użyj Add-AzAccount lub polecenia cmdlet Import-AzPublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="f2d84-114">To add an authenticated account for use with Service Management cmdlets, use the Add-AzAccount or the Import-AzPublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="f2d84-115">Jeśli nie odnaleziono kontekstu dla bieżącego użytkownika, to polecenie wypełni listę kontekstową użytkownika z kontekstem dla każdej z nich (pierwszych 25) subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f2d84-115">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="f2d84-116">Listę kontekstów utworzonych dla użytkownika można znaleźć, uruchamiając "Get-AzContext-ListAvailable".</span><span class="sxs-lookup"><span data-stu-id="f2d84-116">The list of contexts created for the user can be found by running "Get-AzContext -ListAvailable".</span></span> <span data-ttu-id="f2d84-117">Aby pominąć tę populację kontekstu, możesz uruchomić to polecenie za pomocą parametru przełącznika "-SkipContextPopulation".</span><span class="sxs-lookup"><span data-stu-id="f2d84-117">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="f2d84-118">Po wykonaniu tego polecenia cmdlet możesz rozłączyć się z kontem na platformie Azure, korzystając z funkcji Disconnect-AzAccount.</span><span class="sxs-lookup"><span data-stu-id="f2d84-118">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzAccount.</span></span>

## <span data-ttu-id="f2d84-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2d84-119">EXAMPLES</span></span>

### <span data-ttu-id="f2d84-120">Przykład 1. Użyj interakcyjnego logowania, aby połączyć się z kontem platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f2d84-120">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="f2d84-121">To polecenie nawiązuje połączenie z kontem na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f2d84-121">This command connects to an Azure account.</span></span>
<span data-ttu-id="f2d84-122">Aby uruchomić polecenia cmdlet Menedżera zasobów platformy Azure przy użyciu tego konta, w monicie należy podać poświadczenia konta Microsoft lub identyfikatora organizacji.</span><span class="sxs-lookup"><span data-stu-id="f2d84-122">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="f2d84-123">Jeśli dla poświadczeń włączono uwierzytelnianie wieloskładnikowe, należy zalogować się przy użyciu opcji interakcyjnej lub użyć uwierzytelniania głównego usługi.</span><span class="sxs-lookup"><span data-stu-id="f2d84-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="f2d84-124">Przykład 2: (tylko program Windows PowerShell 5,1) Nawiązywanie połączenia z kontem na platformie Azure przy użyciu poświadczeń identyfikatora organizacji</span><span class="sxs-lookup"><span data-stu-id="f2d84-124">Example 2: (Windows PowerShell 5.1 only) Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="f2d84-125">Ten scenariusz działa tylko w programie Windows PowerShell 5,1.</span><span class="sxs-lookup"><span data-stu-id="f2d84-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="f2d84-126">Pierwsze polecenie wyświetli monit o podanie poświadczeń użytkownika (nazwa użytkownika i hasło), a następnie zapisze je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="f2d84-126">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="f2d84-127">Drugie polecenie nawiązuje połączenie z kontem na platformie Azure przy użyciu poświadczeń przechowywanych w $Credential.</span><span class="sxs-lookup"><span data-stu-id="f2d84-127">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="f2d84-128">To konto jest uwierzytelniane za pomocą Menedżera zasobów platformy Azure przy użyciu poświadczeń identyfikatora organizacji.</span><span class="sxs-lookup"><span data-stu-id="f2d84-128">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="f2d84-129">Za pomocą tego konta nie można używać uwierzytelniania wieloskładnikowego ani poświadczeń konta Microsoft w celu uruchamiania poleceń cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f2d84-129">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="f2d84-130">Przykład 3: Nawiązywanie połączenia z kontem głównym usługi Azure</span><span class="sxs-lookup"><span data-stu-id="f2d84-130">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="f2d84-131">Pierwsze polecenie uzyskuje główne poświadczenia usługi (Identyfikator aplikacji i główny klucz tajny usługi), a następnie zapisuje je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="f2d84-131">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="f2d84-132">Drugie polecenie nawiązuje połączenie z platformą Azure przy użyciu głównych poświadczeń usługi przechowywanych w $Credential dla określonego dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="f2d84-132">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="f2d84-133">Parametr serviceprincipal Switch wskazuje, że konto jest uwierzytelniane jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f2d84-133">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="f2d84-134">Przykład 4: używanie interakcyjnego logowania do nawiązywania połączenia z kontem dla konkretnej dzierżawy i abonamentu</span><span class="sxs-lookup"><span data-stu-id="f2d84-134">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="f2d84-135">To polecenie nawiązuje połączenie z kontem na platformie Azure i skonfigurowano program AzureRM PowerShell, aby domyślnie uruchamiać polecenia cmdlet dla określonego dzierżawy i abonamentu.</span><span class="sxs-lookup"><span data-stu-id="f2d84-135">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="f2d84-136">Przykład 5: Dodawanie konta przy użyciu identyfikatora logowania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="f2d84-136">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzAccount -Identity

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="f2d84-137">To polecenie nawiązuje połączenie przy użyciu tożsamości usługi zarządzanej dla środowiska hosta (na przykład w przypadku, gdy w VirtualMachine jest używana tożsamość usługi, która jest skojarzona z daną zarządzaną tożsamością).</span><span class="sxs-lookup"><span data-stu-id="f2d84-137">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="f2d84-138">Przykład 6: Dodawanie konta przy użyciu identyfikatora logowania i ClientId tożsamości zarządzanych usług</span><span class="sxs-lookup"><span data-stu-id="f2d84-138">Example 6: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="f2d84-139">To polecenie nawiązuje połączenie przy użyciu tożsamości "myUserAssignedIdentity", dodając do maszyny wirtualnej tożsamość użytkownika o przypisanej tożsamości, a następnie łącząc się przy użyciu ClientId tożsamości przypisanej do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f2d84-139">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the ClientId of the User Assigned Identity.</span></span>
<span data-ttu-id="f2d84-140">Więcej informacji na temat konfigurowania tożsamości zarządzanych można znaleźć tutaj: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="f2d84-140">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="f2d84-141">Przykład 7: Dodawanie konta przy użyciu identyfikatora logowania i ClientId tożsamości zarządzanych usług</span><span class="sxs-lookup"><span data-stu-id="f2d84-141">Example 7: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.Id # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="f2d84-142">To polecenie nawiązuje połączenie przy użyciu tożsamości "myUserAssignedIdentity", dodając do maszyny wirtualnej tożsamość użytkownika o przypisanej tożsamości, a następnie łącząc się przy użyciu identyfikatora przypisanego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f2d84-142">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the Id of the User Assigned Identity.</span></span>
<span data-ttu-id="f2d84-143">Więcej informacji na temat konfigurowania tożsamości zarządzanych można znaleźć tutaj: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="f2d84-143">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="f2d84-144">Przykład 8: Dodawanie konta przy użyciu certyfikatów</span><span class="sxs-lookup"><span data-stu-id="f2d84-144">Example 8: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="f2d84-145">To polecenie nawiązuje połączenie z kontem na platformie Azure przy użyciu uwierzytelniania głównego usług opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="f2d84-145">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="f2d84-146">Podmiot zabezpieczeń usługi używany do uwierzytelniania powinien być utworzony przy użyciu danego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f2d84-146">The service principal used for authentication should have been created with the given certificate.</span></span>

### <span data-ttu-id="f2d84-147">Przykład 9: Dodawanie konta przy użyciu uwierzytelniania AccessToken</span><span class="sxs-lookup"><span data-stu-id="f2d84-147">Example 9: Add an account using AccessToken authentication</span></span>
```powershell
PS C:\> $url = "https://login.windows.net/<TenantId>/oauth2/token"
PS C:\> $body = "grant_type=refresh_token&refresh_token=<refreshtoken>" # Refresh token obtained from ~/.azure/TokenCache.dat
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body
PS C:\> $AccessToken = $response.access_token
PS C:\> $body1 = $body + "&resource=https%3A%2F%2Fvault.azure.net"
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body1
PS C:\> $body2 = $body + "&resource=https%3A%2F%2Fgraph.windows.net"
PS C:\> $GraphAccessToken = $response.access_token
PS C:\> Connect-AzAccount -AccountId "azureuser@contoso.com" -AccessToken $AccessToken -KeyVaultAccessToken $KeyVaultAccessToken -GraphAccessToken $GraphAccessToken -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="f2d84-148">To polecenie nawiązuje połączenie z kontem platformy Azure określonym w polu "AccountId" przy użyciu podanej AccessToken i KeyVaultAccessToken.</span><span class="sxs-lookup"><span data-stu-id="f2d84-148">This command connects to an Azure account specified in "AccountId" using the AccessToken and KeyVaultAccessToken provided.</span></span>

## <span data-ttu-id="f2d84-149">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2d84-149">PARAMETERS</span></span>

### <span data-ttu-id="f2d84-150">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="f2d84-150">-AccessToken</span></span>
<span data-ttu-id="f2d84-151">Określa token dostępu.</span><span class="sxs-lookup"><span data-stu-id="f2d84-151">Specifies an access token.</span></span>

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

### <span data-ttu-id="f2d84-152">-AccountId</span><span class="sxs-lookup"><span data-stu-id="f2d84-152">-AccountId</span></span>
<span data-ttu-id="f2d84-153">Identyfikator konta dla tokenu dostępu w zestawie parametrów AccessToken.</span><span class="sxs-lookup"><span data-stu-id="f2d84-153">Account Id for access token in AccessToken parameter set.</span></span> <span data-ttu-id="f2d84-154">Identyfikator konta dla usługi zarządzanej w zestawie parametrów ManagedService.</span><span class="sxs-lookup"><span data-stu-id="f2d84-154">Account Id for managed service in ManagedService parameter set.</span></span> <span data-ttu-id="f2d84-155">Może to być zarządzany identyfikator zasobu usługi lub skojarzony identyfikator klienta. Aby użyć tożsamości SystemAssigned, pozostaw to pole puste.</span><span class="sxs-lookup"><span data-stu-id="f2d84-155">Can be a managed service resource Id, or the associated client id. To use the SystemAssigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="f2d84-156">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="f2d84-156">-ApplicationId</span></span>
<span data-ttu-id="f2d84-157">NAZWY</span><span class="sxs-lookup"><span data-stu-id="f2d84-157">SPN</span></span>

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

### <span data-ttu-id="f2d84-158">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="f2d84-158">-CertificateThumbprint</span></span>
<span data-ttu-id="f2d84-159">Skrót certyfikatu (odcisk palca)</span><span class="sxs-lookup"><span data-stu-id="f2d84-159">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="f2d84-160">-Ontextname</span><span class="sxs-lookup"><span data-stu-id="f2d84-160">-ContextName</span></span>
<span data-ttu-id="f2d84-161">Nazwa kontekstu domyślnego w tej nazwie logowania.</span><span class="sxs-lookup"><span data-stu-id="f2d84-161">Name of the default context from this login.</span></span>  <span data-ttu-id="f2d84-162">Po zalogowaniu będzie można wybrać ten kontekst według tej nazwy.</span><span class="sxs-lookup"><span data-stu-id="f2d84-162">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="f2d84-163">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="f2d84-163">-Credential</span></span>
<span data-ttu-id="f2d84-164">Określa obiekt PSCredential.</span><span class="sxs-lookup"><span data-stu-id="f2d84-164">Specifies a PSCredential object.</span></span>
<span data-ttu-id="f2d84-165">Aby uzyskać więcej informacji na temat obiektu PSCredential, wpisz Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="f2d84-165">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="f2d84-166">Obiekt PSCredential zapewnia identyfikator użytkownika i hasło dla poświadczeń identyfikatora organizacji lub identyfikator aplikacji oraz klucz tajny dla poświadczeń głównych usługi.</span><span class="sxs-lookup"><span data-stu-id="f2d84-166">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="f2d84-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2d84-167">-DefaultProfile</span></span>
<span data-ttu-id="f2d84-168">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2d84-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2d84-169">-Środowisko</span><span class="sxs-lookup"><span data-stu-id="f2d84-169">-Environment</span></span>
<span data-ttu-id="f2d84-170">Środowisko zawierające konto do logowania</span><span class="sxs-lookup"><span data-stu-id="f2d84-170">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="f2d84-171">-Force</span><span class="sxs-lookup"><span data-stu-id="f2d84-171">-Force</span></span>
<span data-ttu-id="f2d84-172">Zastąp istniejący kontekst o tej samej nazwie (jeśli istnieje).</span><span class="sxs-lookup"><span data-stu-id="f2d84-172">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="f2d84-173">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="f2d84-173">-GraphAccessToken</span></span>
<span data-ttu-id="f2d84-174">AccessToken dla usługi Graph</span><span class="sxs-lookup"><span data-stu-id="f2d84-174">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="f2d84-175">-Identity (tożsamość)</span><span class="sxs-lookup"><span data-stu-id="f2d84-175">-Identity</span></span>
<span data-ttu-id="f2d84-176">Logowanie przy użyciu tożsamości usługi zarządzanej w bieżącym środowisku.</span><span class="sxs-lookup"><span data-stu-id="f2d84-176">Login using managed service identity in the current environment.</span></span>

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

### <span data-ttu-id="f2d84-177">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="f2d84-177">-KeyVaultAccessToken</span></span>
<span data-ttu-id="f2d84-178">AccessToken dla usługi magazynu</span><span class="sxs-lookup"><span data-stu-id="f2d84-178">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="f2d84-179">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="f2d84-179">-ManagedServiceHostName</span></span>
<span data-ttu-id="f2d84-180">Nazwa hosta na potrzeby zarządzanego logowania usługi</span><span class="sxs-lookup"><span data-stu-id="f2d84-180">Host name for managed service login</span></span>

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

### <span data-ttu-id="f2d84-181">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="f2d84-181">-ManagedServicePort</span></span>
<span data-ttu-id="f2d84-182">Numer portu dla zarządzanego logowania usługi</span><span class="sxs-lookup"><span data-stu-id="f2d84-182">Port number for managed service login</span></span>

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

### <span data-ttu-id="f2d84-183">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="f2d84-183">-ManagedServiceSecret</span></span>
<span data-ttu-id="f2d84-184">Klucz tajny, który jest wykorzystywany w przypadku określonych rodzajów logowania zarządzanych usług.</span><span class="sxs-lookup"><span data-stu-id="f2d84-184">Secret, used for some kinds of managed service login.</span></span>

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

### <span data-ttu-id="f2d84-185">-Zakres</span><span class="sxs-lookup"><span data-stu-id="f2d84-185">-Scope</span></span>
<span data-ttu-id="f2d84-186">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f2d84-186">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="f2d84-187">-Serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="f2d84-187">-ServicePrincipal</span></span>
<span data-ttu-id="f2d84-188">Wskazuje, że to konto uwierzytelnia się, dostarczając poświadczenia podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f2d84-188">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="f2d84-189">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="f2d84-189">-SkipContextPopulation</span></span>
<span data-ttu-id="f2d84-190">Pomija populację kontekstu, jeśli nie zostaną znalezione żadne konteksty.</span><span class="sxs-lookup"><span data-stu-id="f2d84-190">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="f2d84-191">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="f2d84-191">-SkipValidation</span></span>
<span data-ttu-id="f2d84-192">Pomijanie sprawdzania poprawności tokenu dostępu</span><span class="sxs-lookup"><span data-stu-id="f2d84-192">Skip validation for access token</span></span>

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

### <span data-ttu-id="f2d84-193">-Subscription</span><span class="sxs-lookup"><span data-stu-id="f2d84-193">-Subscription</span></span>
<span data-ttu-id="f2d84-194">Nazwa lub Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f2d84-194">Subscription Name or ID</span></span>

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

### <span data-ttu-id="f2d84-195">-Dzierżawca</span><span class="sxs-lookup"><span data-stu-id="f2d84-195">-Tenant</span></span>
<span data-ttu-id="f2d84-196">Opcjonalna nazwa lub identyfikator dzierżawy</span><span class="sxs-lookup"><span data-stu-id="f2d84-196">Optional tenant name or ID</span></span>

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

### <span data-ttu-id="f2d84-197">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="f2d84-197">-UseDeviceAuthentication</span></span>
<span data-ttu-id="f2d84-198">Używanie uwierzytelniania kodu urządzenia zamiast kontrolki przeglądarki</span><span class="sxs-lookup"><span data-stu-id="f2d84-198">Use device code authentication instead of a browser control</span></span>

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

### <span data-ttu-id="f2d84-199">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2d84-199">-Confirm</span></span>
<span data-ttu-id="f2d84-200">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2d84-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2d84-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2d84-201">-WhatIf</span></span>
<span data-ttu-id="f2d84-202">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2d84-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2d84-203">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f2d84-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2d84-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d84-204">CommonParameters</span></span>
<span data-ttu-id="f2d84-205">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2d84-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d84-206">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2d84-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d84-207">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2d84-207">INPUTS</span></span>

### <span data-ttu-id="f2d84-208">System. String</span><span class="sxs-lookup"><span data-stu-id="f2d84-208">System.String</span></span>

## <span data-ttu-id="f2d84-209">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2d84-209">OUTPUTS</span></span>

### <span data-ttu-id="f2d84-210">Microsoft. Azure. Commands. profile. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="f2d84-210">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="f2d84-211">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2d84-211">NOTES</span></span>

## <span data-ttu-id="f2d84-212">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2d84-212">RELATED LINKS</span></span>
