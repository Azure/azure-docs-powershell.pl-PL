---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetric
schema: 2.0.0
ms.openlocfilehash: 5a0594bc1a90457874a590628076daf7e7d49d8d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897450"
---
# <span data-ttu-id="212c1-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="212c1-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="212c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="212c1-102">SYNOPSIS</span></span>
<span data-ttu-id="212c1-103">Pobiera wartości metryki zasobu.</span><span class="sxs-lookup"><span data-stu-id="212c1-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="212c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="212c1-104">SYNTAX</span></span>

### <span data-ttu-id="212c1-105">GetWithDefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="212c1-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="212c1-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="212c1-106">GetWithFullParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="212c1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="212c1-107">DESCRIPTION</span></span>
<span data-ttu-id="212c1-108">Polecenie cmdlet **Get-AzureRmMetric** pobiera wartości metryk dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="212c1-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="212c1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="212c1-109">EXAMPLES</span></span>

### <span data-ttu-id="212c1-110">Przykład 1: uzyskiwanie metryki z podsumowaniem wyników</span><span class="sxs-lookup"><span data-stu-id="212c1-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
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

<span data-ttu-id="212c1-111">To polecenie pobiera wartości metryczne dla website3 z ziarnem czasowym o wartości 1 minuta.</span><span class="sxs-lookup"><span data-stu-id="212c1-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="212c1-112">Przykład 2: uzyskiwanie metryki ze szczegółowym wyjściem</span><span class="sxs-lookup"><span data-stu-id="212c1-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
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

<span data-ttu-id="212c1-113">To polecenie pobiera wartości metryczne dla website3 z ziarnem czasowym o wartości 1 minuta.</span><span class="sxs-lookup"><span data-stu-id="212c1-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="212c1-114">Wynik jest szczegółowy.</span><span class="sxs-lookup"><span data-stu-id="212c1-114">The output is detailed.</span></span>

### <span data-ttu-id="212c1-115">Przykład 3: uzyskiwanie szczegółowych danych wyjściowych dla określonej metryki</span><span class="sxs-lookup"><span data-stu-id="212c1-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -MetricNames "Requests" -TimeGrain 00:01:00 -DetailedOutput
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

<span data-ttu-id="212c1-116">To polecenie pobiera szczegółowe dane wyjściowe metryki żądań.</span><span class="sxs-lookup"><span data-stu-id="212c1-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="212c1-117">Przykład 4: uzyskiwanie podsumowania wyników dla określonej metryki z określonym filtrem wymiaru</span><span class="sxs-lookup"><span data-stu-id="212c1-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
```
PS C:\> $dimFilter = @((New-AzureRmMetricFilter -Dimension City -Operator eq -Values "Seattle","Toronto"), (New-AzureRmMetricDimensionFilter -Dimension AuthenticationType -Operator eq -Values User))

PS C:\> Get-AzureRmMetricValues -ResourceId <resourcId> -MetricName PageViews -TimeGrain PT5M -MetricFilter $dimFilter -StartTime 2018-02-01T12:00:00Z -EndTime 2018-02-01T12:10:00Z -AggregationType -Average
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

<span data-ttu-id="212c1-118">To polecenie pobiera podsumowanie danych wyjściowych dla metryki PageViews z określonym filtrem dimesion i typem agregacji.</span><span class="sxs-lookup"><span data-stu-id="212c1-118">This command gets summarized output for the PageViews metric with specified dimesion filter and aggregation type.</span></span>

## <span data-ttu-id="212c1-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="212c1-119">PARAMETERS</span></span>

### <span data-ttu-id="212c1-120">-Agregacja</span><span class="sxs-lookup"><span data-stu-id="212c1-120">-AggregationType</span></span>
<span data-ttu-id="212c1-121">Typ agregacji zapytania</span><span class="sxs-lookup"><span data-stu-id="212c1-121">The aggregation type of the query</span></span>

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

### <span data-ttu-id="212c1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="212c1-122">-DefaultProfile</span></span>
<span data-ttu-id="212c1-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="212c1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="212c1-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="212c1-124">-DetailedOutput</span></span>
<span data-ttu-id="212c1-125">Wskazuje, że w tym poleceniu cmdlet są wyświetlane szczegółowe dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="212c1-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="212c1-126">Domyślnie dane wyjściowe są sumowane.</span><span class="sxs-lookup"><span data-stu-id="212c1-126">By default, output is summarized.</span></span>

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

### <span data-ttu-id="212c1-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="212c1-127">-EndTime</span></span>
<span data-ttu-id="212c1-128">Określa godzinę zakończenia kwerendy w czasie lokalnym.</span><span class="sxs-lookup"><span data-stu-id="212c1-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="212c1-129">Wartością domyślną jest bieżąca godzina.</span><span class="sxs-lookup"><span data-stu-id="212c1-129">The default is the current time.</span></span>

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

### <span data-ttu-id="212c1-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="212c1-130">-MetricFilter</span></span>
<span data-ttu-id="212c1-131">Określa filtr wymiaru metrycznego, dla którego mają być zbadane metryki.</span><span class="sxs-lookup"><span data-stu-id="212c1-131">Specifies the metric dimension filter to query metrics for.</span></span>

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

### <span data-ttu-id="212c1-132">-Metricname</span><span class="sxs-lookup"><span data-stu-id="212c1-132">-MetricName</span></span>
<span data-ttu-id="212c1-133">Określa tablicę nazw metryk.</span><span class="sxs-lookup"><span data-stu-id="212c1-133">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="212c1-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="212c1-134">-MetricNamespace</span></span>
<span data-ttu-id="212c1-135">Określa obszar nazw metryki, dla którego mają być zbadane metryki.</span><span class="sxs-lookup"><span data-stu-id="212c1-135">Specifies the metric namespace to query metrics for.</span></span>

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

### <span data-ttu-id="212c1-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="212c1-136">-OrderBy</span></span>
<span data-ttu-id="212c1-137">Określa agregację używaną do sortowania wyników i kierunku sortowania (przykład: suma. asc).</span><span class="sxs-lookup"><span data-stu-id="212c1-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

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

### <span data-ttu-id="212c1-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="212c1-138">-ResourceId</span></span>
<span data-ttu-id="212c1-139">Określa identyfikator zasobu metryki.</span><span class="sxs-lookup"><span data-stu-id="212c1-139">Specifies the resource ID of the metric.</span></span>

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

### <span data-ttu-id="212c1-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="212c1-140">-ResultType</span></span>
<span data-ttu-id="212c1-141">Określa typ wyników, który ma być zwracany (metadane lub dane).</span><span class="sxs-lookup"><span data-stu-id="212c1-141">Specifies the result type to be returned (metadata or data).</span></span>

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

### <span data-ttu-id="212c1-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="212c1-142">-StartTime</span></span>
<span data-ttu-id="212c1-143">Określa godzinę rozpoczęcia kwerendy w czasie lokalnym.</span><span class="sxs-lookup"><span data-stu-id="212c1-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="212c1-144">Domyślnie jest to bieżący czas lokalny minus jedna godzina.</span><span class="sxs-lookup"><span data-stu-id="212c1-144">The default is the current local time minus one hour.</span></span>

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

### <span data-ttu-id="212c1-145">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="212c1-145">-TimeGrain</span></span>
<span data-ttu-id="212c1-146">Określa ziarno czasu metryki jako obiektu **TimeSpan** w formacie gg: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="212c1-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

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

### <span data-ttu-id="212c1-147">-Początek</span><span class="sxs-lookup"><span data-stu-id="212c1-147">-Top</span></span>
<span data-ttu-id="212c1-148">Określa maksymalną liczbę rekordów do pobrania (domyślnie: 10), które mają być określane za pomocą $filter.</span><span class="sxs-lookup"><span data-stu-id="212c1-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

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

### <span data-ttu-id="212c1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="212c1-149">CommonParameters</span></span>
<span data-ttu-id="212c1-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="212c1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="212c1-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="212c1-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="212c1-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="212c1-152">INPUTS</span></span>

### <span data-ttu-id="212c1-153">System. String</span><span class="sxs-lookup"><span data-stu-id="212c1-153">System.String</span></span>

### <span data-ttu-id="212c1-154">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="212c1-154">System.TimeSpan</span></span>

### <span data-ttu-id="212c1-155">System. Nullable "1 [[Microsoft. Azure. Management. Monitor. MODELES. agregacja, Microsoft. Azure. Management. Monitor, Version = 0.19.1.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="212c1-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.19.1.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="212c1-156">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="212c1-156">System.DateTime</span></span>

### <span data-ttu-id="212c1-157">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="212c1-157">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="212c1-158">System. Nullable "1 [[Microsoft. Azure. Management. Monitor. MODELES. Result., Microsoft. Azure. Management. Monitor, Version = 0.19.1.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="212c1-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.19.1.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="212c1-159">System. String []</span><span class="sxs-lookup"><span data-stu-id="212c1-159">System.String[]</span></span>

### <span data-ttu-id="212c1-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="212c1-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="212c1-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="212c1-161">OUTPUTS</span></span>

### <span data-ttu-id="212c1-162">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric</span><span class="sxs-lookup"><span data-stu-id="212c1-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="212c1-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="212c1-163">NOTES</span></span>

## <span data-ttu-id="212c1-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="212c1-164">RELATED LINKS</span></span>

<span data-ttu-id="212c1-165">[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md) 
 [Nowe — AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="212c1-165">[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)
[New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span></span>


