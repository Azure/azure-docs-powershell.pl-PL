---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: 7398dd0a80e2f84dcce929019038c616f6c7c1c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342145"
---
# <span data-ttu-id="ece85-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ece85-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="ece85-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ece85-102">SYNOPSIS</span></span>
<span data-ttu-id="ece85-103">Aktualizowanie właściwości subskrypcji zdarzenia w siatce zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ece85-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="ece85-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ece85-104">SYNTAX</span></span>

### <span data-ttu-id="ece85-105">ResourceGroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ece85-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece85-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece85-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece85-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece85-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ece85-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece85-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece85-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece85-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece85-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece85-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece85-111">Opis</span><span class="sxs-lookup"><span data-stu-id="ece85-111">DESCRIPTION</span></span>
<span data-ttu-id="ece85-112">Aktualizowanie właściwości subskrypcji zdarzenia w siatce zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ece85-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="ece85-113">Za pomocą tej funkcji można aktualizować filtr, miejsce docelowe lub etykiety istniejącego abonamentu zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ece85-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="ece85-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ece85-114">EXAMPLES</span></span>

### <span data-ttu-id="ece85-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ece85-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="ece85-116">Umożliwia zaktualizowanie punktu końcowego ES1 subskrypcji \` zdarzeń \` dla tematu \` Temat1 \` w \` usłudze MyResourceGroupName w grupie zasobów \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="ece85-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="ece85-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ece85-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="ece85-118">Umożliwia zaktualizowanie punktu końcowego ES1 subskrypcji \` zdarzeń \` dla tematu \` Temat1 \` w \` usłudze MyResourceGroupName w grupie zasobów \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="ece85-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="ece85-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ece85-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="ece85-120">Aktualizuje właściwości ES1 subskrypcji zdarzeń \` \` dla obszaru nazw EventHub ContosoNamespace z nowym punktem końcowym jako \` https://requestb.in/1kxxoui1\ "i nowym SubjectEndsWith Filter jako \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="ece85-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="ece85-121">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="ece85-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="ece85-122">Aktualizuje właściwości ES1 subskrypcji zdarzeń \` \` dla grupy zasobów \` MyResourceGroupName \` przy użyciu nowych etykiet $labels.</span><span class="sxs-lookup"><span data-stu-id="ece85-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="ece85-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ece85-123">PARAMETERS</span></span>

### <span data-ttu-id="ece85-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="ece85-124">-AdvancedFilter</span></span>
<span data-ttu-id="ece85-125">Filtr zaawansowany określający tablicę wielu wartości Hashtable, które są używane do filtrowania opartego na atrybutach.</span><span class="sxs-lookup"><span data-stu-id="ece85-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="ece85-126">Każda wartość Hashtable zawiera następujące klucze — informacje o wartości: operacja, klucz i wartość lub wartości.</span><span class="sxs-lookup"><span data-stu-id="ece85-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="ece85-127">Operator może należeć do jednej z następujących wartości: liczba, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, String, StringNotIn, StringBeginsWith, StringEndsWith lub StringContains.</span><span class="sxs-lookup"><span data-stu-id="ece85-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="ece85-128">Klucz reprezentuje właściwość ładunku, w której są stosowane zaawansowane zasady filtrowania.</span><span class="sxs-lookup"><span data-stu-id="ece85-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="ece85-129">Wreszcie wartość lub wartości reprezentują wartość lub zestaw wartości, które mają zostać dopasowane.</span><span class="sxs-lookup"><span data-stu-id="ece85-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="ece85-130">Może to być pojedyncza wartość odpowiedniego typu lub tablica wartości.</span><span class="sxs-lookup"><span data-stu-id="ece85-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="ece85-131">Przykładowe parametry filtru zaawansowanego: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), gdzie $AdvFilter 1 = @ {operator = "numerowanie"; Key = "Data. KEY1"; Wartości = @ (1, 2)} i $AdvFilter 2 = @ {operator = "StringBeginsWith"; Key = "subject"; Values = @ ("SubjectPrefix1"; "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="ece85-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="ece85-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="ece85-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="ece85-133">Identyfikator lub identyfikator URI aplikacji usługi Azure Active Directory (AAD) w celu uzyskania tokenu dostępu, który zostanie uwzględniony jako token okaziciela w żądaniach dostarczenia. Dotyczy tylko elementu webhook jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="ece85-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="ece85-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="ece85-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="ece85-135">Identyfikator dzierżawy usługi Azure Active Directory (AAD), aby uzyskać token dostępu, który będzie dołączany jako token okaziciela w żądaniach dostarczenia. Dotyczy tylko elementu webhook jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="ece85-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="ece85-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="ece85-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="ece85-137">Punkt końcowy służący do przechowywania zdarzeń niedostarczonych.</span><span class="sxs-lookup"><span data-stu-id="ece85-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="ece85-138">Określ identyfikator zasobu platformy Azure kontenera obiektu blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="ece85-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="ece85-139">Na przykład:/subscriptions/[subskrypcji]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="ece85-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="ece85-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece85-140">-DefaultProfile</span></span>
<span data-ttu-id="ece85-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ece85-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ece85-142">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="ece85-142">-DomainName</span></span>
<span data-ttu-id="ece85-143">Nazwa domeny, w której ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="ece85-143">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="ece85-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="ece85-144">-DomainTopicName</span></span>
<span data-ttu-id="ece85-145">Nazwa tematu domeny, dla którego ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="ece85-145">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="ece85-146">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece85-146">-Endpoint</span></span>
<span data-ttu-id="ece85-147">Docelowy punkt końcowy subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ece85-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="ece85-148">Może to być adres URL elementu webhook lub identyfikator zasobu platformy Azure w kolejce EventHub, Storage, hybridconnection lub servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="ece85-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="ece85-149">Na przykład identyfikator zasobu dla połączenia hybrydowego przyjmuje następujący formularz:/subscriptions/[Identyfikator subskrypcji Azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[Obszar_nazwname]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="ece85-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="ece85-150">Oczekuje się, że docelowy punkt końcowy zostanie utworzony i będzie dostępny do użytku przed wykonaniem poleceń cmdlet dotyczących siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ece85-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="ece85-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="ece85-151">-EndpointType</span></span>
<span data-ttu-id="ece85-152">Typ punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ece85-152">Endpoint Type.</span></span>
<span data-ttu-id="ece85-153">Może to być element webhook, eventhub, storagequeue, hybridconnection lub servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="ece85-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="ece85-154">Wartość domyślna to webhook.</span><span class="sxs-lookup"><span data-stu-id="ece85-154">Default value is webhook.</span></span>

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

### <span data-ttu-id="ece85-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ece85-155">-EventSubscriptionName</span></span>
<span data-ttu-id="ece85-156">Nazwa subskrypcji wydarzenia</span><span class="sxs-lookup"><span data-stu-id="ece85-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="ece85-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="ece85-157">-EventTtl</span></span>
<span data-ttu-id="ece85-158">Czas w minutach dostarczenia imprezy.</span><span class="sxs-lookup"><span data-stu-id="ece85-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="ece85-159">Ta wartość musi zawierać się między 1 a 1440</span><span class="sxs-lookup"><span data-stu-id="ece85-159">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="ece85-160">-Wartość datawygaśnięcia</span><span class="sxs-lookup"><span data-stu-id="ece85-160">-ExpirationDate</span></span>
<span data-ttu-id="ece85-161">Określa wartość daty wygaśnięcia dla subskrypcji zdarzenia, po której abonament zdarzenia zostanie wycofany.</span><span class="sxs-lookup"><span data-stu-id="ece85-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="ece85-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="ece85-162">-IncludedEventType</span></span>
<span data-ttu-id="ece85-163">Filtr określający listę typów zdarzeń, które mają zostać uwzględnione. Jeśli nie określono tego parametru, zostaną uwzględnione wszystkie typy zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ece85-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="ece85-164">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ece85-164">-InputObject</span></span>
<span data-ttu-id="ece85-165">Obiekt EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="ece85-165">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="ece85-166">-Label</span><span class="sxs-lookup"><span data-stu-id="ece85-166">-Label</span></span>
<span data-ttu-id="ece85-167">Etykiety dla subskrypcji zdarzeń</span><span class="sxs-lookup"><span data-stu-id="ece85-167">Labels for the event subscription</span></span>

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

### <span data-ttu-id="ece85-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="ece85-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="ece85-169">Maksymalna liczba prób dostarczenia zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="ece85-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="ece85-170">Ta wartość musi należeć do zakresu od 1 do 30</span><span class="sxs-lookup"><span data-stu-id="ece85-170">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="ece85-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="ece85-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="ece85-172">Maksymalna liczba zdarzeń w partii.</span><span class="sxs-lookup"><span data-stu-id="ece85-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="ece85-173">Ta wartość musi zawierać się między 1 a 5000.</span><span class="sxs-lookup"><span data-stu-id="ece85-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="ece85-174">Ten parametr jest prawidłowy, gdy typ Endpint jest tylko webhook.</span><span class="sxs-lookup"><span data-stu-id="ece85-174">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="ece85-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="ece85-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="ece85-176">Preferowany rozmiar wsadu w kilobajtach.</span><span class="sxs-lookup"><span data-stu-id="ece85-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="ece85-177">Ta wartość musi zawierać się między 1 a 1024.</span><span class="sxs-lookup"><span data-stu-id="ece85-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="ece85-178">Ten parametr jest prawidłowy, gdy typ Endpint jest tylko webhook.</span><span class="sxs-lookup"><span data-stu-id="ece85-178">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="ece85-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece85-179">-ResourceGroupName</span></span>
<span data-ttu-id="ece85-180">Grupa zasobów tematu.</span><span class="sxs-lookup"><span data-stu-id="ece85-180">The resource group of the topic.</span></span>

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

### <span data-ttu-id="ece85-181">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ece85-181">-ResourceId</span></span>
<span data-ttu-id="ece85-182">Identyfikator zasobu, do którego utworzono subskrypcję zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="ece85-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="ece85-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="ece85-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="ece85-184">Filtr określający, że będą uwzględniane tylko zdarzenia pasujące do określonego prefiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="ece85-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="ece85-185">Jeśli nie określono tego parametru, zostaną uwzględnione zdarzenia ze wszystkimi prefiksami tematów.</span><span class="sxs-lookup"><span data-stu-id="ece85-185">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="ece85-186">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="ece85-186">-SubjectEndsWith</span></span>
<span data-ttu-id="ece85-187">Filtr określający, że będą uwzględniane tylko zdarzenia pasujące do określonego sufiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="ece85-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="ece85-188">Jeśli nie określono tego parametru, zostaną uwzględnione zdarzenia ze wszystkimi sufiksami tematów.</span><span class="sxs-lookup"><span data-stu-id="ece85-188">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="ece85-189">-Tematname</span><span class="sxs-lookup"><span data-stu-id="ece85-189">-TopicName</span></span>
<span data-ttu-id="ece85-190">Nazwa tematu, do którego ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="ece85-190">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="ece85-191">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ece85-191">-Confirm</span></span>
<span data-ttu-id="ece85-192">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ece85-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece85-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece85-193">-WhatIf</span></span>
<span data-ttu-id="ece85-194">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ece85-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ece85-195">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ece85-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece85-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece85-196">CommonParameters</span></span>
<span data-ttu-id="ece85-197">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece85-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece85-198">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ece85-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece85-199">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ece85-199">INPUTS</span></span>

### <span data-ttu-id="ece85-200">System. String</span><span class="sxs-lookup"><span data-stu-id="ece85-200">System.String</span></span>

### <span data-ttu-id="ece85-201">Microsoft. Azure. Commands. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="ece85-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="ece85-202">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ece85-202">OUTPUTS</span></span>

### <span data-ttu-id="ece85-203">Microsoft. Azure. Commands. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="ece85-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="ece85-204">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ece85-204">NOTES</span></span>

## <span data-ttu-id="ece85-205">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ece85-205">RELATED LINKS</span></span>
