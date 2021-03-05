---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 339569d3415edadbf284f904358f889e7210267a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015985"
---
# <span data-ttu-id="26bb3-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="26bb3-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="26bb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="26bb3-103">Usuwa zestaw networkruleset dla danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="26bb3-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="26bb3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="26bb3-104">SYNTAX</span></span>

### <span data-ttu-id="26bb3-105">NetworkRuleSetPropertiesSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="26bb3-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26bb3-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="26bb3-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26bb3-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26bb3-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26bb3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="26bb3-108">DESCRIPTION</span></span>
<span data-ttu-id="26bb3-109">Usuwa zestaw networkruleset dla danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="26bb3-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="26bb3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="26bb3-110">EXAMPLES</span></span>

### <span data-ttu-id="26bb3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="26bb3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="26bb3-112">Nazwa: defaultAction: Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="26bb3-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="26bb3-113">Usuwa zestaw networkruleset dla danej przestrzeni nazw "ServiceBus-Namespace1-1375"</span><span class="sxs-lookup"><span data-stu-id="26bb3-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="26bb3-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="26bb3-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="26bb3-115">Nazwa: defaultAction: Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="26bb3-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="26bb3-116">Usuwa zestaw NetworkRuleSet przy użyciu inputObject</span><span class="sxs-lookup"><span data-stu-id="26bb3-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="26bb3-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="26bb3-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="26bb3-118">Nazwa: defaultAction: Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="26bb3-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="26bb3-119">Usuwa zestaw NetworkRuleSet przy użyciu funkcji ResourceId przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="26bb3-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="26bb3-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26bb3-120">PARAMETERS</span></span>

### <span data-ttu-id="26bb3-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="26bb3-121">-AsJob</span></span>
<span data-ttu-id="26bb3-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="26bb3-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26bb3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26bb3-123">-DefaultProfile</span></span>
<span data-ttu-id="26bb3-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="26bb3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26bb3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26bb3-125">-InputObject</span></span>
<span data-ttu-id="26bb3-126">Obiekt Przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="26bb3-126">Namespace Object</span></span>

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

### <span data-ttu-id="26bb3-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="26bb3-127">-Name</span></span>
<span data-ttu-id="26bb3-128">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="26bb3-128">Namespace Name</span></span>

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

### <span data-ttu-id="26bb3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26bb3-129">-PassThru</span></span>
<span data-ttu-id="26bb3-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="26bb3-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="26bb3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26bb3-131">-ResourceGroupName</span></span>
<span data-ttu-id="26bb3-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="26bb3-132">Resource Group Name</span></span>

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

### <span data-ttu-id="26bb3-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26bb3-133">-ResourceId</span></span>
<span data-ttu-id="26bb3-134">Identyfikator zasobu przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="26bb3-134">Namespace Resource Id</span></span>

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

### <span data-ttu-id="26bb3-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26bb3-135">-Confirm</span></span>
<span data-ttu-id="26bb3-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="26bb3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26bb3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26bb3-137">-WhatIf</span></span>
<span data-ttu-id="26bb3-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26bb3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26bb3-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="26bb3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26bb3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26bb3-140">CommonParameters</span></span>
<span data-ttu-id="26bb3-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26bb3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="26bb3-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26bb3-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26bb3-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26bb3-143">INPUTS</span></span>

### <span data-ttu-id="26bb3-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="26bb3-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="26bb3-145">System.String</span><span class="sxs-lookup"><span data-stu-id="26bb3-145">System.String</span></span>

## <span data-ttu-id="26bb3-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26bb3-146">OUTPUTS</span></span>

### <span data-ttu-id="26bb3-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26bb3-147">System.Boolean</span></span>

## <span data-ttu-id="26bb3-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="26bb3-148">NOTES</span></span>

## <span data-ttu-id="26bb3-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26bb3-149">RELATED LINKS</span></span>
