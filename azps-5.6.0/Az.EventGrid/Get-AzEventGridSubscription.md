---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 665f090f8de059afa4a7f1bd95685e3364a21611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991362"
---
# <span data-ttu-id="99b56-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="99b56-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="99b56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99b56-102">SYNOPSIS</span></span>
<span data-ttu-id="99b56-103">Pobiera szczegóły subskrypcji zdarzeń lub pobiera listę wszystkich subskrypcji zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="99b56-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="99b56-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="99b56-104">SYNTAX</span></span>

### <span data-ttu-id="99b56-105">EventSubscriptionTopicNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="99b56-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b56-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="99b56-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b56-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="99b56-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b56-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="99b56-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99b56-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99b56-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b56-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99b56-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b56-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99b56-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b56-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="99b56-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99b56-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="99b56-113">DESCRIPTION</span></span>
<span data-ttu-id="99b56-114">Polecenie cmdlet Get-AzEventGridSubscription pobiera szczegóły określonej subskrypcji siatki zdarzeń lub listę wszystkich subskrypcji siatki zdarzeń w bieżącej subskrypcji platformy Azure lub grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="99b56-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="99b56-115">Jeśli podano nazwę subskrypcji zdarzenia, zwracane są szczegóły pojedynczej subskrypcji siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="99b56-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="99b56-116">Jeśli nazwa subskrypcji wydarzenia nie jest podano, zostanie zwrócona lista wszystkich subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="99b56-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="99b56-117">Liczba elementów zwracanych na tej liście jest kontrolowana przez parametr Top.</span><span class="sxs-lookup"><span data-stu-id="99b56-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="99b56-118">Jeśli wartość Top nie zostanie określona lub $null, lista będzie zawierać wszystkie elementy subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="99b56-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="99b56-119">W przeciwnym razie top wskaże maksymalną liczbę elementów, które mają zostać zwrócone na liście.</span><span class="sxs-lookup"><span data-stu-id="99b56-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="99b56-120">Jeśli nadal dostępnych jest więcej subskrypcji zdarzeń, wartość w programie NextLink powinna być używana podczas następnego połączenia w celu uzyskania następnej strony subskrypcji zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="99b56-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="99b56-121">Na koniec parametr ODataQuery służy do filtrowania wyników wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="99b56-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="99b56-122">Zapytanie filtrujące korzysta ze składni OData tylko przy użyciu właściwości Name.</span><span class="sxs-lookup"><span data-stu-id="99b56-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="99b56-123">Obsługiwane operacje to: CONTAINS, eq (dla równości), ne (dla nie równa się), ORAZ, LUB i NIE.</span><span class="sxs-lookup"><span data-stu-id="99b56-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="99b56-124">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="99b56-124">EXAMPLES</span></span>

### <span data-ttu-id="99b56-125">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99b56-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="99b56-126">Pobiera szczegóły subskrypcji zdarzenia EventSubscription1 utworzonej dla tematu Topic1 w grupie zasobów \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="99b56-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="99b56-127">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="99b56-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="99b56-128">Pobiera szczegółowe informacje dotyczące subskrypcji zdarzeń EventSubscription1 utworzonej dla tematu Topic1 w grupie zasobów \` \` Nazwa_grupy Zasobów \` \` \` MyResourceGroupName, \` w tym pełny adres URL punktu końcowego, jeśli jest to subskrypcja zdarzeń oparta na sieci Web.</span><span class="sxs-lookup"><span data-stu-id="99b56-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="99b56-129">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="99b56-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="99b56-130">Uzyskaj listę wszystkich subskrypcji zdarzeń utworzonych dla tematu Temat1 w grupie zasobów \` \` \` Nazwa_grupy_zasobów Bez \` podziałów na strony.</span><span class="sxs-lookup"><span data-stu-id="99b56-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="99b56-131">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="99b56-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="99b56-132">Lista pierwszych 10 subskrypcji zdarzeń (jeśli są) utworzonych dla tematu Temat1 w grupie zasobów Nazwa_grupy zasobów, która spełnia $odataFilter \` \` \` \` zapytania.</span><span class="sxs-lookup"><span data-stu-id="99b56-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="99b56-133">Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink.</span><span class="sxs-lookup"><span data-stu-id="99b56-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="99b56-134">W celu uzyskania kolejnych stron subskrypcji zdarzeń użytkownik powinien ponownie na Get-AzEventGridSubscription korzysta z wyników. Przycisk NextLink uzyskany z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="99b56-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="99b56-135">Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.</span><span class="sxs-lookup"><span data-stu-id="99b56-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="99b56-136">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="99b56-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="99b56-137">Pobiera szczegółowe informacje dotyczące subskrypcji zdarzeń \` EventSubscription1 utworzonej dla \` grupy zasobów \` Nazwa_grupy_zasobów. \`</span><span class="sxs-lookup"><span data-stu-id="99b56-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="99b56-138">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="99b56-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="99b56-139">Pobiera szczegóły subskrypcji zdarzeń \` EventSubscription1 \` utworzonej dla obecnie wybranej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="99b56-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="99b56-140">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="99b56-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="99b56-141">Pobiera listę wszystkich subskrypcji zdarzeń globalnych utworzonych w ramach grupy zasobów \` MyResourceGroupName \` bez podziałów na strony.</span><span class="sxs-lookup"><span data-stu-id="99b56-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="99b56-142">Przykład 8</span><span class="sxs-lookup"><span data-stu-id="99b56-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="99b56-143">Lista pierwszych 5 subskrypcji zdarzeń (jeśli są tworzone) utworzonych w ramach grupy zasobów Nazwa_grupy zasobów, spełniających $odataFilter \` \` grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="99b56-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="99b56-144">Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink.</span><span class="sxs-lookup"><span data-stu-id="99b56-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="99b56-145">W celu uzyskania kolejnych stron subskrypcji zdarzeń użytkownik powinien ponownie na Get-AzEventGridSubscription korzysta z wyników. Przycisk NextLink uzyskany z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="99b56-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="99b56-146">Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.</span><span class="sxs-lookup"><span data-stu-id="99b56-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="99b56-147">Przykład 9</span><span class="sxs-lookup"><span data-stu-id="99b56-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="99b56-148">Pobiera listę wszystkich subskrypcji wydarzenia globalnego utworzonych w ramach obecnie wybranej subskrypcji platformy Azure bez podziałów na strony.</span><span class="sxs-lookup"><span data-stu-id="99b56-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="99b56-149">Przykład 10</span><span class="sxs-lookup"><span data-stu-id="99b56-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="99b56-150">Lista pierwszych 15 subskrypcji zdarzeń globalnych (jeśli są dostępne) utworzonych w ramach obecnie wybranej subskrypcji platformy Azure, które zaspokajają $odataFilter usługi.</span><span class="sxs-lookup"><span data-stu-id="99b56-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="99b56-151">Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink.</span><span class="sxs-lookup"><span data-stu-id="99b56-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="99b56-152">W celu uzyskania kolejnych stron subskrypcji zdarzeń użytkownik powinien ponownie na Get-AzEventGridSubscription korzysta z wyników. Przycisk NextLink uzyskany z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="99b56-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="99b56-153">Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.</span><span class="sxs-lookup"><span data-stu-id="99b56-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="99b56-154">Przykład 11</span><span class="sxs-lookup"><span data-stu-id="99b56-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="99b56-155">Pobiera listę wszystkich subskrypcji zdarzeń regionalnych utworzonych w grupie zasobów MyResourceGroupName w określonej lokalizacji \` \` na \` zachódus2 \` bez podziałów na strony.</span><span class="sxs-lookup"><span data-stu-id="99b56-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="99b56-156">Przykład 12</span><span class="sxs-lookup"><span data-stu-id="99b56-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="99b56-157">Lista pierwszych 15 subskrypcji zdarzeń regionalnych (jeśli są tworzone) utworzonych w ramach grupy zasobów Nazwa_grupy zasobów MyResourceGroupName w określonej lokalizacji \` \` \` westus2, która spełnia $odataFilter \` grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="99b56-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="99b56-158">Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink.</span><span class="sxs-lookup"><span data-stu-id="99b56-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="99b56-159">W celu uzyskania kolejnych stron subskrypcji zdarzeń użytkownik powinien ponownie na Get-AzEventGridSubscription korzysta z wyników. Przycisk NextLink uzyskany z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="99b56-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="99b56-160">Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.</span><span class="sxs-lookup"><span data-stu-id="99b56-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="99b56-161">Przykład 13</span><span class="sxs-lookup"><span data-stu-id="99b56-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="99b56-162">Pobiera listę wszystkich subskrypcji zdarzeń utworzonych dla określonej przestrzeni nazw aplikacji EventHub bez podziałów na strony.</span><span class="sxs-lookup"><span data-stu-id="99b56-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="99b56-163">Przykład 14</span><span class="sxs-lookup"><span data-stu-id="99b56-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="99b56-164">Lista pierwszych 25 subskrypcji zdarzeń (jeśli są one utworzone) dla określonej przestrzeni nazw aplikacji EventHub, która spełnia $odataFilter zapytania.</span><span class="sxs-lookup"><span data-stu-id="99b56-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="99b56-165">Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink.</span><span class="sxs-lookup"><span data-stu-id="99b56-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="99b56-166">W celu uzyskania kolejnych stron subskrypcji zdarzeń użytkownik powinien ponownie na Get-AzEventGridSubscription korzysta z wyników. Przycisk NextLink uzyskany z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="99b56-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="99b56-167">Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.</span><span class="sxs-lookup"><span data-stu-id="99b56-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="99b56-168">Przykład 15</span><span class="sxs-lookup"><span data-stu-id="99b56-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="99b56-169">Pobiera listę wszystkich subskrypcji zdarzeń utworzonych dla określonego typu tematu (przestrzenie nazw aplikacji EventHub) w określonej lokalizacji bez podziałów na strony.</span><span class="sxs-lookup"><span data-stu-id="99b56-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="99b56-170">Przykład 16</span><span class="sxs-lookup"><span data-stu-id="99b56-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="99b56-171">Lista pierwszych 15 subskrypcji zdarzeń (jeśli są one utworzone) dla określonego typu tematu (przestrzenie nazw aplikacji EventHub) w określonej lokalizacji, która spełnia $odataFilter zapytania.</span><span class="sxs-lookup"><span data-stu-id="99b56-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="99b56-172">Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink.</span><span class="sxs-lookup"><span data-stu-id="99b56-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="99b56-173">W celu uzyskania kolejnych stron subskrypcji zdarzeń użytkownik powinien ponownie na Get-AzEventGridSubscription korzysta z wyników. Przycisk NextLink uzyskany z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="99b56-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="99b56-174">Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.</span><span class="sxs-lookup"><span data-stu-id="99b56-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="99b56-175">Przykład 17</span><span class="sxs-lookup"><span data-stu-id="99b56-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="99b56-176">Pobiera listę wszystkich subskrypcji zdarzeń utworzonych dla określonej grupy zasobów bez podziałów na strony.</span><span class="sxs-lookup"><span data-stu-id="99b56-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="99b56-177">Przykład 18</span><span class="sxs-lookup"><span data-stu-id="99b56-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="99b56-178">Lista pierwszych 100 subskrypcji zdarzeń (jeśli są) utworzonych dla określonej grupy zasobów, która spełnia $odataFilter zapytania.</span><span class="sxs-lookup"><span data-stu-id="99b56-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="99b56-179">Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink.</span><span class="sxs-lookup"><span data-stu-id="99b56-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="99b56-180">W celu uzyskania kolejnych stron subskrypcji zdarzeń użytkownik powinien ponownie na Get-AzEventGridSubscription korzysta z wyników. Przycisk NextLink uzyskany z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="99b56-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="99b56-181">Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.</span><span class="sxs-lookup"><span data-stu-id="99b56-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="99b56-182">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99b56-182">PARAMETERS</span></span>

### <span data-ttu-id="99b56-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b56-183">-DefaultProfile</span></span>
<span data-ttu-id="99b56-184">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="99b56-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99b56-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="99b56-185">-DomainInputObject</span></span>
<span data-ttu-id="99b56-186">Obiekt Domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="99b56-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="99b56-187">-DomainName</span><span class="sxs-lookup"><span data-stu-id="99b56-187">-DomainName</span></span>
<span data-ttu-id="99b56-188">Nazwa domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="99b56-188">EventGrid domain name.</span></span>

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

### <span data-ttu-id="99b56-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="99b56-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="99b56-190">Obiekt tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="99b56-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="99b56-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="99b56-191">-DomainTopicName</span></span>
<span data-ttu-id="99b56-192">Nazwa tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="99b56-192">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="99b56-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="99b56-193">-EventSubscriptionName</span></span>
<span data-ttu-id="99b56-194">Nazwa subskrypcji wydarzenia</span><span class="sxs-lookup"><span data-stu-id="99b56-194">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b56-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="99b56-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="99b56-196">Uwzględnij pełny adres URL punktu końcowego miejsca docelowego subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="99b56-196">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="99b56-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99b56-197">-InputObject</span></span>
<span data-ttu-id="99b56-198">Obiekt tematu w aplikacji EventGrid.</span><span class="sxs-lookup"><span data-stu-id="99b56-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="99b56-199">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="99b56-199">-Location</span></span>
<span data-ttu-id="99b56-200">Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="99b56-200">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b56-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="99b56-201">-NextLink</span></span>
<span data-ttu-id="99b56-202">Link do następnej strony zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="99b56-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="99b56-203">Ta wartość jest uzyskiwana w przypadku pierwszego Get-AzEventGrid cmdlet, gdy nadal jest dostępnych więcej zasobów do zapytania.</span><span class="sxs-lookup"><span data-stu-id="99b56-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="99b56-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="99b56-204">-ODataQuery</span></span>
<span data-ttu-id="99b56-205">Zapytanie OData używane do filtrowania wyników listy.</span><span class="sxs-lookup"><span data-stu-id="99b56-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="99b56-206">Filtrowanie jest obecnie dozwolone tylko we właściwości Name. Obsługiwane operacje to: CONTAINS, eq (dla równości), ne (dla nie równa się), ORAZ, LUB i NIE.</span><span class="sxs-lookup"><span data-stu-id="99b56-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="99b56-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99b56-207">-ResourceGroupName</span></span>
<span data-ttu-id="99b56-208">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="99b56-208">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b56-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99b56-209">-ResourceId</span></span>
<span data-ttu-id="99b56-210">Identyfikator zasobu, do którego utworzono subskrypcje zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="99b56-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="99b56-211">— Na górze</span><span class="sxs-lookup"><span data-stu-id="99b56-211">-Top</span></span>
<span data-ttu-id="99b56-212">Zapytanie OData używane do filtrowania wyników listy.</span><span class="sxs-lookup"><span data-stu-id="99b56-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="99b56-213">Filtrowanie jest obecnie dozwolone tylko we właściwości Name. Obsługiwane operacje to: CONTAINS, eq (dla równości), ne (dla nie równa się), ORAZ, LUB i NIE.</span><span class="sxs-lookup"><span data-stu-id="99b56-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="99b56-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="99b56-214">-TopicName</span></span>
<span data-ttu-id="99b56-215">Nazwa tematu w aplikacji EventGrid.</span><span class="sxs-lookup"><span data-stu-id="99b56-215">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b56-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="99b56-216">-TopicTypeName</span></span>
<span data-ttu-id="99b56-217">Nazwa topicType</span><span class="sxs-lookup"><span data-stu-id="99b56-217">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b56-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b56-218">CommonParameters</span></span>
<span data-ttu-id="99b56-219">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99b56-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b56-220">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99b56-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b56-221">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99b56-221">INPUTS</span></span>

### <span data-ttu-id="99b56-222">System.String</span><span class="sxs-lookup"><span data-stu-id="99b56-222">System.String</span></span>

### <span data-ttu-id="99b56-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="99b56-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="99b56-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="99b56-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="99b56-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="99b56-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="99b56-226">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="99b56-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="99b56-227">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99b56-227">OUTPUTS</span></span>

### <span data-ttu-id="99b56-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="99b56-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="99b56-229">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="99b56-229">NOTES</span></span>

## <span data-ttu-id="99b56-230">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99b56-230">RELATED LINKS</span></span>
