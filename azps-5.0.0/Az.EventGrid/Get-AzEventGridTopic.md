---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231934"
---
# <span data-ttu-id="22121-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="22121-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="22121-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22121-102">SYNOPSIS</span></span>
<span data-ttu-id="22121-103">Pobiera szczegóły dotyczące siatki zdarzeń lub zawiera listę wszystkich tematów dotyczących siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="22121-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="22121-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22121-104">SYNTAX</span></span>

### <span data-ttu-id="22121-105">ResourceGroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="22121-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22121-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="22121-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22121-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="22121-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22121-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="22121-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22121-109">Opis</span><span class="sxs-lookup"><span data-stu-id="22121-109">DESCRIPTION</span></span>
<span data-ttu-id="22121-110">Polecenie cmdlet Get-AzEventGridTopic pobiera szczegóły określonego tematu siatki zdarzeń lub listę wszystkich tematów siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="22121-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="22121-111">W przypadku podanej nazwy tematu jest zwracana wartość szczegółów pojedynczego tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="22121-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="22121-112">Jeśli nie podano nazwy tematu, zostanie zwrócona Lista tematów.</span><span class="sxs-lookup"><span data-stu-id="22121-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="22121-113">Liczba elementów zwróconych na tej liście jest kontrolowana przez parametr najwyższy.</span><span class="sxs-lookup"><span data-stu-id="22121-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="22121-114">Jeśli najszukana wartość nie jest określona lub $null, lista będzie zawierać wszystkie elementy tematów.</span><span class="sxs-lookup"><span data-stu-id="22121-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="22121-115">W przeciwnym razie na początku będzie wskazywana Maksymalna liczba elementów, które mają zostać zwrócone na liście.</span><span class="sxs-lookup"><span data-stu-id="22121-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="22121-116">Jeśli więcej tematów jest wciąż dostępnych, w następnej rozmowie należy użyć wartości z NextLink, aby uzyskać następną stronę tematów.</span><span class="sxs-lookup"><span data-stu-id="22121-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="22121-117">Na koniec parametr ODataQuery jest wykorzystywany do filtrowania wyników wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="22121-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="22121-118">Kwerenda filtrująca podąża za składnią funkcji OData tylko przy użyciu właściwości Name.</span><span class="sxs-lookup"><span data-stu-id="22121-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="22121-119">Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.</span><span class="sxs-lookup"><span data-stu-id="22121-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="22121-120">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22121-120">EXAMPLES</span></span>

### <span data-ttu-id="22121-121">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="22121-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="22121-122">Pobiera Szczegóły tematu w siatce zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="22121-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="22121-123">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="22121-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="22121-124">Pobiera Szczegóły tematu w siatce zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="22121-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="22121-125">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="22121-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="22121-126">Wyświetlanie wszystkich tematów siatki zdarzeń w MyResourceGroupName grupy zasobów \` \` bez stronicowania.</span><span class="sxs-lookup"><span data-stu-id="22121-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="22121-127">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="22121-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="22121-128">Lista pierwszych 10 tematów dotyczących siatki zdarzeń (jeśli istnieją) w \` MyResourceGroupNameach grupy zasobów \` , które spełniają zapytanie $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="22121-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="22121-129">Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null.</span><span class="sxs-lookup"><span data-stu-id="22121-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="22121-130">Aby uzyskać kolejne strony tematów, użytkownik powinien ponownie zadzwonić Get-AzEventGridTopic i używa wyników. NextLink uzyskana z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="22121-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="22121-131">Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.</span><span class="sxs-lookup"><span data-stu-id="22121-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="22121-132">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="22121-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="22121-133">Wyświetlanie listy wszystkich tematów dotyczących siatki zdarzeń w subskrypcji bez dzielenia na strony.</span><span class="sxs-lookup"><span data-stu-id="22121-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="22121-134">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="22121-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="22121-135">Lista pierwszych 10 tematów siatki zdarzeń (jeśli istnieją) w subskrypcji spełniającej zapytanie $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="22121-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="22121-136">Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null.</span><span class="sxs-lookup"><span data-stu-id="22121-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="22121-137">Aby uzyskać kolejne strony tematów, użytkownik powinien ponownie zadzwonić Get-AzEventGridTopic i używa wyników. NextLink uzyskana z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="22121-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="22121-138">Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.</span><span class="sxs-lookup"><span data-stu-id="22121-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="22121-139">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22121-139">PARAMETERS</span></span>

### <span data-ttu-id="22121-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22121-140">-DefaultProfile</span></span>
<span data-ttu-id="22121-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="22121-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22121-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="22121-142">-Name</span></span>
<span data-ttu-id="22121-143">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="22121-143">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="22121-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="22121-144">-NextLink</span></span>
<span data-ttu-id="22121-145">Łącze do następnej strony, które mają zostać uzyskane.</span><span class="sxs-lookup"><span data-stu-id="22121-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="22121-146">Ta wartość jest uzyskiwana za pomocą pierwszego Get-AzEventGrid polecenia cmdlet, gdy więcej zasobów jest wciąż dostępnych do zbadania.</span><span class="sxs-lookup"><span data-stu-id="22121-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="22121-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="22121-147">-ODataQuery</span></span>
<span data-ttu-id="22121-148">Kwerenda OData używana do filtrowania wyników listy.</span><span class="sxs-lookup"><span data-stu-id="22121-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="22121-149">Filtrowanie jest obecnie dozwolone tylko w przypadku właściwości Name. Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.</span><span class="sxs-lookup"><span data-stu-id="22121-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="22121-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22121-150">-ResourceGroupName</span></span>
<span data-ttu-id="22121-151">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="22121-151">Resource Group Name.</span></span>

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

### <span data-ttu-id="22121-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22121-152">-ResourceId</span></span>
<span data-ttu-id="22121-153">Identyfikator zasobu reprezentujący temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="22121-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="22121-154">-Początek</span><span class="sxs-lookup"><span data-stu-id="22121-154">-Top</span></span>
<span data-ttu-id="22121-155">Maksymalna liczba zasobów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="22121-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="22121-156">Prawidłowa wartość należy do zakresu od 1 do 100.</span><span class="sxs-lookup"><span data-stu-id="22121-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="22121-157">Jeśli określona jest największa wartość, a dalsze wyniki są nadal dostępne, wynik będzie zawierał link do następnej strony, do której ma zostać przeszukana w NextLink.</span><span class="sxs-lookup"><span data-stu-id="22121-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="22121-158">Jeśli nie określono najwyższych wartości, pełna lista zasobów zostanie zwrócona jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="22121-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

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

### <span data-ttu-id="22121-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22121-159">CommonParameters</span></span>
<span data-ttu-id="22121-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22121-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22121-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22121-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22121-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22121-162">INPUTS</span></span>

### <span data-ttu-id="22121-163">System. String</span><span class="sxs-lookup"><span data-stu-id="22121-163">System.String</span></span>

### <span data-ttu-id="22121-164">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="22121-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="22121-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22121-165">OUTPUTS</span></span>

### <span data-ttu-id="22121-166">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="22121-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="22121-167">Microsoft. Azure. Commands. EventGrid. models. PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="22121-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="22121-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22121-168">NOTES</span></span>

## <span data-ttu-id="22121-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22121-169">RELATED LINKS</span></span>
