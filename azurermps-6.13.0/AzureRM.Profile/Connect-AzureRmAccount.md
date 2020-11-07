---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: a0f29e666a289faddbfce848b97cb0272ce67d0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719071"
---
# <span data-ttu-id="37042-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="37042-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="37042-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37042-102">SYNOPSIS</span></span>
<span data-ttu-id="37042-103">Połącz się z usługą Azure za pomocą konta uwierzytelnionego do użycia z żądaniami polecenia cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="37042-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37042-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37042-104">SYNTAX</span></span>

### <span data-ttu-id="37042-105">UserWithSubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="37042-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37042-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37042-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37042-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37042-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37042-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37042-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37042-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="37042-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37042-110">Opis</span><span class="sxs-lookup"><span data-stu-id="37042-110">DESCRIPTION</span></span>
<span data-ttu-id="37042-111">Polecenie cmdlet Connect-AzureRmAccount łączy się z usługą Azure za pomocą konta uwierzytelnionego do użycia z żądaniami polecenia cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="37042-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="37042-112">Tego konta można używać tylko z poleceniami cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="37042-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="37042-113">Aby dodać uwierzytelnione konto do użycia z poleceniami cmdlet zarządzania usługami, użyj Add-AzureAccount lub polecenia cmdlet Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="37042-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="37042-114">Jeśli nie odnaleziono kontekstu dla bieżącego użytkownika, to polecenie wypełni listę kontekstową użytkownika z kontekstem dla każdej z nich (pierwszych 25) subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="37042-114">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="37042-115">Listę kontekstów utworzonych dla użytkownika można znaleźć, uruchamiając "Get-AzureRmContext-ListAvailable".</span><span class="sxs-lookup"><span data-stu-id="37042-115">The list of contexts created for the user can be found by running "Get-AzureRmContext -ListAvailable".</span></span> <span data-ttu-id="37042-116">Aby pominąć tę populację kontekstu, możesz uruchomić to polecenie za pomocą parametru przełącznika "-SkipContextPopulation".</span><span class="sxs-lookup"><span data-stu-id="37042-116">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="37042-117">Po wykonaniu tego polecenia cmdlet możesz rozłączyć się z kontem na platformie Azure, korzystając z funkcji Disconnect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="37042-117">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="37042-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37042-118">EXAMPLES</span></span>

### <span data-ttu-id="37042-119">Przykład 1. Użyj interakcyjnego logowania, aby połączyć się z kontem platformy Azure</span><span class="sxs-lookup"><span data-stu-id="37042-119">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzureRmAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="37042-120">To polecenie nawiązuje połączenie z kontem na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="37042-120">This command connects to an Azure account.</span></span>
<span data-ttu-id="37042-121">Aby uruchomić polecenia cmdlet Menedżera zasobów platformy Azure przy użyciu tego konta, w monicie należy podać poświadczenia konta Microsoft lub identyfikatora organizacji.</span><span class="sxs-lookup"><span data-stu-id="37042-121">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="37042-122">Jeśli dla poświadczeń włączono uwierzytelnianie wieloskładnikowe, należy zalogować się przy użyciu opcji interakcyjnej lub użyć uwierzytelniania głównego usługi.</span><span class="sxs-lookup"><span data-stu-id="37042-122">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="37042-123">Przykład 2: Nawiązywanie połączenia z kontem na platformie Azure przy użyciu poświadczeń identyfikatora organizacji</span><span class="sxs-lookup"><span data-stu-id="37042-123">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="37042-124">Pierwsze polecenie wyświetli monit o podanie poświadczeń użytkownika (nazwa użytkownika i hasło), a następnie zapisze je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="37042-124">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="37042-125">Drugie polecenie nawiązuje połączenie z kontem na platformie Azure przy użyciu poświadczeń przechowywanych w $Credential.</span><span class="sxs-lookup"><span data-stu-id="37042-125">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="37042-126">To konto jest uwierzytelniane za pomocą Menedżera zasobów platformy Azure przy użyciu poświadczeń identyfikatora organizacji.</span><span class="sxs-lookup"><span data-stu-id="37042-126">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="37042-127">Za pomocą tego konta nie można używać uwierzytelniania wieloskładnikowego ani poświadczeń konta Microsoft w celu uruchamiania poleceń cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="37042-127">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="37042-128">Przykład 3: Nawiązywanie połączenia z kontem głównym usługi Azure</span><span class="sxs-lookup"><span data-stu-id="37042-128">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential

PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="37042-129">Pierwsze polecenie uzyskuje główne poświadczenia usługi (Identyfikator aplikacji i główny klucz tajny usługi), a następnie zapisuje je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="37042-129">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="37042-130">Drugie polecenie nawiązuje połączenie z platformą Azure przy użyciu głównych poświadczeń usługi przechowywanych w $Credential dla określonego dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="37042-130">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="37042-131">Parametr serviceprincipal Switch wskazuje, że konto jest uwierzytelniane jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="37042-131">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="37042-132">Przykład 4: używanie interakcyjnego logowania do nawiązywania połączenia z kontem dla konkretnej dzierżawy i abonamentu</span><span class="sxs-lookup"><span data-stu-id="37042-132">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="37042-133">To polecenie nawiązuje połączenie z kontem na platformie Azure i skonfigurowano program AzureRM PowerShell, aby domyślnie uruchamiać polecenia cmdlet dla określonego dzierżawy i abonamentu.</span><span class="sxs-lookup"><span data-stu-id="37042-133">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="37042-134">Przykład 5: Dodawanie konta przy użyciu identyfikatora logowania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="37042-134">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -MSI

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="37042-135">To polecenie nawiązuje połączenie przy użyciu tożsamości usługi zarządzanej dla środowiska hosta (na przykład w przypadku, gdy w VirtualMachine jest używana tożsamość usługi, która jest skojarzona z daną zarządzaną tożsamością).</span><span class="sxs-lookup"><span data-stu-id="37042-135">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="37042-136">Przykład 6: Dodawanie konta przy użyciu certyfikatów</span><span class="sxs-lookup"><span data-stu-id="37042-136">Example 6: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzureRmAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="37042-137">To polecenie nawiązuje połączenie z kontem na platformie Azure przy użyciu uwierzytelniania głównego usług opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="37042-137">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="37042-138">Theservice podmiot zabezpieczeń używany do uwierzytelniania powinien być utworzony przy użyciu danego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="37042-138">Theservice principal used for authentication should have been created with the given certificate.</span></span>

## <span data-ttu-id="37042-139">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37042-139">PARAMETERS</span></span>

### <span data-ttu-id="37042-140">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="37042-140">-AccessToken</span></span>
<span data-ttu-id="37042-141">Określa token dostępu.</span><span class="sxs-lookup"><span data-stu-id="37042-141">Specifies an access token.</span></span>

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

### <span data-ttu-id="37042-142">-AccountId</span><span class="sxs-lookup"><span data-stu-id="37042-142">-AccountId</span></span>
<span data-ttu-id="37042-143">Identyfikator konta dla tokenu dostępu</span><span class="sxs-lookup"><span data-stu-id="37042-143">Account Id for access token</span></span>

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

### <span data-ttu-id="37042-144">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="37042-144">-ApplicationId</span></span>
<span data-ttu-id="37042-145">NAZWY</span><span class="sxs-lookup"><span data-stu-id="37042-145">SPN</span></span>

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

### <span data-ttu-id="37042-146">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="37042-146">-CertificateThumbprint</span></span>
<span data-ttu-id="37042-147">Skrót certyfikatu (odcisk palca)</span><span class="sxs-lookup"><span data-stu-id="37042-147">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="37042-148">-Ontextname</span><span class="sxs-lookup"><span data-stu-id="37042-148">-ContextName</span></span>
<span data-ttu-id="37042-149">Nazwa kontekstu domyślnego w tej nazwie logowania.</span><span class="sxs-lookup"><span data-stu-id="37042-149">Name of the default context from this login.</span></span>  <span data-ttu-id="37042-150">Po zalogowaniu będzie można wybrać ten kontekst według tej nazwy.</span><span class="sxs-lookup"><span data-stu-id="37042-150">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="37042-151">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="37042-151">-Credential</span></span>
<span data-ttu-id="37042-152">Określa obiekt PSCredential.</span><span class="sxs-lookup"><span data-stu-id="37042-152">Specifies a PSCredential object.</span></span>
<span data-ttu-id="37042-153">Aby uzyskać więcej informacji na temat obiektu PSCredential, wpisz Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="37042-153">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="37042-154">Obiekt PSCredential zapewnia identyfikator użytkownika i hasło dla poświadczeń identyfikatora organizacji lub identyfikator aplikacji oraz klucz tajny dla poświadczeń głównych usługi.</span><span class="sxs-lookup"><span data-stu-id="37042-154">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37042-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37042-155">-DefaultProfile</span></span>
<span data-ttu-id="37042-156">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="37042-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37042-157">-Środowisko</span><span class="sxs-lookup"><span data-stu-id="37042-157">-Environment</span></span>
<span data-ttu-id="37042-158">Środowisko zawierające konto do logowania</span><span class="sxs-lookup"><span data-stu-id="37042-158">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="37042-159">-Force</span><span class="sxs-lookup"><span data-stu-id="37042-159">-Force</span></span>
<span data-ttu-id="37042-160">Zastąp istniejący kontekst o tej samej nazwie (jeśli istnieje).</span><span class="sxs-lookup"><span data-stu-id="37042-160">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="37042-161">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="37042-161">-GraphAccessToken</span></span>
<span data-ttu-id="37042-162">AccessToken dla usługi Graph</span><span class="sxs-lookup"><span data-stu-id="37042-162">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="37042-163">-Identity (tożsamość)</span><span class="sxs-lookup"><span data-stu-id="37042-163">-Identity</span></span>
<span data-ttu-id="37042-164">Logowanie przy użyciu tożsamości usługi zarządzanej w bieżącym środowisku.</span><span class="sxs-lookup"><span data-stu-id="37042-164">Login using managed service identity in the current environment.</span></span>

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

### <span data-ttu-id="37042-165">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="37042-165">-KeyVaultAccessToken</span></span>
<span data-ttu-id="37042-166">AccessToken dla usługi magazynu</span><span class="sxs-lookup"><span data-stu-id="37042-166">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="37042-167">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="37042-167">-ManagedServiceHostName</span></span>
<span data-ttu-id="37042-168">Nazwa hosta na potrzeby zarządzanego logowania usługi</span><span class="sxs-lookup"><span data-stu-id="37042-168">Host name for managed service login</span></span>

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

### <span data-ttu-id="37042-169">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="37042-169">-ManagedServicePort</span></span>
<span data-ttu-id="37042-170">Numer portu dla zarządzanego logowania usługi</span><span class="sxs-lookup"><span data-stu-id="37042-170">Port number for managed service login</span></span>

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

### <span data-ttu-id="37042-171">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="37042-171">-ManagedServiceSecret</span></span>
<span data-ttu-id="37042-172">Klucz tajny, który jest wykorzystywany w przypadku określonych rodzajów logowania zarządzanych usług.</span><span class="sxs-lookup"><span data-stu-id="37042-172">Secret, used for some kinds of managed service login.</span></span>

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

### <span data-ttu-id="37042-173">-Zakres</span><span class="sxs-lookup"><span data-stu-id="37042-173">-Scope</span></span>
<span data-ttu-id="37042-174">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="37042-174">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="37042-175">-Serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="37042-175">-ServicePrincipal</span></span>
<span data-ttu-id="37042-176">Wskazuje, że to konto uwierzytelnia się, dostarczając poświadczenia podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="37042-176">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="37042-177">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="37042-177">-SkipContextPopulation</span></span>
<span data-ttu-id="37042-178">Pomija populację kontekstu, jeśli nie zostaną znalezione żadne konteksty.</span><span class="sxs-lookup"><span data-stu-id="37042-178">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="37042-179">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="37042-179">-SkipValidation</span></span>
<span data-ttu-id="37042-180">Pomijanie sprawdzania poprawności tokenu dostępu</span><span class="sxs-lookup"><span data-stu-id="37042-180">Skip validation for access token</span></span>

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

### <span data-ttu-id="37042-181">-Subscription</span><span class="sxs-lookup"><span data-stu-id="37042-181">-Subscription</span></span>
<span data-ttu-id="37042-182">Nazwa lub Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="37042-182">Subscription Name or ID</span></span>

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

### <span data-ttu-id="37042-183">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="37042-183">-TenantId</span></span>
<span data-ttu-id="37042-184">Opcjonalna nazwa domeny lub identyfikator dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="37042-184">Optional domain name or tenant ID.</span></span> <span data-ttu-id="37042-185">Nazwa domeny nie będzie działać we wszystkich sytuacjach logowania.</span><span class="sxs-lookup"><span data-stu-id="37042-185">Domain name will not work in all sign-in situations.</span></span> <span data-ttu-id="37042-186">W przypadku logowania dostawcy rozwiązań w chmurze (CSP) jest wymagany identyfikator dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="37042-186">For Cloud Solution Provider (CSP) sign-in, tenant ID is required.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37042-187">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37042-187">-Confirm</span></span>
<span data-ttu-id="37042-188">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37042-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37042-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37042-189">-WhatIf</span></span>
<span data-ttu-id="37042-190">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37042-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37042-191">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="37042-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37042-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37042-192">CommonParameters</span></span>
<span data-ttu-id="37042-193">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37042-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37042-194">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37042-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37042-195">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37042-195">INPUTS</span></span>

### <span data-ttu-id="37042-196">System. String</span><span class="sxs-lookup"><span data-stu-id="37042-196">System.String</span></span>
<span data-ttu-id="37042-197">Parametry: subskrypcja (ByValue)</span><span class="sxs-lookup"><span data-stu-id="37042-197">Parameters: Subscription (ByValue)</span></span>

## <span data-ttu-id="37042-198">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37042-198">OUTPUTS</span></span>

### <span data-ttu-id="37042-199">Microsoft. Azure. Commands. profile. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="37042-199">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="37042-200">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37042-200">NOTES</span></span>

## <span data-ttu-id="37042-201">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37042-201">RELATED LINKS</span></span>
