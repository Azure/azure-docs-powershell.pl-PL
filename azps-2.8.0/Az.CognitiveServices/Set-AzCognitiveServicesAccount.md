---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 57d136691d6ca0ac9bcd85f205d70cf267437b7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706499"
---
# <span data-ttu-id="fd303-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fd303-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="fd303-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd303-102">SYNOPSIS</span></span>
<span data-ttu-id="fd303-103">Modyfikuje konto.</span><span class="sxs-lookup"><span data-stu-id="fd303-103">Modifies an account.</span></span>

## <span data-ttu-id="fd303-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd303-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd303-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fd303-105">DESCRIPTION</span></span>
<span data-ttu-id="fd303-106">Polecenie cmdlet **Set-AzCognitiveServicesAccount** modyfikuje jednostkę SKU lub Tagi określonego konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="fd303-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="fd303-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd303-107">EXAMPLES</span></span>

### <span data-ttu-id="fd303-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd303-108">Example 1</span></span>
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

## <span data-ttu-id="fd303-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd303-109">PARAMETERS</span></span>

### <span data-ttu-id="fd303-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="fd303-110">-CustomSubdomainName</span></span>
<span data-ttu-id="fd303-111">Nazwa poddomeny konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="fd303-111">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="fd303-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd303-112">-DefaultProfile</span></span>
<span data-ttu-id="fd303-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fd303-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd303-114">-Force</span><span class="sxs-lookup"><span data-stu-id="fd303-114">-Force</span></span>
<span data-ttu-id="fd303-115">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fd303-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fd303-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd303-116">-Name</span></span>
<span data-ttu-id="fd303-117">Określa nazwę konta, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="fd303-117">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="fd303-118">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fd303-118">-NetworkRuleSet</span></span>
<span data-ttu-id="fd303-119">NetworkRuleSet jest używana do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych oraz do ustawiania wartości właściwości sieci, takich jak obsługa żądań niezgodnych z żadną z zdefiniowanych reguł</span><span class="sxs-lookup"><span data-stu-id="fd303-119">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="fd303-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd303-120">-ResourceGroupName</span></span>
<span data-ttu-id="fd303-121">Określa nazwę grupy zasobów, do której przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="fd303-121">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="fd303-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fd303-122">-SkuName</span></span>
<span data-ttu-id="fd303-123">Określa jednostkę SKU konta.</span><span class="sxs-lookup"><span data-stu-id="fd303-123">Specifies the SKU for the account.</span></span>
<span data-ttu-id="fd303-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fd303-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fd303-125">F0 (warstwa wolna)</span><span class="sxs-lookup"><span data-stu-id="fd303-125">F0 (free tier)</span></span>
- <span data-ttu-id="fd303-126">S0</span><span class="sxs-lookup"><span data-stu-id="fd303-126">S0</span></span>
- <span data-ttu-id="fd303-127">S1</span><span class="sxs-lookup"><span data-stu-id="fd303-127">S1</span></span>
- <span data-ttu-id="fd303-128">S2</span><span class="sxs-lookup"><span data-stu-id="fd303-128">S2</span></span>
- <span data-ttu-id="fd303-129">S3</span><span class="sxs-lookup"><span data-stu-id="fd303-129">S3</span></span>
- <span data-ttu-id="fd303-130">Stanu</span><span class="sxs-lookup"><span data-stu-id="fd303-130">S4</span></span>

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

### <span data-ttu-id="fd303-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="fd303-131">-Tag</span></span>
<span data-ttu-id="fd303-132">Określa tag jako parę nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="fd303-132">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="fd303-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd303-133">-Confirm</span></span>
<span data-ttu-id="fd303-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd303-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd303-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd303-135">-WhatIf</span></span>
<span data-ttu-id="fd303-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd303-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd303-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd303-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd303-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd303-138">CommonParameters</span></span>
<span data-ttu-id="fd303-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd303-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd303-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd303-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd303-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd303-141">INPUTS</span></span>

### <span data-ttu-id="fd303-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fd303-142">System.String</span></span>

### <span data-ttu-id="fd303-143">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="fd303-143">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="fd303-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd303-144">OUTPUTS</span></span>

### <span data-ttu-id="fd303-145">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fd303-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="fd303-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd303-146">NOTES</span></span>

## <span data-ttu-id="fd303-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd303-147">RELATED LINKS</span></span>

[<span data-ttu-id="fd303-148">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fd303-148">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="fd303-149">Nowe — AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fd303-149">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="fd303-150">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fd303-150">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
