---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 0c7e22174b0306a3b9b5a37bd99edeb06f124334
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504179"
---
# <span data-ttu-id="92e7e-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="92e7e-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="92e7e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92e7e-102">SYNOPSIS</span></span>
<span data-ttu-id="92e7e-103">Tworzy konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="92e7e-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="92e7e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92e7e-104">SYNTAX</span></span>

### <span data-ttu-id="92e7e-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="92e7e-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92e7e-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="92e7e-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92e7e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="92e7e-107">DESCRIPTION</span></span>
<span data-ttu-id="92e7e-108">Polecenie cmdlet **New-AzCognitiveServicesAccount** umożliwia utworzenie konta usług poznawczych z określonym typem i magazynem SKU.</span><span class="sxs-lookup"><span data-stu-id="92e7e-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="92e7e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92e7e-109">EXAMPLES</span></span>

### <span data-ttu-id="92e7e-110">1:1</span><span class="sxs-lookup"><span data-stu-id="92e7e-110">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="92e7e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92e7e-111">PARAMETERS</span></span>

### <span data-ttu-id="92e7e-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="92e7e-112">-ApiProperty</span></span>
<span data-ttu-id="92e7e-113">ApiProperties konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="92e7e-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="92e7e-114">Wymagane przez określone typy kont.</span><span class="sxs-lookup"><span data-stu-id="92e7e-114">Required by specific account types.</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e7e-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="92e7e-115">-AssignIdentity</span></span>
<span data-ttu-id="92e7e-116">Wygeneruj i przypisz nową tożsamość konta usług poznawczych dla tego konta magazynu do użycia z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="92e7e-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="92e7e-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="92e7e-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="92e7e-118">Czy chcesz ustawić źródło klucza szyfrowania konta usług poznawczych na Microsoft. CognitiveServices, czy nie.</span><span class="sxs-lookup"><span data-stu-id="92e7e-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CognitiveServicesEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e7e-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="92e7e-119">-CustomSubdomainName</span></span>
<span data-ttu-id="92e7e-120">Nazwa poddomeny konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="92e7e-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="92e7e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e7e-121">-DefaultProfile</span></span>
<span data-ttu-id="92e7e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="92e7e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92e7e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="92e7e-123">-Force</span></span>
<span data-ttu-id="92e7e-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92e7e-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="92e7e-125">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="92e7e-125">-KeyName</span></span>
<span data-ttu-id="92e7e-126">Konto usług poznawczych usługa klucza źródłowego klucza KeyName</span><span class="sxs-lookup"><span data-stu-id="92e7e-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e7e-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="92e7e-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="92e7e-128">Określa, czy skonfigurować źródło klucza szyfrowania konta usług poznawczych w usłudze Microsoft. czy w magazynie.</span><span class="sxs-lookup"><span data-stu-id="92e7e-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="92e7e-129">Jeśli określisz wartość KeyName, wersja klucza i KeyVaultUri, źródłem klucza szyfrowania konta usług poznawczych będzie także Microsoft. Pogoda dla magazynu danych ten parametr jest ustawiony lub nie.</span><span class="sxs-lookup"><span data-stu-id="92e7e-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyVaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e7e-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="92e7e-130">-KeyVaultUri</span></span>
<span data-ttu-id="92e7e-131">Konto usług poznawczych KeyVaultUri magazynie klucza źródłowego klucza</span><span class="sxs-lookup"><span data-stu-id="92e7e-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e7e-132">-Wersja-</span><span class="sxs-lookup"><span data-stu-id="92e7e-132">-KeyVersion</span></span>
<span data-ttu-id="92e7e-133">Konto usług poznawczych usługa klucza źródłowego</span><span class="sxs-lookup"><span data-stu-id="92e7e-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e7e-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="92e7e-134">-Location</span></span>
<span data-ttu-id="92e7e-135">Określa lokalizację, w której ma zostać utworzone konto.</span><span class="sxs-lookup"><span data-stu-id="92e7e-135">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e7e-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="92e7e-136">-Name</span></span>
<span data-ttu-id="92e7e-137">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="92e7e-137">Specifies the name for the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e7e-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="92e7e-138">-NetworkRuleSet</span></span>
<span data-ttu-id="92e7e-139">NetworkRuleSet jest używana do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych oraz do ustawiania wartości właściwości sieci, takich jak obsługa żądań niezgodnych z żadną z zdefiniowanych reguł</span><span class="sxs-lookup"><span data-stu-id="92e7e-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e7e-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="92e7e-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="92e7e-141">Typ dostępu do sieci dla konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="92e7e-141">The network access type for Cognitive Services Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e7e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e7e-142">-ResourceGroupName</span></span>
<span data-ttu-id="92e7e-143">Określa nazwę grupy zasobów, do której ma zostać przypisane konto.</span><span class="sxs-lookup"><span data-stu-id="92e7e-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="92e7e-144">Grupa zasobów musi już istnieć.</span><span class="sxs-lookup"><span data-stu-id="92e7e-144">The resource group must already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e7e-145">-SkuName</span><span class="sxs-lookup"><span data-stu-id="92e7e-145">-SkuName</span></span>
<span data-ttu-id="92e7e-146">Określa jednostkę SKU konta.</span><span class="sxs-lookup"><span data-stu-id="92e7e-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="92e7e-147">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="92e7e-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92e7e-148">F0 (warstwa wolna)</span><span class="sxs-lookup"><span data-stu-id="92e7e-148">F0 (free tier)</span></span>
- <span data-ttu-id="92e7e-149">S0</span><span class="sxs-lookup"><span data-stu-id="92e7e-149">S0</span></span>
- <span data-ttu-id="92e7e-150">S1</span><span class="sxs-lookup"><span data-stu-id="92e7e-150">S1</span></span>
- <span data-ttu-id="92e7e-151">S2</span><span class="sxs-lookup"><span data-stu-id="92e7e-151">S2</span></span>
- <span data-ttu-id="92e7e-152">S3</span><span class="sxs-lookup"><span data-stu-id="92e7e-152">S3</span></span>
- <span data-ttu-id="92e7e-153">S4 Aby uzyskać więcej informacji, zobacz [interfejsy API usług poznawczych](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="92e7e-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e7e-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="92e7e-154">-StorageAccountId</span></span>
<span data-ttu-id="92e7e-155">Lista kont magazynu będących własnością użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92e7e-155">List of User Owned Storage Accounts.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e7e-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="92e7e-156">-Tag</span></span>
<span data-ttu-id="92e7e-157">Określa tag jako parę nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="92e7e-157">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e7e-158">-Type</span><span class="sxs-lookup"><span data-stu-id="92e7e-158">-Type</span></span>
<span data-ttu-id="92e7e-159">Określa typ konta, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="92e7e-159">Specifies the type of account to create.</span></span> <span data-ttu-id="92e7e-160">Użyj `Get-AzCognitiveServicesAccountType` polecenia cmdlet, aby uzyskać bieżące dopuszczalne wartości.</span><span class="sxs-lookup"><span data-stu-id="92e7e-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e7e-161">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92e7e-161">-Confirm</span></span>
<span data-ttu-id="92e7e-162">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92e7e-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92e7e-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92e7e-163">-WhatIf</span></span>
<span data-ttu-id="92e7e-164">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92e7e-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92e7e-165">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="92e7e-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92e7e-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e7e-166">CommonParameters</span></span>
<span data-ttu-id="92e7e-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e7e-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e7e-168">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92e7e-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e7e-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92e7e-169">INPUTS</span></span>

### <span data-ttu-id="92e7e-170">System. String</span><span class="sxs-lookup"><span data-stu-id="92e7e-170">System.String</span></span>

## <span data-ttu-id="92e7e-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92e7e-171">OUTPUTS</span></span>

### <span data-ttu-id="92e7e-172">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="92e7e-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="92e7e-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92e7e-173">NOTES</span></span>

## <span data-ttu-id="92e7e-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92e7e-174">RELATED LINKS</span></span>

[<span data-ttu-id="92e7e-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="92e7e-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="92e7e-176">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="92e7e-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="92e7e-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="92e7e-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
