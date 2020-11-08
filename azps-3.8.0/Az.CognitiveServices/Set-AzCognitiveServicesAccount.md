---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: fc510ebede11168dd8d8b090cd2069ce3e6de52c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049266"
---
# <span data-ttu-id="d51dd-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d51dd-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="d51dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d51dd-102">SYNOPSIS</span></span>
<span data-ttu-id="d51dd-103">Modyfikuje konto.</span><span class="sxs-lookup"><span data-stu-id="d51dd-103">Modifies an account.</span></span>

## <span data-ttu-id="d51dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d51dd-104">SYNTAX</span></span>

### <span data-ttu-id="d51dd-105">CognitiveServicesEncryption (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d51dd-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d51dd-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="d51dd-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d51dd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d51dd-107">DESCRIPTION</span></span>
<span data-ttu-id="d51dd-108">Polecenie cmdlet **Set-AzCognitiveServicesAccount** modyfikuje jednostkę SKU lub Tagi określonego konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="d51dd-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="d51dd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d51dd-109">EXAMPLES</span></span>

### <span data-ttu-id="d51dd-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d51dd-110">Example 1</span></span>
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

## <span data-ttu-id="d51dd-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d51dd-111">PARAMETERS</span></span>

### <span data-ttu-id="d51dd-112">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d51dd-112">-AssignIdentity</span></span>
<span data-ttu-id="d51dd-113">Wygeneruj i przypisz nową tożsamość konta usług poznawczych dla tego konta magazynu do użycia z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d51dd-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="d51dd-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="d51dd-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="d51dd-115">Czy chcesz ustawić źródło klucza szyfrowania konta usług poznawczych na Microsoft. CognitiveServices, czy nie.</span><span class="sxs-lookup"><span data-stu-id="d51dd-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="d51dd-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="d51dd-116">-CustomSubdomainName</span></span>
<span data-ttu-id="d51dd-117">Nazwa poddomeny konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="d51dd-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="d51dd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d51dd-118">-DefaultProfile</span></span>
<span data-ttu-id="d51dd-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d51dd-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d51dd-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d51dd-120">-Force</span></span>
<span data-ttu-id="d51dd-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d51dd-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d51dd-122">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d51dd-122">-IdentityType</span></span>
<span data-ttu-id="d51dd-123">Typ zarządzanej tożsamości usługi.</span><span class="sxs-lookup"><span data-stu-id="d51dd-123">Type of managed service identity.</span></span>

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

### <span data-ttu-id="d51dd-124">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="d51dd-124">-KeyName</span></span>
<span data-ttu-id="d51dd-125">Konto usług poznawczych usługa klucza źródłowego klucza KeyName</span><span class="sxs-lookup"><span data-stu-id="d51dd-125">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="d51dd-126">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="d51dd-126">-KeyVaultEncryption</span></span>
<span data-ttu-id="d51dd-127">Określa, czy skonfigurować źródło klucza szyfrowania konta usług poznawczych w usłudze Microsoft. czy w magazynie.</span><span class="sxs-lookup"><span data-stu-id="d51dd-127">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="d51dd-128">Jeśli określisz wartość KeyName, wersja klucza i KeyVaultUri, źródłem klucza szyfrowania konta usług poznawczych będzie także Microsoft. Pogoda dla magazynu danych ten parametr jest ustawiony lub nie.</span><span class="sxs-lookup"><span data-stu-id="d51dd-128">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="d51dd-129">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="d51dd-129">-KeyVaultUri</span></span>
<span data-ttu-id="d51dd-130">Konto usług poznawczych KeyVaultUri magazynie klucza źródłowego klucza</span><span class="sxs-lookup"><span data-stu-id="d51dd-130">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="d51dd-131">-Wersja-</span><span class="sxs-lookup"><span data-stu-id="d51dd-131">-KeyVersion</span></span>
<span data-ttu-id="d51dd-132">Konto usług poznawczych usługa klucza źródłowego</span><span class="sxs-lookup"><span data-stu-id="d51dd-132">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="d51dd-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d51dd-133">-Name</span></span>
<span data-ttu-id="d51dd-134">Określa nazwę konta, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="d51dd-134">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="d51dd-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d51dd-135">-NetworkRuleSet</span></span>
<span data-ttu-id="d51dd-136">NetworkRuleSet jest używana do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych oraz do ustawiania wartości właściwości sieci, takich jak obsługa żądań niezgodnych z żadną z zdefiniowanych reguł</span><span class="sxs-lookup"><span data-stu-id="d51dd-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="d51dd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d51dd-137">-ResourceGroupName</span></span>
<span data-ttu-id="d51dd-138">Określa nazwę grupy zasobów, do której przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="d51dd-138">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="d51dd-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d51dd-139">-SkuName</span></span>
<span data-ttu-id="d51dd-140">Określa jednostkę SKU konta.</span><span class="sxs-lookup"><span data-stu-id="d51dd-140">Specifies the SKU for the account.</span></span>
<span data-ttu-id="d51dd-141">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d51dd-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d51dd-142">F0 (warstwa wolna)</span><span class="sxs-lookup"><span data-stu-id="d51dd-142">F0 (free tier)</span></span>
- <span data-ttu-id="d51dd-143">S0</span><span class="sxs-lookup"><span data-stu-id="d51dd-143">S0</span></span>
- <span data-ttu-id="d51dd-144">S1</span><span class="sxs-lookup"><span data-stu-id="d51dd-144">S1</span></span>
- <span data-ttu-id="d51dd-145">S2</span><span class="sxs-lookup"><span data-stu-id="d51dd-145">S2</span></span>
- <span data-ttu-id="d51dd-146">S3</span><span class="sxs-lookup"><span data-stu-id="d51dd-146">S3</span></span>
- <span data-ttu-id="d51dd-147">Stanu</span><span class="sxs-lookup"><span data-stu-id="d51dd-147">S4</span></span>

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

### <span data-ttu-id="d51dd-148">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d51dd-148">-StorageAccountId</span></span>
<span data-ttu-id="d51dd-149">Lista kont magazynu będących własnością użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d51dd-149">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="d51dd-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="d51dd-150">-Tag</span></span>
<span data-ttu-id="d51dd-151">Określa tag jako parę nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="d51dd-151">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="d51dd-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d51dd-152">-Confirm</span></span>
<span data-ttu-id="d51dd-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d51dd-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d51dd-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d51dd-154">-WhatIf</span></span>
<span data-ttu-id="d51dd-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d51dd-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d51dd-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d51dd-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d51dd-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d51dd-157">CommonParameters</span></span>
<span data-ttu-id="d51dd-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d51dd-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d51dd-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d51dd-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d51dd-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d51dd-160">INPUTS</span></span>

### <span data-ttu-id="d51dd-161">System. String</span><span class="sxs-lookup"><span data-stu-id="d51dd-161">System.String</span></span>

### <span data-ttu-id="d51dd-162">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="d51dd-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="d51dd-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d51dd-163">OUTPUTS</span></span>

### <span data-ttu-id="d51dd-164">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d51dd-164">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="d51dd-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d51dd-165">NOTES</span></span>

## <span data-ttu-id="d51dd-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d51dd-166">RELATED LINKS</span></span>

[<span data-ttu-id="d51dd-167">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d51dd-167">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="d51dd-168">Nowe — AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d51dd-168">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="d51dd-169">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d51dd-169">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
