---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: 01cc9210e57edbb19caa8406e9015b36942b99d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525037"
---
# <span data-ttu-id="0083a-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="0083a-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="0083a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0083a-102">SYNOPSIS</span></span>
<span data-ttu-id="0083a-103">Połącz się z usługą Azure za pomocą konta uwierzytelnionego do użycia z żądaniami polecenia cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0083a-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0083a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0083a-104">SYNTAX</span></span>

### <span data-ttu-id="0083a-105">UserWithSubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0083a-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0083a-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0083a-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0083a-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0083a-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0083a-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0083a-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0083a-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="0083a-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0083a-110">Opis</span><span class="sxs-lookup"><span data-stu-id="0083a-110">DESCRIPTION</span></span>
<span data-ttu-id="0083a-111">Polecenie cmdlet Connect-AzureRmAccount łączy się z usługą Azure za pomocą konta uwierzytelnionego do użycia z żądaniami polecenia cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0083a-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="0083a-112">Tego konta można używać tylko z poleceniami cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0083a-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>

<span data-ttu-id="0083a-113">Aby dodać uwierzytelnione konto do użycia z poleceniami cmdlet zarządzania usługami, użyj Add-AzureAccount lub polecenia cmdlet Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="0083a-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

<span data-ttu-id="0083a-114">Po wykonaniu tego polecenia cmdlet możesz rozłączyć się z kontem na platformie Azure, korzystając z funkcji Disconnect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="0083a-114">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="0083a-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0083a-115">EXAMPLES</span></span>

### <span data-ttu-id="0083a-116">Przykład 1. Użyj interakcyjnego logowania, aby połączyć się z kontem platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0083a-116">Example 1: Use an interactive login to connect to an Azure account</span></span>
```
PS C:\> Connect-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="0083a-117">To polecenie nawiązuje połączenie z kontem na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="0083a-117">This command connects to an Azure account.</span></span>

<span data-ttu-id="0083a-118">Aby uruchomić polecenia cmdlet Menedżera zasobów platformy Azure przy użyciu tego konta, w monicie należy podać poświadczenia konta Microsoft lub identyfikatora organizacji.</span><span class="sxs-lookup"><span data-stu-id="0083a-118">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="0083a-119">Jeśli dla poświadczeń włączono uwierzytelnianie wieloskładnikowe, należy zalogować się przy użyciu opcji interakcyjnej lub użyć uwierzytelniania głównego usługi.</span><span class="sxs-lookup"><span data-stu-id="0083a-119">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="0083a-120">Przykład 2: Nawiązywanie połączenia z kontem na platformie Azure przy użyciu poświadczeń identyfikatora organizacji</span><span class="sxs-lookup"><span data-stu-id="0083a-120">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="0083a-121">Pierwsze polecenie uzyskuje poświadczenia użytkownika, a następnie zapisuje je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="0083a-121">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="0083a-122">Drugie polecenie nawiązuje połączenie z kontem na platformie Azure przy użyciu poświadczeń przechowywanych w $Credential.</span><span class="sxs-lookup"><span data-stu-id="0083a-122">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>

<span data-ttu-id="0083a-123">To konto jest uwierzytelniane za pomocą Menedżera zasobów platformy Azure przy użyciu poświadczeń identyfikatora organizacji.</span><span class="sxs-lookup"><span data-stu-id="0083a-123">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>

<span data-ttu-id="0083a-124">Za pomocą tego konta nie można używać uwierzytelniania wieloskładnikowego ani poświadczeń konta Microsoft w celu uruchamiania poleceń cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0083a-124">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="0083a-125">Przykład 3: Nawiązywanie połączenia z kontem głównym usługi Azure</span><span class="sxs-lookup"><span data-stu-id="0083a-125">Example 3: Connect to an Azure service principal account</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="0083a-126">Pierwsze polecenie uzyskuje poświadczenia użytkownika, a następnie zapisuje je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="0083a-126">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="0083a-127">Drugie polecenie nawiązuje połączenie z platformą Azure przy użyciu głównych poświadczeń usługi przechowywanych w $Credential dla określonego dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="0083a-127">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>

<span data-ttu-id="0083a-128">Parametr serviceprincipal Switch wskazuje, że konto jest uwierzytelniane jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="0083a-128">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="0083a-129">Przykład 4: używanie interakcyjnego logowania do nawiązywania połączenia z kontem dla konkretnej dzierżawy i abonamentu</span><span class="sxs-lookup"><span data-stu-id="0083a-129">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="0083a-130">To polecenie nawiązuje połączenie z kontem na platformie Azure i skonfigurowano program AzureRM PowerShell, aby domyślnie uruchamiać polecenia cmdlet dla określonego dzierżawy i abonamentu.</span><span class="sxs-lookup"><span data-stu-id="0083a-130">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="0083a-131">Przykład 5: Dodawanie konta przy użyciu identyfikatora logowania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="0083a-131">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```
PS C:\>Add-AzureRmAccount -MSI
Account: MSI@50342
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="0083a-132">To polecenie loguje się przy użyciu tożsamości usługi zarządzanej dla środowiska hosta (na przykład, jeśli jest wykonywana na VirtualMachine z przypisaną tożsamością hostowanej usługi, umożliwi to logowanie kodu przy użyciu przypisanej tożsamości).</span><span class="sxs-lookup"><span data-stu-id="0083a-132">This command logs in using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

## <span data-ttu-id="0083a-133">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0083a-133">PARAMETERS</span></span>

### <span data-ttu-id="0083a-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="0083a-134">-AccessToken</span></span>
<span data-ttu-id="0083a-135">Określa token dostępu.</span><span class="sxs-lookup"><span data-stu-id="0083a-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="0083a-136">-AccountId</span></span>
<span data-ttu-id="0083a-137">Identyfikator konta dla tokenu dostępu</span><span class="sxs-lookup"><span data-stu-id="0083a-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-138">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="0083a-138">-ApplicationId</span></span>
<span data-ttu-id="0083a-139">NAZWY</span><span class="sxs-lookup"><span data-stu-id="0083a-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="0083a-140">-CertificateThumbprint</span></span>
<span data-ttu-id="0083a-141">Skrót certyfikatu (odcisk palca)</span><span class="sxs-lookup"><span data-stu-id="0083a-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-142">-Ontextname</span><span class="sxs-lookup"><span data-stu-id="0083a-142">-ContextName</span></span>
<span data-ttu-id="0083a-143">Nazwa kontekstu domyślnego w tej nazwie logowania.</span><span class="sxs-lookup"><span data-stu-id="0083a-143">Name of the default context from this login.</span></span>  <span data-ttu-id="0083a-144">Po zalogowaniu będzie można wybrać ten kontekst według tej nazwy.</span><span class="sxs-lookup"><span data-stu-id="0083a-144">You will be able to select this context by this name after login.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-145">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="0083a-145">-Credential</span></span>
<span data-ttu-id="0083a-146">Określa obiekt PSCredential.</span><span class="sxs-lookup"><span data-stu-id="0083a-146">Specifies a PSCredential object.</span></span>
<span data-ttu-id="0083a-147">Aby uzyskać więcej informacji na temat obiektu PSCredential, wpisz Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="0083a-147">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="0083a-148">Obiekt PSCredential zapewnia identyfikator użytkownika i hasło dla poświadczeń identyfikatora organizacji lub identyfikator aplikacji oraz klucz tajny dla poświadczeń głównych usługi.</span><span class="sxs-lookup"><span data-stu-id="0083a-148">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0083a-149">-DefaultProfile</span></span>
<span data-ttu-id="0083a-150">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0083a-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-151">-Środowisko</span><span class="sxs-lookup"><span data-stu-id="0083a-151">-Environment</span></span>
<span data-ttu-id="0083a-152">Środowisko zawierające konto do logowania</span><span class="sxs-lookup"><span data-stu-id="0083a-152">Environment containing the account to log into</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-153">-Force</span><span class="sxs-lookup"><span data-stu-id="0083a-153">-Force</span></span>
<span data-ttu-id="0083a-154">Zastąp istniejący kontekst o tej samej nazwie (jeśli istnieje).</span><span class="sxs-lookup"><span data-stu-id="0083a-154">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-155">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="0083a-155">-GraphAccessToken</span></span>
<span data-ttu-id="0083a-156">AccessToken dla usługi Graph</span><span class="sxs-lookup"><span data-stu-id="0083a-156">AccessToken for Graph Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-157">-Identity (tożsamość)</span><span class="sxs-lookup"><span data-stu-id="0083a-157">-Identity</span></span>
<span data-ttu-id="0083a-158">Logowanie przy użyciu tożsamości usługi zarządzanej w bieżącym środowisku.</span><span class="sxs-lookup"><span data-stu-id="0083a-158">Login using managed service identity in the current environment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-159">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="0083a-159">-KeyVaultAccessToken</span></span>
<span data-ttu-id="0083a-160">AccessToken dla usługi magazynu</span><span class="sxs-lookup"><span data-stu-id="0083a-160">AccessToken for KeyVault Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-161">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="0083a-161">-ManagedServiceHostName</span></span>
<span data-ttu-id="0083a-162">Nazwa hosta na potrzeby zarządzanego logowania usługi</span><span class="sxs-lookup"><span data-stu-id="0083a-162">Host name for managed service login</span></span>

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-163">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="0083a-163">-ManagedServicePort</span></span>
<span data-ttu-id="0083a-164">Numer portu dla zarządzanego logowania usługi</span><span class="sxs-lookup"><span data-stu-id="0083a-164">Port number for managed service login</span></span>

```yaml
Type: Int32
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-165">-Zakres</span><span class="sxs-lookup"><span data-stu-id="0083a-165">-Scope</span></span>
<span data-ttu-id="0083a-166">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0083a-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-167">-Serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="0083a-167">-ServicePrincipal</span></span>
<span data-ttu-id="0083a-168">Wskazuje, że to konto uwierzytelnia się, dostarczając poświadczenia podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="0083a-168">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-169">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="0083a-169">-SkipValidation</span></span>
<span data-ttu-id="0083a-170">Pomijanie sprawdzania poprawności tokenu dostępu</span><span class="sxs-lookup"><span data-stu-id="0083a-170">Skip validation for access token</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-171">-Subscription</span><span class="sxs-lookup"><span data-stu-id="0083a-171">-Subscription</span></span>
<span data-ttu-id="0083a-172">Nazwa lub Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0083a-172">Subscription Name or ID</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-173">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="0083a-173">-TenantId</span></span>
<span data-ttu-id="0083a-174">Opcjonalna nazwa lub identyfikator dzierżawy</span><span class="sxs-lookup"><span data-stu-id="0083a-174">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-175">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0083a-175">-Confirm</span></span>
<span data-ttu-id="0083a-176">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0083a-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0083a-177">-WhatIf</span></span>
<span data-ttu-id="0083a-178">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0083a-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0083a-179">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0083a-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0083a-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0083a-180">CommonParameters</span></span>
<span data-ttu-id="0083a-181">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0083a-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0083a-182">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0083a-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0083a-183">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0083a-183">INPUTS</span></span>

### <span data-ttu-id="0083a-184">Ciąg</span><span class="sxs-lookup"><span data-stu-id="0083a-184">String</span></span>
<span data-ttu-id="0083a-185">Parametr "Identyfikator subskrypcji" akceptuje wartość typu "ciąg" z procesu.</span><span class="sxs-lookup"><span data-stu-id="0083a-185">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="0083a-186">Ciąg</span><span class="sxs-lookup"><span data-stu-id="0083a-186">String</span></span>
<span data-ttu-id="0083a-187">Parametr "Subscriptionname" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="0083a-187">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="0083a-188">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0083a-188">OUTPUTS</span></span>

### <span data-ttu-id="0083a-189">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="0083a-189">PSAzureProfile</span></span>
<span data-ttu-id="0083a-190">Informacje o poświadczeniach, abonamentach, kontach i dzierżawie dla zalogowanego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0083a-190">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="0083a-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0083a-191">NOTES</span></span>

## <span data-ttu-id="0083a-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0083a-192">RELATED LINKS</span></span>

