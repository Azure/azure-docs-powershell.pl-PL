---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 533982757e4ea953c1f5d07ba67ac70af2161a10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523273"
---
# <span data-ttu-id="e65bc-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="e65bc-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="e65bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e65bc-102">SYNOPSIS</span></span>
<span data-ttu-id="e65bc-103">Dodaje uwierzytelnione konto, które będzie używane dla żądań polecenia cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e65bc-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="e65bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e65bc-104">SYNTAX</span></span>

### <span data-ttu-id="e65bc-105">UserWithSubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e65bc-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e65bc-106">UserWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e65bc-106">UserWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e65bc-107">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e65bc-107">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e65bc-108">ServicePrincipalWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e65bc-108">ServicePrincipalWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e65bc-109">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e65bc-109">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e65bc-110">ServicePrincipalCertificateWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e65bc-110">ServicePrincipalCertificateWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e65bc-111">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e65bc-111">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e65bc-112">AccessTokenWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e65bc-112">AccessTokenWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e65bc-113">Opis</span><span class="sxs-lookup"><span data-stu-id="e65bc-113">DESCRIPTION</span></span>
<span data-ttu-id="e65bc-114">Polecenie cmdlet Add-AzureRmAcccount umożliwia dodanie uwierzytelnionego konta platformy Azure do obsługi żądań polecenia cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e65bc-114">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="e65bc-115">Tego konta można używać tylko z poleceniami cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e65bc-115">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="e65bc-116">Aby dodać uwierzytelnione konto do użycia z poleceniami cmdlet zarządzania usługami, użyj Add-AzureAccount lub polecenia cmdlet Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="e65bc-116">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="e65bc-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e65bc-117">EXAMPLES</span></span>

### <span data-ttu-id="e65bc-118">Przykład 1. Dodaj konto wymagające interakcyjnego logowania</span><span class="sxs-lookup"><span data-stu-id="e65bc-118">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="e65bc-119">To polecenie dodaje konto usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="e65bc-119">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="e65bc-120">Aby uruchomić polecenia cmdlet Menedżera zasobów platformy Azure przy użyciu tego konta, w monicie należy podać poświadczenia konta Microsoft lub identyfikatora organizacji.</span><span class="sxs-lookup"><span data-stu-id="e65bc-120">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="e65bc-121">Jeśli dla poświadczeń włączono uwierzytelnianie wieloskładnikowe, należy zalogować się przy użyciu opcji interakcyjnej lub użyć uwierzytelniania głównego usługi.</span><span class="sxs-lookup"><span data-stu-id="e65bc-121">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="e65bc-122">Przykład 2: Dodawanie konta uwierzytelniającego się za pomocą poświadczeń identyfikatora organizacji</span><span class="sxs-lookup"><span data-stu-id="e65bc-122">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="e65bc-123">Pierwsze polecenie uzyskuje poświadczenia użytkownika, a następnie zapisuje je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="e65bc-123">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="e65bc-124">Drugie polecenie dodaje konto menedżera zasobów platformy Azure z poświadczeniami w $Credential.</span><span class="sxs-lookup"><span data-stu-id="e65bc-124">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="e65bc-125">To konto jest uwierzytelniane za pomocą Menedżera zasobów platformy Azure przy użyciu poświadczeń identyfikatora organizacji.</span><span class="sxs-lookup"><span data-stu-id="e65bc-125">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="e65bc-126">Za pomocą tego konta nie można używać uwierzytelniania wieloskładnikowego ani poświadczeń konta Microsoft w celu uruchamiania poleceń cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e65bc-126">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="e65bc-127">Przykład 3: Dodawanie konta uwierzytelniającego się za pomocą poświadczeń podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="e65bc-127">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="e65bc-128">Pierwsze polecenie uzyskuje poświadczenia użytkownika, a następnie zapisuje je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="e65bc-128">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="e65bc-129">Drugie polecenie dodaje konto menedżera zasobów platformy Azure z poświadczeniami przechowywanymi w $Credential dla określonego dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e65bc-129">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="e65bc-130">Parametr serviceprincipal Switch wskazuje, że konto jest uwierzytelniane jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="e65bc-130">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="e65bc-131">Przykład 4: Dodawanie konta dla konkretnej dzierżawy i abonamentu</span><span class="sxs-lookup"><span data-stu-id="e65bc-131">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="e65bc-132">To polecenie dodaje konto menedżera zasobów platformy Azure, aby domyślnie uruchamiać polecenia cmdlet dla określonego dzierżawy i abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e65bc-132">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="e65bc-133">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e65bc-133">PARAMETERS</span></span>

### <span data-ttu-id="e65bc-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="e65bc-134">-AccessToken</span></span>
<span data-ttu-id="e65bc-135">Określa token dostępu.</span><span class="sxs-lookup"><span data-stu-id="e65bc-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e65bc-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="e65bc-136">-AccountId</span></span>
<span data-ttu-id="e65bc-137">Identyfikator konta dla tokenu dostępu</span><span class="sxs-lookup"><span data-stu-id="e65bc-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e65bc-138">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="e65bc-138">-ApplicationId</span></span>
<span data-ttu-id="e65bc-139">NAZWY</span><span class="sxs-lookup"><span data-stu-id="e65bc-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e65bc-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e65bc-140">-CertificateThumbprint</span></span>
<span data-ttu-id="e65bc-141">Skrót certyfikatu (odcisk palca)</span><span class="sxs-lookup"><span data-stu-id="e65bc-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e65bc-142">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="e65bc-142">-Credential</span></span>
<span data-ttu-id="e65bc-143">Określa obiekt PSCredential.</span><span class="sxs-lookup"><span data-stu-id="e65bc-143">Specifies a PSCredential object.</span></span>
<span data-ttu-id="e65bc-144">Aby uzyskać więcej informacji na temat obiektu PSCredential, wpisz Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="e65bc-144">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="e65bc-145">Obiekt PSCredential zapewnia identyfikator użytkownika i hasło dla poświadczeń identyfikatora organizacji lub identyfikator aplikacji oraz klucz tajny dla poświadczeń głównych usługi.</span><span class="sxs-lookup"><span data-stu-id="e65bc-145">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e65bc-146">-Środowisko</span><span class="sxs-lookup"><span data-stu-id="e65bc-146">-Environment</span></span>
<span data-ttu-id="e65bc-147">Środowisko zawierające konto do logowania</span><span class="sxs-lookup"><span data-stu-id="e65bc-147">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="e65bc-148">-Serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="e65bc-148">-ServicePrincipal</span></span>
<span data-ttu-id="e65bc-149">Wskazuje, że to konto uwierzytelnia się, dostarczając poświadczenia podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="e65bc-149">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e65bc-150">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e65bc-150">-SubscriptionId</span></span>
<span data-ttu-id="e65bc-151">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e65bc-151">Specifies the ID of the subscription.</span></span>
<span data-ttu-id="e65bc-152">Jeśli nie określisz tego parametru, zostanie wykorzystana Pierwsza subskrypcja z listy abonamentów.</span><span class="sxs-lookup"><span data-stu-id="e65bc-152">If you do not specify this parameter, the first subscription from the subscription list is used.</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId, AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e65bc-153">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="e65bc-153">-SubscriptionName</span></span>
<span data-ttu-id="e65bc-154">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e65bc-154">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionName, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionName, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e65bc-155">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="e65bc-155">-TenantId</span></span>
<span data-ttu-id="e65bc-156">Opcjonalna nazwa lub identyfikator dzierżawy</span><span class="sxs-lookup"><span data-stu-id="e65bc-156">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName, AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e65bc-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e65bc-157">-Confirm</span></span>
<span data-ttu-id="e65bc-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e65bc-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e65bc-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e65bc-159">-WhatIf</span></span>
<span data-ttu-id="e65bc-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e65bc-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e65bc-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e65bc-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e65bc-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e65bc-162">CommonParameters</span></span>
<span data-ttu-id="e65bc-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e65bc-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e65bc-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e65bc-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e65bc-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e65bc-165">INPUTS</span></span>

## <span data-ttu-id="e65bc-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e65bc-166">OUTPUTS</span></span>

### <span data-ttu-id="e65bc-167">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="e65bc-167">PSAzureProfile</span></span>

## <span data-ttu-id="e65bc-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e65bc-168">NOTES</span></span>

## <span data-ttu-id="e65bc-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e65bc-169">RELATED LINKS</span></span>

