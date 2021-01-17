---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 0b2b27855e0c8248f0e7ceb9f1c096370a54e2fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356652"
---
# <span data-ttu-id="c24f0-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="c24f0-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="c24f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c24f0-102">SYNOPSIS</span></span>
<span data-ttu-id="c24f0-103">Zwraca wyniki wyszukiwania na podstawie określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="c24f0-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="c24f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c24f0-104">SYNTAX</span></span>

### <span data-ttu-id="c24f0-105">ByWorkspaceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c24f0-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c24f0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c24f0-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c24f0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c24f0-107">DESCRIPTION</span></span>
<span data-ttu-id="c24f0-108">Polecenie cmdlet **Invoke-AzOperationalInsightsQuery** zwraca wyniki wyszukiwania na podstawie określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="c24f0-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="c24f0-109">Możesz uzyskać dostęp do stanu wyszukiwania we właściwości Metadata zwracanego obiektu.</span><span class="sxs-lookup"><span data-stu-id="c24f0-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="c24f0-110">Jeśli stan jest oczekujący, wyszukiwanie nie zostało wykonane, a wyniki będą pochodzić z archiwum.</span><span class="sxs-lookup"><span data-stu-id="c24f0-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="c24f0-111">Wyniki wyszukiwania można pobrać z właściwości Value zwróconego obiektu.</span><span class="sxs-lookup"><span data-stu-id="c24f0-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>
<span data-ttu-id="c24f0-112">Szczegółowe informacje na temat ogólnych limitów kwerend można znaleźć tutaj: https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language .</span><span class="sxs-lookup"><span data-stu-id="c24f0-112">Please check detail of general query limits here: https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language.</span></span>

## <span data-ttu-id="c24f0-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c24f0-113">EXAMPLES</span></span>

### <span data-ttu-id="c24f0-114">Przykład 1: uzyskiwanie wyników wyszukiwania za pomocą kwerendy</span><span class="sxs-lookup"><span data-stu-id="c24f0-114">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="c24f0-115">Po wywołaniu $queryResults. wyniki będą zawierać wszystkie wiersze wynikowe z zapytania.</span><span class="sxs-lookup"><span data-stu-id="c24f0-115">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="c24f0-116">Przykład 2: konwertowanie $results. Wynik interfejsu IEnumerable z tablicą</span><span class="sxs-lookup"><span data-stu-id="c24f0-116">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="c24f0-117">Niektóre kwerendy mogą powodować zwracanie bardzo dużych zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="c24f0-117">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="c24f0-118">W związku z tym domyślnym zachowaniem polecenia cmdlet jest zwrócenie interfejsu IEnumerable w celu zmniejszenia kosztów pamięci.</span><span class="sxs-lookup"><span data-stu-id="c24f0-118">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="c24f0-119">Jeśli wolisz uzyskać tablicę wyników, możesz użyć metody rozszerzenia wyliczalna Metoda LINQ. ToArray () w celu przekonwertowania interfejsu IEnumerable na tablicę.</span><span class="sxs-lookup"><span data-stu-id="c24f0-119">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="c24f0-120">Przykład 3: uzyskiwanie wyników wyszukiwania przy użyciu zapytania w określonym przedziale czasu</span><span class="sxs-lookup"><span data-stu-id="c24f0-120">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="c24f0-121">Wyniki z tego zapytania będą ograniczone do ciągu 24 godzin.</span><span class="sxs-lookup"><span data-stu-id="c24f0-121">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="c24f0-122">Przykład 4: uwzględnianie statystyk & renderowania w wynikach zapytania</span><span class="sxs-lookup"><span data-stu-id="c24f0-122">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="c24f0-123">[https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions)Aby uzyskać szczegółowe informacje, zobacz informacje dotyczące renderowania i statystyk.</span><span class="sxs-lookup"><span data-stu-id="c24f0-123">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="c24f0-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c24f0-124">PARAMETERS</span></span>

### <span data-ttu-id="c24f0-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c24f0-125">-AsJob</span></span>
<span data-ttu-id="c24f0-126">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c24f0-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c24f0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c24f0-127">-DefaultProfile</span></span>
<span data-ttu-id="c24f0-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c24f0-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c24f0-129">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="c24f0-129">-IncludeRender</span></span>
<span data-ttu-id="c24f0-130">Jeśli ta wartość jest określona, w odpowiedzi zostaną uwzględnione informacje dotyczące renderowania zapytań metrycznych.</span><span class="sxs-lookup"><span data-stu-id="c24f0-130">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="c24f0-131">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="c24f0-131">-IncludeStatistics</span></span>
<span data-ttu-id="c24f0-132">Jeśli ta argument jest określona, statystyki kwerend zostaną uwzględnione w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="c24f0-132">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="c24f0-133">-Query</span><span class="sxs-lookup"><span data-stu-id="c24f0-133">-Query</span></span>
<span data-ttu-id="c24f0-134">Kwerenda do wykonania.</span><span class="sxs-lookup"><span data-stu-id="c24f0-134">The query to execute.</span></span>

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

### <span data-ttu-id="c24f0-135">-TimeSpan</span><span class="sxs-lookup"><span data-stu-id="c24f0-135">-Timespan</span></span>
<span data-ttu-id="c24f0-136">Obiekt TimeSpan, według którego ma zostać powiązany kwerenda.</span><span class="sxs-lookup"><span data-stu-id="c24f0-136">The timespan to bound the query by.</span></span>

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

### <span data-ttu-id="c24f0-137">-Czekaj</span><span class="sxs-lookup"><span data-stu-id="c24f0-137">-Wait</span></span>
<span data-ttu-id="c24f0-138">Umieszcza górną granicę czasu, jaki serwer będzie poświęcał na przetwarzanie kwerendy.</span><span class="sxs-lookup"><span data-stu-id="c24f0-138">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="c24f0-139">Widz https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="c24f0-139">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

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

### <span data-ttu-id="c24f0-140">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="c24f0-140">-Workspace</span></span>
<span data-ttu-id="c24f0-141">Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="c24f0-141">The workspace</span></span>

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

### <span data-ttu-id="c24f0-142">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="c24f0-142">-WorkspaceId</span></span>
<span data-ttu-id="c24f0-143">Identyfikator obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="c24f0-143">The workspace ID.</span></span>

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

### <span data-ttu-id="c24f0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c24f0-144">CommonParameters</span></span>
<span data-ttu-id="c24f0-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c24f0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c24f0-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c24f0-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c24f0-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c24f0-147">INPUTS</span></span>

### <span data-ttu-id="c24f0-148">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c24f0-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="c24f0-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c24f0-149">OUTPUTS</span></span>

### <span data-ttu-id="c24f0-150">Microsoft. Azure. Commands. OperationalInsights. models. PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="c24f0-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="c24f0-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c24f0-151">NOTES</span></span>

## <span data-ttu-id="c24f0-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c24f0-152">RELATED LINKS</span></span>
