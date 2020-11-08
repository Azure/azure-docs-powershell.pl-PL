---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 5cfbfa0452fba4d01d2af5aa8e6acc3a141a4426
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220168"
---
# <span data-ttu-id="864ab-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="864ab-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="864ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="864ab-102">SYNOPSIS</span></span>
<span data-ttu-id="864ab-103">Modyfikuje konto.</span><span class="sxs-lookup"><span data-stu-id="864ab-103">Modifies an account.</span></span>

## <span data-ttu-id="864ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="864ab-104">SYNTAX</span></span>

### <span data-ttu-id="864ab-105">CognitiveServicesEncryption (domyślny)</span><span class="sxs-lookup"><span data-stu-id="864ab-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="864ab-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="864ab-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="864ab-107">Opis</span><span class="sxs-lookup"><span data-stu-id="864ab-107">DESCRIPTION</span></span>
<span data-ttu-id="864ab-108">Polecenie cmdlet **Set-AzCognitiveServicesAccount** modyfikuje jednostkę SKU lub Tagi określonego konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="864ab-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="864ab-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="864ab-109">EXAMPLES</span></span>

### <span data-ttu-id="864ab-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="864ab-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="864ab-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="864ab-111">PARAMETERS</span></span>

### <span data-ttu-id="864ab-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="864ab-112">-ApiProperty</span></span>
<span data-ttu-id="864ab-113">ApiProperties konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="864ab-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="864ab-114">Wymagane przez określone typy kont.</span><span class="sxs-lookup"><span data-stu-id="864ab-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="864ab-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="864ab-115">-AssignIdentity</span></span>
<span data-ttu-id="864ab-116">Wygeneruj i przypisz nową tożsamość konta usług poznawczych dla tego konta magazynu do użycia z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="864ab-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="864ab-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="864ab-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="864ab-118">Czy chcesz ustawić źródło klucza szyfrowania konta usług poznawczych na Microsoft. CognitiveServices, czy nie.</span><span class="sxs-lookup"><span data-stu-id="864ab-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="864ab-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="864ab-119">-CustomSubdomainName</span></span>
<span data-ttu-id="864ab-120">Nazwa poddomeny konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="864ab-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="864ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="864ab-121">-DefaultProfile</span></span>
<span data-ttu-id="864ab-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="864ab-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="864ab-123">-Force</span><span class="sxs-lookup"><span data-stu-id="864ab-123">-Force</span></span>
<span data-ttu-id="864ab-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="864ab-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="864ab-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="864ab-125">-IdentityType</span></span>
<span data-ttu-id="864ab-126">Typ zarządzanej tożsamości usługi.</span><span class="sxs-lookup"><span data-stu-id="864ab-126">Type of managed service identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.CognitiveServices.Models.IdentityType]
Parameter Sets: (All)
Aliases:
Accepted values: None, SystemAssigned, UserAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864ab-127">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="864ab-127">-KeyName</span></span>
<span data-ttu-id="864ab-128">Konto usług poznawczych usługa klucza źródłowego klucza KeyName</span><span class="sxs-lookup"><span data-stu-id="864ab-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="864ab-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="864ab-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="864ab-130">Określa, czy skonfigurować źródło klucza szyfrowania konta usług poznawczych w usłudze Microsoft. czy w magazynie.</span><span class="sxs-lookup"><span data-stu-id="864ab-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="864ab-131">Jeśli określisz wartość KeyName, wersja klucza i KeyVaultUri, źródłem klucza szyfrowania konta usług poznawczych będzie także Microsoft. Pogoda dla magazynu danych ten parametr jest ustawiony lub nie.</span><span class="sxs-lookup"><span data-stu-id="864ab-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="864ab-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="864ab-132">-KeyVaultUri</span></span>
<span data-ttu-id="864ab-133">Konto usług poznawczych KeyVaultUri magazynie klucza źródłowego klucza</span><span class="sxs-lookup"><span data-stu-id="864ab-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="864ab-134">-Wersja-</span><span class="sxs-lookup"><span data-stu-id="864ab-134">-KeyVersion</span></span>
<span data-ttu-id="864ab-135">Konto usług poznawczych usługa klucza źródłowego</span><span class="sxs-lookup"><span data-stu-id="864ab-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="864ab-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="864ab-136">-Name</span></span>
<span data-ttu-id="864ab-137">Określa nazwę konta, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="864ab-137">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="864ab-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="864ab-138">-NetworkRuleSet</span></span>
<span data-ttu-id="864ab-139">NetworkRuleSet jest używana do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych oraz do ustawiania wartości właściwości sieci, takich jak obsługa żądań niezgodnych z żadną z zdefiniowanych reguł</span><span class="sxs-lookup"><span data-stu-id="864ab-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="864ab-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="864ab-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="864ab-141">Typ dostępu do sieci dla konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="864ab-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="864ab-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="864ab-142">-ResourceGroupName</span></span>
<span data-ttu-id="864ab-143">Określa nazwę grupy zasobów, do której przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="864ab-143">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="864ab-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="864ab-144">-SkuName</span></span>
<span data-ttu-id="864ab-145">Określa jednostkę SKU konta.</span><span class="sxs-lookup"><span data-stu-id="864ab-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="864ab-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="864ab-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="864ab-147">F0 (warstwa wolna)</span><span class="sxs-lookup"><span data-stu-id="864ab-147">F0 (free tier)</span></span>
- <span data-ttu-id="864ab-148">S0</span><span class="sxs-lookup"><span data-stu-id="864ab-148">S0</span></span>
- <span data-ttu-id="864ab-149">S1</span><span class="sxs-lookup"><span data-stu-id="864ab-149">S1</span></span>
- <span data-ttu-id="864ab-150">S2</span><span class="sxs-lookup"><span data-stu-id="864ab-150">S2</span></span>
- <span data-ttu-id="864ab-151">S3</span><span class="sxs-lookup"><span data-stu-id="864ab-151">S3</span></span>
- <span data-ttu-id="864ab-152">Stanu</span><span class="sxs-lookup"><span data-stu-id="864ab-152">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="864ab-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="864ab-153">-StorageAccountId</span></span>
<span data-ttu-id="864ab-154">Lista kont magazynu będących własnością użytkownika.</span><span class="sxs-lookup"><span data-stu-id="864ab-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="864ab-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="864ab-155">-Tag</span></span>
<span data-ttu-id="864ab-156">Określa tag jako parę nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="864ab-156">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="864ab-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="864ab-157">-Confirm</span></span>
<span data-ttu-id="864ab-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="864ab-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="864ab-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="864ab-159">-WhatIf</span></span>
<span data-ttu-id="864ab-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="864ab-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="864ab-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="864ab-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="864ab-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="864ab-162">CommonParameters</span></span>
<span data-ttu-id="864ab-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="864ab-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="864ab-164">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="864ab-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="864ab-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="864ab-165">INPUTS</span></span>

### <span data-ttu-id="864ab-166">System. String</span><span class="sxs-lookup"><span data-stu-id="864ab-166">System.String</span></span>

### <span data-ttu-id="864ab-167">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="864ab-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="864ab-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="864ab-168">OUTPUTS</span></span>

### <span data-ttu-id="864ab-169">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="864ab-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="864ab-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="864ab-170">NOTES</span></span>

## <span data-ttu-id="864ab-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="864ab-171">RELATED LINKS</span></span>

[<span data-ttu-id="864ab-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="864ab-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="864ab-173">Nowe — AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="864ab-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="864ab-174">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="864ab-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
