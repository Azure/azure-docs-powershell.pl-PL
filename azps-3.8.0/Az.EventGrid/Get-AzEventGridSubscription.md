---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 5adc6e203166903b0c76d906ce03cd72cb73c3d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895241"
---
# <span data-ttu-id="6aacf-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6aacf-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="6aacf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6aacf-102">SYNOPSIS</span></span>
<span data-ttu-id="6aacf-103">Pobiera szczegóły abonamentu wydarzenia lub pobiera listę wszystkich subskrypcji zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6aacf-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="6aacf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6aacf-104">SYNTAX</span></span>

### <span data-ttu-id="6aacf-105">EventSubscriptionTopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6aacf-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6aacf-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aacf-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6aacf-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aacf-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6aacf-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aacf-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6aacf-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aacf-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6aacf-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aacf-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6aacf-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aacf-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6aacf-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aacf-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6aacf-113">Opis</span><span class="sxs-lookup"><span data-stu-id="6aacf-113">DESCRIPTION</span></span>
<span data-ttu-id="6aacf-114">Polecenie cmdlet Get-AzEventGridSubscription pobiera szczegóły określonego abonamentu w siatce zdarzeń lub listę wszystkich subskrypcji siatki zdarzeń w bieżącej subskrypcji platformy Azure lub grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="6aacf-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="6aacf-115">Jeśli jest podana nazwa subskrypcji zdarzenia, zostanie zwrócona wartość szczegółów pojedynczego abonamentu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6aacf-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="6aacf-116">Jeśli nie podano nazwy subskrypcji zdarzeń, zostanie zwrócona lista wszystkich subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6aacf-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="6aacf-117">Liczba elementów zwróconych na tej liście jest kontrolowana przez parametr najwyższy.</span><span class="sxs-lookup"><span data-stu-id="6aacf-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="6aacf-118">Jeśli najszukana wartość nie jest określona lub $null, lista będzie zawierać wszystkie elementy subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6aacf-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="6aacf-119">W przeciwnym razie na początku będzie wskazywana Maksymalna liczba elementów, które mają zostać zwrócone na liście.</span><span class="sxs-lookup"><span data-stu-id="6aacf-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="6aacf-120">Jeśli dalsze subskrypcje zdarzeń są nadal dostępne, w następnej rozmowie należy użyć wartości z NextLink, aby uzyskać następną stronę abonamentów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6aacf-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="6aacf-121">Na koniec parametr ODataQuery jest wykorzystywany do filtrowania wyników wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6aacf-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="6aacf-122">Kwerenda filtrująca podąża za składnią funkcji OData tylko przy użyciu właściwości Name.</span><span class="sxs-lookup"><span data-stu-id="6aacf-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="6aacf-123">Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.</span><span class="sxs-lookup"><span data-stu-id="6aacf-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="6aacf-124">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6aacf-124">EXAMPLES</span></span>

### <span data-ttu-id="6aacf-125">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6aacf-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6aacf-126">Pobiera szczegóły subskrypcji zdarzeń \` EventSubscription1 \` utworzonych dla tematu \` Temat1 \` w MyResourceGroupNameach grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="6aacf-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6aacf-127">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6aacf-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="6aacf-128">Pobiera szczegóły subskrypcji zdarzeń \` EventSubscription1 \` utworzonych dla tematu \` Temat1 \` w grupie zasobów \` MyResourceGroupName \` , w tym pełny adres URL punktu końcowego, jeśli jest to subskrypcja zdarzeń oparta na składniku webhook.</span><span class="sxs-lookup"><span data-stu-id="6aacf-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="6aacf-129">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="6aacf-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="6aacf-130">Zapoznaj się z listą wszystkich subskrypcji zdarzeń utworzonych dla tematu \` Temat1 \` w grupie zasób \` MyResourceGroupName \` bez stronicowania.</span><span class="sxs-lookup"><span data-stu-id="6aacf-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="6aacf-131">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="6aacf-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="6aacf-132">Lista pierwszych 10 abonamentów zdarzeń utworzonych dla tematu \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` , które spełniają zapytanie $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="6aacf-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="6aacf-133">Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null.</span><span class="sxs-lookup"><span data-stu-id="6aacf-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="6aacf-134">Aby uzyskać kolejne strony subskrypcji zdarzeń, użytkownik powinien ponownie zadzwonić Get-AzEventGridSubscription i używa wyniku. NextLink uzyskana z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="6aacf-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="6aacf-135">Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.</span><span class="sxs-lookup"><span data-stu-id="6aacf-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="6aacf-136">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="6aacf-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6aacf-137">Pobiera szczegóły subskrypcji zdarzeń \` EventSubscription1 \` utworzonych dla MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="6aacf-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6aacf-138">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="6aacf-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6aacf-139">Pobiera szczegóły subskrypcji zdarzeń \` EventSubscription1 \` utworzonych dla obecnie wybranej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6aacf-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="6aacf-140">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="6aacf-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="6aacf-141">Pobiera listę wszystkich globalnych subskrypcji zdarzeń utworzonych w ramach grupy zasobów \` MyResourceGroupName \` bez stronicowania.</span><span class="sxs-lookup"><span data-stu-id="6aacf-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="6aacf-142">Przykład 8</span><span class="sxs-lookup"><span data-stu-id="6aacf-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="6aacf-143">Lista pierwszych 5 abonamentów zdarzeń utworzonych w ramach grupy zasobów \` MyResourceGroupName \` , które spełniają zapytanie $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="6aacf-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="6aacf-144">Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null.</span><span class="sxs-lookup"><span data-stu-id="6aacf-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="6aacf-145">Aby uzyskać kolejne strony subskrypcji zdarzeń, użytkownik powinien ponownie zadzwonić Get-AzEventGridSubscription i używa wyniku. NextLink uzyskana z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="6aacf-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="6aacf-146">Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.</span><span class="sxs-lookup"><span data-stu-id="6aacf-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="6aacf-147">Przykład 9</span><span class="sxs-lookup"><span data-stu-id="6aacf-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="6aacf-148">Pobiera listę wszystkich globalnych subskrypcji zdarzeń utworzonych w ramach obecnie wybranej subskrypcji platformy Azure bez stronicowania.</span><span class="sxs-lookup"><span data-stu-id="6aacf-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="6aacf-149">Przykład 10</span><span class="sxs-lookup"><span data-stu-id="6aacf-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="6aacf-150">Lista pierwszych 15 abonamentów zdarzeń globalnych (jeśli istnieją) utworzonych w ramach obecnie wybranej subskrypcji platformy Azure spełniającej zapytanie $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="6aacf-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="6aacf-151">Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null.</span><span class="sxs-lookup"><span data-stu-id="6aacf-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="6aacf-152">Aby uzyskać kolejne strony subskrypcji zdarzeń, użytkownik powinien ponownie zadzwonić Get-AzEventGridSubscription i używa wyniku. NextLink uzyskana z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="6aacf-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="6aacf-153">Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.</span><span class="sxs-lookup"><span data-stu-id="6aacf-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="6aacf-154">Przykład 11</span><span class="sxs-lookup"><span data-stu-id="6aacf-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="6aacf-155">Pobiera listę wszystkich regionalnych subskrypcji zdarzeń utworzonych w obszarze grupy zasobów \` MyResourceGroupName \` w określonej lokalizacji \` westus2 \` bez stronicowania.</span><span class="sxs-lookup"><span data-stu-id="6aacf-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="6aacf-156">Przykład 12</span><span class="sxs-lookup"><span data-stu-id="6aacf-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="6aacf-157">Lista pierwszych 15 abonamentów zdarzeń regionalnych (jeśli istnieją) utworzonych w obszarze grup zasobów \` MyResourceGroupName \` w określonej lokalizacji \` westus2 \` , która spełnia zapytanie $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="6aacf-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="6aacf-158">Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null.</span><span class="sxs-lookup"><span data-stu-id="6aacf-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="6aacf-159">Aby uzyskać kolejne strony subskrypcji zdarzeń, użytkownik powinien ponownie zadzwonić Get-AzEventGridSubscription i używa wyniku. NextLink uzyskana z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="6aacf-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="6aacf-160">Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.</span><span class="sxs-lookup"><span data-stu-id="6aacf-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="6aacf-161">Przykład 13</span><span class="sxs-lookup"><span data-stu-id="6aacf-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="6aacf-162">Pobiera listę wszystkich subskrypcji zdarzeń utworzonych dla określonego obszaru nazw EventHub bez stronicowania.</span><span class="sxs-lookup"><span data-stu-id="6aacf-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="6aacf-163">Przykład 14</span><span class="sxs-lookup"><span data-stu-id="6aacf-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="6aacf-164">Lista pierwszych 25 abonamentów zdarzeń utworzonych dla określonego obszaru nazw EventHub, który spełnia warunki kwerendy $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="6aacf-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="6aacf-165">Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null.</span><span class="sxs-lookup"><span data-stu-id="6aacf-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="6aacf-166">Aby uzyskać kolejne strony subskrypcji zdarzeń, użytkownik powinien ponownie zadzwonić Get-AzEventGridSubscription i używa wyniku. NextLink uzyskana z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="6aacf-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="6aacf-167">Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.</span><span class="sxs-lookup"><span data-stu-id="6aacf-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="6aacf-168">Przykład 15</span><span class="sxs-lookup"><span data-stu-id="6aacf-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="6aacf-169">Pobiera listę wszystkich subskrypcji zdarzeń utworzonych dla określonego typu tematu (obszary nazw EventHub) w określonej lokalizacji bez podziału na strony.</span><span class="sxs-lookup"><span data-stu-id="6aacf-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="6aacf-170">Przykład 16</span><span class="sxs-lookup"><span data-stu-id="6aacf-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="6aacf-171">Lista pierwszych 15 abonamentów zdarzeń utworzonych dla określonego typu tematu (obszary nazw EventHub) w określonej lokalizacji spełniającej zapytanie $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="6aacf-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="6aacf-172">Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null.</span><span class="sxs-lookup"><span data-stu-id="6aacf-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="6aacf-173">Aby uzyskać kolejne strony subskrypcji zdarzeń, użytkownik powinien ponownie zadzwonić Get-AzEventGridSubscription i używa wyniku. NextLink uzyskana z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="6aacf-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="6aacf-174">Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.</span><span class="sxs-lookup"><span data-stu-id="6aacf-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="6aacf-175">Przykład 17</span><span class="sxs-lookup"><span data-stu-id="6aacf-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="6aacf-176">Pobiera listę wszystkich subskrypcji zdarzeń utworzonych dla konkretnej grupy zasobów bez podziału na strony.</span><span class="sxs-lookup"><span data-stu-id="6aacf-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="6aacf-177">Przykład 18</span><span class="sxs-lookup"><span data-stu-id="6aacf-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="6aacf-178">Lista pierwszych 100ych subskrypcji zdarzeń (jeśli istnieją) utworzonych dla konkretnej grupy zasobów, które spełniają zapytanie $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="6aacf-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="6aacf-179">Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null.</span><span class="sxs-lookup"><span data-stu-id="6aacf-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="6aacf-180">Aby uzyskać kolejne strony subskrypcji zdarzeń, użytkownik powinien ponownie zadzwonić Get-AzEventGridSubscription i używa wyniku. NextLink uzyskana z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="6aacf-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="6aacf-181">Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.</span><span class="sxs-lookup"><span data-stu-id="6aacf-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="6aacf-182">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6aacf-182">PARAMETERS</span></span>

### <span data-ttu-id="6aacf-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aacf-183">-DefaultProfile</span></span>
<span data-ttu-id="6aacf-184">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6aacf-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6aacf-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="6aacf-185">-DomainInputObject</span></span>
<span data-ttu-id="6aacf-186">Obiekt domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6aacf-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="6aacf-187">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="6aacf-187">-DomainName</span></span>
<span data-ttu-id="6aacf-188">EventGrid nazwa domeny.</span><span class="sxs-lookup"><span data-stu-id="6aacf-188">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aacf-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="6aacf-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="6aacf-190">Obiekt tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6aacf-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="6aacf-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="6aacf-191">-DomainTopicName</span></span>
<span data-ttu-id="6aacf-192">Nazwa tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6aacf-192">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aacf-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6aacf-193">-EventSubscriptionName</span></span>
<span data-ttu-id="6aacf-194">Nazwa subskrypcji wydarzenia</span><span class="sxs-lookup"><span data-stu-id="6aacf-194">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aacf-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="6aacf-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="6aacf-196">Dołącz pełny adres URL punktu końcowego do miejsca docelowego subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="6aacf-196">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aacf-197">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6aacf-197">-InputObject</span></span>
<span data-ttu-id="6aacf-198">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6aacf-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="6aacf-199">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6aacf-199">-Location</span></span>
<span data-ttu-id="6aacf-200">Pozycję</span><span class="sxs-lookup"><span data-stu-id="6aacf-200">Location</span></span>

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

### <span data-ttu-id="6aacf-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="6aacf-201">-NextLink</span></span>
<span data-ttu-id="6aacf-202">Łącze do następnej strony, które mają zostać uzyskane.</span><span class="sxs-lookup"><span data-stu-id="6aacf-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="6aacf-203">Ta wartość jest uzyskiwana za pomocą pierwszego Get-AzEventGrid polecenia cmdlet, gdy więcej zasobów jest wciąż dostępnych do zbadania.</span><span class="sxs-lookup"><span data-stu-id="6aacf-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aacf-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="6aacf-204">-ODataQuery</span></span>
<span data-ttu-id="6aacf-205">Kwerenda OData używana do filtrowania wyników listy.</span><span class="sxs-lookup"><span data-stu-id="6aacf-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="6aacf-206">Filtrowanie jest obecnie dozwolone tylko w przypadku właściwości Name. Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.</span><span class="sxs-lookup"><span data-stu-id="6aacf-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aacf-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aacf-207">-ResourceGroupName</span></span>
<span data-ttu-id="6aacf-208">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6aacf-208">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aacf-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6aacf-209">-ResourceId</span></span>
<span data-ttu-id="6aacf-210">Identyfikator zasobu, do którego utworzono subskrypcje zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6aacf-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="6aacf-211">-Początek</span><span class="sxs-lookup"><span data-stu-id="6aacf-211">-Top</span></span>
<span data-ttu-id="6aacf-212">Kwerenda OData używana do filtrowania wyników listy.</span><span class="sxs-lookup"><span data-stu-id="6aacf-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="6aacf-213">Filtrowanie jest obecnie dozwolone tylko w przypadku właściwości Name. Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.</span><span class="sxs-lookup"><span data-stu-id="6aacf-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aacf-214">-Tematname</span><span class="sxs-lookup"><span data-stu-id="6aacf-214">-TopicName</span></span>
<span data-ttu-id="6aacf-215">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6aacf-215">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="6aacf-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="6aacf-216">-TopicTypeName</span></span>
<span data-ttu-id="6aacf-217">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="6aacf-217">TopicType name</span></span>

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

### <span data-ttu-id="6aacf-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aacf-218">CommonParameters</span></span>
<span data-ttu-id="6aacf-219">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aacf-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aacf-220">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aacf-220">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aacf-221">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6aacf-221">INPUTS</span></span>

### <span data-ttu-id="6aacf-222">System. String</span><span class="sxs-lookup"><span data-stu-id="6aacf-222">System.String</span></span>

### <span data-ttu-id="6aacf-223">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="6aacf-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="6aacf-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="6aacf-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="6aacf-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6aacf-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="6aacf-226">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6aacf-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6aacf-227">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6aacf-227">OUTPUTS</span></span>

### <span data-ttu-id="6aacf-228">Microsoft. Azure. Commands. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="6aacf-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="6aacf-229">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6aacf-229">NOTES</span></span>

## <span data-ttu-id="6aacf-230">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6aacf-230">RELATED LINKS</span></span>
