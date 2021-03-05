---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: 919d8d0557fd6bb57cc826da8ac18bc71b911c62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984684"
---
# <span data-ttu-id="14a85-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="14a85-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="14a85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14a85-102">SYNOPSIS</span></span>
<span data-ttu-id="14a85-103">Pobiera szczegółowe informacje dotyczące domeny siatki zdarzeń lub pobiera listę wszystkich domen siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="14a85-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="14a85-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="14a85-104">SYNTAX</span></span>

### <span data-ttu-id="14a85-105">ResourceGroupNameParameterSet (Ustawienie domyślne)</span><span class="sxs-lookup"><span data-stu-id="14a85-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14a85-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="14a85-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14a85-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="14a85-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14a85-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="14a85-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14a85-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="14a85-109">DESCRIPTION</span></span>
<span data-ttu-id="14a85-110">Polecenie Get-AzEventGridDomain pobiera szczegóły określonej domeny siatki zdarzeń lub listę wszystkich domen siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="14a85-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="14a85-111">Jeśli podano nazwę domeny, zwracane są szczegóły pojedynczej domeny siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="14a85-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="14a85-112">Jeśli nazwa domeny nie jest podano, zostanie zwrócona lista domen.</span><span class="sxs-lookup"><span data-stu-id="14a85-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="14a85-113">Liczba elementów zwracanych na tej liście jest kontrolowana przez parametr Top.</span><span class="sxs-lookup"><span data-stu-id="14a85-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="14a85-114">Jeśli wartość Najwyższa nie zostanie określona lub $null, lista będzie zawierać wszystkie zwrócone jednocześnie elementy domen.</span><span class="sxs-lookup"><span data-stu-id="14a85-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="14a85-115">W przeciwnym razie top wskaże maksymalną liczbę elementów, które mają zostać zwrócone na liście.</span><span class="sxs-lookup"><span data-stu-id="14a85-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="14a85-116">Jeśli więcej domen jest nadal dostępnych, wartość w programie NextLink powinna zostać użyta w następnym wywołaniu w celu uzyskania następnej strony domen.</span><span class="sxs-lookup"><span data-stu-id="14a85-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="14a85-117">Na koniec parametr ODataQuery służy do filtrowania wyników wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="14a85-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="14a85-118">Zapytanie filtrujące korzysta ze składni OData tylko przy użyciu właściwości Name.</span><span class="sxs-lookup"><span data-stu-id="14a85-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="14a85-119">Obsługiwane operacje to: CONTAINS, eq (dla równości), ne (dla nie równa się), ORAZ, LUB i NIE.</span><span class="sxs-lookup"><span data-stu-id="14a85-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="14a85-120">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="14a85-120">EXAMPLES</span></span>

### <span data-ttu-id="14a85-121">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="14a85-121">Example 1</span></span>

<span data-ttu-id="14a85-122">Pobiera szczegółowe informacje o domenie \` Siatki zdarzeń Domain1 \` w grupie zasobów \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="14a85-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

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

### <span data-ttu-id="14a85-123">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="14a85-123">Example 2</span></span>

<span data-ttu-id="14a85-124">Pobiera szczegółowe informacje o domenie Siatki zdarzeń \` Domain1 \` w grupie zasobów \` MyResourceGroupName \` przy użyciu opcji ResourceId.</span><span class="sxs-lookup"><span data-stu-id="14a85-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

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

### <span data-ttu-id="14a85-125">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="14a85-125">Example 3</span></span>

<span data-ttu-id="14a85-126">Lista wszystkich domen siatki zdarzeń w grupie zasobów MyResourceGroupName bez podziałów na strony (wszystkie domeny są zwracane \` \` w jednym ujęciu)</span><span class="sxs-lookup"><span data-stu-id="14a85-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="14a85-127">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="14a85-127">Example 4</span></span>

<span data-ttu-id="14a85-128">Lista domen siatki zdarzeń (jeśli są) w grupie zasobów Nazwa_grupy zasobów, które zaspokajają $odataFilter \` \` 10 domen na raz.</span><span class="sxs-lookup"><span data-stu-id="14a85-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="14a85-129">Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink.</span><span class="sxs-lookup"><span data-stu-id="14a85-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="14a85-130">W celu uzyskania kolejnych stron domen użytkownik powinien na przykład ponownie na Get-AzEventGridDomain z wynikami. Przycisk NextLink uzyskany z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="14a85-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="14a85-131">Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.</span><span class="sxs-lookup"><span data-stu-id="14a85-131">Caller should stop when result.NextLink becomes $null.</span></span>

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

### <span data-ttu-id="14a85-132">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="14a85-132">Example 5</span></span>

<span data-ttu-id="14a85-133">Lista wszystkich domen siatki zdarzeń w subskrypcji platformy Azure bez podziałów na strony (wszystkie domeny są zwracane w jednym ujęciu)</span><span class="sxs-lookup"><span data-stu-id="14a85-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="14a85-134">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="14a85-134">Example 6</span></span>

<span data-ttu-id="14a85-135">W subskrypcji platformy Azure można wyświetlić listę domen siatki zdarzeń (jeśli są takie), które zaspokajają $odataFilter 20 domen jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="14a85-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="14a85-136">Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink.</span><span class="sxs-lookup"><span data-stu-id="14a85-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="14a85-137">W celu uzyskania kolejnych stron domen użytkownik powinien na przykład ponownie na Get-AzEventGridDomain z wynikami. Przycisk NextLink uzyskany z poprzedniej rozmowy.</span><span class="sxs-lookup"><span data-stu-id="14a85-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="14a85-138">Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.</span><span class="sxs-lookup"><span data-stu-id="14a85-138">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="14a85-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14a85-139">PARAMETERS</span></span>

### <span data-ttu-id="14a85-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a85-140">-DefaultProfile</span></span>
<span data-ttu-id="14a85-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="14a85-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14a85-142">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="14a85-142">-Name</span></span>
<span data-ttu-id="14a85-143">Nazwa domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="14a85-143">EventGrid domain name.</span></span>

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

### <span data-ttu-id="14a85-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="14a85-144">-NextLink</span></span>
<span data-ttu-id="14a85-145">Link do następnej strony zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="14a85-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="14a85-146">Ta wartość jest uzyskiwana w przypadku pierwszego Get-AzEventGrid cmdlet, gdy nadal jest dostępnych więcej zasobów do zapytania.</span><span class="sxs-lookup"><span data-stu-id="14a85-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="14a85-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="14a85-147">-ODataQuery</span></span>
<span data-ttu-id="14a85-148">Zapytanie OData używane do filtrowania wyników listy.</span><span class="sxs-lookup"><span data-stu-id="14a85-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="14a85-149">Filtrowanie jest obecnie dozwolone tylko we właściwości Name. Obsługiwane operacje to: CONTAINS, eq (dla równości), ne (dla nie równa się), ORAZ, LUB i NIE.</span><span class="sxs-lookup"><span data-stu-id="14a85-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="14a85-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14a85-150">-ResourceGroupName</span></span>
<span data-ttu-id="14a85-151">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="14a85-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="14a85-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14a85-152">-ResourceId</span></span>
<span data-ttu-id="14a85-153">Identyfikator zasobu reprezentujący domenę siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="14a85-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="14a85-154">— Na górze</span><span class="sxs-lookup"><span data-stu-id="14a85-154">-Top</span></span>
<span data-ttu-id="14a85-155">Maksymalna liczba zasobów, które mają zostać uzyskane.</span><span class="sxs-lookup"><span data-stu-id="14a85-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="14a85-156">Prawidłowa wartość to między 1 a 100.</span><span class="sxs-lookup"><span data-stu-id="14a85-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="14a85-157">Jeśli zostanie określona najwyższa wartość i nadal będzie dostępnych więcej wyników, wynik będzie zawierać link do następnej strony, do czego ma zostać zaadysowane zapytanie w programie NextLink.</span><span class="sxs-lookup"><span data-stu-id="14a85-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="14a85-158">Jeśli nie zostanie określona najwyższa wartość, pełna lista zasobów zostanie zwrócona jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="14a85-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

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

### <span data-ttu-id="14a85-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a85-159">CommonParameters</span></span>
<span data-ttu-id="14a85-160">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14a85-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a85-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14a85-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a85-162">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14a85-162">INPUTS</span></span>

### <span data-ttu-id="14a85-163">System.String</span><span class="sxs-lookup"><span data-stu-id="14a85-163">System.String</span></span>

## <span data-ttu-id="14a85-164">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14a85-164">OUTPUTS</span></span>

### <span data-ttu-id="14a85-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="14a85-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="14a85-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="14a85-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="14a85-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="14a85-167">NOTES</span></span>

## <span data-ttu-id="14a85-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14a85-168">RELATED LINKS</span></span>
