---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
ms.openlocfilehash: ed2855571ccd3ce10a8a41fd72f5e14fde7bba16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553925"
---
# <span data-ttu-id="35db2-101">New-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="35db2-101">New-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="35db2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35db2-102">SYNOPSIS</span></span>
<span data-ttu-id="35db2-103">Tworzy nowy abonament zdarzeń w siatce zdarzeń platformy Azure dla tematu, zasobu platformy Azure, subskrypcji platformy Azure lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="35db2-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35db2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35db2-104">SYNTAX</span></span>

### <span data-ttu-id="35db2-105">ResourceGroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="35db2-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35db2-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="35db2-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35db2-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="35db2-107">EventSubscriptionInputObjectSet</span></span>
```
New-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35db2-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="35db2-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35db2-109">Opis</span><span class="sxs-lookup"><span data-stu-id="35db2-109">DESCRIPTION</span></span>
<span data-ttu-id="35db2-110">Utwórz nowy abonament zdarzenia w temacie poświęconym siatce zdarzeń platformy Azure, obsługiwany zasób platformy Azure, subskrypcja platformy Azure lub Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="35db2-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="35db2-111">Aby utworzyć subskrypcję zdarzeń dla obecnie wybranej subskrypcji platformy Azure, określ nazwę subskrypcji zdarzeń oraz punkt końcowy miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="35db2-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="35db2-112">Aby utworzyć subskrypcję zdarzeń dla grupy zasobów, określ nazwę grupy zasobów oprócz nazwy subskrypcji zdarzeń i punktu końcowego miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="35db2-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="35db2-113">Aby utworzyć subskrypcję zdarzeń w temacie Azure Event Grid, określ również nazwę tematu.</span><span class="sxs-lookup"><span data-stu-id="35db2-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="35db2-114">Aby utworzyć subskrypcję zdarzeń dla obsługiwanego zasobu platformy Azure, określ pełny identyfikator zasobu tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="35db2-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="35db2-115">Aby wyświetlić listę obsługiwanych typów, uruchom polecenie cmdlet Get-AzureRmEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="35db2-115">To view the list of supported types, run the Get-AzureRmEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="35db2-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35db2-116">EXAMPLES</span></span>

### <span data-ttu-id="35db2-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="35db2-117">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="35db2-118">Tworzy nowe EventSubscription1 abonamentu \` zdarzeń \` na temat siatki zdarzeń usługi Azure \` Temat1 \` w grupie zasobów \` MyResourceGroupName \` z docelowym punktem końcowym elementu webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="35db2-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="35db2-119">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="35db2-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="35db2-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="35db2-120">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="35db2-121">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w grupie zasobów \` MyResourceGroupName \` z docelowym punktem końcowym elementu webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="35db2-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="35db2-122">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="35db2-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="35db2-123">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="35db2-123">Example 3</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="35db2-124">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w obecnie wybranej subskrypcji platformy Azure z punktem końcowym elementu webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="35db2-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="35db2-125">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="35db2-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="35db2-126">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="35db2-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="35db2-127">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w obecnie wybranej subskrypcji platformy Azure z punktem końcowym elementu webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="35db2-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="35db2-128">Ten abonament zdarzeń określa dodatkowe filtry dla typów zdarzeń i tematu, a tylko te zdarzenia, które pasują do tych filtrów, będą dostarczane do docelowego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="35db2-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="35db2-129">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="35db2-129">Example 5</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="35db2-130">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w obecnie wybranej subskrypcji platformy Azure z określonym centrum zdarzeń jako miejscem docelowym zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="35db2-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="35db2-131">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="35db2-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="35db2-132">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="35db2-132">Example 6</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="35db2-133">Tworzy nową subskrypcję zdarzenia \` EventSubscription1 \` do obszaru nazw EventHub za pomocą określonego webhhok docelowego punktu końcowego https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="35db2-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhhok destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="35db2-134">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="35db2-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="35db2-135">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35db2-135">PARAMETERS</span></span>

### <span data-ttu-id="35db2-136">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="35db2-136">-Endpoint</span></span>
<span data-ttu-id="35db2-137">Docelowy punkt końcowy subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="35db2-137">Event subscription destination endpoint.</span></span>
<span data-ttu-id="35db2-138">Może to być adres URL elementu webhook lub identyfikator zasobu platformy Azure centrum EventHub.</span><span class="sxs-lookup"><span data-stu-id="35db2-138">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35db2-139">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="35db2-139">-EndpointType</span></span>
<span data-ttu-id="35db2-140">Typ punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="35db2-140">Endpoint Type.</span></span>
<span data-ttu-id="35db2-141">Może to być element webhook lub eventhub</span><span class="sxs-lookup"><span data-stu-id="35db2-141">This can be webhook or eventhub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 
Accepted values: webhook, eventhub, webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 
Accepted values: webhook, eventhub, webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35db2-142">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="35db2-142">-EventSubscriptionName</span></span>
<span data-ttu-id="35db2-143">Nazwa subskrypcji wydarzenia</span><span class="sxs-lookup"><span data-stu-id="35db2-143">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35db2-144">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="35db2-144">-IncludedEventType</span></span>
<span data-ttu-id="35db2-145">Filtr określający listę typów zdarzeń, które mają zostać uwzględnione. Jeśli nie określono tego parametru, zostaną uwzględnione wszystkie typy zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="35db2-145">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35db2-146">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="35db2-146">-InputObject</span></span>
<span data-ttu-id="35db2-147">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="35db2-147">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35db2-148">-Label</span><span class="sxs-lookup"><span data-stu-id="35db2-148">-Label</span></span>
<span data-ttu-id="35db2-149">Etykiety dla subskrypcji zdarzeń</span><span class="sxs-lookup"><span data-stu-id="35db2-149">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35db2-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35db2-150">-ResourceGroupName</span></span>
<span data-ttu-id="35db2-151">Grupa zasobów tematu.</span><span class="sxs-lookup"><span data-stu-id="35db2-151">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35db2-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35db2-152">-ResourceId</span></span>
<span data-ttu-id="35db2-153">Identyfikator zasobu, dla którego ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="35db2-153">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="35db2-154">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="35db2-154">-SubjectBeginsWith</span></span>
<span data-ttu-id="35db2-155">Filtr określający, że będą uwzględniane tylko zdarzenia pasujące do określonego prefiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="35db2-155">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="35db2-156">Jeśli nie określono tego parametru, zostaną uwzględnione zdarzenia ze wszystkimi prefiksami tematów.</span><span class="sxs-lookup"><span data-stu-id="35db2-156">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35db2-157">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="35db2-157">-SubjectCaseSensitive</span></span>
<span data-ttu-id="35db2-158">Filtr określający, że pole temat powinno być porównywane w sposób uwzględniający wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="35db2-158">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="35db2-159">Jeśli nie określono, temat będzie porównywany w sposób niewrażliwy na wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="35db2-159">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="35db2-160">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="35db2-160">-SubjectEndsWith</span></span>
<span data-ttu-id="35db2-161">Filtr określający, że będą uwzględniane tylko zdarzenia pasujące do określonego sufiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="35db2-161">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="35db2-162">Jeśli nie określono tego parametru, zostaną uwzględnione zdarzenia ze wszystkimi sufiksami tematów.</span><span class="sxs-lookup"><span data-stu-id="35db2-162">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35db2-163">-Tematname</span><span class="sxs-lookup"><span data-stu-id="35db2-163">-TopicName</span></span>
<span data-ttu-id="35db2-164">Nazwa tematu, do którego ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="35db2-164">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35db2-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35db2-165">-Confirm</span></span>
<span data-ttu-id="35db2-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35db2-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35db2-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35db2-167">-WhatIf</span></span>
<span data-ttu-id="35db2-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35db2-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35db2-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="35db2-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35db2-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35db2-170">-DefaultProfile</span></span>
<span data-ttu-id="35db2-171">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="35db2-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35db2-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35db2-172">CommonParameters</span></span>
<span data-ttu-id="35db2-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35db2-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35db2-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35db2-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35db2-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35db2-175">INPUTS</span></span>

### <span data-ttu-id="35db2-176">System. String</span><span class="sxs-lookup"><span data-stu-id="35db2-176">System.String</span></span>
<span data-ttu-id="35db2-177">Microsoft. Azure. Commands. EventGrid. models. PSTopic system. Management. Automation. SwitchParameter system. String []</span><span class="sxs-lookup"><span data-stu-id="35db2-177">Microsoft.Azure.Commands.EventGrid.Models.PSTopic System.Management.Automation.SwitchParameter System.String[]</span></span>

## <span data-ttu-id="35db2-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35db2-178">OUTPUTS</span></span>

### <span data-ttu-id="35db2-179">Microsoft. Azure. Commands. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="35db2-179">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="35db2-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35db2-180">NOTES</span></span>

## <span data-ttu-id="35db2-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35db2-181">RELATED LINKS</span></span>

