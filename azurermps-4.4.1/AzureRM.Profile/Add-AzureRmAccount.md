---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
ms.openlocfilehash: 11303438a50839bbe05139888cc665198ed09810
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553171"
---
# <span data-ttu-id="72803-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="72803-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="72803-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72803-102">SYNOPSIS</span></span>
<span data-ttu-id="72803-103">Dodaje uwierzytelnione konto, które będzie używane dla żądań polecenia cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="72803-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72803-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72803-104">SYNTAX</span></span>

### <span data-ttu-id="72803-105">UserWithSubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="72803-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72803-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72803-106">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72803-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72803-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72803-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72803-108">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72803-109">Opis</span><span class="sxs-lookup"><span data-stu-id="72803-109">DESCRIPTION</span></span>
<span data-ttu-id="72803-110">Polecenie cmdlet Add-AzureRmAcccount umożliwia dodanie uwierzytelnionego konta platformy Azure do obsługi żądań polecenia cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="72803-110">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="72803-111">Tego konta można używać tylko z poleceniami cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="72803-111">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="72803-112">Aby dodać uwierzytelnione konto do użycia z poleceniami cmdlet zarządzania usługami, użyj Add-AzureAccount lub polecenia cmdlet Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="72803-112">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="72803-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72803-113">EXAMPLES</span></span>

### <span data-ttu-id="72803-114">Przykład 1. Dodaj konto wymagające interakcyjnego logowania</span><span class="sxs-lookup"><span data-stu-id="72803-114">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="72803-115">To polecenie dodaje konto usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="72803-115">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="72803-116">Aby uruchomić polecenia cmdlet Menedżera zasobów platformy Azure przy użyciu tego konta, w monicie należy podać poświadczenia konta Microsoft lub identyfikatora organizacji.</span><span class="sxs-lookup"><span data-stu-id="72803-116">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="72803-117">Jeśli dla poświadczeń włączono uwierzytelnianie wieloskładnikowe, należy zalogować się przy użyciu opcji interakcyjnej lub użyć uwierzytelniania głównego usługi.</span><span class="sxs-lookup"><span data-stu-id="72803-117">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="72803-118">Przykład 2: Dodawanie konta uwierzytelniającego się za pomocą poświadczeń identyfikatora organizacji</span><span class="sxs-lookup"><span data-stu-id="72803-118">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="72803-119">Pierwsze polecenie uzyskuje poświadczenia użytkownika, a następnie zapisuje je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="72803-119">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="72803-120">Drugie polecenie dodaje konto menedżera zasobów platformy Azure z poświadczeniami w $Credential.</span><span class="sxs-lookup"><span data-stu-id="72803-120">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="72803-121">To konto jest uwierzytelniane za pomocą Menedżera zasobów platformy Azure przy użyciu poświadczeń identyfikatora organizacji.</span><span class="sxs-lookup"><span data-stu-id="72803-121">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="72803-122">Za pomocą tego konta nie można używać uwierzytelniania wieloskładnikowego ani poświadczeń konta Microsoft w celu uruchamiania poleceń cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="72803-122">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="72803-123">Przykład 3: Dodawanie konta uwierzytelniającego się za pomocą poświadczeń podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="72803-123">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="72803-124">Pierwsze polecenie uzyskuje poświadczenia użytkownika, a następnie zapisuje je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="72803-124">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="72803-125">Drugie polecenie dodaje konto menedżera zasobów platformy Azure z poświadczeniami przechowywanymi w $Credential dla określonego dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="72803-125">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="72803-126">Parametr serviceprincipal Switch wskazuje, że konto jest uwierzytelniane jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="72803-126">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="72803-127">Przykład 4: Dodawanie konta dla konkretnej dzierżawy i abonamentu</span><span class="sxs-lookup"><span data-stu-id="72803-127">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="72803-128">To polecenie dodaje konto menedżera zasobów platformy Azure, aby domyślnie uruchamiać polecenia cmdlet dla określonego dzierżawy i abonamentu.</span><span class="sxs-lookup"><span data-stu-id="72803-128">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="72803-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72803-129">PARAMETERS</span></span>

### <span data-ttu-id="72803-130">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="72803-130">-AccessToken</span></span>
<span data-ttu-id="72803-131">Określa token dostępu.</span><span class="sxs-lookup"><span data-stu-id="72803-131">Specifies an access token.</span></span>

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

### <span data-ttu-id="72803-132">-AccountId</span><span class="sxs-lookup"><span data-stu-id="72803-132">-AccountId</span></span>
<span data-ttu-id="72803-133">Identyfikator konta dla tokenu dostępu</span><span class="sxs-lookup"><span data-stu-id="72803-133">Account Id for access token</span></span>

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

### <span data-ttu-id="72803-134">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="72803-134">-ApplicationId</span></span>
<span data-ttu-id="72803-135">NAZWY</span><span class="sxs-lookup"><span data-stu-id="72803-135">SPN</span></span>

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

### <span data-ttu-id="72803-136">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="72803-136">-CertificateThumbprint</span></span>
<span data-ttu-id="72803-137">Skrót certyfikatu (odcisk palca)</span><span class="sxs-lookup"><span data-stu-id="72803-137">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="72803-138">-Ontextname</span><span class="sxs-lookup"><span data-stu-id="72803-138">-ContextName</span></span>
<span data-ttu-id="72803-139">Nazwa kontekstu domyślnego w tej nazwie logowania.</span><span class="sxs-lookup"><span data-stu-id="72803-139">Name of the default context from this login.</span></span>  <span data-ttu-id="72803-140">Po zalogowaniu będzie można wybrać ten kontekst według tej nazwy.</span><span class="sxs-lookup"><span data-stu-id="72803-140">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="72803-141">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="72803-141">-Credential</span></span>
<span data-ttu-id="72803-142">Określa obiekt PSCredential.</span><span class="sxs-lookup"><span data-stu-id="72803-142">Specifies a PSCredential object.</span></span>
<span data-ttu-id="72803-143">Aby uzyskać więcej informacji na temat obiektu PSCredential, wpisz Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="72803-143">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="72803-144">Obiekt PSCredential zapewnia identyfikator użytkownika i hasło dla poświadczeń identyfikatora organizacji lub identyfikator aplikacji oraz klucz tajny dla poświadczeń głównych usługi.</span><span class="sxs-lookup"><span data-stu-id="72803-144">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="72803-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72803-145">-DefaultProfile</span></span>
<span data-ttu-id="72803-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72803-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72803-147">-Środowisko</span><span class="sxs-lookup"><span data-stu-id="72803-147">-Environment</span></span>
<span data-ttu-id="72803-148">Środowisko zawierające konto do logowania</span><span class="sxs-lookup"><span data-stu-id="72803-148">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="72803-149">-Force</span><span class="sxs-lookup"><span data-stu-id="72803-149">-Force</span></span>
<span data-ttu-id="72803-150">Zastąp istniejący kontekst o tej samej nazwie (jeśli istnieje).</span><span class="sxs-lookup"><span data-stu-id="72803-150">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="72803-151">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="72803-151">-GraphAccessToken</span></span>
<span data-ttu-id="72803-152">AccessToken dla usługi Graph</span><span class="sxs-lookup"><span data-stu-id="72803-152">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="72803-153">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="72803-153">-KeyVaultAccessToken</span></span>
<span data-ttu-id="72803-154">AccessToken dla usługi magazynu</span><span class="sxs-lookup"><span data-stu-id="72803-154">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="72803-155">-Zakres</span><span class="sxs-lookup"><span data-stu-id="72803-155">-Scope</span></span>
<span data-ttu-id="72803-156">Określa zakres zmian kontekstu, na przykład wheher zmiany dotyczą tylko procesu cusrrent lub wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="72803-156">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="72803-157">-Serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="72803-157">-ServicePrincipal</span></span>
<span data-ttu-id="72803-158">Wskazuje, że to konto uwierzytelnia się, dostarczając poświadczenia podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="72803-158">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72803-159">-Subscription</span><span class="sxs-lookup"><span data-stu-id="72803-159">-Subscription</span></span>
<span data-ttu-id="72803-160">Nazwa lub Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="72803-160">Subscription Name or ID</span></span>

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

### <span data-ttu-id="72803-161">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="72803-161">-TenantId</span></span>
<span data-ttu-id="72803-162">Opcjonalna nazwa lub identyfikator dzierżawy</span><span class="sxs-lookup"><span data-stu-id="72803-162">Optional tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId
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

### <span data-ttu-id="72803-163">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72803-163">-Confirm</span></span>
<span data-ttu-id="72803-164">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72803-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72803-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72803-165">-WhatIf</span></span>
<span data-ttu-id="72803-166">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72803-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72803-167">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="72803-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72803-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72803-168">CommonParameters</span></span>
<span data-ttu-id="72803-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72803-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72803-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72803-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72803-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72803-171">INPUTS</span></span>

### <span data-ttu-id="72803-172">Ciąg</span><span class="sxs-lookup"><span data-stu-id="72803-172">String</span></span>
<span data-ttu-id="72803-173">Parametr "Identyfikator subskrypcji" akceptuje wartość typu "ciąg" z procesu.</span><span class="sxs-lookup"><span data-stu-id="72803-173">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="72803-174">Ciąg</span><span class="sxs-lookup"><span data-stu-id="72803-174">String</span></span>
<span data-ttu-id="72803-175">Parametr "Subscriptionname" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="72803-175">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="72803-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72803-176">OUTPUTS</span></span>

### <span data-ttu-id="72803-177">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="72803-177">PSAzureProfile</span></span>
<span data-ttu-id="72803-178">Informacje o poświadczeniach, abonamentach, kontach i dzierżawie dla zalogowanego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="72803-178">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="72803-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72803-179">NOTES</span></span>

## <span data-ttu-id="72803-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72803-180">RELATED LINKS</span></span>

