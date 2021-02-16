---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194427"
---
# <span data-ttu-id="6afd8-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="6afd8-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="6afd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6afd8-102">SYNOPSIS</span></span>
<span data-ttu-id="6afd8-103">Pobiera szczegółowe informacje na temat siatki zdarzeń lub pobiera listę wszystkich tematów dotyczących siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6afd8-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="6afd8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6afd8-104">SYNTAX</span></span>

### <span data-ttu-id="6afd8-105">ResourceGroupNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6afd8-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6afd8-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6afd8-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6afd8-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6afd8-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6afd8-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="6afd8-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6afd8-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="6afd8-109">DESCRIPTION</span></span>
<span data-ttu-id="6afd8-110">Polecenie Get-AzEventGridTopic pobiera szczegóły określonego tematu siatki zdarzeń lub listę wszystkich tematów dotyczących siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6afd8-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="6afd8-111">Jeśli podano nazwę tematu, są zwracane szczegóły pojedynczego tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6afd8-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="6afd8-112">Jeśli nazwa tematu nie jest podano, zostanie zwrócona lista tematów.</span><span class="sxs-lookup"><span data-stu-id="6afd8-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="6afd8-113">Liczba elementów zwracanych na tej liście jest kontrolowana przez parametr Top.</span><span class="sxs-lookup"><span data-stu-id="6afd8-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="6afd8-114">Jeśli wartość najwyższa nie zostanie określona lub $null, lista będzie zawierać wszystkie pozycje tematów.</span><span class="sxs-lookup"><span data-stu-id="6afd8-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="6afd8-115">W przeciwnym razie top wskaże maksymalną liczbę elementów, które mają zostać zwrócone na liście.</span><span class="sxs-lookup"><span data-stu-id="6afd8-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="6afd8-116">Jeśli nadal dostępnych jest więcej tematów, wartość w programie NextLink powinna być używana podczas następnego połączenia w celu uzyskania następnej strony tematów.</span><span class="sxs-lookup"><span data-stu-id="6afd8-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="6afd8-117">Na koniec parametr ODataQuery służy do filtrowania wyników wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6afd8-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="6afd8-118">Zapytanie filtrujące korzysta ze składni OData tylko przy użyciu właściwości Name.</span><span class="sxs-lookup"><span data-stu-id="6afd8-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="6afd8-119">Obsługiwane operacje to: CONTAINS, eq (dla równości), ne (dla nie równa się), ORAZ, LUB i NIE.</span><span class="sxs-lookup"><span data-stu-id="6afd8-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="6afd8-120">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6afd8-120">EXAMPLES</span></span>

### <span data-ttu-id="6afd8-121">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6afd8-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="6afd8-122">Pobiera szczegółowe informacje na temat siatki \` zdarzeń tematu1 \` w grupie zasobów \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="6afd8-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6afd8-123">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6afd8-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="6afd8-124">Pobiera szczegółowe informacje na temat siatki \` zdarzeń tematu1 \` w grupie zasobów \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="6afd8-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6afd8-125">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="6afd8-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="6afd8-126">Lista wszystkich tematów dotyczących siatki zdarzeń w grupie zasobów \` MyResourceGroupName \` bez podziałów na strony.</span><span class="sxs-lookup"><span data-stu-id="6afd8-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="6afd8-127">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="6afd8-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="6afd8-128">Lista pierwszych 10 tematów dotyczących siatki zdarzeń (jeśli są takie tematy) w grupie zasobów Nazwa_grupy Zasobów, która spełnia $odataFilter \` \` grupy.</span><span class="sxs-lookup"><span data-stu-id="6afd8-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="6afd8-129">Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink.</span><span class="sxs-lookup"><span data-stu-id="6afd8-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="6afd8-130">Aby uzyskać dostęp do kolejnych stron tematów, użytkownik powinien ponownie na Get-AzEventGridTopic z wynikami. NextLink uzyskany z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="6afd8-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="6afd8-131">Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.</span><span class="sxs-lookup"><span data-stu-id="6afd8-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="6afd8-132">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="6afd8-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="6afd8-133">Wymień wszystkie tematy siatki zdarzeń w subskrypcji bez podziałów na strony.</span><span class="sxs-lookup"><span data-stu-id="6afd8-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="6afd8-134">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="6afd8-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="6afd8-135">W subskrypcji należy wyświetlić 10 pierwszych tematów dotyczących siatki zdarzeń (jeśli są takie), które spełnią $odataFilter zapytania.</span><span class="sxs-lookup"><span data-stu-id="6afd8-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="6afd8-136">Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink.</span><span class="sxs-lookup"><span data-stu-id="6afd8-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="6afd8-137">Aby uzyskać dostęp do kolejnych stron tematów, użytkownik powinien ponownie na Get-AzEventGridTopic z wynikami. NextLink uzyskany z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="6afd8-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="6afd8-138">Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.</span><span class="sxs-lookup"><span data-stu-id="6afd8-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="6afd8-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6afd8-139">PARAMETERS</span></span>

### <span data-ttu-id="6afd8-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6afd8-140">-DefaultProfile</span></span>
<span data-ttu-id="6afd8-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6afd8-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6afd8-142">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6afd8-142">-Name</span></span>
<span data-ttu-id="6afd8-143">Nazwa tematu w aplikacji EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6afd8-143">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afd8-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="6afd8-144">-NextLink</span></span>
<span data-ttu-id="6afd8-145">Link do następnej strony zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="6afd8-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="6afd8-146">Ta wartość jest uzyskiwana w przypadku pierwszego Get-AzEventGrid cmdlet, gdy nadal dostępnych jest więcej zasobów do zapytania.</span><span class="sxs-lookup"><span data-stu-id="6afd8-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="6afd8-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="6afd8-147">-ODataQuery</span></span>
<span data-ttu-id="6afd8-148">Zapytanie OData używane do filtrowania wyników listy.</span><span class="sxs-lookup"><span data-stu-id="6afd8-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="6afd8-149">Filtrowanie jest obecnie dozwolone tylko we właściwości Name. Obsługiwane operacje to: CONTAINS, eq (dla równości), ne (dla nie równa się), ORAZ, LUB i NIE.</span><span class="sxs-lookup"><span data-stu-id="6afd8-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afd8-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6afd8-150">-ResourceGroupName</span></span>
<span data-ttu-id="6afd8-151">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6afd8-151">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afd8-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6afd8-152">-ResourceId</span></span>
<span data-ttu-id="6afd8-153">Identyfikator zasobu reprezentujący temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6afd8-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="6afd8-154">— Na górze</span><span class="sxs-lookup"><span data-stu-id="6afd8-154">-Top</span></span>
<span data-ttu-id="6afd8-155">Maksymalna liczba zasobów, które mają zostać uzyskane.</span><span class="sxs-lookup"><span data-stu-id="6afd8-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="6afd8-156">Prawidłowa wartość należy do od 1 do 100.</span><span class="sxs-lookup"><span data-stu-id="6afd8-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="6afd8-157">Jeśli zostanie określona najwyższa wartość, a więcej wyników będzie nadal dostępnych, wynik będzie zawierał link do następnej strony, do czego ma zostać dodane zapytanie w programie NextLink.</span><span class="sxs-lookup"><span data-stu-id="6afd8-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="6afd8-158">Jeśli nie zostanie określona górna wartość, pełna lista zasobów zostanie zwrócona jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="6afd8-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afd8-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6afd8-159">CommonParameters</span></span>
<span data-ttu-id="6afd8-160">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6afd8-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6afd8-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6afd8-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6afd8-162">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6afd8-162">INPUTS</span></span>

### <span data-ttu-id="6afd8-163">System.String</span><span class="sxs-lookup"><span data-stu-id="6afd8-163">System.String</span></span>

### <span data-ttu-id="6afd8-164">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6afd8-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6afd8-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6afd8-165">OUTPUTS</span></span>

### <span data-ttu-id="6afd8-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="6afd8-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="6afd8-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="6afd8-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="6afd8-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6afd8-168">NOTES</span></span>

## <span data-ttu-id="6afd8-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6afd8-169">RELATED LINKS</span></span>
