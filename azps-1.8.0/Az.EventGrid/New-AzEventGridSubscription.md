---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 1c0391fa266e498c717bc4eb43bd92ab93be508f
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395190"
---
# <span data-ttu-id="c74e3-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="c74e3-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="c74e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c74e3-102">SYNOPSIS</span></span>
<span data-ttu-id="c74e3-103">Tworzy nowy abonament zdarzeń w siatce zdarzeń platformy Azure dla tematu, zasobu platformy Azure, subskrypcji platformy Azure lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c74e3-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="c74e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c74e3-104">SYNTAX</span></span>

### <span data-ttu-id="c74e3-105">ResourceGroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c74e3-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c74e3-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c74e3-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c74e3-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c74e3-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c74e3-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c74e3-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c74e3-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c74e3-109">DESCRIPTION</span></span>
<span data-ttu-id="c74e3-110">Utwórz nowy abonament zdarzenia w temacie poświęconym siatce zdarzeń platformy Azure, obsługiwany zasób platformy Azure, subskrypcja platformy Azure lub Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="c74e3-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="c74e3-111">Aby utworzyć subskrypcję zdarzeń dla obecnie wybranej subskrypcji platformy Azure, określ nazwę subskrypcji zdarzeń oraz punkt końcowy miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="c74e3-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="c74e3-112">Aby utworzyć subskrypcję zdarzeń dla grupy zasobów, określ nazwę grupy zasobów oprócz nazwy subskrypcji zdarzeń i punktu końcowego miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="c74e3-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="c74e3-113">Aby utworzyć subskrypcję zdarzeń w temacie Azure Event Grid, określ również nazwę tematu.</span><span class="sxs-lookup"><span data-stu-id="c74e3-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="c74e3-114">Aby utworzyć subskrypcję zdarzeń dla obsługiwanego zasobu platformy Azure, określ pełny identyfikator zasobu tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="c74e3-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="c74e3-115">Aby wyświetlić listę obsługiwanych typów, uruchom polecenie cmdlet Get-AzEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="c74e3-115">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="c74e3-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c74e3-116">EXAMPLES</span></span>

### <span data-ttu-id="c74e3-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c74e3-117">Example 1</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c74e3-118">Tworzy nowe EventSubscription1 abonamentu \` zdarzeń \` na temat siatki zdarzeń usługi Azure \` Temat1 \` w grupie zasobów \` MyResourceGroupName \` z docelowym punktem końcowym elementu webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="c74e3-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="c74e3-119">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="c74e3-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="c74e3-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c74e3-120">Example 2</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c74e3-121">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w grupie zasobów \` MyResourceGroupName \` z docelowym punktem końcowym elementu webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="c74e3-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="c74e3-122">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="c74e3-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="c74e3-123">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c74e3-123">Example 3</span></span>
```
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c74e3-124">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w obecnie wybranej subskrypcji platformy Azure z punktem końcowym elementu webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="c74e3-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="c74e3-125">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="c74e3-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="c74e3-126">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="c74e3-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="c74e3-127">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w obecnie wybranej subskrypcji platformy Azure z punktem końcowym elementu webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="c74e3-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="c74e3-128">Ten abonament zdarzeń określa dodatkowe filtry dla typów zdarzeń i tematu, a tylko te zdarzenia, które pasują do tych filtrów, będą dostarczane do docelowego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="c74e3-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="c74e3-129">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="c74e3-129">Example 5</span></span>
```
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="c74e3-130">Tworzy nowy EventSubscription1 abonamentu \` zdarzeń \` w obecnie wybranej subskrypcji platformy Azure z określonym centrum zdarzeń jako miejscem docelowym zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c74e3-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="c74e3-131">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="c74e3-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="c74e3-132">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="c74e3-132">Example 6</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c74e3-133">Tworzy nową subskrypcję zdarzeń \` EventSubscription1 \` do obszaru nazw EventHub przy użyciu określonego punktu końcowego elementu webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="c74e3-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="c74e3-134">W przypadku tej subskrypcji zdarzeń są używane filtry domyślne.</span><span class="sxs-lookup"><span data-stu-id="c74e3-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="c74e3-135">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c74e3-135">PARAMETERS</span></span>

### <span data-ttu-id="c74e3-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="c74e3-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="c74e3-137">Punkt końcowy służący do przechowywania zdarzeń niedostarczonych.</span><span class="sxs-lookup"><span data-stu-id="c74e3-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="c74e3-138">Określ identyfikator zasobu platformy Azure kontenera obiektu blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="c74e3-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="c74e3-139">Na przykład:/subscriptions/[subskrypcji]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="c74e3-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c74e3-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c74e3-140">-DefaultProfile</span></span>
<span data-ttu-id="c74e3-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c74e3-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c74e3-142">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="c74e3-142">-Endpoint</span></span>
<span data-ttu-id="c74e3-143">Docelowy punkt końcowy subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c74e3-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="c74e3-144">Może to być adres URL elementu webhook lub identyfikator zasobu platformy Azure centrum EventHub, kolejki przechowywania lub hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="c74e3-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="c74e3-145">Na przykład identyfikator zasobu dla połączenia hybrydowego przyjmuje następujący formularz:/subscriptions/[Identyfikator subskrypcji Azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[Obszar_nazwname]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="c74e3-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="c74e3-146">Oczekuje się, że docelowy punkt końcowy zostanie utworzony i będzie dostępny do użytku przed wykonaniem poleceń cmdlet dotyczących siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c74e3-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c74e3-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="c74e3-147">-EndpointType</span></span>
<span data-ttu-id="c74e3-148">Typ punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="c74e3-148">Endpoint Type.</span></span>
<span data-ttu-id="c74e3-149">Może to być element webhook, eventhub, storagequeue lub hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="c74e3-149">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="c74e3-150">Wartość domyślna to webhook.</span><span class="sxs-lookup"><span data-stu-id="c74e3-150">Default value is webhook.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c74e3-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c74e3-151">-EventSubscriptionName</span></span>
<span data-ttu-id="c74e3-152">Nazwa subskrypcji wydarzenia</span><span class="sxs-lookup"><span data-stu-id="c74e3-152">The name of the event subscription</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c74e3-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="c74e3-153">-EventTtl</span></span>
<span data-ttu-id="c74e3-154">Czas w minutach dostarczenia imprezy.</span><span class="sxs-lookup"><span data-stu-id="c74e3-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="c74e3-155">Ta wartość musi zawierać się między 1 a 1440</span><span class="sxs-lookup"><span data-stu-id="c74e3-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c74e3-156">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="c74e3-156">-IncludedEventType</span></span>
<span data-ttu-id="c74e3-157">Filtr określający listę typów zdarzeń, które mają zostać uwzględnione. Jeśli nie określono tego parametru, zostaną uwzględnione wszystkie typy zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c74e3-157">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c74e3-158">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c74e3-158">-InputObject</span></span>
<span data-ttu-id="c74e3-159">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c74e3-159">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="c74e3-160">-Label</span><span class="sxs-lookup"><span data-stu-id="c74e3-160">-Label</span></span>
<span data-ttu-id="c74e3-161">Etykiety dla subskrypcji zdarzeń</span><span class="sxs-lookup"><span data-stu-id="c74e3-161">Labels for the event subscription</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c74e3-162">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="c74e3-162">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="c74e3-163">Maksymalna liczba prób dostarczenia zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="c74e3-163">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="c74e3-164">Ta wartość musi należeć do zakresu od 1 do 30</span><span class="sxs-lookup"><span data-stu-id="c74e3-164">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c74e3-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c74e3-165">-ResourceGroupName</span></span>
<span data-ttu-id="c74e3-166">Grupa zasobów tematu.</span><span class="sxs-lookup"><span data-stu-id="c74e3-166">The resource group of the topic.</span></span>

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

### <span data-ttu-id="c74e3-167">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c74e3-167">-ResourceId</span></span>
<span data-ttu-id="c74e3-168">Identyfikator zasobu, dla którego ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="c74e3-168">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="c74e3-169">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="c74e3-169">-SubjectBeginsWith</span></span>
<span data-ttu-id="c74e3-170">Filtr określający, że będą uwzględniane tylko zdarzenia pasujące do określonego prefiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="c74e3-170">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="c74e3-171">Jeśli nie określono tego parametru, zostaną uwzględnione zdarzenia ze wszystkimi prefiksami tematów.</span><span class="sxs-lookup"><span data-stu-id="c74e3-171">If not specified, events with all subject prefixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c74e3-172">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="c74e3-172">-SubjectCaseSensitive</span></span>
<span data-ttu-id="c74e3-173">Filtr określający, że pole temat powinno być porównywane w sposób uwzględniający wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="c74e3-173">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="c74e3-174">Jeśli nie określono, temat będzie porównywany w sposób niewrażliwy na wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="c74e3-174">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="c74e3-175">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="c74e3-175">-SubjectEndsWith</span></span>
<span data-ttu-id="c74e3-176">Filtr określający, że będą uwzględniane tylko zdarzenia pasujące do określonego sufiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="c74e3-176">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="c74e3-177">Jeśli nie określono tego parametru, zostaną uwzględnione zdarzenia ze wszystkimi sufiksami tematów.</span><span class="sxs-lookup"><span data-stu-id="c74e3-177">If not specified, events with all subject suffixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c74e3-178">-Tematname</span><span class="sxs-lookup"><span data-stu-id="c74e3-178">-TopicName</span></span>
<span data-ttu-id="c74e3-179">Nazwa tematu, do którego ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="c74e3-179">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="c74e3-180">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c74e3-180">-Confirm</span></span>
<span data-ttu-id="c74e3-181">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c74e3-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c74e3-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c74e3-182">-WhatIf</span></span>
<span data-ttu-id="c74e3-183">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c74e3-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c74e3-184">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c74e3-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c74e3-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c74e3-185">CommonParameters</span></span>
<span data-ttu-id="c74e3-186">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c74e3-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c74e3-187">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c74e3-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c74e3-188">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c74e3-188">INPUTS</span></span>

### <span data-ttu-id="c74e3-189">System. String</span><span class="sxs-lookup"><span data-stu-id="c74e3-189">System.String</span></span>

### <span data-ttu-id="c74e3-190">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="c74e3-190">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="c74e3-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="c74e3-191">System.String[]</span></span>

## <span data-ttu-id="c74e3-192">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c74e3-192">OUTPUTS</span></span>

### <span data-ttu-id="c74e3-193">Microsoft. Azure. Commands. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="c74e3-193">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="c74e3-194">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c74e3-194">NOTES</span></span>

## <span data-ttu-id="c74e3-195">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c74e3-195">RELATED LINKS</span></span>
