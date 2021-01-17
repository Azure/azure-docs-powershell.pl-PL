---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: d72c7e1ebfdd7543740ea8fafeb62861f4394093
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345709"
---
# <span data-ttu-id="6d8fe-101">Remove-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6d8fe-101">Remove-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="6d8fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d8fe-102">SYNOPSIS</span></span>
<span data-ttu-id="6d8fe-103">Usuwa jedną z podanych VirtualNetworkRule dla NetworkRuleSet obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="6d8fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d8fe-104">SYNTAX</span></span>

### <span data-ttu-id="6d8fe-105">VirtualNetworkRulePropertiesParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6d8fe-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d8fe-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d8fe-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d8fe-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6d8fe-107">DESCRIPTION</span></span>
<span data-ttu-id="6d8fe-108">Usuwa jedną z podanych VirtualNetworkRule dla NetworkRuleSet obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="6d8fe-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d8fe-109">EXAMPLES</span></span>

### <span data-ttu-id="6d8fe-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6d8fe-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="6d8fe-111">Usuwa jedną z podanych VirtualNetworkRule dla NetworkRuleSet obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="6d8fe-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6d8fe-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="6d8fe-113">Usuwanie $virtualruleset 1 z NetworkRuleSet dla danego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="6d8fe-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="6d8fe-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d8fe-114">PARAMETERS</span></span>

### <span data-ttu-id="6d8fe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d8fe-115">-AsJob</span></span>
<span data-ttu-id="6d8fe-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6d8fe-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d8fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d8fe-117">-DefaultProfile</span></span>
<span data-ttu-id="6d8fe-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d8fe-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6d8fe-119">-Name</span></span>
<span data-ttu-id="6d8fe-120">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="6d8fe-120">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d8fe-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d8fe-121">-PassThru</span></span>
<span data-ttu-id="6d8fe-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6d8fe-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6d8fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d8fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="6d8fe-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6d8fe-124">Resource Group Name</span></span>

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

### <span data-ttu-id="6d8fe-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6d8fe-125">-SubnetId</span></span>
<span data-ttu-id="6d8fe-126">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="6d8fe-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d8fe-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="6d8fe-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="6d8fe-128">Obiekt konfiguracji IPRule</span><span class="sxs-lookup"><span data-stu-id="6d8fe-128">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d8fe-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d8fe-129">-Confirm</span></span>
<span data-ttu-id="6d8fe-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d8fe-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d8fe-131">-WhatIf</span></span>
<span data-ttu-id="6d8fe-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d8fe-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d8fe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d8fe-134">CommonParameters</span></span>
<span data-ttu-id="6d8fe-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6d8fe-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d8fe-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d8fe-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d8fe-137">INPUTS</span></span>

### <span data-ttu-id="6d8fe-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6d8fe-138">System.String</span></span>

### <span data-ttu-id="6d8fe-139">Microsoft. Azure. Commands. ServiceBus. models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="6d8fe-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="6d8fe-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d8fe-140">OUTPUTS</span></span>

### <span data-ttu-id="6d8fe-141">Microsoft. Azure. Commands. ServiceBus. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="6d8fe-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="6d8fe-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d8fe-142">NOTES</span></span>

## <span data-ttu-id="6d8fe-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d8fe-143">RELATED LINKS</span></span>
