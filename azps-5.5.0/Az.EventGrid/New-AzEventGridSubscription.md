---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 44441fa364c43242a7a4454ccdf62f920cb321e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188506"
---
# <span data-ttu-id="25253-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="25253-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="25253-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25253-102">SYNOPSIS</span></span>
<span data-ttu-id="25253-103">Tworzy nową subskrypcję zdarzenia siatki zdarzeń platformy Azure dla tematu, zasobu Azure, subskrypcji platformy Azure lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25253-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="25253-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="25253-104">SYNTAX</span></span>

### <span data-ttu-id="25253-105">ResourceGroupNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="25253-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25253-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="25253-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25253-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25253-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25253-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25253-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25253-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25253-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25253-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="25253-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25253-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="25253-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25253-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="25253-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [-EndpointType <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25253-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="25253-113">DESCRIPTION</span></span>
<span data-ttu-id="25253-114">Utwórz nową subskrypcję zdarzeń dla tematu Azure Event Grid, obsługiwanego zasobu platformy Azure, subskrypcji platformy Azure lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25253-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="25253-115">Aby utworzyć subskrypcję zdarzenia dla obecnie wybranej subskrypcji platformy Azure, określ nazwę subskrypcji zdarzenia i docelowy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="25253-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="25253-116">Aby utworzyć subskrypcję zdarzenia dla grupy zasobów, oprócz nazwy subskrypcji zdarzenia i punktu końcowego docelowego określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25253-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="25253-117">Aby utworzyć subskrypcję zdarzenia dla tematu w usłudze Azure Event Grid, określ także nazwę tematu.</span><span class="sxs-lookup"><span data-stu-id="25253-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="25253-118">Aby utworzyć subskrypcję zdarzenia dla obsługiwanego zasobu platformy Azure, określ pełny identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="25253-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="25253-119">Aby wyświetlić listę obsługiwanych typów, uruchom Get-AzEventGridTopicType cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25253-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="25253-120">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="25253-120">EXAMPLES</span></span>

### <span data-ttu-id="25253-121">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="25253-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="25253-122">Tworzy nową subskrypcję zdarzenia EventSubscription1 do tematu Siatka zdarzeń Azure, temat1 w grupie zasobów \` \` Nazwa_grupy zasobów \` \` \` MyResourceGroupName z punktem końcowym docelowym \` webhook. `https://requestb.in/19qlscd1`</span><span class="sxs-lookup"><span data-stu-id="25253-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="25253-123">Ta subskrypcja zdarzeń korzysta z filtrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="25253-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="25253-124">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="25253-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="25253-125">Tworzy nową subskrypcję zdarzenia EventSubscription1 dla grupy zasobów \` \` \` Nazwa_grupy_zasobów z punktem końcowym docelowym \` sieci `https://requestb.in/19qlscd1` Web.</span><span class="sxs-lookup"><span data-stu-id="25253-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="25253-126">Ta subskrypcja zdarzeń korzysta z filtrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="25253-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="25253-127">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="25253-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="25253-128">Tworzy nową subskrypcję zdarzenia \` EventSubscription1 do obecnie wybranej subskrypcji platformy Azure z punktem końcowym docelowym \` webhook. `https://requestb.in/19qlscd1`</span><span class="sxs-lookup"><span data-stu-id="25253-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="25253-129">Ta subskrypcja zdarzeń korzysta z filtrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="25253-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="25253-130">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="25253-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="25253-131">Tworzy nową subskrypcję zdarzeń EventSubscription1 do obecnie wybranej subskrypcji platformy Azure z punktem końcowym docelowym \` \` webhook. `https://requestb.in/19qlscd1`</span><span class="sxs-lookup"><span data-stu-id="25253-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="25253-132">Ta subskrypcja zdarzeń określa dodatkowe filtry dla typów zdarzeń i tematu, a do punktu końcowego będą dostarczane tylko zdarzenia pasujące do tych filtrów.</span><span class="sxs-lookup"><span data-stu-id="25253-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="25253-133">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="25253-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="25253-134">Tworzy nową subskrypcję zdarzeń EventSubscription1 do obecnie wybranej subskrypcji platformy Azure z określonym centrum zdarzeń jako miejscem docelowym \` \` zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="25253-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="25253-135">Ta subskrypcja zdarzeń korzysta z filtrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="25253-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="25253-136">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="25253-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="25253-137">Tworzy nową subskrypcję zdarzeń \` EventSubscription1 do przestrzeni nazw aplikacji EventHub z określonym punktem końcowym docelowym \` sieci `https://requestb.in/19qlscd1` Web.</span><span class="sxs-lookup"><span data-stu-id="25253-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="25253-138">Ta subskrypcja zdarzeń korzysta z filtrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="25253-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="25253-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25253-139">PARAMETERS</span></span>

### <span data-ttu-id="25253-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="25253-140">-AdvancedFilter</span></span>
<span data-ttu-id="25253-141">Filtr zaawansowany określający tablicę wielu wartości w formie skrótów, które są używane do filtrowania opartego na atrybutach.</span><span class="sxs-lookup"><span data-stu-id="25253-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="25253-142">Każda wartość w tabeli skrótów ma następujące informacje key-value: Operation (Operacja), Key (Klucz) i Value (Wartości).</span><span class="sxs-lookup"><span data-stu-id="25253-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="25253-143">Operator może być jedną z następujących wartości: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith lub StringContains.</span><span class="sxs-lookup"><span data-stu-id="25253-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="25253-144">Klucz reprezentuje właściwość ładowania, do której są stosowane zaawansowane zasady filtrowania.</span><span class="sxs-lookup"><span data-stu-id="25253-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="25253-145">Natomiast wartość lub wartości reprezentują wartość lub zestaw wartości do dopasowania.</span><span class="sxs-lookup"><span data-stu-id="25253-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="25253-146">Może to być pojedyncza wartość odpowiedniego typu lub tablica wartości.</span><span class="sxs-lookup"><span data-stu-id="25253-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="25253-147">Jako przykład zaawansowanych parametrów filtru: $AdvancedFilters=@($AdvFilter 1; $AdvFilter 2), gdzie $AdvFilter 1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1;2)} and $AdvFilter 2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="25253-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25253-148">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="25253-148">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="25253-149">Identyfikator aplikacji lub identyfikator Uri aplikacji usługi Azure Active Directory (AAD) w celu uzyskania tokenu dostępu, który zostanie uwzględniony jako token użytkownika w żądaniach dostarczenia. Dotyczy tylko sieci Webhook jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="25253-149">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-150">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="25253-150">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="25253-151">Identyfikator dzierżawy usługi Azure Active Directory (AAD) w celu uzyskania tokenu dostępu, który zostanie uwzględniony jako token użytkownika w żądaniach dostarczenia. Ma zastosowanie tylko w przypadku webhook jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="25253-151">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-152">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="25253-152">-DeadLetterEndpoint</span></span>
<span data-ttu-id="25253-153">Punkt końcowy używany do przechowywania niedostarczanych zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="25253-153">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="25253-154">Określ identyfikator zasobu Azure kontenera obiektów blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="25253-154">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="25253-155">Na przykład: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="25253-155">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25253-156">-DefaultProfile</span></span>
<span data-ttu-id="25253-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="25253-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25253-158">-DeliverySchema</span><span class="sxs-lookup"><span data-stu-id="25253-158">-DeliverySchema</span></span>
<span data-ttu-id="25253-159">Schemat, który ma być używany podczas dostarczania zdarzeń do miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="25253-159">The schema to be used when delivering events to the destination.</span></span> <span data-ttu-id="25253-160">Dopuszczalne wartości to: eventgridschema, CustomInputSchema lub cloudeventv01schema.</span><span class="sxs-lookup"><span data-stu-id="25253-160">The possible values are: eventgridschema, CustomInputSchema, or cloudeventv01schema.</span></span> <span data-ttu-id="25253-161">Wartość domyślna to CustomInputSchema.</span><span class="sxs-lookup"><span data-stu-id="25253-161">Default value is CustomInputSchema.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-162">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="25253-162">-DomainInputObject</span></span>
<span data-ttu-id="25253-163">Obiekt Domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="25253-163">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="25253-164">-DomainName</span><span class="sxs-lookup"><span data-stu-id="25253-164">-DomainName</span></span>
<span data-ttu-id="25253-165">Nazwa domeny siatki zdarzeń, do której należy utworzyć subskrypcję zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="25253-165">The name of the Event Grid domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-166">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="25253-166">-DomainTopicInputObject</span></span>
<span data-ttu-id="25253-167">Obiekt tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="25253-167">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="25253-168">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="25253-168">-DomainTopicName</span></span>
<span data-ttu-id="25253-169">Nazwa tematu domeny, do którego ma zostać utworzona subskrypcja zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="25253-169">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-170">- Punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="25253-170">-Endpoint</span></span>
<span data-ttu-id="25253-171">Punkt końcowy docelowej subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="25253-171">Event subscription destination endpoint.</span></span>
<span data-ttu-id="25253-172">Może to być adres URL sieci Web lub identyfikator zasobu Azure aplikacji EventHub, kolejka magazynu, połączenie hybrydowe lub kolejka usługi.</span><span class="sxs-lookup"><span data-stu-id="25253-172">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="25253-173">Na przykład identyfikator zasobu dla połączenia hybrydowego ma następującą postać: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="25253-173">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="25253-174">Przed wykonaniem jakichkolwiek cmdlet siatki zdarzeń oczekuje się, że docelowy punkt końcowy zostanie utworzony i dostępny do użycia.</span><span class="sxs-lookup"><span data-stu-id="25253-174">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-175">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="25253-175">-EndpointType</span></span>
<span data-ttu-id="25253-176">Typ punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="25253-176">Endpoint Type.</span></span>
<span data-ttu-id="25253-177">Może to być sieć Webhook, aplikacja EventHub, kolejka magazynowania, połączenie hybrydowe lub usługa kolejkowania usługi.</span><span class="sxs-lookup"><span data-stu-id="25253-177">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="25253-178">Wartość domyślna to webhook.</span><span class="sxs-lookup"><span data-stu-id="25253-178">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-179">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="25253-179">-EventSubscriptionName</span></span>
<span data-ttu-id="25253-180">Nazwa subskrypcji wydarzenia</span><span class="sxs-lookup"><span data-stu-id="25253-180">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
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

### <span data-ttu-id="25253-181">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="25253-181">-EventTtl</span></span>
<span data-ttu-id="25253-182">Czas (w minutach) na dostarczenie zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="25253-182">The time in minutes for the event delivery.</span></span> <span data-ttu-id="25253-183">Ta wartość musi być między 1 a 1440</span><span class="sxs-lookup"><span data-stu-id="25253-183">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-184">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="25253-184">-ExpirationDate</span></span>
<span data-ttu-id="25253-185">Określa datę wygaśnięcia subskrypcji wydarzenia DateTime, po upływie której subskrypcja zdarzeń zostanie wycofana.</span><span class="sxs-lookup"><span data-stu-id="25253-185">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25253-186">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="25253-186">-IncludedEventType</span></span>
<span data-ttu-id="25253-187">Filtr określający listę typów zdarzeń, które mają być dołączane. Jeśli nie zostanie określona, zostaną uwzględnione wszystkie typy zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="25253-187">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-188">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25253-188">-InputObject</span></span>
<span data-ttu-id="25253-189">Obiekt tematu w aplikacji EventGrid.</span><span class="sxs-lookup"><span data-stu-id="25253-189">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="25253-190">— Etykieta</span><span class="sxs-lookup"><span data-stu-id="25253-190">-Label</span></span>
<span data-ttu-id="25253-191">Etykiety dla subskrypcji wydarzenia</span><span class="sxs-lookup"><span data-stu-id="25253-191">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-192">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="25253-192">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="25253-193">Maksymalna liczba prób dostarczenia zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="25253-193">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="25253-194">Ta wartość musi być między 1 a 30</span><span class="sxs-lookup"><span data-stu-id="25253-194">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-195">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="25253-195">-MaxEventsPerBatch</span></span>
<span data-ttu-id="25253-196">Maksymalna liczba zdarzeń w partii.</span><span class="sxs-lookup"><span data-stu-id="25253-196">The maximum number of events in a batch.</span></span> <span data-ttu-id="25253-197">Ta wartość musi być między 1 a 5000.</span><span class="sxs-lookup"><span data-stu-id="25253-197">This value must be between 1 and 5000.</span></span> <span data-ttu-id="25253-198">Ten parametr jest prawidłowy, gdy typem endpint jest tylko webhook.</span><span class="sxs-lookup"><span data-stu-id="25253-198">This parameter is valid when Endpint Type is webhook only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-199">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="25253-199">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="25253-200">Preferowany rozmiar partii w kilobajtach.</span><span class="sxs-lookup"><span data-stu-id="25253-200">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="25253-201">Ta wartość musi być między 1 a 1024.</span><span class="sxs-lookup"><span data-stu-id="25253-201">This value must be between 1 and 1024.</span></span> <span data-ttu-id="25253-202">Ten parametr jest prawidłowy, gdy typem endpint jest tylko webhook.</span><span class="sxs-lookup"><span data-stu-id="25253-202">This parameter is valid when Endpint Type is webhook only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25253-203">-ResourceGroupName</span></span>
<span data-ttu-id="25253-204">Grupa zasobów tematu.</span><span class="sxs-lookup"><span data-stu-id="25253-204">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-205">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25253-205">-ResourceId</span></span>
<span data-ttu-id="25253-206">Identyfikator zasobu, do którego ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="25253-206">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="25253-207">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="25253-207">-SubjectBeginsWith</span></span>
<span data-ttu-id="25253-208">Filtr określający, że zostaną uwzględnione tylko zdarzenia o określonym prefiksie tematu.</span><span class="sxs-lookup"><span data-stu-id="25253-208">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="25253-209">Jeśli nie zostanie określone, zostaną uwzględnione zdarzenia ze wszystkimi prefiksami tematu.</span><span class="sxs-lookup"><span data-stu-id="25253-209">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-210">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="25253-210">-SubjectCaseSensitive</span></span>
<span data-ttu-id="25253-211">Filtr określający, że pole tematu ma zostać porównane z wielkością liter.</span><span class="sxs-lookup"><span data-stu-id="25253-211">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="25253-212">Jeśli temat nie zostanie określony, temat zostanie porównany bez uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="25253-212">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="25253-213">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="25253-213">-SubjectEndsWith</span></span>
<span data-ttu-id="25253-214">Filtr określający, że zostaną uwzględnione tylko zdarzenia pasujące do określonego sufiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="25253-214">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="25253-215">Jeśli nie zostanie określona, zostaną uwzględnione zdarzenia ze wszystkimi sufiksami tematu.</span><span class="sxs-lookup"><span data-stu-id="25253-215">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25253-216">-TopicName</span><span class="sxs-lookup"><span data-stu-id="25253-216">-TopicName</span></span>
<span data-ttu-id="25253-217">Nazwa tematu, do którego ma zostać utworzona subskrypcja wydarzenia.</span><span class="sxs-lookup"><span data-stu-id="25253-217">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="25253-218">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25253-218">-Confirm</span></span>
<span data-ttu-id="25253-219">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="25253-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25253-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25253-220">-WhatIf</span></span>
<span data-ttu-id="25253-221">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25253-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25253-222">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="25253-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25253-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25253-223">CommonParameters</span></span>
<span data-ttu-id="25253-224">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25253-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25253-225">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25253-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25253-226">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25253-226">INPUTS</span></span>

### <span data-ttu-id="25253-227">System.String</span><span class="sxs-lookup"><span data-stu-id="25253-227">System.String</span></span>

### <span data-ttu-id="25253-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="25253-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="25253-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="25253-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="25253-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="25253-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="25253-231">System.String[]</span><span class="sxs-lookup"><span data-stu-id="25253-231">System.String[]</span></span>

### <span data-ttu-id="25253-232">System.Int32</span><span class="sxs-lookup"><span data-stu-id="25253-232">System.Int32</span></span>

## <span data-ttu-id="25253-233">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="25253-233">OUTPUTS</span></span>

### <span data-ttu-id="25253-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="25253-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="25253-235">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="25253-235">NOTES</span></span>

## <span data-ttu-id="25253-236">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25253-236">RELATED LINKS</span></span>
