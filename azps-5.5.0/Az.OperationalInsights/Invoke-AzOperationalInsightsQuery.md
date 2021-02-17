---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 0b2b27855e0c8248f0e7ceb9f1c096370a54e2fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202342"
---
# <span data-ttu-id="3e8d5-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="3e8d5-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="3e8d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e8d5-102">SYNOPSIS</span></span>
<span data-ttu-id="3e8d5-103">Zwraca wyniki wyszukiwania na podstawie określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="3e8d5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3e8d5-104">SYNTAX</span></span>

### <span data-ttu-id="3e8d5-105">ByWorkspaceId (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="3e8d5-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e8d5-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3e8d5-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e8d5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3e8d5-107">DESCRIPTION</span></span>
<span data-ttu-id="3e8d5-108">Polecenie cmdlet **Invoke-AzOperationalInsightsQuery** zwraca wyniki wyszukiwania na podstawie określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="3e8d5-109">Stan wyszukiwania można uzyskać we właściwości Metadane zwróconego obiektu.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="3e8d5-110">Jeśli stan to Oczekiwanie, wyszukiwanie nie zostało ukończone, a wyniki zostaną z archiwum.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="3e8d5-111">Wyniki wyszukiwania można pobrać z właściwości Wartość zwróconego obiektu.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>
<span data-ttu-id="3e8d5-112">Tutaj możesz sprawdzić szczegółowe informacje dotyczące ogólnych limitów https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language zapytań:</span><span class="sxs-lookup"><span data-stu-id="3e8d5-112">Please check detail of general query limits here: https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language.</span></span>

## <span data-ttu-id="3e8d5-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3e8d5-113">EXAMPLES</span></span>

### <span data-ttu-id="3e8d5-114">Przykład 1. Uzyskiwanie wyników wyszukiwania przy użyciu zapytania</span><span class="sxs-lookup"><span data-stu-id="3e8d5-114">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="3e8d5-115">Po wywołaniu funkcja $queryResults.Results będzie zawierać wszystkie wiersze wynikowe z zapytania.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-115">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="3e8d5-116">Przykład 2. Konwertowanie $results. Wynik IEnumerable do tablicy</span><span class="sxs-lookup"><span data-stu-id="3e8d5-116">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="3e8d5-117">Niektóre zapytania mogą powodować zwracanie bardzo dużych zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-117">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="3e8d5-118">Z tego powodu domyślnym zachowaniem polecenia cmdlet jest zwracanie wartości IEnumerable w celu zmniejszenia kosztów pamięci.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-118">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="3e8d5-119">Jeśli wolisz uzyskać tablicę wyników, możesz użyć metody rozszerzenia LINQ enumerable.ToArray() w celu przekonwertowania wartości IEnumerable na tablicę.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-119">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="3e8d5-120">Przykład 3. Uzyskiwanie wyników wyszukiwania przy użyciu zapytania w określonym czasie</span><span class="sxs-lookup"><span data-stu-id="3e8d5-120">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="3e8d5-121">Wyniki tego zapytania będą ograniczone do ostatnich 24 godzin.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-121">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="3e8d5-122">Przykład 4. Uwzględnianie & renderowania w wynikach zapytania</span><span class="sxs-lookup"><span data-stu-id="3e8d5-122">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="3e8d5-123">Aby [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) uzyskać szczegółowe informacje na temat renderowania i statystyki, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-123">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="3e8d5-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e8d5-124">PARAMETERS</span></span>

### <span data-ttu-id="3e8d5-125">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3e8d5-125">-AsJob</span></span>
<span data-ttu-id="3e8d5-126">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3e8d5-126">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8d5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e8d5-127">-DefaultProfile</span></span>
<span data-ttu-id="3e8d5-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e8d5-129">- IncludeRender</span><span class="sxs-lookup"><span data-stu-id="3e8d5-129">-IncludeRender</span></span>
<span data-ttu-id="3e8d5-130">Jeśli zostanie określona, informacje o renderowaniu dla zapytań metrycznych będą uwzględniane w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-130">If specified, rendering information for metric queries will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8d5-131">— IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="3e8d5-131">-IncludeStatistics</span></span>
<span data-ttu-id="3e8d5-132">Jeśli zostanie określona, w odpowiedzi zostaną uwzględnione statystyki zapytań.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-132">If specified, query statistics will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8d5-133">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="3e8d5-133">-Query</span></span>
<span data-ttu-id="3e8d5-134">Kwerenda do wykonania.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-134">The query to execute.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8d5-135">- Timespan</span><span class="sxs-lookup"><span data-stu-id="3e8d5-135">-Timespan</span></span>
<span data-ttu-id="3e8d5-136">Czas, przez który zapytanie jest powiązane.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-136">The timespan to bound the query by.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8d5-137">— Czekanie</span><span class="sxs-lookup"><span data-stu-id="3e8d5-137">-Wait</span></span>
<span data-ttu-id="3e8d5-138">Dodaje górną granicę czasu przetwarzania zapytania przez serwer.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-138">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="3e8d5-139">Zobacz: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="3e8d5-139">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8d5-140">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="3e8d5-140">-Workspace</span></span>
<span data-ttu-id="3e8d5-141">Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="3e8d5-141">The workspace</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e8d5-142">- WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="3e8d5-142">-WorkspaceId</span></span>
<span data-ttu-id="3e8d5-143">Identyfikator obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-143">The workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8d5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e8d5-144">CommonParameters</span></span>
<span data-ttu-id="3e8d5-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e8d5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e8d5-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e8d5-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e8d5-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e8d5-147">INPUTS</span></span>

### <span data-ttu-id="3e8d5-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3e8d5-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="3e8d5-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3e8d5-149">OUTPUTS</span></span>

### <span data-ttu-id="3e8d5-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="3e8d5-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="3e8d5-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3e8d5-151">NOTES</span></span>

## <span data-ttu-id="3e8d5-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e8d5-152">RELATED LINKS</span></span>
