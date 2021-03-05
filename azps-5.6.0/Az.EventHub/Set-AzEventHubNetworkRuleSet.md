---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: b8027083225b774d1795d8c96132a0e031f8a51e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007898"
---
# <span data-ttu-id="bfcd3-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="bfcd3-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="bfcd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfcd3-102">SYNOPSIS</span></span>
<span data-ttu-id="bfcd3-103">Zaktualizuj zestaw networkrule danej przestrzeni nazw w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="bfcd3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bfcd3-104">SYNTAX</span></span>

### <span data-ttu-id="bfcd3-105">NetworkRuleSetPropertiesSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="bfcd3-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-TrustedServiceAccessEnabled] [-IPRule] <PSNWRuleSetIpRulesAttributes[]>
 [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfcd3-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bfcd3-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bfcd3-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfcd3-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfcd3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bfcd3-108">DESCRIPTION</span></span>
<span data-ttu-id="bfcd3-109">Zaktualizuj zestaw networkrule danej przestrzeni nazw w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="bfcd3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bfcd3-110">EXAMPLES</span></span>

### <span data-ttu-id="bfcd3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bfcd3-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="bfcd3-112">Nazwa: defaultAction: Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="bfcd3-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="bfcd3-113">Aktualizowanie zestawu NetworkRuleSet przy użyciu parametrów -IPRule i -VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bfcd3-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="bfcd3-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bfcd3-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="bfcd3-115">Nazwa: defaultAction: Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="bfcd3-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="bfcd3-116">Aktualizowanie zestawu NetworkRuleSet przy użyciu funkcji -InputObject</span><span class="sxs-lookup"><span data-stu-id="bfcd3-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="bfcd3-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="bfcd3-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="bfcd3-118">Nazwa: defaultAction: Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="bfcd3-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="bfcd3-119">Zaktualizuj zestaw NetworkRuleSet, używając nazwy -ResourceId innej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="bfcd3-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfcd3-120">PARAMETERS</span></span>

### <span data-ttu-id="bfcd3-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="bfcd3-121">-DefaultAction</span></span>
<span data-ttu-id="bfcd3-122">Akcja domyślna dla zestawu NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="bfcd3-122">Default Action for NetworkRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcd3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfcd3-123">-DefaultProfile</span></span>
<span data-ttu-id="bfcd3-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfcd3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfcd3-125">-InputObject</span></span>
<span data-ttu-id="bfcd3-126">Obiekt konfiguracji zestawu sieci</span><span class="sxs-lookup"><span data-stu-id="bfcd3-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcd3-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="bfcd3-127">-IPRule</span></span>
<span data-ttu-id="bfcd3-128">Lista zestawu IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="bfcd3-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcd3-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bfcd3-129">-Name</span></span>
<span data-ttu-id="bfcd3-130">Nazwa przestrzeni nazw aplikacji EventHub.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-130">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcd3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfcd3-131">-ResourceGroupName</span></span>
<span data-ttu-id="bfcd3-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcd3-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfcd3-133">-ResourceId</span></span>
<span data-ttu-id="bfcd3-134">Identyfikator zasobu przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="bfcd3-134">Resource ID of Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcd3-135">-TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="bfcd3-135">-TrustedServiceAccessEnabled</span></span>
<span data-ttu-id="bfcd3-136">Wskazuje, czy funkcja TrustedServiceAccessEnabled jest włączona.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-136">Indicates whether TrustedServiceAccessEnabled is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcd3-137">— VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bfcd3-137">-VirtualNetworkRule</span></span>
<span data-ttu-id="bfcd3-138">Lista wirtualnych sieci (VirtualNetworkRules)</span><span class="sxs-lookup"><span data-stu-id="bfcd3-138">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcd3-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bfcd3-139">-Confirm</span></span>
<span data-ttu-id="bfcd3-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfcd3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfcd3-141">-WhatIf</span></span>
<span data-ttu-id="bfcd3-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfcd3-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfcd3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfcd3-144">CommonParameters</span></span>
<span data-ttu-id="bfcd3-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bfcd3-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfcd3-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfcd3-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfcd3-147">INPUTS</span></span>

### <span data-ttu-id="bfcd3-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="bfcd3-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="bfcd3-149">System.String</span><span class="sxs-lookup"><span data-stu-id="bfcd3-149">System.String</span></span>

## <span data-ttu-id="bfcd3-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfcd3-150">OUTPUTS</span></span>

### <span data-ttu-id="bfcd3-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="bfcd3-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="bfcd3-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bfcd3-152">NOTES</span></span>

## <span data-ttu-id="bfcd3-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfcd3-153">RELATED LINKS</span></span>