---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: 3ff1f64bf65a4474dc9f47aa6bd419c442b49698
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197882"
---
# <span data-ttu-id="06f2e-101">Add-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="06f2e-101">Add-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="06f2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="06f2e-103">Dodawanie pojedynczego elementu VirtualNetworkRule do zestawu NetworkRuleSet dla danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="06f2e-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="06f2e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06f2e-104">SYNTAX</span></span>

### <span data-ttu-id="06f2e-105">VirtualNetworkRulePropertiesParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="06f2e-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06f2e-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06f2e-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06f2e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="06f2e-107">DESCRIPTION</span></span>
<span data-ttu-id="06f2e-108">Dodawanie pojedynczego elementu VirtualNetworkRule do zestawu NetworkRuleSet dla danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="06f2e-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="06f2e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06f2e-109">EXAMPLES</span></span>

### <span data-ttu-id="06f2e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="06f2e-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```
<span data-ttu-id="06f2e-111">Nazwa: defaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="06f2e-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="06f2e-112">Dodaje podsieć i ignorujMissingVnetServiceEndpoint (VirtualNetworkRule) do zestawu NetworkRuleSet dla danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="06f2e-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="06f2e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="06f2e-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```
<span data-ttu-id="06f2e-114">Nazwa: defaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="06f2e-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="06f2e-115">Dodaje $virtualruleset 1 do zestawu NetworkRuleSet dla danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="06f2e-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="06f2e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06f2e-116">PARAMETERS</span></span>

### <span data-ttu-id="06f2e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f2e-117">-DefaultProfile</span></span>
<span data-ttu-id="06f2e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06f2e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06f2e-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="06f2e-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="06f2e-120">ARM identyfikator podsieci</span><span class="sxs-lookup"><span data-stu-id="06f2e-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="06f2e-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="06f2e-121">-Name</span></span>
<span data-ttu-id="06f2e-122">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="06f2e-122">Namespace Name</span></span>

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

### <span data-ttu-id="06f2e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06f2e-123">-ResourceGroupName</span></span>
<span data-ttu-id="06f2e-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="06f2e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="06f2e-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="06f2e-125">-SubnetId</span></span>
<span data-ttu-id="06f2e-126">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="06f2e-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="06f2e-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="06f2e-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="06f2e-128">Obiekt konfiguracji VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="06f2e-128">VirtualNetworkRule Configuration Object</span></span>

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

### <span data-ttu-id="06f2e-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06f2e-129">-Confirm</span></span>
<span data-ttu-id="06f2e-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06f2e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06f2e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06f2e-131">-WhatIf</span></span>
<span data-ttu-id="06f2e-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06f2e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06f2e-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="06f2e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06f2e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f2e-134">CommonParameters</span></span>
<span data-ttu-id="06f2e-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06f2e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="06f2e-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06f2e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f2e-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06f2e-137">INPUTS</span></span>

### <span data-ttu-id="06f2e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="06f2e-138">System.String</span></span>

### <span data-ttu-id="06f2e-139">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="06f2e-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="06f2e-140">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="06f2e-140">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="06f2e-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06f2e-141">OUTPUTS</span></span>

### <span data-ttu-id="06f2e-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="06f2e-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="06f2e-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06f2e-143">NOTES</span></span>

## <span data-ttu-id="06f2e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06f2e-144">RELATED LINKS</span></span>