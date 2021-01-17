---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 627519cd4325e7fb9677c358146f2f8a9081151a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376714"
---
# <span data-ttu-id="17577-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="17577-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="17577-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17577-102">SYNOPSIS</span></span>
<span data-ttu-id="17577-103">Dodawanie pojedynczego VirtualNetworkRule do NetworkRuleSet dla danego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="17577-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="17577-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17577-104">SYNTAX</span></span>

### <span data-ttu-id="17577-105">VirtualNetworkRulePropertiesParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="17577-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17577-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17577-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17577-107">Opis</span><span class="sxs-lookup"><span data-stu-id="17577-107">DESCRIPTION</span></span>
<span data-ttu-id="17577-108">Dodawanie pojedynczego VirtualNetworkRule do NetworkRuleSet dla danego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="17577-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="17577-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17577-109">EXAMPLES</span></span>

### <span data-ttu-id="17577-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="17577-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="17577-111">Nazwa: domyślna DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; false}</span><span class="sxs-lookup"><span data-stu-id="17577-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="17577-112">Dodaje określoną podsieć i IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) do NetworkRuleSet dla danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="17577-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="17577-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="17577-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="17577-114">Nazwa: domyślna DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; false}</span><span class="sxs-lookup"><span data-stu-id="17577-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="17577-115">Dodaje $virtualruleset 1 do NetworkRuleSet dla danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="17577-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="17577-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17577-116">PARAMETERS</span></span>

### <span data-ttu-id="17577-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17577-117">-DefaultProfile</span></span>
<span data-ttu-id="17577-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="17577-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17577-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="17577-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="17577-120">Identyfikator ARM w podsieci</span><span class="sxs-lookup"><span data-stu-id="17577-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="17577-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="17577-121">-Name</span></span>
<span data-ttu-id="17577-122">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="17577-122">Namespace Name</span></span>

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

### <span data-ttu-id="17577-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17577-123">-ResourceGroupName</span></span>
<span data-ttu-id="17577-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="17577-124">Resource Group Name</span></span>

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

### <span data-ttu-id="17577-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="17577-125">-SubnetId</span></span>
<span data-ttu-id="17577-126">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="17577-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="17577-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="17577-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="17577-128">Obiekt konfiguracji VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="17577-128">VirtualNetworkRule Configuration Object</span></span>

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

### <span data-ttu-id="17577-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="17577-129">-Confirm</span></span>
<span data-ttu-id="17577-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17577-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17577-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17577-131">-WhatIf</span></span>
<span data-ttu-id="17577-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17577-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17577-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="17577-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17577-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17577-134">CommonParameters</span></span>
<span data-ttu-id="17577-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17577-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="17577-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17577-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17577-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17577-137">INPUTS</span></span>

### <span data-ttu-id="17577-138">System. String</span><span class="sxs-lookup"><span data-stu-id="17577-138">System.String</span></span>

### <span data-ttu-id="17577-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="17577-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="17577-140">Microsoft. Azure. Commands. EventHub. modele. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="17577-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="17577-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17577-141">OUTPUTS</span></span>

### <span data-ttu-id="17577-142">Microsoft. Azure. Commands. EventHub. modele. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="17577-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="17577-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17577-143">NOTES</span></span>

## <span data-ttu-id="17577-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17577-144">RELATED LINKS</span></span>
