---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
ms.openlocfilehash: 3117433c677330eba4585d45337c44658225ee0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546643"
---
# <span data-ttu-id="c1470-101">Get-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="c1470-101">Get-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="c1470-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1470-102">SYNOPSIS</span></span>
<span data-ttu-id="c1470-103">Pobiera szczegóły abonamentu wydarzenia lub pobiera listę wszystkich subskrypcji zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c1470-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1470-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1470-104">SYNTAX</span></span>

### <span data-ttu-id="c1470-105">EventSubscriptionTopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c1470-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1470-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1470-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1470-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1470-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>]
 [[-Location] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1470-108">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c1470-108">EventSubscriptionInputObjectSet</span></span>
```
Get-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1470-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c1470-109">DESCRIPTION</span></span>
<span data-ttu-id="c1470-110">Polecenie cmdlet Get-AzureRmEventGridSubscription pobiera szczegóły określonego abonamentu w siatce zdarzeń lub listę wszystkich subskrypcji siatki zdarzeń w bieżącej subskrypcji platformy Azure lub grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c1470-110">The Get-AzureRmEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="c1470-111">Jeśli jest podana nazwa subskrypcji zdarzenia, zostanie zwrócona wartość szczegółów pojedynczego abonamentu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c1470-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="c1470-112">Jeśli nie podano nazwy subskrypcji zdarzeń, zostanie zwrócona lista wszystkich subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c1470-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="c1470-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1470-113">EXAMPLES</span></span>

### <span data-ttu-id="c1470-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c1470-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c1470-115">Pobiera szczegóły subskrypcji zdarzeń \` EventSubscription1 \` utworzonych dla tematu \` Temat1 \` w MyResourceGroupNameach grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="c1470-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c1470-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c1470-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="c1470-117">Pobiera szczegóły subskrypcji zdarzeń \` EventSubscription1 \` utworzonych dla tematu \` Temat1 \` w grupie zasobów \` MyResourceGroupName \` , w tym pełny adres URL punktu końcowego, jeśli jest to subskrypcja zdarzeń oparta na składniku webhook.</span><span class="sxs-lookup"><span data-stu-id="c1470-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="c1470-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c1470-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="c1470-119">Zapoznaj się z listą wszystkich subskrypcji zdarzeń utworzonych dla tematu \` Temat1 \` w grupie zasób \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c1470-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c1470-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="c1470-120">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c1470-121">Pobiera szczegóły subskrypcji zdarzeń \` EventSubscription1 \` utworzonych dla MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="c1470-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c1470-122">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="c1470-122">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c1470-123">Pobiera szczegóły subskrypcji zdarzeń \` EventSubscription1 \` utworzonych dla obecnie wybranej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c1470-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="c1470-124">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="c1470-124">Example 6</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="c1470-125">Pobiera listę wszystkich globalnych subskrypcji zdarzeń utworzonych w ramach grupy zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c1470-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c1470-126">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="c1470-126">Example 7</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription
```

<span data-ttu-id="c1470-127">Pobiera listę wszystkich globalnych subskrypcji zdarzeń utworzonych w ramach obecnie wybranej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c1470-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="c1470-128">Przykład 8</span><span class="sxs-lookup"><span data-stu-id="c1470-128">Example 8</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="c1470-129">Pobiera listę wszystkich regionalnych subskrypcji zdarzeń utworzonych w obszarze grupy zasobów \` MyResourceGroupName \` w określonej lokalizacji \` westus2 \` .</span><span class="sxs-lookup"><span data-stu-id="c1470-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="c1470-130">Przykład 9</span><span class="sxs-lookup"><span data-stu-id="c1470-130">Example 9</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="c1470-131">Pobiera listę wszystkich subskrypcji zdarzeń utworzonych dla określonego obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="c1470-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="c1470-132">Przykład 10</span><span class="sxs-lookup"><span data-stu-id="c1470-132">Example 10</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="c1470-133">Pobiera listę wszystkich subskrypcji zdarzeń utworzonych dla określonego typu tematu (obszarów nazw EventHub) w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c1470-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="c1470-134">Przykład 11</span><span class="sxs-lookup"><span data-stu-id="c1470-134">Example 11</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="c1470-135">Pobiera listę wszystkich subskrypcji zdarzeń utworzonych dla konkretnej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c1470-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="c1470-136">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1470-136">PARAMETERS</span></span>

### <span data-ttu-id="c1470-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1470-137">-DefaultProfile</span></span>
<span data-ttu-id="c1470-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c1470-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1470-139">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c1470-139">-EventSubscriptionName</span></span>
<span data-ttu-id="c1470-140">Nazwa subskrypcji wydarzenia</span><span class="sxs-lookup"><span data-stu-id="c1470-140">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1470-141">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="c1470-141">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="c1470-142">Dołącz pełny adres URL punktu końcowego do miejsca docelowego subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="c1470-142">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1470-143">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c1470-143">-InputObject</span></span>
<span data-ttu-id="c1470-144">Obiekt subskrypcji zdarzenia EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c1470-144">EventGrid Event Subscription object.</span></span>

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

### <span data-ttu-id="c1470-145">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c1470-145">-Location</span></span>
<span data-ttu-id="c1470-146">Pozycję</span><span class="sxs-lookup"><span data-stu-id="c1470-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1470-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1470-147">-ResourceGroupName</span></span>
<span data-ttu-id="c1470-148">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c1470-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1470-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1470-149">-ResourceId</span></span>
<span data-ttu-id="c1470-150">Identyfikator zasobu, do którego utworzono subskrypcje zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c1470-150">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1470-151">-Tematname</span><span class="sxs-lookup"><span data-stu-id="c1470-151">-TopicName</span></span>
<span data-ttu-id="c1470-152">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c1470-152">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1470-153">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="c1470-153">-TopicTypeName</span></span>
<span data-ttu-id="c1470-154">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="c1470-154">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1470-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1470-155">CommonParameters</span></span>
<span data-ttu-id="c1470-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1470-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1470-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1470-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1470-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1470-158">INPUTS</span></span>

### <span data-ttu-id="c1470-159">System. String</span><span class="sxs-lookup"><span data-stu-id="c1470-159">System.String</span></span>

### <span data-ttu-id="c1470-160">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="c1470-160">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="c1470-161">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c1470-161">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c1470-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1470-162">OUTPUTS</span></span>

### <span data-ttu-id="c1470-163">Microsoft. Azure. Commands. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="c1470-163">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="c1470-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1470-164">NOTES</span></span>

## <span data-ttu-id="c1470-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1470-165">RELATED LINKS</span></span>
