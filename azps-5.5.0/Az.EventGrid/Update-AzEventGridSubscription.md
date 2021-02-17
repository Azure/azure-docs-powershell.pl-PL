---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: 7398dd0a80e2f84dcce929019038c616f6c7c1c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243666"
---
# <span data-ttu-id="dccf1-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="dccf1-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="dccf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dccf1-102">SYNOPSIS</span></span>
<span data-ttu-id="dccf1-103">Aktualizowanie właściwości subskrypcji zdarzeń siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="dccf1-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="dccf1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dccf1-104">SYNTAX</span></span>

### <span data-ttu-id="dccf1-105">ResourceGroupNameParameterSet (Ustawienie domyślne)</span><span class="sxs-lookup"><span data-stu-id="dccf1-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dccf1-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="dccf1-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dccf1-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dccf1-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dccf1-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="dccf1-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dccf1-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="dccf1-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dccf1-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="dccf1-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dccf1-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="dccf1-111">DESCRIPTION</span></span>
<span data-ttu-id="dccf1-112">Aktualizowanie właściwości subskrypcji zdarzeń siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="dccf1-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="dccf1-113">Za jego pomocą można zaktualizować filtr, miejsce docelowe lub etykiety istniejącej subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="dccf1-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="dccf1-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dccf1-114">EXAMPLES</span></span>

### <span data-ttu-id="dccf1-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dccf1-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="dccf1-116">Aktualizacja punktu końcowego ES1 subskrypcji zdarzenia dla tematu Temat1 w grupie zasobów \` \` \` \` \` Nazwa_grupy_Zasobów \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="dccf1-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="dccf1-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dccf1-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="dccf1-118">Aktualizacja punktu końcowego ES1 subskrypcji zdarzenia dla tematu Temat1 w grupie zasobów \` \` \` \` \` Nazwa_grupy_Zasobów \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="dccf1-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="dccf1-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="dccf1-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="dccf1-120">Aktualizuje właściwości subskrypcji zdarzeń ES1 dla przestrzeni nazw ContosoNamespace aplikacji EventHub przy użyciu nowego punktu końcowego jako " oraz nowego filtru \` \` \` https://requestb.in/1kxxoui1\ SubjectEndsWith jako \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="dccf1-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="dccf1-121">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="dccf1-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="dccf1-122">Aktualizuje właściwości subskrypcji zdarzenia ES1 dla grupy zasobów \` \` \` MyResourceGroupName przy użyciu nowych \` etykiet $labels.</span><span class="sxs-lookup"><span data-stu-id="dccf1-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="dccf1-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dccf1-123">PARAMETERS</span></span>

### <span data-ttu-id="dccf1-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="dccf1-124">-AdvancedFilter</span></span>
<span data-ttu-id="dccf1-125">Filtr zaawansowany określający tablicę wielu wartości w formie skrótów, które są używane do filtrowania opartego na atrybutach.</span><span class="sxs-lookup"><span data-stu-id="dccf1-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="dccf1-126">Każda wartość w tabeli skrótów ma następujące informacje key-value: Operation (Operacja), Key (Klucz) i Value (Wartości).</span><span class="sxs-lookup"><span data-stu-id="dccf1-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="dccf1-127">Operator może być jedną z następujących wartości: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith lub StringContains.</span><span class="sxs-lookup"><span data-stu-id="dccf1-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="dccf1-128">Klucz reprezentuje właściwość ładowania, do której są stosowane zaawansowane zasady filtrowania.</span><span class="sxs-lookup"><span data-stu-id="dccf1-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="dccf1-129">Natomiast wartość lub wartości reprezentują wartość lub zestaw wartości do dopasowania.</span><span class="sxs-lookup"><span data-stu-id="dccf1-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="dccf1-130">Może to być pojedyncza wartość odpowiedniego typu lub tablica wartości.</span><span class="sxs-lookup"><span data-stu-id="dccf1-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="dccf1-131">Jako przykład zaawansowanych parametrów filtru: $AdvancedFilters=@($AdvFilter 1; $AdvFilter 2), gdzie $AdvFilter 1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1;2)} and $AdvFilter 2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="dccf1-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="dccf1-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="dccf1-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="dccf1-133">Identyfikator aplikacji lub identyfikator Uri aplikacji usługi Azure Active Directory (AAD) w celu uzyskania tokenu dostępu, który zostanie uwzględniony jako token użytkownika w żądaniach dostarczenia. Ma zastosowanie tylko w przypadku webhook jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="dccf1-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dccf1-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="dccf1-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="dccf1-135">Identyfikator dzierżawy usługi Azure Active Directory (AAD) w celu uzyskania tokenu dostępu, który zostanie uwzględniony jako token użytkownika w żądaniach dostarczenia. Ma zastosowanie tylko w przypadku webhook jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="dccf1-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dccf1-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="dccf1-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="dccf1-137">Punkt końcowy używany do przechowywania niedostarczonych zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="dccf1-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="dccf1-138">Określ identyfikator zasobu Azure kontenera obiektów blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="dccf1-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="dccf1-139">Na przykład: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="dccf1-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="dccf1-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dccf1-140">-DefaultProfile</span></span>
<span data-ttu-id="dccf1-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dccf1-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dccf1-142">-DomainName</span><span class="sxs-lookup"><span data-stu-id="dccf1-142">-DomainName</span></span>
<span data-ttu-id="dccf1-143">Nazwa domeny, do której ma zostać utworzona subskrypcja zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="dccf1-143">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="dccf1-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="dccf1-144">-DomainTopicName</span></span>
<span data-ttu-id="dccf1-145">Nazwa tematu domeny, do którego ma zostać utworzona subskrypcja zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="dccf1-145">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="dccf1-146">- Punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="dccf1-146">-Endpoint</span></span>
<span data-ttu-id="dccf1-147">Punkt końcowy docelowej subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="dccf1-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="dccf1-148">Może to być adres URL sieci Web lub identyfikator zasobu Azure aplikacji EventHub, kolejka magazynu, połączenie hybrydowe lub kolejka usługi.</span><span class="sxs-lookup"><span data-stu-id="dccf1-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="dccf1-149">Na przykład identyfikator zasobu dla połączenia hybrydowego ma następującą postać: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="dccf1-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="dccf1-150">Przed wykonaniem jakichkolwiek cmdlet siatki zdarzeń oczekuje się, że docelowy punkt końcowy zostanie utworzony i dostępny do użycia.</span><span class="sxs-lookup"><span data-stu-id="dccf1-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="dccf1-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="dccf1-151">-EndpointType</span></span>
<span data-ttu-id="dccf1-152">Typ punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="dccf1-152">Endpoint Type.</span></span>
<span data-ttu-id="dccf1-153">Może to być usługa Webhook, EventHub, kolejka magazynowania, połączenie hybrydowe lub usługa kolejkowania usługi.</span><span class="sxs-lookup"><span data-stu-id="dccf1-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="dccf1-154">Wartość domyślna to webhook.</span><span class="sxs-lookup"><span data-stu-id="dccf1-154">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dccf1-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="dccf1-155">-EventSubscriptionName</span></span>
<span data-ttu-id="dccf1-156">Nazwa subskrypcji wydarzenia</span><span class="sxs-lookup"><span data-stu-id="dccf1-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="dccf1-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="dccf1-157">-EventTtl</span></span>
<span data-ttu-id="dccf1-158">Czas (w minutach) na dostarczenie zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="dccf1-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="dccf1-159">Ta wartość musi być między 1 a 1440</span><span class="sxs-lookup"><span data-stu-id="dccf1-159">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="dccf1-160">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="dccf1-160">-ExpirationDate</span></span>
<span data-ttu-id="dccf1-161">Określa datę wygaśnięcia subskrypcji wydarzenia DateTime, po upływie której subskrypcja zdarzeń zostanie wycofana.</span><span class="sxs-lookup"><span data-stu-id="dccf1-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="dccf1-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="dccf1-162">-IncludedEventType</span></span>
<span data-ttu-id="dccf1-163">Filtr określający listę typów zdarzeń, które mają być dołączane. Jeśli nie zostanie określone, zostaną uwzględnione wszystkie typy zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="dccf1-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="dccf1-164">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dccf1-164">-InputObject</span></span>
<span data-ttu-id="dccf1-165">Obiekt EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="dccf1-165">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="dccf1-166">— Etykieta</span><span class="sxs-lookup"><span data-stu-id="dccf1-166">-Label</span></span>
<span data-ttu-id="dccf1-167">Etykiety dla subskrypcji wydarzenia</span><span class="sxs-lookup"><span data-stu-id="dccf1-167">Labels for the event subscription</span></span>

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

### <span data-ttu-id="dccf1-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="dccf1-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="dccf1-169">Maksymalna liczba prób dostarczenia zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="dccf1-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="dccf1-170">Ta wartość musi być między 1 a 30</span><span class="sxs-lookup"><span data-stu-id="dccf1-170">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="dccf1-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="dccf1-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="dccf1-172">Maksymalna liczba zdarzeń w partii.</span><span class="sxs-lookup"><span data-stu-id="dccf1-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="dccf1-173">Ta wartość musi być między 1 a 5000.</span><span class="sxs-lookup"><span data-stu-id="dccf1-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="dccf1-174">Ten parametr jest prawidłowy, gdy typem endpint jest tylko webhook.</span><span class="sxs-lookup"><span data-stu-id="dccf1-174">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="dccf1-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="dccf1-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="dccf1-176">Preferowany rozmiar partii w kilobajtach.</span><span class="sxs-lookup"><span data-stu-id="dccf1-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="dccf1-177">Ta wartość musi być między 1 a 1024.</span><span class="sxs-lookup"><span data-stu-id="dccf1-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="dccf1-178">Ten parametr jest prawidłowy, gdy typem endpint jest tylko webhook.</span><span class="sxs-lookup"><span data-stu-id="dccf1-178">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="dccf1-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dccf1-179">-ResourceGroupName</span></span>
<span data-ttu-id="dccf1-180">Grupa zasobów tematu.</span><span class="sxs-lookup"><span data-stu-id="dccf1-180">The resource group of the topic.</span></span>

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

### <span data-ttu-id="dccf1-181">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dccf1-181">-ResourceId</span></span>
<span data-ttu-id="dccf1-182">Identyfikator zasobu, dla którego utworzono subskrypcję zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="dccf1-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="dccf1-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="dccf1-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="dccf1-184">Filtr określający, że zostaną uwzględnione tylko zdarzenia o określonym prefiksie tematu.</span><span class="sxs-lookup"><span data-stu-id="dccf1-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="dccf1-185">Jeśli nie zostanie określone, zostaną uwzględnione zdarzenia ze wszystkimi prefiksami tematu.</span><span class="sxs-lookup"><span data-stu-id="dccf1-185">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="dccf1-186">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="dccf1-186">-SubjectEndsWith</span></span>
<span data-ttu-id="dccf1-187">Filtr określający, że zostaną uwzględnione tylko zdarzenia pasujące do określonego sufiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="dccf1-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="dccf1-188">Jeśli nie zostanie określona, zostaną uwzględnione zdarzenia ze wszystkimi sufiksami tematu.</span><span class="sxs-lookup"><span data-stu-id="dccf1-188">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="dccf1-189">-TopicName</span><span class="sxs-lookup"><span data-stu-id="dccf1-189">-TopicName</span></span>
<span data-ttu-id="dccf1-190">Nazwa tematu, do którego ma zostać utworzona subskrypcja wydarzenia.</span><span class="sxs-lookup"><span data-stu-id="dccf1-190">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="dccf1-191">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dccf1-191">-Confirm</span></span>
<span data-ttu-id="dccf1-192">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dccf1-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dccf1-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dccf1-193">-WhatIf</span></span>
<span data-ttu-id="dccf1-194">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dccf1-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dccf1-195">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dccf1-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dccf1-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dccf1-196">CommonParameters</span></span>
<span data-ttu-id="dccf1-197">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dccf1-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dccf1-198">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dccf1-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dccf1-199">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dccf1-199">INPUTS</span></span>

### <span data-ttu-id="dccf1-200">System.String</span><span class="sxs-lookup"><span data-stu-id="dccf1-200">System.String</span></span>

### <span data-ttu-id="dccf1-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="dccf1-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="dccf1-202">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dccf1-202">OUTPUTS</span></span>

### <span data-ttu-id="dccf1-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="dccf1-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="dccf1-204">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dccf1-204">NOTES</span></span>

## <span data-ttu-id="dccf1-205">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dccf1-205">RELATED LINKS</span></span>
