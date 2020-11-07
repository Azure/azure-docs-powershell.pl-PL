---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: eaf9a89a8c610d8666a356e563681accfced4a7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705471"
---
# <span data-ttu-id="eead5-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="eead5-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="eead5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eead5-102">SYNOPSIS</span></span>
<span data-ttu-id="eead5-103">Aktualizowanie właściwości subskrypcji zdarzenia w siatce zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="eead5-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="eead5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eead5-104">SYNTAX</span></span>

### <span data-ttu-id="eead5-105">ResourceGroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eead5-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eead5-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="eead5-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eead5-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eead5-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eead5-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="eead5-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eead5-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="eead5-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eead5-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="eead5-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eead5-111">Opis</span><span class="sxs-lookup"><span data-stu-id="eead5-111">DESCRIPTION</span></span>
<span data-ttu-id="eead5-112">Aktualizowanie właściwości subskrypcji zdarzenia w siatce zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="eead5-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="eead5-113">Za pomocą tej funkcji można aktualizować filtr, miejsce docelowe lub etykiety istniejącego abonamentu zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="eead5-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="eead5-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eead5-114">EXAMPLES</span></span>

### <span data-ttu-id="eead5-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eead5-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="eead5-116">Umożliwia zaktualizowanie punktu końcowego ES1 subskrypcji \` zdarzeń \` dla tematu \` Temat1 \` w \` usłudze MyResourceGroupName w grupie zasobów \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="eead5-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="eead5-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="eead5-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="eead5-118">Umożliwia zaktualizowanie punktu końcowego ES1 subskrypcji \` zdarzeń \` dla tematu \` Temat1 \` w \` usłudze MyResourceGroupName w grupie zasobów \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="eead5-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="eead5-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="eead5-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="eead5-120">Aktualizuje właściwości ES1 subskrypcji zdarzeń \` \` dla obszaru nazw EventHub ContosoNamespace z nowym punktem końcowym jako \` https://requestb.in/1kxxoui1\ "i nowym SubjectEndsWith Filter jako \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="eead5-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="eead5-121">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="eead5-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="eead5-122">Aktualizuje właściwości ES1 subskrypcji zdarzeń \` \` dla grupy zasobów \` MyResourceGroupName \` przy użyciu nowych etykiet $labels.</span><span class="sxs-lookup"><span data-stu-id="eead5-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="eead5-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eead5-123">PARAMETERS</span></span>

### <span data-ttu-id="eead5-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="eead5-124">-AdvancedFilter</span></span>
<span data-ttu-id="eead5-125">Filtr zaawansowany określający tablicę wielu wartości Hashtable, które są używane do filtrowania opartego na atrybutach.</span><span class="sxs-lookup"><span data-stu-id="eead5-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="eead5-126">Każda wartość Hashtable zawiera następujące klucze — informacje o wartości: operacja, klucz i wartość lub wartości.</span><span class="sxs-lookup"><span data-stu-id="eead5-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="eead5-127">Operator może należeć do jednej z następujących wartości: liczba, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, String, StringNotIn, StringBeginsWith, StringEndsWith lub StringContains.</span><span class="sxs-lookup"><span data-stu-id="eead5-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="eead5-128">Klucz reprezentuje właściwość ładunku, w której są stosowane zaawansowane zasady filtrowania.</span><span class="sxs-lookup"><span data-stu-id="eead5-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="eead5-129">Wreszcie wartość lub wartości reprezentują wartość lub zestaw wartości, które mają zostać dopasowane.</span><span class="sxs-lookup"><span data-stu-id="eead5-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="eead5-130">Może to być pojedyncza wartość odpowiedniego typu lub tablica wartości.</span><span class="sxs-lookup"><span data-stu-id="eead5-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="eead5-131">Przykładowe parametry filtru zaawansowanego: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), gdzie $AdvFilter 1 = @ {operator = "numerowanie"; Key = "Data. KEY1"; Wartości = @ (1, 2)} i $AdvFilter 2 = @ {operator = "StringBringsWith"; Key = "subject"; Values = @ ("SubjectPrefix1"; "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="eead5-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="eead5-132">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="eead5-132">-DeadLetterEndpoint</span></span>
<span data-ttu-id="eead5-133">Punkt końcowy służący do przechowywania zdarzeń niedostarczonych.</span><span class="sxs-lookup"><span data-stu-id="eead5-133">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="eead5-134">Określ identyfikator zasobu platformy Azure kontenera obiektu blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="eead5-134">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="eead5-135">Na przykład:/subscriptions/[subskrypcji]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="eead5-135">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eead5-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eead5-136">-DefaultProfile</span></span>
<span data-ttu-id="eead5-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eead5-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eead5-138">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="eead5-138">-DomainName</span></span>
<span data-ttu-id="eead5-139">Nazwa domeny, w której ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="eead5-139">The name of the domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eead5-140">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="eead5-140">-DomainTopicName</span></span>
<span data-ttu-id="eead5-141">Nazwa tematu domeny, dla którego ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="eead5-141">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eead5-142">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="eead5-142">-Endpoint</span></span>
<span data-ttu-id="eead5-143">Docelowy punkt końcowy subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="eead5-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="eead5-144">Może to być adres URL elementu webhook lub identyfikator zasobu platformy Azure w kolejce EventHub, Storage, hybridconnection lub servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="eead5-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="eead5-145">Na przykład identyfikator zasobu dla połączenia hybrydowego przyjmuje następujący formularz:/subscriptions/[Identyfikator subskrypcji Azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[Obszar_nazwname]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="eead5-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="eead5-146">Oczekuje się, że docelowy punkt końcowy zostanie utworzony i będzie dostępny do użytku przed wykonaniem poleceń cmdlet dotyczących siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="eead5-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eead5-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="eead5-147">-EndpointType</span></span>
<span data-ttu-id="eead5-148">Typ punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="eead5-148">Endpoint Type.</span></span>
<span data-ttu-id="eead5-149">Może to być element webhook, eventhub, storagequeue, hybridconnection lub servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="eead5-149">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="eead5-150">Wartość domyślna to webhook.</span><span class="sxs-lookup"><span data-stu-id="eead5-150">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eead5-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="eead5-151">-EventSubscriptionName</span></span>
<span data-ttu-id="eead5-152">Nazwa subskrypcji wydarzenia</span><span class="sxs-lookup"><span data-stu-id="eead5-152">The name of the event subscription</span></span>

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

### <span data-ttu-id="eead5-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="eead5-153">-EventTtl</span></span>
<span data-ttu-id="eead5-154">Czas w minutach dostarczenia imprezy.</span><span class="sxs-lookup"><span data-stu-id="eead5-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="eead5-155">Ta wartość musi zawierać się między 1 a 1440</span><span class="sxs-lookup"><span data-stu-id="eead5-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eead5-156">-Wartość datawygaśnięcia</span><span class="sxs-lookup"><span data-stu-id="eead5-156">-ExpirationDate</span></span>
<span data-ttu-id="eead5-157">Określa wartość daty wygaśnięcia dla subskrypcji zdarzenia, po której abonament zdarzenia zostanie wycofany.</span><span class="sxs-lookup"><span data-stu-id="eead5-157">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="eead5-158">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="eead5-158">-IncludedEventType</span></span>
<span data-ttu-id="eead5-159">Filtr określający listę typów zdarzeń, które mają zostać uwzględnione. Jeśli nie określono tego parametru, zostaną uwzględnione wszystkie typy zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="eead5-159">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eead5-160">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="eead5-160">-InputObject</span></span>
<span data-ttu-id="eead5-161">Obiekt EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="eead5-161">EventGridSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eead5-162">-Label</span><span class="sxs-lookup"><span data-stu-id="eead5-162">-Label</span></span>
<span data-ttu-id="eead5-163">Etykiety dla subskrypcji zdarzeń</span><span class="sxs-lookup"><span data-stu-id="eead5-163">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eead5-164">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="eead5-164">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="eead5-165">Maksymalna liczba prób dostarczenia zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="eead5-165">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="eead5-166">Ta wartość musi należeć do zakresu od 1 do 30</span><span class="sxs-lookup"><span data-stu-id="eead5-166">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eead5-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eead5-167">-ResourceGroupName</span></span>
<span data-ttu-id="eead5-168">Grupa zasobów tematu.</span><span class="sxs-lookup"><span data-stu-id="eead5-168">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eead5-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eead5-169">-ResourceId</span></span>
<span data-ttu-id="eead5-170">Identyfikator zasobu, do którego utworzono subskrypcję zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="eead5-170">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="eead5-171">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="eead5-171">-SubjectBeginsWith</span></span>
<span data-ttu-id="eead5-172">Filtr określający, że będą uwzględniane tylko zdarzenia pasujące do określonego prefiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="eead5-172">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="eead5-173">Jeśli nie określono tego parametru, zostaną uwzględnione zdarzenia ze wszystkimi prefiksami tematów.</span><span class="sxs-lookup"><span data-stu-id="eead5-173">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eead5-174">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="eead5-174">-SubjectEndsWith</span></span>
<span data-ttu-id="eead5-175">Filtr określający, że będą uwzględniane tylko zdarzenia pasujące do określonego sufiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="eead5-175">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="eead5-176">Jeśli nie określono tego parametru, zostaną uwzględnione zdarzenia ze wszystkimi sufiksami tematów.</span><span class="sxs-lookup"><span data-stu-id="eead5-176">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eead5-177">-Tematname</span><span class="sxs-lookup"><span data-stu-id="eead5-177">-TopicName</span></span>
<span data-ttu-id="eead5-178">Nazwa tematu, do którego ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="eead5-178">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eead5-179">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eead5-179">-Confirm</span></span>
<span data-ttu-id="eead5-180">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eead5-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eead5-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eead5-181">-WhatIf</span></span>
<span data-ttu-id="eead5-182">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eead5-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eead5-183">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eead5-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eead5-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eead5-184">CommonParameters</span></span>
<span data-ttu-id="eead5-185">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eead5-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eead5-186">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eead5-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eead5-187">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eead5-187">INPUTS</span></span>

### <span data-ttu-id="eead5-188">System. String</span><span class="sxs-lookup"><span data-stu-id="eead5-188">System.String</span></span>

### <span data-ttu-id="eead5-189">Microsoft. Azure. Commands. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="eead5-189">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="eead5-190">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eead5-190">OUTPUTS</span></span>

### <span data-ttu-id="eead5-191">Microsoft. Azure. Commands. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="eead5-191">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="eead5-192">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eead5-192">NOTES</span></span>

## <span data-ttu-id="eead5-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eead5-193">RELATED LINKS</span></span>
