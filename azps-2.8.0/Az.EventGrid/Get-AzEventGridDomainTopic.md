---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: b12369fb0a4140bea1693fd9074a601cd73fa9cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705507"
---
# <span data-ttu-id="a5569-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a5569-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="a5569-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5569-102">SYNOPSIS</span></span>
<span data-ttu-id="a5569-103">Umożliwia wyświetlenie szczegółów dotyczących domeny siatki zdarzeń lub wyświetlenie listy wszystkich tematów dotyczących domeny siatki zdarzeń w obszarze określona domena siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a5569-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="a5569-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5569-104">SYNTAX</span></span>

### <span data-ttu-id="a5569-105">DomainTopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a5569-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5569-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5569-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5569-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5569-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5569-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a5569-108">DESCRIPTION</span></span>
<span data-ttu-id="a5569-109">Polecenie cmdlet Get-AzEventGridDomainTopic powoduje wyświetlenie szczegółów określonego tematu domeny siatki zdarzeń lub listy wszystkich tematów dotyczących domeny w siatce zdarzeń w określonej domenie w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a5569-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="a5569-110">Jeśli jest podana nazwa tematu domeny, zostaną zwrócone szczegóły dotyczące jednej z nich.</span><span class="sxs-lookup"><span data-stu-id="a5569-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="a5569-111">Jeśli nie podano nazwy tematu domeny, zostanie zwrócona Lista tematów dotyczących domeny pod określoną nazwą domeny.</span><span class="sxs-lookup"><span data-stu-id="a5569-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="a5569-112">Liczba elementów zwróconych na tej liście jest kontrolowana przez parametr najwyższy.</span><span class="sxs-lookup"><span data-stu-id="a5569-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="a5569-113">Jeśli najszukana wartość nie jest określona lub $null, lista będzie zawierać wszystkie elementy tematów domeny.</span><span class="sxs-lookup"><span data-stu-id="a5569-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="a5569-114">W przeciwnym razie na początku będzie wskazywana Maksymalna liczba elementów, które mają zostać zwrócone na liście.</span><span class="sxs-lookup"><span data-stu-id="a5569-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="a5569-115">Jeśli więcej tematów dotyczących domeny jest wciąż dostępnych, w następnej rozmowie należy użyć wartości z NextLink, aby uzyskać następną stronę tematów domeny.</span><span class="sxs-lookup"><span data-stu-id="a5569-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="a5569-116">Na koniec parametr ODataQuery jest wykorzystywany do filtrowania wyników wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a5569-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="a5569-117">Kwerenda filtrująca podąża za składnią funkcji OData tylko przy użyciu właściwości Name.</span><span class="sxs-lookup"><span data-stu-id="a5569-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="a5569-118">Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.</span><span class="sxs-lookup"><span data-stu-id="a5569-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="a5569-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5569-119">EXAMPLES</span></span>

### <span data-ttu-id="a5569-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5569-120">Example 1</span></span>

<span data-ttu-id="a5569-121">Pobiera Szczegóły tematu domeny w siatce zdarzeń \` DomainTopic1 w \` obszarze Domena zdarzeń \` Domain1 \` w grupie zasób \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a5569-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="a5569-122">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a5569-122">Example 2</span></span>

<span data-ttu-id="a5569-123">Umożliwia wyświetlenie szczegółów tematu domeny w siatce zdarzeń \` DomainTopic1 w \` obszarze domeny \` Domain1 \` w grupie zasobów \` MyResourceGroupName \` przy użyciu opcji ResourceID.</span><span class="sxs-lookup"><span data-stu-id="a5569-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="a5569-124">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a5569-124">Example 3</span></span>

<span data-ttu-id="a5569-125">Lista wszystkich tematów dotyczących domeny siatki zdarzeń w obszarze Domena zdarzeń \` Domain1 \` w grupie zasób \` MyResourceGroupName \` bez stronicowania (wszystkie wyniki są zwracane w jednym zasobie).</span><span class="sxs-lookup"><span data-stu-id="a5569-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="a5569-126">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="a5569-126">Example 4</span></span>

<span data-ttu-id="a5569-127">Lista wszystkich tematów dotyczących domeny w siatce zdarzeń \` w obszarze Domain1 domeny \` w grupie zasób \` MyResourceGroupName \` bez stronicowania (wszystkie wyniki są zwracane w jednym zasobie) przy użyciu opcji ResourceID</span><span class="sxs-lookup"><span data-stu-id="a5569-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="a5569-128">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="a5569-128">Example 5</span></span>

<span data-ttu-id="a5569-129">Wyświetlanie tematów dotyczących domeny w siatce zdarzeń (jeśli istnieją) w obszarze Domain Domain1 (jeśli istnieje) \` \` w grupie zasoby \` MyResourceGroupName \` , która spełnia tematy $odataFilter 10 tematów dotyczących domeny w danym momencie.</span><span class="sxs-lookup"><span data-stu-id="a5569-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="a5569-130">Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null.</span><span class="sxs-lookup"><span data-stu-id="a5569-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a5569-131">Aby uzyskać dostęp do kolejnych stron tematów domeny, użytkownik powinien ponownie zadzwonić Get-AzEventGridDomainTopic i używa wyników. NextLink uzyskana z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="a5569-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a5569-132">Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.</span><span class="sxs-lookup"><span data-stu-id="a5569-132">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomainTopic -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domain topics is $Total"
```

## <span data-ttu-id="a5569-133">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5569-133">PARAMETERS</span></span>

### <span data-ttu-id="a5569-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5569-134">-DefaultProfile</span></span>
<span data-ttu-id="a5569-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5569-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5569-136">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="a5569-136">-DomainName</span></span>
<span data-ttu-id="a5569-137">EventGrid nazwa domeny.</span><span class="sxs-lookup"><span data-stu-id="a5569-137">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5569-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5569-138">-Name</span></span>
<span data-ttu-id="a5569-139">Nazwa tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a5569-139">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5569-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="a5569-140">-NextLink</span></span>
<span data-ttu-id="a5569-141">Łącze do następnej strony, które mają zostać uzyskane.</span><span class="sxs-lookup"><span data-stu-id="a5569-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="a5569-142">Ta wartość jest uzyskiwana za pomocą pierwszego Get-AzEventGrid polecenia cmdlet, gdy więcej zasobów jest wciąż dostępnych do zbadania.</span><span class="sxs-lookup"><span data-stu-id="a5569-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5569-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="a5569-143">-ODataQuery</span></span>
<span data-ttu-id="a5569-144">Kwerenda OData używana do filtrowania wyników listy.</span><span class="sxs-lookup"><span data-stu-id="a5569-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="a5569-145">Filtrowanie jest obecnie dozwolone tylko w przypadku właściwości Name. Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.</span><span class="sxs-lookup"><span data-stu-id="a5569-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5569-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5569-146">-ResourceGroupName</span></span>
<span data-ttu-id="a5569-147">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a5569-147">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5569-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5569-148">-ResourceId</span></span>
<span data-ttu-id="a5569-149">Identyfikator zasobu reprezentujący temat domeny lub domeny siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="a5569-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5569-150">-Początek</span><span class="sxs-lookup"><span data-stu-id="a5569-150">-Top</span></span>
<span data-ttu-id="a5569-151">Kwerenda OData używana do filtrowania wyników listy.</span><span class="sxs-lookup"><span data-stu-id="a5569-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="a5569-152">Filtrowanie jest obecnie dozwolone tylko w przypadku właściwości Name. Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.</span><span class="sxs-lookup"><span data-stu-id="a5569-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5569-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5569-153">CommonParameters</span></span>
<span data-ttu-id="a5569-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5569-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5569-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5569-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5569-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5569-156">INPUTS</span></span>

### <span data-ttu-id="a5569-157">System. String</span><span class="sxs-lookup"><span data-stu-id="a5569-157">System.String</span></span>

### <span data-ttu-id="a5569-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a5569-158">System.Int32</span></span>

## <span data-ttu-id="a5569-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5569-159">OUTPUTS</span></span>

### <span data-ttu-id="a5569-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a5569-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="a5569-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="a5569-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="a5569-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5569-162">NOTES</span></span>

## <span data-ttu-id="a5569-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5569-163">RELATED LINKS</span></span>
