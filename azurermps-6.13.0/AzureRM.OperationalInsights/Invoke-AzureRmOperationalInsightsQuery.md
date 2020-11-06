---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/invoke-azurermoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
ms.openlocfilehash: 6672bb6f788b06896fdfe9cde44c68639077e5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543567"
---
# <span data-ttu-id="70435-101">Invoke-AzureRmOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="70435-101">Invoke-AzureRmOperationalInsightsQuery</span></span>

## <span data-ttu-id="70435-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70435-102">SYNOPSIS</span></span>
<span data-ttu-id="70435-103">Zwraca wyniki wyszukiwania na podstawie określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="70435-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70435-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70435-104">SYNTAX</span></span>

### <span data-ttu-id="70435-105">ByWorkspaceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="70435-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzureRmOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="70435-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="70435-106">ByWorkspaceObject</span></span>
```
Invoke-AzureRmOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70435-107">Opis</span><span class="sxs-lookup"><span data-stu-id="70435-107">DESCRIPTION</span></span>
<span data-ttu-id="70435-108">Polecenie cmdlet **Invoke-AzureRmOperationalInsightsQuery** zwraca wyniki wyszukiwania na podstawie określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="70435-108">The **Invoke-AzureRmOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="70435-109">Możesz uzyskać dostęp do stanu wyszukiwania we właściwości Metadata zwracanego obiektu.</span><span class="sxs-lookup"><span data-stu-id="70435-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="70435-110">Jeśli stan jest oczekujący, wyszukiwanie nie zostało wykonane, a wyniki będą pochodzić z archiwum.</span><span class="sxs-lookup"><span data-stu-id="70435-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="70435-111">Wyniki wyszukiwania można pobrać z właściwości Value zwróconego obiektu.</span><span class="sxs-lookup"><span data-stu-id="70435-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="70435-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70435-112">EXAMPLES</span></span>

### <span data-ttu-id="70435-113">Przykład 1: uzyskiwanie wyników wyszukiwania za pomocą kwerendy</span><span class="sxs-lookup"><span data-stu-id="70435-113">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="70435-114">Po wywołaniu $queryResults. wyniki będą zawierać wszystkie wiersze wynikowe z zapytania.</span><span class="sxs-lookup"><span data-stu-id="70435-114">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="70435-115">Przykład 2: konwertowanie $results. Wyniki IEnumberable do tablicy</span><span class="sxs-lookup"><span data-stu-id="70435-115">Example 2: Convert $results.Result IEnumberable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($results.Results)
...
```

<span data-ttu-id="70435-116">Niektóre kwerendy mogą powodować zwracanie bardzo dużych zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="70435-116">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="70435-117">W związku z tym domyślnym zachowaniem polecenia cmdlet jest zwrócenie interfejsu IEnumerable w celu zmniejszenia kosztów pamięci.</span><span class="sxs-lookup"><span data-stu-id="70435-117">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="70435-118">Jeśli wolisz uzyskać tablicę wyników, możesz użyć metody rozszerzenia wyliczalna Metoda LINQ. ToArray () w celu przekonwertowania interfejsu IEnumerable na tablicę.</span><span class="sxs-lookup"><span data-stu-id="70435-118">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="70435-119">Przykład 3: uzyskiwanie wyników wyszukiwania przy użyciu zapytania w określonym przedziale czasu</span><span class="sxs-lookup"><span data-stu-id="70435-119">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="70435-120">Wyniki z tego zapytania będą ograniczone do ciągu 24 godzin.</span><span class="sxs-lookup"><span data-stu-id="70435-120">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="70435-121">Przykład 4: uwzględnianie statystyk & renderowania w wynikach zapytania</span><span class="sxs-lookup"><span data-stu-id="70435-121">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="70435-122">[https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions)Aby uzyskać szczegółowe informacje, zobacz informacje dotyczące renderowania i statystyk.</span><span class="sxs-lookup"><span data-stu-id="70435-122">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="70435-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70435-123">PARAMETERS</span></span>

### <span data-ttu-id="70435-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70435-124">-AsJob</span></span>
<span data-ttu-id="70435-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="70435-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70435-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70435-126">-DefaultProfile</span></span>
<span data-ttu-id="70435-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70435-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70435-128">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="70435-128">-IncludeRender</span></span>
<span data-ttu-id="70435-129">Jeśli ta wartość jest określona, w odpowiedzi zostaną uwzględnione informacje dotyczące renderowania zapytań metrycznych.</span><span class="sxs-lookup"><span data-stu-id="70435-129">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="70435-130">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="70435-130">-IncludeStatistics</span></span>
<span data-ttu-id="70435-131">Jeśli ta argument jest określona, statystyki kwerend zostaną uwzględnione w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="70435-131">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="70435-132">-Query</span><span class="sxs-lookup"><span data-stu-id="70435-132">-Query</span></span>
<span data-ttu-id="70435-133">Kwerenda do wykonania.</span><span class="sxs-lookup"><span data-stu-id="70435-133">The query to execute.</span></span>

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

### <span data-ttu-id="70435-134">-TimeSpan</span><span class="sxs-lookup"><span data-stu-id="70435-134">-Timespan</span></span>
<span data-ttu-id="70435-135">Obiekt TimeSpan, według którego ma zostać powiązany kwerenda.</span><span class="sxs-lookup"><span data-stu-id="70435-135">The timespan to bound the query by.</span></span>

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

### <span data-ttu-id="70435-136">-Czekaj</span><span class="sxs-lookup"><span data-stu-id="70435-136">-Wait</span></span>
<span data-ttu-id="70435-137">Umieszcza górną granicę czasu, jaki serwer będzie poświęcał na przetwarzanie kwerendy.</span><span class="sxs-lookup"><span data-stu-id="70435-137">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="70435-138">Widz https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="70435-138">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

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

### <span data-ttu-id="70435-139">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="70435-139">-Workspace</span></span>
<span data-ttu-id="70435-140">Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="70435-140">The workspace</span></span>

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

### <span data-ttu-id="70435-141">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="70435-141">-WorkspaceId</span></span>
<span data-ttu-id="70435-142">Identyfikator obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="70435-142">The workspace ID.</span></span>

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

### <span data-ttu-id="70435-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70435-143">CommonParameters</span></span>
<span data-ttu-id="70435-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70435-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70435-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70435-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70435-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70435-146">INPUTS</span></span>

### <span data-ttu-id="70435-147">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="70435-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="70435-148">Parametry: przestrzeń robocza (ByValue)</span><span class="sxs-lookup"><span data-stu-id="70435-148">Parameters: Workspace (ByValue)</span></span>

## <span data-ttu-id="70435-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70435-149">OUTPUTS</span></span>

### <span data-ttu-id="70435-150">Microsoft. Azure. Commands. OperationalInsights. models. PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="70435-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="70435-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70435-151">NOTES</span></span>

## <span data-ttu-id="70435-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70435-152">RELATED LINKS</span></span>
