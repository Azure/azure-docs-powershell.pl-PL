---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 87f735a098057beb67b76fd4a0f763732c2e816a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502864"
---
# <span data-ttu-id="f9257-101">Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9257-101">Set-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="f9257-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9257-102">SYNOPSIS</span></span>
<span data-ttu-id="f9257-103">Zaktualizuj NetworkruleSetę podanej przestrzeni nazw w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f9257-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="f9257-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9257-104">SYNTAX</span></span>

### <span data-ttu-id="f9257-105">NetworkRuleSetPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f9257-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9257-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f9257-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9257-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9257-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9257-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f9257-108">DESCRIPTION</span></span>
<span data-ttu-id="f9257-109">Zaktualizuj NetwrokruleSetę podanej przestrzeni nazw w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f9257-109">Update the NetwrokruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="f9257-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9257-110">EXAMPLES</span></span>

### <span data-ttu-id="f9257-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9257-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\>  Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="f9257-112">Nazwa: domyślna DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; true}</span><span class="sxs-lookup"><span data-stu-id="f9257-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="f9257-113">Aktualizowanie parametrów NetworkRuleSet-IPRule i-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f9257-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="f9257-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f9257-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="f9257-115">Nazwa: domyślna DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; true}</span><span class="sxs-lookup"><span data-stu-id="f9257-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="f9257-116">Aktualizowanie funkcji NetworkRuleSet.-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9257-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="f9257-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f9257-117">Example 3</span></span>
```powershell
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```

<span data-ttu-id="f9257-118">Nazwa: domyślna DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; true}</span><span class="sxs-lookup"><span data-stu-id="f9257-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="f9257-119">Zaktualizuj NetworkRuleSet, używając-ResourceId innej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="f9257-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="f9257-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9257-120">PARAMETERS</span></span>

### <span data-ttu-id="f9257-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="f9257-121">-DefaultAction</span></span>
<span data-ttu-id="f9257-122">Domyślna akcja dla NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9257-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="f9257-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9257-123">-DefaultProfile</span></span>
<span data-ttu-id="f9257-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9257-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9257-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9257-125">-InputObject</span></span>
<span data-ttu-id="f9257-126">Obiekt konfiguracji NetworkruleSet</span><span class="sxs-lookup"><span data-stu-id="f9257-126">NetworkruleSet Configuration Object</span></span>

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

### <span data-ttu-id="f9257-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="f9257-127">-IPRule</span></span>
<span data-ttu-id="f9257-128">Lista IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9257-128">List of IPRuleSet</span></span>

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

### <span data-ttu-id="f9257-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f9257-129">-Name</span></span>
<span data-ttu-id="f9257-130">Nazwa obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="f9257-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="f9257-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9257-131">-ResourceGroupName</span></span>
<span data-ttu-id="f9257-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9257-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="f9257-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9257-133">-ResourceId</span></span>
<span data-ttu-id="f9257-134">Identyfikator zasobu w obszarze nazw</span><span class="sxs-lookup"><span data-stu-id="f9257-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="f9257-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f9257-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="f9257-136">Lista VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="f9257-136">List of VirtualNetworkRules</span></span>

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

### <span data-ttu-id="f9257-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9257-137">-Confirm</span></span>
<span data-ttu-id="f9257-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9257-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9257-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9257-139">-WhatIf</span></span>
<span data-ttu-id="f9257-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9257-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9257-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f9257-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9257-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9257-142">CommonParameters</span></span>
<span data-ttu-id="f9257-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9257-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f9257-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9257-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9257-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9257-145">INPUTS</span></span>

### <span data-ttu-id="f9257-146">Microsoft. Azure. Commands. ServiceBus. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="f9257-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="f9257-147">System. String</span><span class="sxs-lookup"><span data-stu-id="f9257-147">System.String</span></span>

## <span data-ttu-id="f9257-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9257-148">OUTPUTS</span></span>

### <span data-ttu-id="f9257-149">Microsoft. Azure. Commands. ServiceBus. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="f9257-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="f9257-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9257-150">NOTES</span></span>

## <span data-ttu-id="f9257-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9257-151">RELATED LINKS</span></span>