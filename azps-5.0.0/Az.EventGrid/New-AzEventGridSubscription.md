---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 44441fa364c43242a7a4454ccdf62f920cb321e5
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395428"
---
# <span data-ttu-id="9b120-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="9b120-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="9b120-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b120-102">SYNOPSIS</span></span>
<span data-ttu-id="9b120-103">Tworzy nowy abonament zdarzeń w siatce zdarzeń platformy Azure dla tematu, zasobu platformy Azure, subskrypcji platformy Azure lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b120-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="9b120-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b120-104">SYNTAX</span></span>

### <span data-ttu-id="9b120-105">ResourceGroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9b120-105">ResourceGroupNameParameterSet (Default)</span></span>
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

### <span data-ttu-id="9b120-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b120-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b120-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b120-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b120-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b120-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
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

### <span data-ttu-id="9b120-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b120-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
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

### <span data-ttu-id="9b120-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b120-110">CustomTopicEventSubscriptionParameterSet</span></span>
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

### <span data-ttu-id="9b120-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b120-111">DomainEventSubscriptionParameterSet</span></span>
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

### <span data-ttu-id="9b120-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b120-112">DomainTopicEventSubscriptionParameterSet</span></span>
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

## <span data-ttu-id="9b120-113">Opis</span><span class="sxs-lookup"><span data-stu-id="9b120-113">DESCRIPTION</span></span>
<span data-ttu-id="9b120-114">Utwórz nowy abonament zdarzenia w temacie poświęconym siatce zdarzeń platformy Azure, obsługiwany zasób platformy Azure, subskrypcja platformy Azure lub Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b120-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="9b120-115">Aby utworzyć subskrypcję zdarzeń dla obecnie wybranej subskrypcji platformy Azure, określ nazwę subskrypcji zdarzeń oraz punkt końcowy miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="9b120-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="9b120-116">Aby utworzyć subskrypcję zdarzeń dla grupy zasobów, określ nazwę grupy zasobów oprócz nazwy subskrypcji zdarzeń i punktu końcowego miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="9b120-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="9b120-117">Aby utworzyć subskrypcję zdarzeń w temacie Azure Event Grid, określ również nazwę tematu.</span><span class="sxs-lookup"><span data-stu-id="9b120-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="9b120-118">Aby utworzyć subskrypcję zdarzeń dla obsługiwanego zasobu platformy Azure, określ pełny identyfikator zasobu tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="9b120-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="9b120-119">Aby wyświetlić listę obsługiwanych typów, uruchom polecenie cmdlet Get-AzEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="9b120-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="9b120-120">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b120-120">EXAMPLES</span></span>

### <span data-ttu-id="9b120-121">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9b120-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="9b120-122">Tworzy nowe EventSubscription1 abonamentu \` zdarzeń \` na temat siatki zdarzeń usługi Azure \` Temat1 \` w grupie zasobów \` MyResourceGroupName \` z docelowym punktem końcowym elementu webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="9b120-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="9b120-123">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="9b120-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="9b120-124">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9b120-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="9b120-125">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w grupie zasobów \` MyResourceGroupName \` z docelowym punktem końcowym elementu webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="9b120-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="9b120-126">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="9b120-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="9b120-127">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9b120-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="9b120-128">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w obecnie wybranej subskrypcji platformy Azure z punktem końcowym elementu webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="9b120-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="9b120-129">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="9b120-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="9b120-130">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="9b120-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="9b120-131">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w obecnie wybranej subskrypcji platformy Azure z punktem końcowym elementu webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="9b120-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="9b120-132">Ten abonament zdarzeń określa dodatkowe filtry dla typów zdarzeń i tematu, a tylko te zdarzenia, które pasują do tych filtrów, będą dostarczane do docelowego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9b120-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="9b120-133">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="9b120-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="9b120-134">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w obecnie wybranej subskrypcji platformy Azure z określonym centrum zdarzeń jako miejscem docelowym zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="9b120-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="9b120-135">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="9b120-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="9b120-136">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="9b120-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="9b120-137">Tworzy nową subskrypcję zdarzeń \` EventSubscription1 \` do obszaru nazw EventHub przy użyciu określonego punktu końcowego elementu webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="9b120-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="9b120-138">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="9b120-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="9b120-139">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b120-139">PARAMETERS</span></span>

### <span data-ttu-id="9b120-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="9b120-140">-AdvancedFilter</span></span>
<span data-ttu-id="9b120-141">Filtr zaawansowany określający tablicę wielu wartości Hashtable, które są używane do filtrowania opartego na atrybutach.</span><span class="sxs-lookup"><span data-stu-id="9b120-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="9b120-142">Każda wartość Hashtable zawiera następujące klucze — informacje o wartości: operacja, klucz i wartość lub wartości.</span><span class="sxs-lookup"><span data-stu-id="9b120-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="9b120-143">Operator może należeć do jednej z następujących wartości: liczba, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, String, StringNotIn, StringBeginsWith, StringEndsWith lub StringContains.</span><span class="sxs-lookup"><span data-stu-id="9b120-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="9b120-144">Klucz reprezentuje właściwość ładunku, w której są stosowane zaawansowane zasady filtrowania.</span><span class="sxs-lookup"><span data-stu-id="9b120-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="9b120-145">Wreszcie wartość lub wartości reprezentują wartość lub zestaw wartości, które mają zostać dopasowane.</span><span class="sxs-lookup"><span data-stu-id="9b120-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="9b120-146">Może to być pojedyncza wartość odpowiedniego typu lub tablica wartości.</span><span class="sxs-lookup"><span data-stu-id="9b120-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="9b120-147">Przykładowe parametry filtru zaawansowanego: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), gdzie $AdvFilter 1 = @ {operator = "numerowanie"; Key = "Data. KEY1"; Wartości = @ (1, 2)} i $AdvFilter 2 = @ {operator = "StringBringsWith"; Key = "subject"; Values = @ ("SubjectPrefix1"; "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="9b120-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="9b120-148">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="9b120-148">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="9b120-149">Identyfikator lub identyfikator URI aplikacji usługi Azure Active Directory (AAD) w celu uzyskania tokenu dostępu, który zostanie uwzględniony jako token okaziciela w żądaniach dostarczenia. Dotyczy tylko elementu webhook jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="9b120-149">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="9b120-150">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="9b120-150">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="9b120-151">Identyfikator dzierżawy usługi Azure Active Directory (AAD), aby uzyskać token dostępu, który będzie dołączany jako token okaziciela w żądaniach dostarczenia. Dotyczy tylko elementu webhook jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="9b120-151">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="9b120-152">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="9b120-152">-DeadLetterEndpoint</span></span>
<span data-ttu-id="9b120-153">Punkt końcowy służący do przechowywania zdarzeń niedostarczonych.</span><span class="sxs-lookup"><span data-stu-id="9b120-153">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="9b120-154">Określ identyfikator zasobu platformy Azure kontenera obiektu blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="9b120-154">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="9b120-155">Na przykład:/subscriptions/[subskrypcji]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="9b120-155">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="9b120-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b120-156">-DefaultProfile</span></span>
<span data-ttu-id="9b120-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9b120-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b120-158">-DeliverySchema</span><span class="sxs-lookup"><span data-stu-id="9b120-158">-DeliverySchema</span></span>
<span data-ttu-id="9b120-159">Schemat, który ma być wykorzystywany podczas dostarczania zdarzeń do miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="9b120-159">The schema to be used when delivering events to the destination.</span></span> <span data-ttu-id="9b120-160">Możliwe wartości: eventgridschema, CustomInputSchema lub cloudeventv01schema.</span><span class="sxs-lookup"><span data-stu-id="9b120-160">The possible values are: eventgridschema, CustomInputSchema, or cloudeventv01schema.</span></span> <span data-ttu-id="9b120-161">Wartość domyślna to CustomInputSchema.</span><span class="sxs-lookup"><span data-stu-id="9b120-161">Default value is CustomInputSchema.</span></span>

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

### <span data-ttu-id="9b120-162">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="9b120-162">-DomainInputObject</span></span>
<span data-ttu-id="9b120-163">Obiekt domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="9b120-163">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="9b120-164">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="9b120-164">-DomainName</span></span>
<span data-ttu-id="9b120-165">Nazwa domeny siatki zdarzeń, do której ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="9b120-165">The name of the Event Grid domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="9b120-166">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="9b120-166">-DomainTopicInputObject</span></span>
<span data-ttu-id="9b120-167">Obiekt tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="9b120-167">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="9b120-168">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="9b120-168">-DomainTopicName</span></span>
<span data-ttu-id="9b120-169">Nazwa tematu domeny, dla którego ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="9b120-169">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="9b120-170">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="9b120-170">-Endpoint</span></span>
<span data-ttu-id="9b120-171">Docelowy punkt końcowy subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="9b120-171">Event subscription destination endpoint.</span></span>
<span data-ttu-id="9b120-172">Może to być adres URL elementu webhook lub identyfikator zasobu platformy Azure w kolejce EventHub, Storage, hybridconnection lub servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="9b120-172">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="9b120-173">Na przykład identyfikator zasobu dla połączenia hybrydowego przyjmuje następujący formularz:/subscriptions/[Identyfikator subskrypcji Azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[Obszar_nazwname]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="9b120-173">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="9b120-174">Oczekuje się, że docelowy punkt końcowy zostanie utworzony i będzie dostępny do użytku przed wykonaniem poleceń cmdlet dotyczących siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="9b120-174">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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

### <span data-ttu-id="9b120-175">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="9b120-175">-EndpointType</span></span>
<span data-ttu-id="9b120-176">Typ punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9b120-176">Endpoint Type.</span></span>
<span data-ttu-id="9b120-177">Może to być element webhook, eventhub, storagequeue, hybridconnection lub servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="9b120-177">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="9b120-178">Wartość domyślna to webhook.</span><span class="sxs-lookup"><span data-stu-id="9b120-178">Default value is webhook.</span></span>

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

### <span data-ttu-id="9b120-179">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9b120-179">-EventSubscriptionName</span></span>
<span data-ttu-id="9b120-180">Nazwa subskrypcji wydarzenia</span><span class="sxs-lookup"><span data-stu-id="9b120-180">The name of the event subscription</span></span>

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

### <span data-ttu-id="9b120-181">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="9b120-181">-EventTtl</span></span>
<span data-ttu-id="9b120-182">Czas w minutach dostarczenia imprezy.</span><span class="sxs-lookup"><span data-stu-id="9b120-182">The time in minutes for the event delivery.</span></span> <span data-ttu-id="9b120-183">Ta wartość musi zawierać się między 1 a 1440</span><span class="sxs-lookup"><span data-stu-id="9b120-183">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="9b120-184">-Wartość datawygaśnięcia</span><span class="sxs-lookup"><span data-stu-id="9b120-184">-ExpirationDate</span></span>
<span data-ttu-id="9b120-185">Określa wartość daty wygaśnięcia dla subskrypcji zdarzenia, po której abonament zdarzenia zostanie wycofany.</span><span class="sxs-lookup"><span data-stu-id="9b120-185">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="9b120-186">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="9b120-186">-IncludedEventType</span></span>
<span data-ttu-id="9b120-187">Filtr określający listę typów zdarzeń, które mają zostać uwzględnione. Jeśli nie określono tego parametru, zostaną uwzględnione wszystkie typy zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="9b120-187">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="9b120-188">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9b120-188">-InputObject</span></span>
<span data-ttu-id="9b120-189">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="9b120-189">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="9b120-190">-Label</span><span class="sxs-lookup"><span data-stu-id="9b120-190">-Label</span></span>
<span data-ttu-id="9b120-191">Etykiety dla subskrypcji zdarzeń</span><span class="sxs-lookup"><span data-stu-id="9b120-191">Labels for the event subscription</span></span>

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

### <span data-ttu-id="9b120-192">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="9b120-192">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="9b120-193">Maksymalna liczba prób dostarczenia zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="9b120-193">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="9b120-194">Ta wartość musi należeć do zakresu od 1 do 30</span><span class="sxs-lookup"><span data-stu-id="9b120-194">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="9b120-195">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="9b120-195">-MaxEventsPerBatch</span></span>
<span data-ttu-id="9b120-196">Maksymalna liczba zdarzeń w partii.</span><span class="sxs-lookup"><span data-stu-id="9b120-196">The maximum number of events in a batch.</span></span> <span data-ttu-id="9b120-197">Ta wartość musi zawierać się między 1 a 5000.</span><span class="sxs-lookup"><span data-stu-id="9b120-197">This value must be between 1 and 5000.</span></span> <span data-ttu-id="9b120-198">Ten parametr jest prawidłowy, gdy typ Endpint jest tylko webhook.</span><span class="sxs-lookup"><span data-stu-id="9b120-198">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="9b120-199">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="9b120-199">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="9b120-200">Preferowany rozmiar wsadu w kilobajtach.</span><span class="sxs-lookup"><span data-stu-id="9b120-200">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="9b120-201">Ta wartość musi zawierać się między 1 a 1024.</span><span class="sxs-lookup"><span data-stu-id="9b120-201">This value must be between 1 and 1024.</span></span> <span data-ttu-id="9b120-202">Ten parametr jest prawidłowy, gdy typ Endpint jest tylko webhook.</span><span class="sxs-lookup"><span data-stu-id="9b120-202">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="9b120-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b120-203">-ResourceGroupName</span></span>
<span data-ttu-id="9b120-204">Grupa zasobów tematu.</span><span class="sxs-lookup"><span data-stu-id="9b120-204">The resource group of the topic.</span></span>

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

### <span data-ttu-id="9b120-205">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b120-205">-ResourceId</span></span>
<span data-ttu-id="9b120-206">Identyfikator zasobu, dla którego ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="9b120-206">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="9b120-207">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="9b120-207">-SubjectBeginsWith</span></span>
<span data-ttu-id="9b120-208">Filtr określający, że będą uwzględniane tylko zdarzenia pasujące do określonego prefiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="9b120-208">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="9b120-209">Jeśli nie określono tego parametru, zostaną uwzględnione zdarzenia ze wszystkimi prefiksami tematów.</span><span class="sxs-lookup"><span data-stu-id="9b120-209">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="9b120-210">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="9b120-210">-SubjectCaseSensitive</span></span>
<span data-ttu-id="9b120-211">Filtr określający, że pole temat powinno być porównywane w sposób uwzględniający wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="9b120-211">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="9b120-212">Jeśli nie określono, temat będzie porównywany w sposób niewrażliwy na wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="9b120-212">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="9b120-213">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="9b120-213">-SubjectEndsWith</span></span>
<span data-ttu-id="9b120-214">Filtr określający, że będą uwzględniane tylko zdarzenia pasujące do określonego sufiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="9b120-214">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="9b120-215">Jeśli nie określono tego parametru, zostaną uwzględnione zdarzenia ze wszystkimi sufiksami tematów.</span><span class="sxs-lookup"><span data-stu-id="9b120-215">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="9b120-216">-Tematname</span><span class="sxs-lookup"><span data-stu-id="9b120-216">-TopicName</span></span>
<span data-ttu-id="9b120-217">Nazwa tematu, do którego ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="9b120-217">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="9b120-218">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b120-218">-Confirm</span></span>
<span data-ttu-id="9b120-219">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b120-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b120-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b120-220">-WhatIf</span></span>
<span data-ttu-id="9b120-221">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b120-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b120-222">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9b120-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b120-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b120-223">CommonParameters</span></span>
<span data-ttu-id="9b120-224">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b120-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b120-225">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b120-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b120-226">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b120-226">INPUTS</span></span>

### <span data-ttu-id="9b120-227">System. String</span><span class="sxs-lookup"><span data-stu-id="9b120-227">System.String</span></span>

### <span data-ttu-id="9b120-228">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="9b120-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="9b120-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="9b120-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="9b120-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="9b120-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="9b120-231">System. String []</span><span class="sxs-lookup"><span data-stu-id="9b120-231">System.String[]</span></span>

### <span data-ttu-id="9b120-232">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9b120-232">System.Int32</span></span>

## <span data-ttu-id="9b120-233">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b120-233">OUTPUTS</span></span>

### <span data-ttu-id="9b120-234">Microsoft. Azure. Commands. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="9b120-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="9b120-235">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b120-235">NOTES</span></span>

## <span data-ttu-id="9b120-236">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b120-236">RELATED LINKS</span></span>
