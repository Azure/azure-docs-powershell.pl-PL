---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 6fef24ebef8417be786896547d43f16b54ea0675
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706501"
---
# <span data-ttu-id="e49d9-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e49d9-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="e49d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e49d9-102">SYNOPSIS</span></span>
<span data-ttu-id="e49d9-103">Usuwanie IpRules lub VirtualNetworkRules z właściwości NetWorkRule konta usług poznawczych</span><span class="sxs-lookup"><span data-stu-id="e49d9-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="e49d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e49d9-104">SYNTAX</span></span>

### <span data-ttu-id="e49d9-105">NetWorkRuleString (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e49d9-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e49d9-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="e49d9-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e49d9-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="e49d9-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e49d9-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="e49d9-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e49d9-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e49d9-109">DESCRIPTION</span></span>
<span data-ttu-id="e49d9-110">Polecenie cmdlet **Remove-AzCognitiveServicesAccountNetworkRule** usuwa IpRules lub VirtualNetworkRules z właściwości NetWorkRule konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="e49d9-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="e49d9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e49d9-111">EXAMPLES</span></span>

### <span data-ttu-id="e49d9-112">Przykład 1: Usuwanie kilku IpRules za pomocą IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e49d9-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="e49d9-113">To polecenie umożliwia usunięcie kilku IpRules z IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="e49d9-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="e49d9-114">Przykład 2: usuwanie VirtualNetworkRule z wejściowym obiektem VirtualNetworkRule w formacie JSON</span><span class="sxs-lookup"><span data-stu-id="e49d9-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="e49d9-115">To polecenie usuwa VirtualNetworkRule z danymi wejściowymi obiektu VirtualNetworkRule w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="e49d9-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="e49d9-116">Przykład 3: usuwanie pierwszego IpRule za pomocą rurociągu</span><span class="sxs-lookup"><span data-stu-id="e49d9-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="e49d9-117">To polecenie usuwa pierwszą IpRule z rurociągiem.</span><span class="sxs-lookup"><span data-stu-id="e49d9-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="e49d9-118">Przykład 4: Usuwanie kilku VirtualNetworkRules za pomocą VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="e49d9-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="e49d9-119">To polecenie umożliwia usunięcie kilku VirtualNetworkRules z VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="e49d9-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="e49d9-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e49d9-120">PARAMETERS</span></span>

### <span data-ttu-id="e49d9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49d9-121">-DefaultProfile</span></span>
<span data-ttu-id="e49d9-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e49d9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e49d9-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e49d9-123">-IpAddressOrRange</span></span>
<span data-ttu-id="e49d9-124">Konto usług poznawczych NetworkRule IpRules IpAddressOrRange w ciągu.</span><span class="sxs-lookup"><span data-stu-id="e49d9-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49d9-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="e49d9-125">-IpRule</span></span>
<span data-ttu-id="e49d9-126">Konto usług poznawczych NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="e49d9-126">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e49d9-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e49d9-127">-Name</span></span>
<span data-ttu-id="e49d9-128">Nazwa konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="e49d9-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="e49d9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e49d9-129">-ResourceGroupName</span></span>
<span data-ttu-id="e49d9-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e49d9-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="e49d9-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e49d9-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="e49d9-132">Konto usług poznawczych NetworkRule VirtualNetworkRules VirtualNetworkResourceId w ciągu.</span><span class="sxs-lookup"><span data-stu-id="e49d9-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49d9-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e49d9-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="e49d9-134">Konto usług poznawczych NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="e49d9-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e49d9-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e49d9-135">-Confirm</span></span>
<span data-ttu-id="e49d9-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e49d9-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49d9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e49d9-137">-WhatIf</span></span>
<span data-ttu-id="e49d9-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e49d9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e49d9-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e49d9-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49d9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49d9-140">CommonParameters</span></span>
<span data-ttu-id="e49d9-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e49d9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49d9-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e49d9-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49d9-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e49d9-143">INPUTS</span></span>

### <span data-ttu-id="e49d9-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e49d9-144">System.String</span></span>

### <span data-ttu-id="e49d9-145">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="e49d9-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="e49d9-146">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="e49d9-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="e49d9-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e49d9-147">OUTPUTS</span></span>

### <span data-ttu-id="e49d9-148">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e49d9-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="e49d9-149">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="e49d9-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="e49d9-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e49d9-150">NOTES</span></span>

## <span data-ttu-id="e49d9-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e49d9-151">RELATED LINKS</span></span>