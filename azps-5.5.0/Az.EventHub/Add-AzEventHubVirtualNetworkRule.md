---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 627519cd4325e7fb9677c358146f2f8a9081151a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243651"
---
# <span data-ttu-id="8b914-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8b914-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="8b914-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b914-102">SYNOPSIS</span></span>
<span data-ttu-id="8b914-103">Dodawanie pojedynczego elementu VirtualNetworkRule do zestawu NetworkRuleSet dla danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="8b914-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="8b914-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8b914-104">SYNTAX</span></span>

### <span data-ttu-id="8b914-105">VirtualNetworkRulePropertiesParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8b914-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b914-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b914-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b914-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8b914-107">DESCRIPTION</span></span>
<span data-ttu-id="8b914-108">Dodawanie pojedynczego elementu VirtualNetworkRule do zestawu NetworkRuleSet dla danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="8b914-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="8b914-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8b914-109">EXAMPLES</span></span>

### <span data-ttu-id="8b914-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b914-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="8b914-111">Nazwa: defaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type: Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="8b914-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="8b914-112">Dodaje podsieć i IgnorujMissingVnetServiceEndpoint (VirtualNetworkRule) do zestawu NetworkRuleSet dla danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="8b914-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="8b914-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8b914-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="8b914-114">Nazwa: defaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type: Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="8b914-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="8b914-115">Dodaje $virtualruleset 1 do zestawu NetworkRuleSet dla danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="8b914-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="8b914-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b914-116">PARAMETERS</span></span>

### <span data-ttu-id="8b914-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b914-117">-DefaultProfile</span></span>
<span data-ttu-id="8b914-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b914-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b914-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b914-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="8b914-120">ARM identyfikator podsieci</span><span class="sxs-lookup"><span data-stu-id="8b914-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="8b914-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8b914-121">-Name</span></span>
<span data-ttu-id="8b914-122">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="8b914-122">Namespace Name</span></span>

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

### <span data-ttu-id="8b914-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b914-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b914-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8b914-124">Resource Group Name</span></span>

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

### <span data-ttu-id="8b914-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8b914-125">-SubnetId</span></span>
<span data-ttu-id="8b914-126">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="8b914-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="8b914-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="8b914-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="8b914-128">Obiekt konfiguracji VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8b914-128">VirtualNetworkRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b914-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b914-129">-Confirm</span></span>
<span data-ttu-id="8b914-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8b914-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b914-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b914-131">-WhatIf</span></span>
<span data-ttu-id="8b914-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b914-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b914-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8b914-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b914-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b914-134">CommonParameters</span></span>
<span data-ttu-id="8b914-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b914-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8b914-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b914-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b914-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b914-137">INPUTS</span></span>

### <span data-ttu-id="8b914-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8b914-138">System.String</span></span>

### <span data-ttu-id="8b914-139">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="8b914-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8b914-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="8b914-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="8b914-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b914-141">OUTPUTS</span></span>

### <span data-ttu-id="8b914-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="8b914-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="8b914-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8b914-143">NOTES</span></span>

## <span data-ttu-id="8b914-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b914-144">RELATED LINKS</span></span>
