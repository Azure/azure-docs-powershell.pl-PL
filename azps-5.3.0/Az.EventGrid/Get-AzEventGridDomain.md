---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: 467b7141735cdce31bbdcf964e058f892238ec1d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376831"
---
# <span data-ttu-id="a056c-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a056c-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="a056c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a056c-102">SYNOPSIS</span></span>
<span data-ttu-id="a056c-103">Pobiera szczegóły domeny siatki zdarzeń lub pobiera listę wszystkich domen w siatce zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a056c-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="a056c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a056c-104">SYNTAX</span></span>

### <span data-ttu-id="a056c-105">ResourceGroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a056c-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a056c-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a056c-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a056c-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a056c-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a056c-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="a056c-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a056c-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a056c-109">DESCRIPTION</span></span>
<span data-ttu-id="a056c-110">Polecenie cmdlet Get-AzEventGridDomain pobiera szczegóły określonej domeny siatki zdarzeń lub listę wszystkich domen w siatce zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a056c-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="a056c-111">Jeśli nazwa domeny jest podana, zostanie zwrócona wartość szczegóły jednej domeny siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="a056c-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="a056c-112">Jeśli nie podano nazwy domeny, zostanie zwrócona Lista domen.</span><span class="sxs-lookup"><span data-stu-id="a056c-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="a056c-113">Liczba elementów zwróconych na tej liście jest kontrolowana przez parametr najwyższy.</span><span class="sxs-lookup"><span data-stu-id="a056c-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="a056c-114">Jeśli najszukana wartość nie jest określona lub $null, lista będzie zawierać wszystkie elementy domeny zwrócone jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="a056c-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="a056c-115">W przeciwnym razie na początku będzie wskazywana Maksymalna liczba elementów, które mają zostać zwrócone na liście.</span><span class="sxs-lookup"><span data-stu-id="a056c-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="a056c-116">Jeśli więcej domen jest wciąż dostępnych, w następnej rozmowie należy użyć wartości w NextLink, aby uzyskać następną stronę domen.</span><span class="sxs-lookup"><span data-stu-id="a056c-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="a056c-117">Na koniec parametr ODataQuery jest wykorzystywany do filtrowania wyników wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a056c-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="a056c-118">Kwerenda filtrująca podąża za składnią funkcji OData tylko przy użyciu właściwości Name.</span><span class="sxs-lookup"><span data-stu-id="a056c-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="a056c-119">Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.</span><span class="sxs-lookup"><span data-stu-id="a056c-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="a056c-120">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a056c-120">EXAMPLES</span></span>

### <span data-ttu-id="a056c-121">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a056c-121">Example 1</span></span>

<span data-ttu-id="a056c-122">Pobiera szczegóły Domain1 domeny siatki zdarzeń \` \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="a056c-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="a056c-123">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a056c-123">Example 2</span></span>

<span data-ttu-id="a056c-124">Pobiera szczegóły Domain1 domeny w siatce zdarzeń \` \` w grupie zasób \` MyResourceGroupName \` przy użyciu opcji ResourceID.</span><span class="sxs-lookup"><span data-stu-id="a056c-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="a056c-125">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a056c-125">Example 3</span></span>

<span data-ttu-id="a056c-126">Wyświetlanie wszystkich domen w siatce zdarzeń w MyResourceGroupName grupy \` zasobów \` bez stronicowania (wszystkie domeny są zwracane w jednym zasobie)</span><span class="sxs-lookup"><span data-stu-id="a056c-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain -ResourceGroup MyResourceGroupName
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="a056c-127">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="a056c-127">Example 4</span></span>

<span data-ttu-id="a056c-128">Lista domen w siatce zdarzeń (jeśli istnieją) w grupie MyResourceGroupName, która jest taka sama jak w \` \` przypadku programu $odataFilter 10 domen.</span><span class="sxs-lookup"><span data-stu-id="a056c-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="a056c-129">Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null.</span><span class="sxs-lookup"><span data-stu-id="a056c-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a056c-130">Aby uzyskać kolejne strony domen, użytkownik powinien ponownie zadzwonić Get-AzEventGridDomain i używa wyników. NextLink uzyskana z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="a056c-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a056c-131">Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.</span><span class="sxs-lookup"><span data-stu-id="a056c-131">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domains is $Total"
```

### <span data-ttu-id="a056c-132">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="a056c-132">Example 5</span></span>

<span data-ttu-id="a056c-133">Wyświetlanie listy wszystkich domen w siatce zdarzeń w ramach subskrypcji platformy Azure bez stronicowania (wszystkie domeny są zwracane w jednym zasobie)</span><span class="sxs-lookup"><span data-stu-id="a056c-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname2/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname3/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="a056c-134">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="a056c-134">Example 6</span></span>

<span data-ttu-id="a056c-135">Lista domen w siatce zdarzeń (jeśli istnieją) w subskrypcji platformy Azure, które są zgodne z podaną $odataFilter 20 domenami w danym momencie.</span><span class="sxs-lookup"><span data-stu-id="a056c-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="a056c-136">Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null.</span><span class="sxs-lookup"><span data-stu-id="a056c-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a056c-137">Aby uzyskać kolejne strony domen, użytkownik powinien ponownie zadzwonić Get-AzEventGridDomain i używa wyników. NextLink uzyskana z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="a056c-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a056c-138">Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.</span><span class="sxs-lookup"><span data-stu-id="a056c-138">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Contains(Name, 'ABCD')"
PS C:\> $result = Get-AzEventGridDomain -Top 20 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }
PS C:\> echo "Total number of domains is $Total"
```

## <span data-ttu-id="a056c-139">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a056c-139">PARAMETERS</span></span>

### <span data-ttu-id="a056c-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a056c-140">-DefaultProfile</span></span>
<span data-ttu-id="a056c-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a056c-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a056c-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a056c-142">-Name</span></span>
<span data-ttu-id="a056c-143">EventGrid nazwa domeny.</span><span class="sxs-lookup"><span data-stu-id="a056c-143">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a056c-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="a056c-144">-NextLink</span></span>
<span data-ttu-id="a056c-145">Łącze do następnej strony, które mają zostać uzyskane.</span><span class="sxs-lookup"><span data-stu-id="a056c-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="a056c-146">Ta wartość jest uzyskiwana za pomocą pierwszego Get-AzEventGrid polecenia cmdlet, gdy więcej zasobów jest wciąż dostępnych do zbadania.</span><span class="sxs-lookup"><span data-stu-id="a056c-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="a056c-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="a056c-147">-ODataQuery</span></span>
<span data-ttu-id="a056c-148">Kwerenda OData używana do filtrowania wyników listy.</span><span class="sxs-lookup"><span data-stu-id="a056c-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="a056c-149">Filtrowanie jest obecnie dozwolone tylko w przypadku właściwości Name. Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.</span><span class="sxs-lookup"><span data-stu-id="a056c-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a056c-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a056c-150">-ResourceGroupName</span></span>
<span data-ttu-id="a056c-151">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a056c-151">The name of the resource group.</span></span>

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
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a056c-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a056c-152">-ResourceId</span></span>
<span data-ttu-id="a056c-153">Identyfikator zasobu reprezentujący domenę siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="a056c-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="a056c-154">-Początek</span><span class="sxs-lookup"><span data-stu-id="a056c-154">-Top</span></span>
<span data-ttu-id="a056c-155">Maksymalna liczba zasobów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="a056c-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="a056c-156">Prawidłowa wartość należy do zakresu od 1 do 100.</span><span class="sxs-lookup"><span data-stu-id="a056c-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="a056c-157">Jeśli określona jest największa wartość, a dalsze wyniki są nadal dostępne, wynik będzie zawierał link do następnej strony, do której ma zostać przeszukana w NextLink.</span><span class="sxs-lookup"><span data-stu-id="a056c-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="a056c-158">Jeśli nie określono najwyższych wartości, pełna lista zasobów zostanie zwrócona jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="a056c-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a056c-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a056c-159">CommonParameters</span></span>
<span data-ttu-id="a056c-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a056c-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a056c-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a056c-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a056c-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a056c-162">INPUTS</span></span>

### <span data-ttu-id="a056c-163">System. String</span><span class="sxs-lookup"><span data-stu-id="a056c-163">System.String</span></span>

## <span data-ttu-id="a056c-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a056c-164">OUTPUTS</span></span>

### <span data-ttu-id="a056c-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="a056c-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="a056c-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="a056c-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="a056c-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a056c-167">NOTES</span></span>

## <span data-ttu-id="a056c-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a056c-168">RELATED LINKS</span></span>
