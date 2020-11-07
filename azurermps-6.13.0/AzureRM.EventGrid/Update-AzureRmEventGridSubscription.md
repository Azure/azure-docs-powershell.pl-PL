---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/update-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
ms.openlocfilehash: d036ba2df289b0b2f84430f01000632a887ec20e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719128"
---
# <span data-ttu-id="f75fd-101">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f75fd-101">Update-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="f75fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f75fd-102">SYNOPSIS</span></span>
<span data-ttu-id="f75fd-103">Aktualizowanie właściwości subskrypcji zdarzenia w siatce zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="f75fd-103">Update the properties of an Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f75fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f75fd-104">SYNTAX</span></span>

### <span data-ttu-id="f75fd-105">ResourceGroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f75fd-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f75fd-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f75fd-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f75fd-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f75fd-107">EventSubscriptionInputObjectSet</span></span>
```
Update-AzureRmEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f75fd-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f75fd-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f75fd-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f75fd-109">DESCRIPTION</span></span>
<span data-ttu-id="f75fd-110">Aktualizowanie właściwości subskrypcji zdarzenia w siatce zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="f75fd-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="f75fd-111">Za pomocą tej funkcji można aktualizować filtr, miejsce docelowe lub etykiety istniejącego abonamentu zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="f75fd-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="f75fd-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f75fd-112">EXAMPLES</span></span>

### <span data-ttu-id="f75fd-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f75fd-113">Example 1</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="f75fd-114">Umożliwia zaktualizowanie punktu końcowego ES1 subskrypcji \` zdarzeń \` dla tematu \` Temat1 \` w \` usłudze MyResourceGroupName w grupie zasobów \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="f75fd-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="f75fd-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f75fd-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzureRmEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="f75fd-116">Umożliwia zaktualizowanie punktu końcowego ES1 subskrypcji \` zdarzeń \` dla tematu \` Temat1 \` w \` usłudze MyResourceGroupName w grupie zasobów \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="f75fd-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="f75fd-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f75fd-117">Example 3</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="f75fd-118">Aktualizuje właściwości ES1 subskrypcji zdarzeń \` \` dla obszaru nazw EventHub ContosoNamespace z nowym punktem końcowym jako \` https://requestb.in/1kxxoui1\ "i nowym SubjectEndsWith Filter jako \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="f75fd-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="f75fd-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="f75fd-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="f75fd-120">Aktualizuje właściwości ES1 subskrypcji zdarzeń \` \` dla grupy zasobów \` MyResourceGroupName \` przy użyciu nowych etykiet $labels.</span><span class="sxs-lookup"><span data-stu-id="f75fd-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="f75fd-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f75fd-121">PARAMETERS</span></span>

### <span data-ttu-id="f75fd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f75fd-122">-DefaultProfile</span></span>
<span data-ttu-id="f75fd-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f75fd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f75fd-124">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="f75fd-124">-Endpoint</span></span>
<span data-ttu-id="f75fd-125">Docelowy punkt końcowy subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="f75fd-125">Event subscription destination endpoint.</span></span>
<span data-ttu-id="f75fd-126">Może to być adres URL elementu webhook lub identyfikator zasobu platformy Azure centrum EventHub.</span><span class="sxs-lookup"><span data-stu-id="f75fd-126">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

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

### <span data-ttu-id="f75fd-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="f75fd-127">-EndpointType</span></span>
<span data-ttu-id="f75fd-128">Typ punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="f75fd-128">Endpoint Type.</span></span>
<span data-ttu-id="f75fd-129">Może to być element webhook lub eventhub</span><span class="sxs-lookup"><span data-stu-id="f75fd-129">This can be webhook or eventhub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75fd-130">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="f75fd-130">-EventSubscriptionName</span></span>
<span data-ttu-id="f75fd-131">Nazwa subskrypcji wydarzenia</span><span class="sxs-lookup"><span data-stu-id="f75fd-131">The name of the event subscription</span></span>

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

### <span data-ttu-id="f75fd-132">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="f75fd-132">-IncludedEventType</span></span>
<span data-ttu-id="f75fd-133">Filtr określający listę typów zdarzeń, które mają zostać uwzględnione. Jeśli nie określono tego parametru, zostaną uwzględnione wszystkie typy zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="f75fd-133">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="f75fd-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f75fd-134">-InputObject</span></span>
<span data-ttu-id="f75fd-135">Obiekt EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="f75fd-135">EventGridSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f75fd-136">-Label</span><span class="sxs-lookup"><span data-stu-id="f75fd-136">-Label</span></span>
<span data-ttu-id="f75fd-137">Etykiety dla subskrypcji zdarzeń</span><span class="sxs-lookup"><span data-stu-id="f75fd-137">Labels for the event subscription</span></span>

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

### <span data-ttu-id="f75fd-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f75fd-138">-ResourceGroupName</span></span>
<span data-ttu-id="f75fd-139">Grupa zasobów tematu.</span><span class="sxs-lookup"><span data-stu-id="f75fd-139">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f75fd-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f75fd-140">-ResourceId</span></span>
<span data-ttu-id="f75fd-141">Identyfikator zasobu, do którego utworzono subskrypcję zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="f75fd-141">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="f75fd-142">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="f75fd-142">-SubjectBeginsWith</span></span>
<span data-ttu-id="f75fd-143">Filtr określający, że będą uwzględniane tylko zdarzenia pasujące do określonego prefiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="f75fd-143">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="f75fd-144">Jeśli nie określono tego parametru, zostaną uwzględnione zdarzenia ze wszystkimi prefiksami tematów.</span><span class="sxs-lookup"><span data-stu-id="f75fd-144">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="f75fd-145">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="f75fd-145">-SubjectEndsWith</span></span>
<span data-ttu-id="f75fd-146">Filtr określający, że będą uwzględniane tylko zdarzenia pasujące do określonego sufiksu tematu.</span><span class="sxs-lookup"><span data-stu-id="f75fd-146">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="f75fd-147">Jeśli nie określono tego parametru, zostaną uwzględnione zdarzenia ze wszystkimi sufiksami tematów.</span><span class="sxs-lookup"><span data-stu-id="f75fd-147">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="f75fd-148">-Tematname</span><span class="sxs-lookup"><span data-stu-id="f75fd-148">-TopicName</span></span>
<span data-ttu-id="f75fd-149">Nazwa tematu, do którego ma zostać utworzona subskrypcja zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="f75fd-149">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="f75fd-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f75fd-150">-Confirm</span></span>
<span data-ttu-id="f75fd-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f75fd-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f75fd-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f75fd-152">-WhatIf</span></span>
<span data-ttu-id="f75fd-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f75fd-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f75fd-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f75fd-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f75fd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75fd-155">CommonParameters</span></span>
<span data-ttu-id="f75fd-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f75fd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75fd-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f75fd-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75fd-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f75fd-158">INPUTS</span></span>

### <span data-ttu-id="f75fd-159">System. String</span><span class="sxs-lookup"><span data-stu-id="f75fd-159">System.String</span></span>

### <span data-ttu-id="f75fd-160">Microsoft. Azure. Commands. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="f75fd-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>
<span data-ttu-id="f75fd-161">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f75fd-161">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f75fd-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f75fd-162">OUTPUTS</span></span>

### <span data-ttu-id="f75fd-163">Microsoft. Azure. Commands. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="f75fd-163">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="f75fd-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f75fd-164">NOTES</span></span>

## <span data-ttu-id="f75fd-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f75fd-165">RELATED LINKS</span></span>
