---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2c995157b56bafb56df7b385c250b6f7c4fdd4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991684"
---
# <span data-ttu-id="37d5a-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="37d5a-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="37d5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="37d5a-103">Modyfikuje konto.</span><span class="sxs-lookup"><span data-stu-id="37d5a-103">Modifies an account.</span></span>

## <span data-ttu-id="37d5a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="37d5a-104">SYNTAX</span></span>

### <span data-ttu-id="37d5a-105">CognitiveServicesEncryption (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="37d5a-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37d5a-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="37d5a-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37d5a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="37d5a-107">DESCRIPTION</span></span>
<span data-ttu-id="37d5a-108">Polecenie **cmdlet Set-AzCognitiveServicesAccount** modyfikuje sku lub tagi określonego konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="37d5a-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="37d5a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="37d5a-109">EXAMPLES</span></span>

### <span data-ttu-id="37d5a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="37d5a-110">Example 1</span></span>
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

## <span data-ttu-id="37d5a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37d5a-111">PARAMETERS</span></span>

### <span data-ttu-id="37d5a-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="37d5a-112">-ApiProperty</span></span>
<span data-ttu-id="37d5a-113">Właściwości ApiProperties konta usług cognitive services.</span><span class="sxs-lookup"><span data-stu-id="37d5a-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="37d5a-114">Wymagane przez określone typy kont.</span><span class="sxs-lookup"><span data-stu-id="37d5a-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="37d5a-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="37d5a-115">-AssignIdentity</span></span>
<span data-ttu-id="37d5a-116">Wygeneruj i przypisz nową tożsamość konta usług Cognitive Services dla tego konta magazynu do użytku z kluczami usług zarządzania, takich jak Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="37d5a-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="37d5a-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="37d5a-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="37d5a-118">Czy ustawić klucz klucza szyfrowania konta usług Cognitive Services na wartość Microsoft.CognitiveServices, czy nie.</span><span class="sxs-lookup"><span data-stu-id="37d5a-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="37d5a-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="37d5a-119">-CustomSubdomainName</span></span>
<span data-ttu-id="37d5a-120">Nazwa poddomeny konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="37d5a-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="37d5a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d5a-121">-DefaultProfile</span></span>
<span data-ttu-id="37d5a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="37d5a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37d5a-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="37d5a-123">-Force</span></span>
<span data-ttu-id="37d5a-124">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="37d5a-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="37d5a-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="37d5a-125">-IdentityType</span></span>
<span data-ttu-id="37d5a-126">Typ tożsamości usługi zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="37d5a-126">Type of managed service identity.</span></span>

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

### <span data-ttu-id="37d5a-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="37d5a-127">-KeyName</span></span>
<span data-ttu-id="37d5a-128">Klucz szyfrowania konta usług Cognitive ServicesSource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="37d5a-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="37d5a-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="37d5a-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="37d5a-130">Czy klucz szyfrowania konta usług Cognitive Services ma być ustawiany na wartość Microsoft.KeyVault, czy nie.</span><span class="sxs-lookup"><span data-stu-id="37d5a-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="37d5a-131">Jeśli określisz kluczNazwę, KeyVersion i KeyVaultUri, źródło klucza szyfrowania konta usług Cognitive Services również zostanie ustawione na pogodę Microsoft.KeyVault dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="37d5a-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="37d5a-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="37d5a-132">-KeyVaultUri</span></span>
<span data-ttu-id="37d5a-133">Klucz szyfrowania konta usług Cognitive ServicesSource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="37d5a-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="37d5a-134">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="37d5a-134">-KeyVersion</span></span>
<span data-ttu-id="37d5a-135">Klucz szyfrowania konta usług Cognitive Services KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="37d5a-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="37d5a-136">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="37d5a-136">-Name</span></span>
<span data-ttu-id="37d5a-137">Określa nazwę konta do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="37d5a-137">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="37d5a-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="37d5a-138">-NetworkRuleSet</span></span>
<span data-ttu-id="37d5a-139">NetworkRuleSet służy do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych, a także do określania wartości właściwości sieciowych, takich jak sposób obsługi żądań, które nie są zgodne z żadnymi zdefiniowanymi regułami</span><span class="sxs-lookup"><span data-stu-id="37d5a-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="37d5a-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="37d5a-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="37d5a-141">Typ dostępu sieciowego dla konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="37d5a-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="37d5a-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37d5a-142">-ResourceGroupName</span></span>
<span data-ttu-id="37d5a-143">Określa nazwę grupy zasobów, do których przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="37d5a-143">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="37d5a-144">-SKUName</span><span class="sxs-lookup"><span data-stu-id="37d5a-144">-SkuName</span></span>
<span data-ttu-id="37d5a-145">Określa sku dla konta.</span><span class="sxs-lookup"><span data-stu-id="37d5a-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="37d5a-146">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="37d5a-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37d5a-147">F0 (bezpłatna warstwa)</span><span class="sxs-lookup"><span data-stu-id="37d5a-147">F0 (free tier)</span></span>
- <span data-ttu-id="37d5a-148">S0</span><span class="sxs-lookup"><span data-stu-id="37d5a-148">S0</span></span>
- <span data-ttu-id="37d5a-149">S1</span><span class="sxs-lookup"><span data-stu-id="37d5a-149">S1</span></span>
- <span data-ttu-id="37d5a-150">S2</span><span class="sxs-lookup"><span data-stu-id="37d5a-150">S2</span></span>
- <span data-ttu-id="37d5a-151">S3</span><span class="sxs-lookup"><span data-stu-id="37d5a-151">S3</span></span>
- <span data-ttu-id="37d5a-152">S4</span><span class="sxs-lookup"><span data-stu-id="37d5a-152">S4</span></span>

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

### <span data-ttu-id="37d5a-153">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="37d5a-153">-StorageAccountId</span></span>
<span data-ttu-id="37d5a-154">Lista kont magazynu należących do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="37d5a-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="37d5a-155">— Tag</span><span class="sxs-lookup"><span data-stu-id="37d5a-155">-Tag</span></span>
<span data-ttu-id="37d5a-156">Określa tag jako parę nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="37d5a-156">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="37d5a-157">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37d5a-157">-Confirm</span></span>
<span data-ttu-id="37d5a-158">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="37d5a-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37d5a-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37d5a-159">-WhatIf</span></span>
<span data-ttu-id="37d5a-160">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37d5a-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37d5a-161">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="37d5a-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37d5a-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d5a-162">CommonParameters</span></span>
<span data-ttu-id="37d5a-163">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37d5a-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d5a-164">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37d5a-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d5a-165">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37d5a-165">INPUTS</span></span>

### <span data-ttu-id="37d5a-166">System.String</span><span class="sxs-lookup"><span data-stu-id="37d5a-166">System.String</span></span>

### <span data-ttu-id="37d5a-167">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="37d5a-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="37d5a-168">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37d5a-168">OUTPUTS</span></span>

### <span data-ttu-id="37d5a-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="37d5a-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="37d5a-170">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="37d5a-170">NOTES</span></span>

## <span data-ttu-id="37d5a-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37d5a-171">RELATED LINKS</span></span>

[<span data-ttu-id="37d5a-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="37d5a-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="37d5a-173">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="37d5a-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="37d5a-174">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="37d5a-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
