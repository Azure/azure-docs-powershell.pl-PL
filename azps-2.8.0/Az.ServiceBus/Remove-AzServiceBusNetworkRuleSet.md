---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: dadabed1a9e78fe44d28eae31adcf70d2aad2ea5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871591"
---
# <span data-ttu-id="9335d-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9335d-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="9335d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9335d-102">SYNOPSIS</span></span>
<span data-ttu-id="9335d-103">Usuwa NetworkRuleSet dla danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="9335d-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="9335d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9335d-104">SYNTAX</span></span>

### <span data-ttu-id="9335d-105">NetworkRuleSetPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9335d-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9335d-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9335d-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9335d-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9335d-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9335d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9335d-108">DESCRIPTION</span></span>
<span data-ttu-id="9335d-109">Usuwa NetworkRuleSet dla danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="9335d-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="9335d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9335d-110">EXAMPLES</span></span>

### <span data-ttu-id="9335d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9335d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="9335d-112">Name: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="9335d-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="9335d-113">Usuwa NetworkRuleSetę dla danej przestrzeni nazw "ServiceBus-Namespace1-1375".</span><span class="sxs-lookup"><span data-stu-id="9335d-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="9335d-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9335d-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="9335d-115">Name: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="9335d-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="9335d-116">Usuwa NetworkRuleSet za pomocą funkcji Inputobject</span><span class="sxs-lookup"><span data-stu-id="9335d-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="9335d-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9335d-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="9335d-118">Name: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="9335d-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="9335d-119">Usuwa NetworkRuleSet za pomocą ResourceId obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="9335d-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="9335d-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9335d-120">PARAMETERS</span></span>

### <span data-ttu-id="9335d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9335d-121">-AsJob</span></span>
<span data-ttu-id="9335d-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9335d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9335d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9335d-123">-DefaultProfile</span></span>
<span data-ttu-id="9335d-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9335d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9335d-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9335d-125">-InputObject</span></span>
<span data-ttu-id="9335d-126">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="9335d-126">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9335d-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9335d-127">-Name</span></span>
<span data-ttu-id="9335d-128">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="9335d-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9335d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9335d-129">-PassThru</span></span>
<span data-ttu-id="9335d-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9335d-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9335d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9335d-131">-ResourceGroupName</span></span>
<span data-ttu-id="9335d-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9335d-132">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9335d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9335d-133">-ResourceId</span></span>
<span data-ttu-id="9335d-134">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="9335d-134">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9335d-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9335d-135">-Confirm</span></span>
<span data-ttu-id="9335d-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9335d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9335d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9335d-137">-WhatIf</span></span>
<span data-ttu-id="9335d-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9335d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9335d-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9335d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9335d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9335d-140">CommonParameters</span></span>
<span data-ttu-id="9335d-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9335d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9335d-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9335d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9335d-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9335d-143">INPUTS</span></span>

### <span data-ttu-id="9335d-144">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="9335d-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="9335d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9335d-145">System.String</span></span>

## <span data-ttu-id="9335d-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9335d-146">OUTPUTS</span></span>

### <span data-ttu-id="9335d-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9335d-147">System.Boolean</span></span>

## <span data-ttu-id="9335d-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9335d-148">NOTES</span></span>

## <span data-ttu-id="9335d-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9335d-149">RELATED LINKS</span></span>
