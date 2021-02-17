---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: a2e2b27023e9af9f08db6446d6d2808402ca27cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188483"
---
# <span data-ttu-id="be2d9-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="be2d9-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="be2d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be2d9-102">SYNOPSIS</span></span>
<span data-ttu-id="be2d9-103">Usuwa subskrypcję zdarzeń usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="be2d9-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="be2d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="be2d9-104">SYNTAX</span></span>

### <span data-ttu-id="be2d9-105">ResourceGroupNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="be2d9-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be2d9-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="be2d9-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be2d9-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be2d9-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be2d9-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be2d9-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be2d9-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be2d9-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be2d9-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="be2d9-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be2d9-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="be2d9-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be2d9-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="be2d9-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be2d9-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="be2d9-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be2d9-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="be2d9-114">DESCRIPTION</span></span>
<span data-ttu-id="be2d9-115">Usuwa subskrypcję zdarzeń usługi Azure Event Grid dla tematu Azure Event Grid, zasobu, subskrypcji platformy Azure lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="be2d9-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="be2d9-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="be2d9-116">EXAMPLES</span></span>

### <span data-ttu-id="be2d9-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="be2d9-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="be2d9-118">Usuwa subskrypcję zdarzeń EventSubscription1 do tematu Siatka zdarzeń azure , temat1 w grupie zasobów \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="be2d9-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="be2d9-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="be2d9-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="be2d9-120">Usuwa subskrypcję zdarzenia \` EventSubscription1 \` do grupy zasobów \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="be2d9-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="be2d9-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="be2d9-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="be2d9-122">Usuwa subskrypcję zdarzeń \` EventSubscription1 \` do domyślnej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="be2d9-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="be2d9-123">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="be2d9-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="be2d9-124">Usuwa subskrypcję zdarzeń \` EventSubscription1 do przestrzeni nazw \` centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="be2d9-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="be2d9-125">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="be2d9-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="be2d9-126">Usuwa subskrypcję zdarzeń \` EventSubscription1 \` do tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="be2d9-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="be2d9-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be2d9-127">PARAMETERS</span></span>

### <span data-ttu-id="be2d9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be2d9-128">-DefaultProfile</span></span>
<span data-ttu-id="be2d9-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="be2d9-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be2d9-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="be2d9-130">-DomainInputObject</span></span>
<span data-ttu-id="be2d9-131">Obiekt Domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="be2d9-131">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be2d9-132">-DomainName</span><span class="sxs-lookup"><span data-stu-id="be2d9-132">-DomainName</span></span>
<span data-ttu-id="be2d9-133">Nazwa domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="be2d9-133">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be2d9-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="be2d9-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="be2d9-135">Obiekt tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="be2d9-135">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be2d9-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="be2d9-136">-DomainTopicName</span></span>
<span data-ttu-id="be2d9-137">Nazwa tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="be2d9-137">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be2d9-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="be2d9-138">-EventSubscriptionName</span></span>
<span data-ttu-id="be2d9-139">Nazwa subskrypcji zdarzeń, która musi zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="be2d9-139">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet, DomainNameParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be2d9-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be2d9-140">-InputObject</span></span>
<span data-ttu-id="be2d9-141">Obiekt tematu w aplikacji EventGrid.</span><span class="sxs-lookup"><span data-stu-id="be2d9-141">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be2d9-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be2d9-142">-PassThru</span></span>
<span data-ttu-id="be2d9-143">Zwraca stan operacji Usuń.</span><span class="sxs-lookup"><span data-stu-id="be2d9-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="be2d9-144">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="be2d9-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="be2d9-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be2d9-145">-ResourceGroupName</span></span>
<span data-ttu-id="be2d9-146">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="be2d9-146">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be2d9-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be2d9-147">-ResourceId</span></span>
<span data-ttu-id="be2d9-148">Identyfikator zasobu, którego subskrypcja zdarzeń musi zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="be2d9-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be2d9-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="be2d9-149">-TopicName</span></span>
<span data-ttu-id="be2d9-150">Nazwa tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="be2d9-150">Event Grid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be2d9-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be2d9-151">-Confirm</span></span>
<span data-ttu-id="be2d9-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="be2d9-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be2d9-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be2d9-153">-WhatIf</span></span>
<span data-ttu-id="be2d9-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be2d9-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be2d9-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="be2d9-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be2d9-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be2d9-156">CommonParameters</span></span>
<span data-ttu-id="be2d9-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be2d9-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be2d9-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be2d9-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be2d9-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be2d9-159">INPUTS</span></span>

### <span data-ttu-id="be2d9-160">System.String</span><span class="sxs-lookup"><span data-stu-id="be2d9-160">System.String</span></span>

### <span data-ttu-id="be2d9-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="be2d9-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="be2d9-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="be2d9-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="be2d9-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="be2d9-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="be2d9-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="be2d9-164">OUTPUTS</span></span>

### <span data-ttu-id="be2d9-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="be2d9-165">System.Boolean</span></span>

## <span data-ttu-id="be2d9-166">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="be2d9-166">NOTES</span></span>

## <span data-ttu-id="be2d9-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be2d9-167">RELATED LINKS</span></span>
