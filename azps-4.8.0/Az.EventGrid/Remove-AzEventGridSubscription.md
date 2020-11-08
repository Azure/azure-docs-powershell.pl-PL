---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: a2e2b27023e9af9f08db6446d6d2808402ca27cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223954"
---
# <span data-ttu-id="b46e5-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="b46e5-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="b46e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b46e5-102">SYNOPSIS</span></span>
<span data-ttu-id="b46e5-103">Usuwa subskrypcję zdarzeń w siatce zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b46e5-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="b46e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b46e5-104">SYNTAX</span></span>

### <span data-ttu-id="b46e5-105">ResourceGroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b46e5-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b46e5-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b46e5-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b46e5-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b46e5-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b46e5-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b46e5-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b46e5-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b46e5-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b46e5-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b46e5-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b46e5-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b46e5-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b46e5-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b46e5-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b46e5-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b46e5-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b46e5-114">Opis</span><span class="sxs-lookup"><span data-stu-id="b46e5-114">DESCRIPTION</span></span>
<span data-ttu-id="b46e5-115">Usuwa subskrypcję zdarzeń w siatce zdarzeń platformy Azure dla tematu siatka zdarzeń Azure, zasób, subskrypcję platformy Azure lub grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="b46e5-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="b46e5-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b46e5-116">EXAMPLES</span></span>

### <span data-ttu-id="b46e5-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b46e5-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="b46e5-118">Usuwa EventSubscription1 abonamentu \` zdarzeń \` do tematu siatka zdarzeń usługi Azure \` Temat1 \` w grupie zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b46e5-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b46e5-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b46e5-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="b46e5-120">Usuwa EventSubscription1 subskrypcji zdarzeń \` \` do MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="b46e5-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b46e5-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b46e5-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="b46e5-122">Usuwa EventSubscription1 subskrypcji zdarzeń \` \` do domyślnej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b46e5-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="b46e5-123">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="b46e5-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="b46e5-124">Usuwa EventSubscription1 subskrypcji zdarzeń \` \` do obszaru nazw centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b46e5-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="b46e5-125">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="b46e5-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="b46e5-126">Usuwa EventSubscription1 subskrypcji zdarzeń \` \` do tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b46e5-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="b46e5-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b46e5-127">PARAMETERS</span></span>

### <span data-ttu-id="b46e5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b46e5-128">-DefaultProfile</span></span>
<span data-ttu-id="b46e5-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b46e5-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b46e5-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="b46e5-130">-DomainInputObject</span></span>
<span data-ttu-id="b46e5-131">Obiekt domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b46e5-131">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="b46e5-132">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="b46e5-132">-DomainName</span></span>
<span data-ttu-id="b46e5-133">EventGrid nazwa domeny.</span><span class="sxs-lookup"><span data-stu-id="b46e5-133">EventGrid domain name.</span></span>

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

### <span data-ttu-id="b46e5-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="b46e5-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="b46e5-135">Obiekt tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b46e5-135">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="b46e5-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="b46e5-136">-DomainTopicName</span></span>
<span data-ttu-id="b46e5-137">Nazwa tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b46e5-137">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="b46e5-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b46e5-138">-EventSubscriptionName</span></span>
<span data-ttu-id="b46e5-139">Nazwa subskrypcji zdarzenia, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="b46e5-139">Name of the event subscription that needs to be removed.</span></span>

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

### <span data-ttu-id="b46e5-140">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b46e5-140">-InputObject</span></span>
<span data-ttu-id="b46e5-141">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b46e5-141">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="b46e5-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b46e5-142">-PassThru</span></span>
<span data-ttu-id="b46e5-143">Zwraca stan operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="b46e5-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="b46e5-144">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b46e5-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b46e5-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b46e5-145">-ResourceGroupName</span></span>
<span data-ttu-id="b46e5-146">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b46e5-146">Resource Group Name.</span></span>

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

### <span data-ttu-id="b46e5-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b46e5-147">-ResourceId</span></span>
<span data-ttu-id="b46e5-148">Identyfikator zasobu, którego abonament zdarzenia należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="b46e5-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="b46e5-149">-Tematname</span><span class="sxs-lookup"><span data-stu-id="b46e5-149">-TopicName</span></span>
<span data-ttu-id="b46e5-150">Nazwa tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b46e5-150">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="b46e5-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b46e5-151">-Confirm</span></span>
<span data-ttu-id="b46e5-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b46e5-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b46e5-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b46e5-153">-WhatIf</span></span>
<span data-ttu-id="b46e5-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b46e5-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b46e5-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b46e5-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b46e5-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b46e5-156">CommonParameters</span></span>
<span data-ttu-id="b46e5-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b46e5-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b46e5-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b46e5-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b46e5-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b46e5-159">INPUTS</span></span>

### <span data-ttu-id="b46e5-160">System. String</span><span class="sxs-lookup"><span data-stu-id="b46e5-160">System.String</span></span>

### <span data-ttu-id="b46e5-161">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="b46e5-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="b46e5-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="b46e5-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="b46e5-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="b46e5-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="b46e5-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b46e5-164">OUTPUTS</span></span>

### <span data-ttu-id="b46e5-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b46e5-165">System.Boolean</span></span>

## <span data-ttu-id="b46e5-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b46e5-166">NOTES</span></span>

## <span data-ttu-id="b46e5-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b46e5-167">RELATED LINKS</span></span>
