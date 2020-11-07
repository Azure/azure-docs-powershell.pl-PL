---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: 22389580fba26f977226452037a42d948f957440
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871656"
---
# <span data-ttu-id="99e26-101">Add-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="99e26-101">Add-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="99e26-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99e26-102">SYNOPSIS</span></span>
<span data-ttu-id="99e26-103">Dodawanie pojedynczego VirtualNetworkRule do NetworkRuleSet dla danego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="99e26-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="99e26-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99e26-104">SYNTAX</span></span>

### <span data-ttu-id="99e26-105">VirtualNetworkRulePropertiesParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="99e26-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99e26-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99e26-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99e26-107">Opis</span><span class="sxs-lookup"><span data-stu-id="99e26-107">DESCRIPTION</span></span>
<span data-ttu-id="99e26-108">Dodawanie pojedynczego VirtualNetworkRule do NetworkRuleSet dla danego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="99e26-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="99e26-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99e26-109">EXAMPLES</span></span>

### <span data-ttu-id="99e26-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99e26-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```
<span data-ttu-id="99e26-111">Nazwa: domyślna DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; false}</span><span class="sxs-lookup"><span data-stu-id="99e26-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="99e26-112">Dodaje określoną podsieć i IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) do NetworkRuleSet dla danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="99e26-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="99e26-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="99e26-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```
<span data-ttu-id="99e26-114">Nazwa: domyślna DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; false}</span><span class="sxs-lookup"><span data-stu-id="99e26-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="99e26-115">Dodaje $virtualruleset 1 do NetworkRuleSet dla danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="99e26-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="99e26-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99e26-116">PARAMETERS</span></span>

### <span data-ttu-id="99e26-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e26-117">-DefaultProfile</span></span>
<span data-ttu-id="99e26-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="99e26-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99e26-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="99e26-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="99e26-120">Identyfikator ARM w podsieci</span><span class="sxs-lookup"><span data-stu-id="99e26-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="99e26-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="99e26-121">-Name</span></span>
<span data-ttu-id="99e26-122">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="99e26-122">Namespace Name</span></span>

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

### <span data-ttu-id="99e26-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99e26-123">-ResourceGroupName</span></span>
<span data-ttu-id="99e26-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="99e26-124">Resource Group Name</span></span>

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

### <span data-ttu-id="99e26-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="99e26-125">-SubnetId</span></span>
<span data-ttu-id="99e26-126">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="99e26-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="99e26-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="99e26-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="99e26-128">Obiekt konfiguracji VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="99e26-128">VirtualNetworkRule Configuration Object</span></span>

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

### <span data-ttu-id="99e26-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99e26-129">-Confirm</span></span>
<span data-ttu-id="99e26-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99e26-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99e26-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99e26-131">-WhatIf</span></span>
<span data-ttu-id="99e26-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99e26-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99e26-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="99e26-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99e26-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e26-134">CommonParameters</span></span>
<span data-ttu-id="99e26-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99e26-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="99e26-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99e26-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e26-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99e26-137">INPUTS</span></span>

### <span data-ttu-id="99e26-138">System. String</span><span class="sxs-lookup"><span data-stu-id="99e26-138">System.String</span></span>

### <span data-ttu-id="99e26-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="99e26-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="99e26-140">Microsoft. Azure. Commands. ServiceBus. models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="99e26-140">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="99e26-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99e26-141">OUTPUTS</span></span>

### <span data-ttu-id="99e26-142">Microsoft. Azure. Commands. ServiceBus. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="99e26-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="99e26-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99e26-143">NOTES</span></span>

## <span data-ttu-id="99e26-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99e26-144">RELATED LINKS</span></span>