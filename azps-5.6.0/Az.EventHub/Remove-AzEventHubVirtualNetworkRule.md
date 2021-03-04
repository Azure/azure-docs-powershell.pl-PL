---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 3d8221d36cdd6ec0845f3f26dfe1526f796c2213
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990291"
---
# <span data-ttu-id="f3875-101">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f3875-101">Remove-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="f3875-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3875-102">SYNOPSIS</span></span>
<span data-ttu-id="f3875-103">Usuwa pojedynczą podaną nazwę VirtualNetworkRule dla zestawu NetworkRuleSet przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="f3875-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="f3875-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f3875-104">SYNTAX</span></span>

### <span data-ttu-id="f3875-105">VirtualNetworkRulePropertiesParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f3875-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3875-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3875-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3875-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f3875-107">DESCRIPTION</span></span>
<span data-ttu-id="f3875-108">Usuwa pojedynczą podaną nazwę VirtualNetworkRule dla zestawu NetworkRuleSet przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="f3875-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="f3875-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f3875-109">EXAMPLES</span></span>

### <span data-ttu-id="f3875-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f3875-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="f3875-111">Usuwa pojedynczą podaną nazwę VirtualNetworkRule dla zestawu NetworkRuleSet przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="f3875-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="f3875-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f3875-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="f3875-113">Usuwanie $virtualruleset 1 zestawu NetworkRuleSet dla danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="f3875-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="f3875-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3875-114">PARAMETERS</span></span>

### <span data-ttu-id="f3875-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f3875-115">-AsJob</span></span>
<span data-ttu-id="f3875-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f3875-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3875-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3875-117">-DefaultProfile</span></span>
<span data-ttu-id="f3875-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3875-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3875-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f3875-119">-Name</span></span>
<span data-ttu-id="f3875-120">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="f3875-120">Namespace Name</span></span>

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

### <span data-ttu-id="f3875-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3875-121">-PassThru</span></span>
<span data-ttu-id="f3875-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f3875-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f3875-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3875-123">-ResourceGroupName</span></span>
<span data-ttu-id="f3875-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f3875-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f3875-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f3875-125">-SubnetId</span></span>
<span data-ttu-id="f3875-126">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="f3875-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="f3875-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="f3875-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="f3875-128">Obiekt konfiguracji protokołu IPRule</span><span class="sxs-lookup"><span data-stu-id="f3875-128">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="f3875-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3875-129">-Confirm</span></span>
<span data-ttu-id="f3875-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f3875-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3875-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3875-131">-WhatIf</span></span>
<span data-ttu-id="f3875-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3875-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3875-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f3875-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3875-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3875-134">CommonParameters</span></span>
<span data-ttu-id="f3875-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3875-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f3875-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3875-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3875-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3875-137">INPUTS</span></span>

### <span data-ttu-id="f3875-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f3875-138">System.String</span></span>

### <span data-ttu-id="f3875-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="f3875-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="f3875-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3875-140">OUTPUTS</span></span>

### <span data-ttu-id="f3875-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="f3875-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="f3875-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f3875-142">NOTES</span></span>

## <span data-ttu-id="f3875-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3875-143">RELATED LINKS</span></span>