---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 87f735a098057beb67b76fd4a0f763732c2e816a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183506"
---
# <span data-ttu-id="5566a-101">Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5566a-101">Set-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="5566a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5566a-102">SYNOPSIS</span></span>
<span data-ttu-id="5566a-103">Zaktualizuj zestaw networkrule danej przestrzeni nazw w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5566a-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="5566a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5566a-104">SYNTAX</span></span>

### <span data-ttu-id="5566a-105">NetworkRuleSetPropertiesSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="5566a-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5566a-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5566a-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5566a-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5566a-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5566a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5566a-108">DESCRIPTION</span></span>
<span data-ttu-id="5566a-109">Zaktualizuj zestaw netwrokruleSet owej przestrzeni nazw w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5566a-109">Update the NetwrokruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="5566a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5566a-110">EXAMPLES</span></span>

### <span data-ttu-id="5566a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5566a-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\>  Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="5566a-112">Nazwa: defaultAction: Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="5566a-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="5566a-113">Aktualizowanie zestawu NetworkRuleSet przy użyciu parametrów -IPRule i -VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5566a-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="5566a-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5566a-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="5566a-115">Nazwa: defaultAction: Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="5566a-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="5566a-116">Aktualizowanie zestawu NetworkRuleSet przy użyciu funkcji -InputObject</span><span class="sxs-lookup"><span data-stu-id="5566a-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="5566a-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5566a-117">Example 3</span></span>
```powershell
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```

<span data-ttu-id="5566a-118">Nazwa: defaultAction: Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="5566a-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="5566a-119">Zaktualizuj zestaw NetworkRuleSet, używając nazwy -ResourceId innej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="5566a-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="5566a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5566a-120">PARAMETERS</span></span>

### <span data-ttu-id="5566a-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="5566a-121">-DefaultAction</span></span>
<span data-ttu-id="5566a-122">Akcja domyślna dla zestawu NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5566a-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="5566a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5566a-123">-DefaultProfile</span></span>
<span data-ttu-id="5566a-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5566a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5566a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5566a-125">-InputObject</span></span>
<span data-ttu-id="5566a-126">Obiekt konfiguracji zestawu sieci</span><span class="sxs-lookup"><span data-stu-id="5566a-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5566a-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="5566a-127">-IPRule</span></span>
<span data-ttu-id="5566a-128">Lista zestawu IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="5566a-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5566a-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5566a-129">-Name</span></span>
<span data-ttu-id="5566a-130">Nazwa przestrzeni nazw aplikacji EventHub.</span><span class="sxs-lookup"><span data-stu-id="5566a-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="5566a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5566a-131">-ResourceGroupName</span></span>
<span data-ttu-id="5566a-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5566a-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="5566a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5566a-133">-ResourceId</span></span>
<span data-ttu-id="5566a-134">Identyfikator zasobu przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="5566a-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="5566a-135">- VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5566a-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="5566a-136">Lista elementów VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="5566a-136">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5566a-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5566a-137">-Confirm</span></span>
<span data-ttu-id="5566a-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5566a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5566a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5566a-139">-WhatIf</span></span>
<span data-ttu-id="5566a-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5566a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5566a-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5566a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5566a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5566a-142">CommonParameters</span></span>
<span data-ttu-id="5566a-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5566a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5566a-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5566a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5566a-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5566a-145">INPUTS</span></span>

### <span data-ttu-id="5566a-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="5566a-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="5566a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="5566a-147">System.String</span></span>

## <span data-ttu-id="5566a-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5566a-148">OUTPUTS</span></span>

### <span data-ttu-id="5566a-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="5566a-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="5566a-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5566a-150">NOTES</span></span>

## <span data-ttu-id="5566a-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5566a-151">RELATED LINKS</span></span>