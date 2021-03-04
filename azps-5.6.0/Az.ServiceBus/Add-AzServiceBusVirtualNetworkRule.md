---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/add-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: e4bb2a3020ba2e07fca065f1f70f9d6b4fadee6c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007626"
---
# <span data-ttu-id="c609b-101">Add-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c609b-101">Add-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="c609b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c609b-102">SYNOPSIS</span></span>
<span data-ttu-id="c609b-103">Dodawanie pojedynczego elementu VirtualNetworkRule do zestawu NetworkRuleSet dla danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="c609b-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="c609b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c609b-104">SYNTAX</span></span>

### <span data-ttu-id="c609b-105">VirtualNetworkRulePropertiesParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c609b-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c609b-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c609b-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c609b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c609b-107">DESCRIPTION</span></span>
<span data-ttu-id="c609b-108">Dodawanie pojedynczego elementu VirtualNetworkRule do zestawu NetworkRuleSet dla danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="c609b-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="c609b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c609b-109">EXAMPLES</span></span>

### <span data-ttu-id="c609b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c609b-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```
<span data-ttu-id="c609b-111">Nazwa: defaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="c609b-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="c609b-112">Dodaje podsieć i IgnorujMissingVnetServiceEndpoint (VirtualNetworkRule) do zestawu NetworkRuleSet dla danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="c609b-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="c609b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c609b-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```
<span data-ttu-id="c609b-114">Nazwa: defaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="c609b-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="c609b-115">Dodaje $virtualruleset 1 do zestawu NetworkRuleSet dla danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="c609b-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="c609b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c609b-116">PARAMETERS</span></span>

### <span data-ttu-id="c609b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c609b-117">-DefaultProfile</span></span>
<span data-ttu-id="c609b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c609b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c609b-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c609b-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="c609b-120">ARM identyfikator podsieci</span><span class="sxs-lookup"><span data-stu-id="c609b-120">ARM ID of Subnet</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c609b-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c609b-121">-Name</span></span>
<span data-ttu-id="c609b-122">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="c609b-122">Namespace Name</span></span>

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

### <span data-ttu-id="c609b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c609b-123">-ResourceGroupName</span></span>
<span data-ttu-id="c609b-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c609b-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c609b-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c609b-125">-SubnetId</span></span>
<span data-ttu-id="c609b-126">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="c609b-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="c609b-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="c609b-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="c609b-128">Obiekt konfiguracji VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c609b-128">VirtualNetworkRule Configuration Object</span></span>

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

### <span data-ttu-id="c609b-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c609b-129">-Confirm</span></span>
<span data-ttu-id="c609b-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c609b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c609b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c609b-131">-WhatIf</span></span>
<span data-ttu-id="c609b-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c609b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c609b-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c609b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c609b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c609b-134">CommonParameters</span></span>
<span data-ttu-id="c609b-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c609b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c609b-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c609b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c609b-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c609b-137">INPUTS</span></span>

### <span data-ttu-id="c609b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c609b-138">System.String</span></span>

### <span data-ttu-id="c609b-139">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="c609b-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c609b-140">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="c609b-140">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="c609b-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c609b-141">OUTPUTS</span></span>

### <span data-ttu-id="c609b-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="c609b-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="c609b-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c609b-143">NOTES</span></span>

## <span data-ttu-id="c609b-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c609b-144">RELATED LINKS</span></span>