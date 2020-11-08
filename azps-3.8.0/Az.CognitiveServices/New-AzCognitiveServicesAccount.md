---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 713c5cb34133a233bace576ea80035b8e004eb7f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049279"
---
# <span data-ttu-id="2f1bf-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2f1bf-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="2f1bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f1bf-102">SYNOPSIS</span></span>
<span data-ttu-id="2f1bf-103">Tworzy konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="2f1bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f1bf-104">SYNTAX</span></span>

### <span data-ttu-id="2f1bf-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="2f1bf-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f1bf-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="2f1bf-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f1bf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2f1bf-107">DESCRIPTION</span></span>
<span data-ttu-id="2f1bf-108">Polecenie cmdlet **New-AzCognitiveServicesAccount** umożliwia utworzenie konta usług poznawczych z określonym typem i magazynem SKU.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="2f1bf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f1bf-109">EXAMPLES</span></span>

### <span data-ttu-id="2f1bf-110">1:1</span><span class="sxs-lookup"><span data-stu-id="2f1bf-110">1:</span></span>
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

## <span data-ttu-id="2f1bf-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f1bf-111">PARAMETERS</span></span>

### <span data-ttu-id="2f1bf-112">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2f1bf-112">-AssignIdentity</span></span>
<span data-ttu-id="2f1bf-113">Wygeneruj i przypisz nową tożsamość konta usług poznawczych dla tego konta magazynu do użycia z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="2f1bf-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="2f1bf-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="2f1bf-115">Czy chcesz ustawić źródło klucza szyfrowania konta usług poznawczych na Microsoft. CognitiveServices, czy nie.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="2f1bf-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="2f1bf-116">-CustomSubdomainName</span></span>
<span data-ttu-id="2f1bf-117">Nazwa poddomeny konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="2f1bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f1bf-118">-DefaultProfile</span></span>
<span data-ttu-id="2f1bf-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2f1bf-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f1bf-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2f1bf-120">-Force</span></span>
<span data-ttu-id="2f1bf-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2f1bf-122">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="2f1bf-122">-KeyName</span></span>
<span data-ttu-id="2f1bf-123">Konto usług poznawczych usługa klucza źródłowego klucza KeyName</span><span class="sxs-lookup"><span data-stu-id="2f1bf-123">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="2f1bf-124">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="2f1bf-124">-KeyVaultEncryption</span></span>
<span data-ttu-id="2f1bf-125">Określa, czy skonfigurować źródło klucza szyfrowania konta usług poznawczych w usłudze Microsoft. czy w magazynie.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-125">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="2f1bf-126">Jeśli określisz wartość KeyName, wersja klucza i KeyVaultUri, źródłem klucza szyfrowania konta usług poznawczych będzie także Microsoft. Pogoda dla magazynu danych ten parametr jest ustawiony lub nie.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-126">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="2f1bf-127">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="2f1bf-127">-KeyVaultUri</span></span>
<span data-ttu-id="2f1bf-128">Konto usług poznawczych KeyVaultUri magazynie klucza źródłowego klucza</span><span class="sxs-lookup"><span data-stu-id="2f1bf-128">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="2f1bf-129">-Wersja-</span><span class="sxs-lookup"><span data-stu-id="2f1bf-129">-KeyVersion</span></span>
<span data-ttu-id="2f1bf-130">Konto usług poznawczych usługa klucza źródłowego</span><span class="sxs-lookup"><span data-stu-id="2f1bf-130">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="2f1bf-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2f1bf-131">-Location</span></span>
<span data-ttu-id="2f1bf-132">Określa lokalizację, w której ma zostać utworzone konto.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-132">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="2f1bf-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2f1bf-133">-Name</span></span>
<span data-ttu-id="2f1bf-134">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-134">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="2f1bf-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f1bf-135">-NetworkRuleSet</span></span>
<span data-ttu-id="2f1bf-136">NetworkRuleSet jest używana do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych oraz do ustawiania wartości właściwości sieci, takich jak obsługa żądań niezgodnych z żadną z zdefiniowanych reguł</span><span class="sxs-lookup"><span data-stu-id="2f1bf-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="2f1bf-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f1bf-137">-ResourceGroupName</span></span>
<span data-ttu-id="2f1bf-138">Określa nazwę grupy zasobów, do której ma zostać przypisane konto.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-138">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="2f1bf-139">Grupa zasobów musi już istnieć.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-139">The resource group must already exist.</span></span>

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

### <span data-ttu-id="2f1bf-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2f1bf-140">-SkuName</span></span>
<span data-ttu-id="2f1bf-141">Określa jednostkę SKU konta.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-141">Specifies the SKU for the account.</span></span>
<span data-ttu-id="2f1bf-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2f1bf-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2f1bf-143">F0 (warstwa wolna)</span><span class="sxs-lookup"><span data-stu-id="2f1bf-143">F0 (free tier)</span></span>
- <span data-ttu-id="2f1bf-144">S0</span><span class="sxs-lookup"><span data-stu-id="2f1bf-144">S0</span></span>
- <span data-ttu-id="2f1bf-145">S1</span><span class="sxs-lookup"><span data-stu-id="2f1bf-145">S1</span></span>
- <span data-ttu-id="2f1bf-146">S2</span><span class="sxs-lookup"><span data-stu-id="2f1bf-146">S2</span></span>
- <span data-ttu-id="2f1bf-147">S3</span><span class="sxs-lookup"><span data-stu-id="2f1bf-147">S3</span></span>
- <span data-ttu-id="2f1bf-148">S4 Aby uzyskać więcej informacji, zobacz [interfejsy API usług poznawczych](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="2f1bf-148">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="2f1bf-149">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2f1bf-149">-StorageAccountId</span></span>
<span data-ttu-id="2f1bf-150">Lista kont magazynu będących własnością użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-150">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="2f1bf-151">-Tag</span><span class="sxs-lookup"><span data-stu-id="2f1bf-151">-Tag</span></span>
<span data-ttu-id="2f1bf-152">Określa tag jako parę nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-152">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="2f1bf-153">-Type</span><span class="sxs-lookup"><span data-stu-id="2f1bf-153">-Type</span></span>
<span data-ttu-id="2f1bf-154">Określa typ konta, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-154">Specifies the type of account to create.</span></span> <span data-ttu-id="2f1bf-155">Użyj `Get-AzCognitiveServicesAccountType` polecenia cmdlet, aby uzyskać bieżące dopuszczalne wartości.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-155">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="2f1bf-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f1bf-156">-Confirm</span></span>
<span data-ttu-id="2f1bf-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f1bf-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f1bf-158">-WhatIf</span></span>
<span data-ttu-id="2f1bf-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f1bf-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f1bf-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f1bf-161">CommonParameters</span></span>
<span data-ttu-id="2f1bf-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f1bf-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f1bf-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f1bf-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f1bf-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f1bf-164">INPUTS</span></span>

### <span data-ttu-id="2f1bf-165">System. String</span><span class="sxs-lookup"><span data-stu-id="2f1bf-165">System.String</span></span>

## <span data-ttu-id="2f1bf-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f1bf-166">OUTPUTS</span></span>

### <span data-ttu-id="2f1bf-167">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2f1bf-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="2f1bf-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f1bf-168">NOTES</span></span>

## <span data-ttu-id="2f1bf-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f1bf-169">RELATED LINKS</span></span>

[<span data-ttu-id="2f1bf-170">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2f1bf-170">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="2f1bf-171">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2f1bf-171">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="2f1bf-172">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2f1bf-172">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
