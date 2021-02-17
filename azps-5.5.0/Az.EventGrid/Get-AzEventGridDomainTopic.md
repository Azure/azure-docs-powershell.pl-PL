---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243659"
---
# <span data-ttu-id="273fd-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="273fd-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="273fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="273fd-102">SYNOPSIS</span></span>
<span data-ttu-id="273fd-103">Pobiera szczegółowe informacje na temat domeny siatki zdarzeń lub pobiera listę wszystkich tematów dotyczących domeny siatki zdarzeń w ramach określonej domeny siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="273fd-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="273fd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="273fd-104">SYNTAX</span></span>

### <span data-ttu-id="273fd-105">DomainTopicNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="273fd-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="273fd-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="273fd-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="273fd-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="273fd-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="273fd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="273fd-108">DESCRIPTION</span></span>
<span data-ttu-id="273fd-109">Polecenie Get-AzEventGridDomainTopic pobiera szczegóły określonego tematu domeny siatki zdarzeń lub listę wszystkich tematów dotyczących domeny siatki zdarzeń w ramach określonej domeny w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="273fd-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="273fd-110">Jeśli podano nazwę tematu domeny, zwracane są szczegóły pojedynczego tematu domeny siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="273fd-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="273fd-111">Jeśli nazwa tematu domeny nie zostanie podana, zostanie zwrócona lista tematów dotyczących domeny poniżej określonej nazwy domeny.</span><span class="sxs-lookup"><span data-stu-id="273fd-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="273fd-112">Liczba elementów zwracanych na tej liście jest kontrolowana przez parametr Top.</span><span class="sxs-lookup"><span data-stu-id="273fd-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="273fd-113">Jeśli wartość Najwyższa nie zostanie określona lub $null, lista będzie zawierać wszystkie elementy tematów dotyczących domeny.</span><span class="sxs-lookup"><span data-stu-id="273fd-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="273fd-114">W przeciwnym razie top wskaże maksymalną liczbę elementów, które mają zostać zwrócone na liście.</span><span class="sxs-lookup"><span data-stu-id="273fd-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="273fd-115">Jeśli nadal dostępnych jest więcej tematów dotyczących domeny, wartość w programie NextLink powinna zostać użyta w następnym wywołaniu w celu uzyskania następnej strony tematów dotyczących domen.</span><span class="sxs-lookup"><span data-stu-id="273fd-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="273fd-116">Na koniec parametr ODataQuery służy do filtrowania wyników wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="273fd-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="273fd-117">Zapytanie filtrujące korzysta ze składni OData tylko przy użyciu właściwości Name.</span><span class="sxs-lookup"><span data-stu-id="273fd-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="273fd-118">Obsługiwane operacje to: CONTAINS, eq (dla równości), ne (dla nie równa się), ORAZ, LUB i NIE.</span><span class="sxs-lookup"><span data-stu-id="273fd-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="273fd-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="273fd-119">EXAMPLES</span></span>

### <span data-ttu-id="273fd-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="273fd-120">Example 1</span></span>

<span data-ttu-id="273fd-121">Pobiera szczegółowe informacje na temat domeny siatki zdarzeń DomainTopic1 w obszarze Domena1 siatki zdarzenia w grupie zasobów \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="273fd-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="273fd-122">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="273fd-122">Example 2</span></span>

<span data-ttu-id="273fd-123">Pobiera szczegóły tematu domeny Siatka zdarzeń DomainTopic1 w obszarze Domena siatki zdarzeń1 w grupie zasobów Nazwa_grupy Zasobów, używając \` \` opcji \` \` \` \` ResourceId.</span><span class="sxs-lookup"><span data-stu-id="273fd-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="273fd-124">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="273fd-124">Example 3</span></span>

<span data-ttu-id="273fd-125">Lista wszystkich tematów dotyczących domeny siatki zdarzeń w obszarze Domena siatki zdarzeń1 w grupie zasobów Nazwa_grupy zasobów Bez podziałów na strony (wszystkie wyniki są zwracane \` \` w jednym \` \` ujęciu).</span><span class="sxs-lookup"><span data-stu-id="273fd-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

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

### <span data-ttu-id="273fd-126">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="273fd-126">Example 4</span></span>

<span data-ttu-id="273fd-127">Lista wszystkich tematów dotyczących domeny Siatki zdarzeń w obszarze Domena siatki zdarzeń1 w grupie zasobów Nazwa_grupy zasobów Bez podziału na strony (wszystkie wyniki są zwracane jednym ujęciem) przy użyciu opcji \` \` \` \` ResourceId</span><span class="sxs-lookup"><span data-stu-id="273fd-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

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

### <span data-ttu-id="273fd-128">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="273fd-128">Example 5</span></span>

<span data-ttu-id="273fd-129">Listę tematów dotyczących domeny siatki zdarzeń (jeśli są takie tematy) w obszarze Domena1 w grupie zasobów Nazwa_grupy zasobów, które zaspokajają jednocześnie \` \` $odataFilter \` 10 tematów dotyczących domeny zapytania \` $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="273fd-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="273fd-130">Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink.</span><span class="sxs-lookup"><span data-stu-id="273fd-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="273fd-131">Aby uzyskać dostęp do kolejnych stron tematów dotyczących domeny, użytkownik powinien ponownie na Get-AzEventGridDomainTopic korzysta z wyników. Przycisk NextLink uzyskany z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="273fd-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="273fd-132">Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.</span><span class="sxs-lookup"><span data-stu-id="273fd-132">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="273fd-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="273fd-133">PARAMETERS</span></span>

### <span data-ttu-id="273fd-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="273fd-134">-DefaultProfile</span></span>
<span data-ttu-id="273fd-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="273fd-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="273fd-136">-DomainName</span><span class="sxs-lookup"><span data-stu-id="273fd-136">-DomainName</span></span>
<span data-ttu-id="273fd-137">Nazwa domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="273fd-137">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273fd-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="273fd-138">-Name</span></span>
<span data-ttu-id="273fd-139">Nazwa tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="273fd-139">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273fd-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="273fd-140">-NextLink</span></span>
<span data-ttu-id="273fd-141">Link do następnej strony zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="273fd-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="273fd-142">Ta wartość jest uzyskiwana w przypadku pierwszego Get-AzEventGrid cmdlet, gdy nadal jest dostępnych więcej zasobów do zapytania.</span><span class="sxs-lookup"><span data-stu-id="273fd-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="273fd-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="273fd-143">-ODataQuery</span></span>
<span data-ttu-id="273fd-144">Zapytanie OData używane do filtrowania wyników listy.</span><span class="sxs-lookup"><span data-stu-id="273fd-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="273fd-145">Filtrowanie jest obecnie dozwolone tylko we właściwości Name. Obsługiwane operacje to: CONTAINS, eq (dla równości), ne (dla nie równa się), ORAZ, LUB i NIE.</span><span class="sxs-lookup"><span data-stu-id="273fd-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273fd-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="273fd-146">-ResourceGroupName</span></span>
<span data-ttu-id="273fd-147">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="273fd-147">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273fd-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="273fd-148">-ResourceId</span></span>
<span data-ttu-id="273fd-149">Identyfikator zasobu reprezentujący domenę siatki zdarzeń lub temat domeny siatki.</span><span class="sxs-lookup"><span data-stu-id="273fd-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

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

### <span data-ttu-id="273fd-150">— Na górze</span><span class="sxs-lookup"><span data-stu-id="273fd-150">-Top</span></span>
<span data-ttu-id="273fd-151">Zapytanie OData używane do filtrowania wyników listy.</span><span class="sxs-lookup"><span data-stu-id="273fd-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="273fd-152">Filtrowanie jest obecnie dozwolone tylko we właściwości Name. Obsługiwane operacje to: CONTAINS, eq (dla równości), ne (dla nie równa się), ORAZ, LUB i NIE.</span><span class="sxs-lookup"><span data-stu-id="273fd-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273fd-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="273fd-153">CommonParameters</span></span>
<span data-ttu-id="273fd-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="273fd-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="273fd-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="273fd-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="273fd-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="273fd-156">INPUTS</span></span>

### <span data-ttu-id="273fd-157">System.String</span><span class="sxs-lookup"><span data-stu-id="273fd-157">System.String</span></span>

### <span data-ttu-id="273fd-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="273fd-158">System.Int32</span></span>

## <span data-ttu-id="273fd-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="273fd-159">OUTPUTS</span></span>

### <span data-ttu-id="273fd-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="273fd-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="273fd-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="273fd-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="273fd-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="273fd-162">NOTES</span></span>

## <span data-ttu-id="273fd-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="273fd-163">RELATED LINKS</span></span>
