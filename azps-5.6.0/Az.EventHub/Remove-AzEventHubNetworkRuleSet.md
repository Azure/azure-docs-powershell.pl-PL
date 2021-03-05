---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9f82f3ac02e9acaf7e715ffb1eeb8c15fa4af3b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012154"
---
# <span data-ttu-id="99801-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="99801-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="99801-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99801-102">SYNOPSIS</span></span>
<span data-ttu-id="99801-103">Usuwa zestaw networkruleset dla danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="99801-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="99801-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="99801-104">SYNTAX</span></span>

### <span data-ttu-id="99801-105">NetworkRuleSetPropertiesSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="99801-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99801-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="99801-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99801-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="99801-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99801-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="99801-108">DESCRIPTION</span></span>
<span data-ttu-id="99801-109">Usuwa zestaw networkruleset dla danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="99801-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="99801-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="99801-110">EXAMPLES</span></span>

### <span data-ttu-id="99801-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99801-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="99801-112">Nazwa: defaultAction: Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="99801-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="99801-113">Usuwa zestaw NetworkRuleSet dla danej przestrzeni nazw "Eventhub-Namespace1-1375"</span><span class="sxs-lookup"><span data-stu-id="99801-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="99801-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="99801-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="99801-115">Usuwa zestaw NetworkRuleSet przy użyciu inputObject</span><span class="sxs-lookup"><span data-stu-id="99801-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="99801-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="99801-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="99801-117">Nazwa: defaultAction: Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="99801-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="99801-118">Usuwa zestaw NetworkRuleSet przy użyciu funkcji ResourceId przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="99801-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="99801-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99801-119">PARAMETERS</span></span>

### <span data-ttu-id="99801-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="99801-120">-AsJob</span></span>
<span data-ttu-id="99801-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="99801-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99801-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99801-122">-DefaultProfile</span></span>
<span data-ttu-id="99801-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="99801-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99801-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99801-124">-InputObject</span></span>
<span data-ttu-id="99801-125">Obiekt Przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="99801-125">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99801-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="99801-126">-Name</span></span>
<span data-ttu-id="99801-127">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="99801-127">Namespace Name</span></span>

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

### <span data-ttu-id="99801-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99801-128">-PassThru</span></span>
<span data-ttu-id="99801-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="99801-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="99801-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99801-130">-ResourceGroupName</span></span>
<span data-ttu-id="99801-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="99801-131">Resource Group Name</span></span>

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

### <span data-ttu-id="99801-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99801-132">-ResourceId</span></span>
<span data-ttu-id="99801-133">Identyfikator zasobu przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="99801-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="99801-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99801-134">-Confirm</span></span>
<span data-ttu-id="99801-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="99801-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99801-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99801-136">-WhatIf</span></span>
<span data-ttu-id="99801-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99801-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99801-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="99801-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99801-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99801-139">CommonParameters</span></span>
<span data-ttu-id="99801-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99801-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="99801-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99801-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99801-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99801-142">INPUTS</span></span>

### <span data-ttu-id="99801-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="99801-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="99801-144">System.String</span><span class="sxs-lookup"><span data-stu-id="99801-144">System.String</span></span>

## <span data-ttu-id="99801-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99801-145">OUTPUTS</span></span>

### <span data-ttu-id="99801-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="99801-146">System.Boolean</span></span>

## <span data-ttu-id="99801-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="99801-147">NOTES</span></span>

## <span data-ttu-id="99801-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99801-148">RELATED LINKS</span></span>