---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 79db413fad4fe9a81d206eadf859f3be4f1a83d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708109"
---
# <span data-ttu-id="76448-101">Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="76448-101">Set-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="76448-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76448-102">SYNOPSIS</span></span>
<span data-ttu-id="76448-103">Zaktualizuj NetwrokruleSet danych Namepsace w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="76448-103">Update the NetwrokruleSet of the given Namepsace in the current Azure subscription.</span></span>

## <span data-ttu-id="76448-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76448-104">SYNTAX</span></span>

### <span data-ttu-id="76448-105">NetworkRuleSetPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="76448-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNteworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76448-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="76448-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76448-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76448-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76448-108">Opis</span><span class="sxs-lookup"><span data-stu-id="76448-108">DESCRIPTION</span></span>
<span data-ttu-id="76448-109">Zaktualizuj NetwrokruleSet danych Namepsace w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="76448-109">Update the NetwrokruleSet of the given Namepsace in the current Azure subscription.</span></span>

## <span data-ttu-id="76448-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76448-110">EXAMPLES</span></span>

### <span data-ttu-id="76448-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76448-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\>  Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -IPRule $IpRules -VirtualNteworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="76448-112">Nazwa: domyślna DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; true}</span><span class="sxs-lookup"><span data-stu-id="76448-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="76448-113">Aktualizowanie parametrów NetworkRuleSet-IPRule i-VirtualNteworkRule</span><span class="sxs-lookup"><span data-stu-id="76448-113">Update the NetworkRuleSet using -IPRule and -VirtualNteworkRule parameters</span></span>

### <span data-ttu-id="76448-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="76448-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="76448-115">Nazwa: domyślna DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; true}</span><span class="sxs-lookup"><span data-stu-id="76448-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="76448-116">Aktualizowanie funkcji NetworkRuleSet.-Inputobject</span><span class="sxs-lookup"><span data-stu-id="76448-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="76448-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="76448-117">Example 3</span></span>
```powershell
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```

<span data-ttu-id="76448-118">Nazwa: domyślna DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; true}</span><span class="sxs-lookup"><span data-stu-id="76448-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="76448-119">Zaktualizuj NetworkRuleSet, używając-ResourceId innej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="76448-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="76448-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76448-120">PARAMETERS</span></span>

### <span data-ttu-id="76448-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="76448-121">-DefaultAction</span></span>
<span data-ttu-id="76448-122">Domyślna akcja dla NetwrokeuleSet</span><span class="sxs-lookup"><span data-stu-id="76448-122">Default Action for NetwrokeuleSet</span></span>

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

### <span data-ttu-id="76448-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76448-123">-DefaultProfile</span></span>
<span data-ttu-id="76448-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76448-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76448-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="76448-125">-InputObject</span></span>
<span data-ttu-id="76448-126">Obiekt konfiguracji NetworkruleSet</span><span class="sxs-lookup"><span data-stu-id="76448-126">NetworkruleSet Configuration Object</span></span>

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

### <span data-ttu-id="76448-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="76448-127">-IPRule</span></span>
<span data-ttu-id="76448-128">Lista IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="76448-128">List of IPRuleSet</span></span>

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

### <span data-ttu-id="76448-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76448-129">-Name</span></span>
<span data-ttu-id="76448-130">Nazwa obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="76448-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="76448-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76448-131">-ResourceGroupName</span></span>
<span data-ttu-id="76448-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="76448-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="76448-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76448-133">-ResourceId</span></span>
<span data-ttu-id="76448-134">Identyfikator zasobu w obszarze nazw</span><span class="sxs-lookup"><span data-stu-id="76448-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="76448-135">-VirtualNteworkRule</span><span class="sxs-lookup"><span data-stu-id="76448-135">-VirtualNteworkRule</span></span>
<span data-ttu-id="76448-136">Lista VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="76448-136">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76448-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76448-137">-Confirm</span></span>
<span data-ttu-id="76448-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76448-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76448-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76448-139">-WhatIf</span></span>
<span data-ttu-id="76448-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76448-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76448-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="76448-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76448-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76448-142">CommonParameters</span></span>
<span data-ttu-id="76448-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76448-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="76448-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76448-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76448-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76448-145">INPUTS</span></span>

### <span data-ttu-id="76448-146">Microsoft. Azure. Commands. ServiceBus. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="76448-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="76448-147">System. String</span><span class="sxs-lookup"><span data-stu-id="76448-147">System.String</span></span>

## <span data-ttu-id="76448-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76448-148">OUTPUTS</span></span>

### <span data-ttu-id="76448-149">Microsoft. Azure. Commands. ServiceBus. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="76448-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="76448-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76448-150">NOTES</span></span>

## <span data-ttu-id="76448-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76448-151">RELATED LINKS</span></span>