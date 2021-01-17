---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
ms.openlocfilehash: d02a6f9ca3f4821fa8a552f92ef90fa24a9e6bd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346201"
---
# <span data-ttu-id="78ff4-101">Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="78ff4-101">Get-AzMetric</span></span>

## <span data-ttu-id="78ff4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="78ff4-103">Pobiera wartości metryki zasobu.</span><span class="sxs-lookup"><span data-stu-id="78ff4-103">Gets the metric values of a resource.</span></span>

## <span data-ttu-id="78ff4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78ff4-104">SYNTAX</span></span>

### <span data-ttu-id="78ff4-105">GetWithDefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="78ff4-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78ff4-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="78ff4-106">GetWithFullParameters</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78ff4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="78ff4-107">DESCRIPTION</span></span>
<span data-ttu-id="78ff4-108">Polecenie cmdlet **Get-AzMetric** pobiera wartości metryk dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="78ff4-108">The **Get-AzMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="78ff4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78ff4-109">EXAMPLES</span></span>

### <span data-ttu-id="78ff4-110">Przykład 1: uzyskiwanie metryki z podsumowaniem wyników</span><span class="sxs-lookup"><span data-stu-id="78ff4-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
DimensionName  : 
DimensionValue : 
Name           : AverageMemoryWorkingSet
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Bytes
```

<span data-ttu-id="78ff4-111">To polecenie pobiera wartości metryczne dla website3 z ziarnem czasowym o wartości 1 minuta.</span><span class="sxs-lookup"><span data-stu-id="78ff4-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="78ff4-112">Przykład 2: uzyskiwanie metryki ze szczegółowym wyjściem</span><span class="sxs-lookup"><span data-stu-id="78ff4-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:37:00 PM
                     Total      : 0
                     Average    : 0.106
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 0.106
                     Average    : 0.064
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 0.064
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:43:33 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:43:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
```

<span data-ttu-id="78ff4-113">To polecenie pobiera wartości metryczne dla website3 z ziarnem czasowym o wartości 1 minuta.</span><span class="sxs-lookup"><span data-stu-id="78ff4-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="78ff4-114">Wynik jest szczegółowy.</span><span class="sxs-lookup"><span data-stu-id="78ff4-114">The output is detailed.</span></span>

### <span data-ttu-id="78ff4-115">Przykład 3: uzyskiwanie szczegółowych danych wyjściowych dla określonej metryki</span><span class="sxs-lookup"><span data-stu-id="78ff4-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -MetricName "Requests" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 1
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:43:00 PM
                     Total      : 0
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:44:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:45:00 PM
                     Total      : 0
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : Requests
EndTime        : 3/20/2015 6:47:56 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:47:00 PM
TimeGrain      : 00:01:00
Unit           : Count
```

<span data-ttu-id="78ff4-116">To polecenie pobiera szczegółowe dane wyjściowe metryki żądań.</span><span class="sxs-lookup"><span data-stu-id="78ff4-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="78ff4-117">Przykład 4: uzyskiwanie podsumowania wyników dla określonej metryki z określonym filtrem wymiaru</span><span class="sxs-lookup"><span data-stu-id="78ff4-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
```
PS C:\> $dimFilter = @((New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","Toronto"), (New-AzMetricFilter -Dimension AuthenticationType -Operator eq -Value User))

PS C:\> Get-AzMetric -ResourceId <resourceId> -MetricName PageViews -TimeGrain PT5M -MetricFilter $dimFilter -StartTime 2018-02-01T12:00:00Z -EndTime 2018-02-01T12:10:00Z -AggregationType -Average
ResourceId  : [ResourceId]
MetricNamespace : Microsoft.Insights/ApplicationInsights
Metric Name :
                    LocalizedValue  : Page Views
                    Value       : PageViews
Unit        : Seconds
Timeseries  :
            City            : Seattle
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 3518

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 1984

            City            : Toronto
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 894

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 967
```

<span data-ttu-id="78ff4-118">To polecenie pobiera podsumowanie danych wyjściowych dla metryki PageViews z określonym filtrem wymiaru i typem agregacji.</span><span class="sxs-lookup"><span data-stu-id="78ff4-118">This command gets summarized output for the PageViews metric with specified dimension filter and aggregation type.</span></span>

## <span data-ttu-id="78ff4-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78ff4-119">PARAMETERS</span></span>

### <span data-ttu-id="78ff4-120">-Agregacja</span><span class="sxs-lookup"><span data-stu-id="78ff4-120">-AggregationType</span></span>
<span data-ttu-id="78ff4-121">Typ agregacji zapytania</span><span class="sxs-lookup"><span data-stu-id="78ff4-121">The aggregation type of the query</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: None, Average, Count, Minimum, Maximum, Total

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78ff4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78ff4-122">-DefaultProfile</span></span>
<span data-ttu-id="78ff4-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78ff4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78ff4-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="78ff4-124">-DetailedOutput</span></span>
<span data-ttu-id="78ff4-125">Wskazuje, że w tym poleceniu cmdlet są wyświetlane szczegółowe dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="78ff4-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="78ff4-126">Domyślnie dane wyjściowe są sumowane.</span><span class="sxs-lookup"><span data-stu-id="78ff4-126">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78ff4-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="78ff4-127">-EndTime</span></span>
<span data-ttu-id="78ff4-128">Określa godzinę zakończenia kwerendy w czasie lokalnym.</span><span class="sxs-lookup"><span data-stu-id="78ff4-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="78ff4-129">Wartością domyślną jest bieżąca godzina.</span><span class="sxs-lookup"><span data-stu-id="78ff4-129">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78ff4-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="78ff4-130">-MetricFilter</span></span>
<span data-ttu-id="78ff4-131">Określa filtr wymiaru metrycznego, dla którego mają być zbadane metryki.</span><span class="sxs-lookup"><span data-stu-id="78ff4-131">Specifies the metric dimension filter to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78ff4-132">-Metricname</span><span class="sxs-lookup"><span data-stu-id="78ff4-132">-MetricName</span></span>
<span data-ttu-id="78ff4-133">Określa tablicę nazw metryk.</span><span class="sxs-lookup"><span data-stu-id="78ff4-133">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: GetWithDefaultParameters
Aliases: MetricNames

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: GetWithFullParameters
Aliases: MetricNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78ff4-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="78ff4-134">-MetricNamespace</span></span>
<span data-ttu-id="78ff4-135">Określa obszar nazw metryki, dla którego mają być zbadane metryki.</span><span class="sxs-lookup"><span data-stu-id="78ff4-135">Specifies the metric namespace to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78ff4-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="78ff4-136">-OrderBy</span></span>
<span data-ttu-id="78ff4-137">Określa agregację używaną do sortowania wyników i kierunku sortowania (przykład: suma. asc).</span><span class="sxs-lookup"><span data-stu-id="78ff4-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78ff4-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78ff4-138">-ResourceId</span></span>
<span data-ttu-id="78ff4-139">Określa identyfikator zasobu metryki.</span><span class="sxs-lookup"><span data-stu-id="78ff4-139">Specifies the resource ID of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78ff4-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="78ff4-140">-ResultType</span></span>
<span data-ttu-id="78ff4-141">Określa typ wyników, który ma być zwracany (metadane lub dane).</span><span class="sxs-lookup"><span data-stu-id="78ff4-141">Specifies the result type to be returned (metadata or data).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.ResultType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: Data, Metadata

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78ff4-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="78ff4-142">-StartTime</span></span>
<span data-ttu-id="78ff4-143">Określa godzinę rozpoczęcia kwerendy w czasie lokalnym.</span><span class="sxs-lookup"><span data-stu-id="78ff4-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="78ff4-144">Domyślnie jest to bieżący czas lokalny minus jedna godzina.</span><span class="sxs-lookup"><span data-stu-id="78ff4-144">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78ff4-145">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="78ff4-145">-TimeGrain</span></span>
<span data-ttu-id="78ff4-146">Określa ziarno czasu metryki jako obiektu **TimeSpan** w formacie gg: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="78ff4-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78ff4-147">-Początek</span><span class="sxs-lookup"><span data-stu-id="78ff4-147">-Top</span></span>
<span data-ttu-id="78ff4-148">Określa maksymalną liczbę rekordów do pobrania (domyślnie: 10), które mają być określane za pomocą $filter.</span><span class="sxs-lookup"><span data-stu-id="78ff4-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78ff4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78ff4-149">CommonParameters</span></span>
<span data-ttu-id="78ff4-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78ff4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78ff4-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78ff4-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78ff4-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78ff4-152">INPUTS</span></span>

### <span data-ttu-id="78ff4-153">System. String</span><span class="sxs-lookup"><span data-stu-id="78ff4-153">System.String</span></span>

### <span data-ttu-id="78ff4-154">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="78ff4-154">System.TimeSpan</span></span>

### <span data-ttu-id="78ff4-155">System. Nullable "1 [[Microsoft. Azure. Management. Monitor. MODELES. agregacja, Microsoft. Azure. Management. Monitor, Version = 0.21.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="78ff4-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="78ff4-156">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="78ff4-156">System.DateTime</span></span>

### <span data-ttu-id="78ff4-157">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="78ff4-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="78ff4-158">System. Nullable "1 [[Microsoft. Azure. Management. Monitor. MODELES. Result., Microsoft. Azure. Management. Monitor, Version = 0.21.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="78ff4-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="78ff4-159">System. String []</span><span class="sxs-lookup"><span data-stu-id="78ff4-159">System.String[]</span></span>

### <span data-ttu-id="78ff4-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="78ff4-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="78ff4-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78ff4-161">OUTPUTS</span></span>

### <span data-ttu-id="78ff4-162">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric</span><span class="sxs-lookup"><span data-stu-id="78ff4-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="78ff4-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78ff4-163">NOTES</span></span>

<span data-ttu-id="78ff4-164">Więcej informacji na temat obsługiwanych metryk można znaleźć pod adresem: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="78ff4-164">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="78ff4-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78ff4-165">RELATED LINKS</span></span>

<span data-ttu-id="78ff4-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md) 
 [Nowe — AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="78ff4-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


