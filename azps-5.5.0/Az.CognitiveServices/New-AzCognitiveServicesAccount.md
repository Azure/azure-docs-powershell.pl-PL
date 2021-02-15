---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 0c7e22174b0306a3b9b5a37bd99edeb06f124334
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244226"
---
# <span data-ttu-id="c0542-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c0542-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="c0542-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0542-102">SYNOPSIS</span></span>
<span data-ttu-id="c0542-103">Tworzy konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="c0542-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="c0542-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0542-104">SYNTAX</span></span>

### <span data-ttu-id="c0542-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="c0542-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0542-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c0542-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0542-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0542-107">DESCRIPTION</span></span>
<span data-ttu-id="c0542-108">Polecenie **cmdlet New-AzCognitiveServicesAccount** tworzy konto usług Cognitive Services o określonym typie i sku.</span><span class="sxs-lookup"><span data-stu-id="c0542-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="c0542-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0542-109">EXAMPLES</span></span>

### <span data-ttu-id="c0542-110">1:</span><span class="sxs-lookup"><span data-stu-id="c0542-110">1:</span></span>
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

## <span data-ttu-id="c0542-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0542-111">PARAMETERS</span></span>

### <span data-ttu-id="c0542-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="c0542-112">-ApiProperty</span></span>
<span data-ttu-id="c0542-113">Właściwości ApiProperties konta usług cognitive services.</span><span class="sxs-lookup"><span data-stu-id="c0542-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="c0542-114">Wymagane przez określone typy kont.</span><span class="sxs-lookup"><span data-stu-id="c0542-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="c0542-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c0542-115">-AssignIdentity</span></span>
<span data-ttu-id="c0542-116">Wygeneruj i przypisz nową tożsamość konta usług Cognitive Services dla tego konta magazynu do użytku z kluczami usług zarządzania, takich jak Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="c0542-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c0542-117">- CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="c0542-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="c0542-118">Czy ustawić klucz klucza szyfrowania konta usług Cognitive Services na wartość Microsoft.CognitiveServices, czy nie.</span><span class="sxs-lookup"><span data-stu-id="c0542-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="c0542-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="c0542-119">-CustomSubdomainName</span></span>
<span data-ttu-id="c0542-120">Nazwa poddomeny konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="c0542-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="c0542-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0542-121">-DefaultProfile</span></span>
<span data-ttu-id="c0542-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c0542-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0542-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c0542-123">-Force</span></span>
<span data-ttu-id="c0542-124">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c0542-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0542-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c0542-125">-KeyName</span></span>
<span data-ttu-id="c0542-126">Klucz szyfrowania konta usług Cognitive ServicesSource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="c0542-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="c0542-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c0542-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="c0542-128">Czy klucz szyfrowania konta usług Cognitive Services ma być ustawiany na wartość Microsoft.KeyVault, czy nie.</span><span class="sxs-lookup"><span data-stu-id="c0542-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="c0542-129">Jeśli określisz kluczNazwę, KeyVersion i KeyVaultUri, źródło klucza szyfrowania konta usług Cognitive Services również zostanie ustawione na pogodę Microsoft.KeyVault ten parametr jest ustawiony lub nie.</span><span class="sxs-lookup"><span data-stu-id="c0542-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="c0542-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="c0542-130">-KeyVaultUri</span></span>
<span data-ttu-id="c0542-131">Klucz szyfrowania konta usług Cognitive ServicesSource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="c0542-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="c0542-132">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="c0542-132">-KeyVersion</span></span>
<span data-ttu-id="c0542-133">Klucz szyfrowania konta usług Cognitive Services KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="c0542-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="c0542-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c0542-134">-Location</span></span>
<span data-ttu-id="c0542-135">Określa lokalizację utworzenia konta.</span><span class="sxs-lookup"><span data-stu-id="c0542-135">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="c0542-136">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c0542-136">-Name</span></span>
<span data-ttu-id="c0542-137">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="c0542-137">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="c0542-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c0542-138">-NetworkRuleSet</span></span>
<span data-ttu-id="c0542-139">NetworkRuleSet służy do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych, a także do określania wartości właściwości sieciowych, takich jak sposób obsługi żądań, które nie są zgodne z żadnymi zdefiniowanymi regułami</span><span class="sxs-lookup"><span data-stu-id="c0542-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="c0542-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="c0542-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="c0542-141">Typ dostępu sieciowego dla konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="c0542-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="c0542-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0542-142">-ResourceGroupName</span></span>
<span data-ttu-id="c0542-143">Określa nazwę grupy zasobów, do której ma zostać przypisane konto.</span><span class="sxs-lookup"><span data-stu-id="c0542-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="c0542-144">Grupa zasobów musi już istnieć.</span><span class="sxs-lookup"><span data-stu-id="c0542-144">The resource group must already exist.</span></span>

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

### <span data-ttu-id="c0542-145">-SKUName</span><span class="sxs-lookup"><span data-stu-id="c0542-145">-SkuName</span></span>
<span data-ttu-id="c0542-146">Określa sku dla konta.</span><span class="sxs-lookup"><span data-stu-id="c0542-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="c0542-147">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c0542-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c0542-148">F0 (bezpłatna warstwa)</span><span class="sxs-lookup"><span data-stu-id="c0542-148">F0 (free tier)</span></span>
- <span data-ttu-id="c0542-149">S0</span><span class="sxs-lookup"><span data-stu-id="c0542-149">S0</span></span>
- <span data-ttu-id="c0542-150">S1</span><span class="sxs-lookup"><span data-stu-id="c0542-150">S1</span></span>
- <span data-ttu-id="c0542-151">S2</span><span class="sxs-lookup"><span data-stu-id="c0542-151">S2</span></span>
- <span data-ttu-id="c0542-152">S3</span><span class="sxs-lookup"><span data-stu-id="c0542-152">S3</span></span>
- <span data-ttu-id="c0542-153">S4 Aby uzyskać więcej informacji, zobacz [interfejsy API usługi cognitive service.](https://www.microsoft.com/cognitive-services/en-us/apis)</span><span class="sxs-lookup"><span data-stu-id="c0542-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="c0542-154">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c0542-154">-StorageAccountId</span></span>
<span data-ttu-id="c0542-155">Lista kont magazynu należących do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c0542-155">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="c0542-156">— Tag</span><span class="sxs-lookup"><span data-stu-id="c0542-156">-Tag</span></span>
<span data-ttu-id="c0542-157">Określa tag jako parę nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="c0542-157">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="c0542-158">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="c0542-158">-Type</span></span>
<span data-ttu-id="c0542-159">Określa typ konta do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="c0542-159">Specifies the type of account to create.</span></span> <span data-ttu-id="c0542-160">Użyj `Get-AzCognitiveServicesAccountType` polecenia cmdlet, aby uzyskać bieżące dopuszczalne wartości.</span><span class="sxs-lookup"><span data-stu-id="c0542-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="c0542-161">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0542-161">-Confirm</span></span>
<span data-ttu-id="c0542-162">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0542-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0542-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0542-163">-WhatIf</span></span>
<span data-ttu-id="c0542-164">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0542-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0542-165">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c0542-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0542-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0542-166">CommonParameters</span></span>
<span data-ttu-id="c0542-167">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0542-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0542-168">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0542-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0542-169">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0542-169">INPUTS</span></span>

### <span data-ttu-id="c0542-170">System.String</span><span class="sxs-lookup"><span data-stu-id="c0542-170">System.String</span></span>

## <span data-ttu-id="c0542-171">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0542-171">OUTPUTS</span></span>

### <span data-ttu-id="c0542-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c0542-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="c0542-173">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0542-173">NOTES</span></span>

## <span data-ttu-id="c0542-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0542-174">RELATED LINKS</span></span>

[<span data-ttu-id="c0542-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c0542-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="c0542-176">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c0542-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="c0542-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c0542-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
