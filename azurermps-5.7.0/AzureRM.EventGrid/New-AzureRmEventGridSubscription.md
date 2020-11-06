---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
ms.openlocfilehash: 0c5c0f0f9739a2f9481989a69ece9aa29f0c67e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549015"
---
# <span data-ttu-id="5a03a-101">New-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="5a03a-101">New-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="5a03a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a03a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a03a-103">Tworzy nowy abonament zdarzeń w siatce zdarzeń platformy Azure dla tematu, zasobu platformy Azure, subskrypcji platformy Azure lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5a03a-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a03a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a03a-104">SYNTAX</span></span>

### <span data-ttu-id="5a03a-105">ResourceGroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5a03a-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a03a-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a03a-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a03a-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5a03a-107">EventSubscriptionInputObjectSet</span></span>
```
New-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a03a-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a03a-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a03a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5a03a-109">DESCRIPTION</span></span>
<span data-ttu-id="5a03a-110">Utwórz nowy abonament zdarzenia w temacie poświęconym siatce zdarzeń platformy Azure, obsługiwany zasób platformy Azure, subskrypcja platformy Azure lub Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="5a03a-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="5a03a-111">Aby utworzyć subskrypcję zdarzeń dla obecnie wybranej subskrypcji platformy Azure, określ nazwę subskrypcji zdarzeń oraz punkt końcowy miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="5a03a-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="5a03a-112">Aby utworzyć subskrypcję zdarzeń dla grupy zasobów, określ nazwę grupy zasobów oprócz nazwy subskrypcji zdarzeń i punktu końcowego miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="5a03a-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="5a03a-113">Aby utworzyć subskrypcję zdarzeń w temacie Azure Event Grid, określ również nazwę tematu.</span><span class="sxs-lookup"><span data-stu-id="5a03a-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="5a03a-114">Aby utworzyć subskrypcję zdarzeń dla obsługiwanego zasobu platformy Azure, określ pełny identyfikator zasobu tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="5a03a-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="5a03a-115">Aby wyświetlić listę obsługiwanych typów, uruchom polecenie cmdlet Get-AzureRmEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="5a03a-115">To view the list of supported types, run the Get-AzureRmEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="5a03a-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a03a-116">EXAMPLES</span></span>

### <span data-ttu-id="5a03a-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5a03a-117">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="5a03a-118">Tworzy nowe EventSubscription1 abonamentu \` zdarzeń \` na temat siatki zdarzeń usługi Azure \` Temat1 \` w grupie zasobów \` MyResourceGroupName \` z docelowym punktem końcowym elementu webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="5a03a-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="5a03a-119">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="5a03a-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="5a03a-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5a03a-120">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="5a03a-121">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w grupie zasobów \` MyResourceGroupName \` z docelowym punktem końcowym elementu webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="5a03a-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="5a03a-122">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="5a03a-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="5a03a-123">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5a03a-123">Example 3</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="5a03a-124">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w obecnie wybranej subskrypcji platformy Azure z punktem końcowym elementu webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="5a03a-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="5a03a-125">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="5a03a-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="5a03a-126">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="5a03a-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="5a03a-127">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w obecnie wybranej subskrypcji platformy Azure z punktem końcowym elementu webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="5a03a-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="5a03a-128">Ten abonament zdarzeń określa dodatkowe filtry dla typów zdarzeń i tematu, a tylko te zdarzenia, które pasują do tych filtrów, będą dostarczane do docelowego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="5a03a-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="5a03a-129">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="5a03a-129">Example 5</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="5a03a-130">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w obecnie wybranej subskrypcji platformy Azure z określonym centrum zdarzeń jako miejscem docelowym zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="5a03a-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="5a03a-131">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="5a03a-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="5a03a-132">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="5a03a-132">Example 6</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="5a03a-133">Tworzy nową subskrypcję zdarzenia \` EventSubscription1 \` do obszaru nazw EventHub za pomocą określonego webhhok docelowego punktu końcowego https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="5a03a-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhhok destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="5a03a-134">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="5a03a-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="5a03a-135">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a03a-135">PARAMETERS</span></span>

### <span data-ttu-id="5a03a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a03a-136">-DefaultProfile</span></span>
<span data-ttu-id="5a03a-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5a03a-137">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a03a-138">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="5a03a-138">-Endpoint</span></span>
<span data-ttu-id="5a03a-139">Docelowy punkt końcowy subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="5a03a-139">Event subscription destination endpoint.</span></span>
<span data-ttu-id="5a03a-140">Może to być adres URL elementu webhook lub identyfikator zasobu platformy Azure centrum EventHub.</span><span class="sxs-lookup"><span data-stu-id="5a03a-140">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a03a-141">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="5a03a-141">-EndpointType</span></span>
<span data-ttu-id="5a03a-142">Typ punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="5a03a-142">Endpoint Type.</span></span>
<span data-ttu-id="5a03a-143">Może to być element webhook lub eventhub</span><span class="sxs-lookup"><span data-stu-id="5a03a-143">This can be webhook or eventhub</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 
Accepted values: webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 
Accepted values: webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a03a-144">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="5a03a-144">-EventSubscriptionName</span></span>
<span data-ttu-id="5a03a-145">Nazwa subskrypcji wydarzenia</span><span class="sxs-lookup"><span data-stu-id="5a03a-145">The name of the event subscription</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a03a-146">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="5a03a-146">-IncludedEventType</span></span>
<span data-ttu-id="5a03a-147">Filtr określający listę typów zdarzeń, które mają zostać uwzględnione. Jeśli nie określono tego parametru, zostaną uwzględnione wszystkie typy zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="5a03a-147">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a03a-148">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5a03a-148">-InputObject</span></span>
<span data-ttu-id="5a03a-149">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="5a03a-149">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a03a-150">-Label</span><span class="sxs-lookup"><span data-stu-id="5a03a-150">-Label</span></span>
<span data-ttu-id="5a03a-151">Etykiety dla subskrypcji zdarzeń</span><span class="sxs-lookup"><span data-stu-id="5a03a-151">Labels for the event subscription</span></span>

```yaml
Type: String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a03a-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a03a-152">-ResourceGroupName</span></span>
<span data-ttu-id="5a03a-153">Grupa zasobów tematu.</span><span class="sxs-lookup"><span data-stu-id="5a03a-153">The resource group of the topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a03a-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a03a-154">-ResourceId</span></span>
<span data-ttu-id="5a03a-155">Identyfikator zasobu, dla którego ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="5a03a-155">The identifier of the resource to which the event subscription should be created.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a03a-156">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="5a03a-156">-SubjectBeginsWith</span></span>
<span data-ttu-id="5a03a-157">Filtr określający, że będą uwzględniane tylko zdarzenia pasujące do określonego prefiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="5a03a-157">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="5a03a-158">Jeśli nie określono tego parametru, zostaną uwzględnione zdarzenia ze wszystkimi prefiksami tematów.</span><span class="sxs-lookup"><span data-stu-id="5a03a-158">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a03a-159">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="5a03a-159">-SubjectCaseSensitive</span></span>
<span data-ttu-id="5a03a-160">Filtr określający, że pole temat powinno być porównywane w sposób uwzględniający wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="5a03a-160">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="5a03a-161">Jeśli nie określono, temat będzie porównywany w sposób niewrażliwy na wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="5a03a-161">If not specified, subject will be compared in a case insensitive manner.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a03a-162">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="5a03a-162">-SubjectEndsWith</span></span>
<span data-ttu-id="5a03a-163">Filtr określający, że będą uwzględniane tylko zdarzenia pasujące do określonego sufiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="5a03a-163">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="5a03a-164">Jeśli nie określono tego parametru, zostaną uwzględnione zdarzenia ze wszystkimi sufiksami tematów.</span><span class="sxs-lookup"><span data-stu-id="5a03a-164">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a03a-165">-Tematname</span><span class="sxs-lookup"><span data-stu-id="5a03a-165">-TopicName</span></span>
<span data-ttu-id="5a03a-166">Nazwa tematu, do którego ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="5a03a-166">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a03a-167">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a03a-167">-Confirm</span></span>
<span data-ttu-id="5a03a-168">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a03a-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a03a-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a03a-169">-WhatIf</span></span>
<span data-ttu-id="5a03a-170">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a03a-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a03a-171">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5a03a-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a03a-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a03a-172">CommonParameters</span></span>
<span data-ttu-id="5a03a-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a03a-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a03a-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a03a-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a03a-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a03a-175">INPUTS</span></span>

### <span data-ttu-id="5a03a-176">System. String</span><span class="sxs-lookup"><span data-stu-id="5a03a-176">System.String</span></span>
<span data-ttu-id="5a03a-177">Microsoft. Azure. Commands. EventGrid. models. PSTopic system. Management. Automation. SwitchParameter system. String []</span><span class="sxs-lookup"><span data-stu-id="5a03a-177">Microsoft.Azure.Commands.EventGrid.Models.PSTopic System.Management.Automation.SwitchParameter System.String[]</span></span>

## <span data-ttu-id="5a03a-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a03a-178">OUTPUTS</span></span>

### <span data-ttu-id="5a03a-179">Microsoft. Azure. Commands. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="5a03a-179">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="5a03a-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a03a-180">NOTES</span></span>

## <span data-ttu-id="5a03a-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a03a-181">RELATED LINKS</span></span>

