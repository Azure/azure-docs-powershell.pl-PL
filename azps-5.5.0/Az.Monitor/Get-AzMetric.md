---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
ms.openlocfilehash: d02a6f9ca3f4821fa8a552f92ef90fa24a9e6bd2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184979"
---
# <span data-ttu-id="85f7d-101">Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="85f7d-101">Get-AzMetric</span></span>

## <span data-ttu-id="85f7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="85f7d-103">Pobiera wartości metryczne zasobu.</span><span class="sxs-lookup"><span data-stu-id="85f7d-103">Gets the metric values of a resource.</span></span>

## <span data-ttu-id="85f7d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="85f7d-104">SYNTAX</span></span>

### <span data-ttu-id="85f7d-105">GetWithDefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="85f7d-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85f7d-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="85f7d-106">GetWithFullParameters</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85f7d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="85f7d-107">DESCRIPTION</span></span>
<span data-ttu-id="85f7d-108">Polecenie **cmdlet Get-AzMetric** pobiera wartości metryczne dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="85f7d-108">The **Get-AzMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="85f7d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="85f7d-109">EXAMPLES</span></span>

### <span data-ttu-id="85f7d-110">Przykład 1. Uzyskiwanie metryki z podsumowaną wartością wyjściową</span><span class="sxs-lookup"><span data-stu-id="85f7d-110">Example 1: Get a metric with summarized output</span></span>
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

<span data-ttu-id="85f7d-111">To polecenie pobiera wartości metryczne dla witryny website3 z okresem 1 minuty.</span><span class="sxs-lookup"><span data-stu-id="85f7d-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="85f7d-112">Przykład 2. Uzyskiwanie metryki ze szczegółowymi danymi wyjściowmi</span><span class="sxs-lookup"><span data-stu-id="85f7d-112">Example 2: Get a metric with detailed output</span></span>
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

<span data-ttu-id="85f7d-113">To polecenie pobiera wartości metryczne dla witryny website3 z okresem 1 minuty.</span><span class="sxs-lookup"><span data-stu-id="85f7d-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="85f7d-114">Dane wyjściowe są szczegółowe.</span><span class="sxs-lookup"><span data-stu-id="85f7d-114">The output is detailed.</span></span>

### <span data-ttu-id="85f7d-115">Przykład 3. Uzyskiwanie szczegółowych danych wyjściowych dla określonej metryki</span><span class="sxs-lookup"><span data-stu-id="85f7d-115">Example 3: Get detailed output for a specified metric</span></span>
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

<span data-ttu-id="85f7d-116">To polecenie uzyskuje szczegółowe dane wyjściowe metryki Żądania.</span><span class="sxs-lookup"><span data-stu-id="85f7d-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="85f7d-117">Przykład 4. Uzyskiwanie podsumowanych danych wyjściowych dla określonej metryki przy użyciu określonego filtru wymiaru</span><span class="sxs-lookup"><span data-stu-id="85f7d-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
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

<span data-ttu-id="85f7d-118">To polecenie pobiera podsumowanie danych wyjściowych metryki PageViews z określonym filtrem wymiaru i typem agregacji.</span><span class="sxs-lookup"><span data-stu-id="85f7d-118">This command gets summarized output for the PageViews metric with specified dimension filter and aggregation type.</span></span>

## <span data-ttu-id="85f7d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85f7d-119">PARAMETERS</span></span>

### <span data-ttu-id="85f7d-120">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="85f7d-120">-AggregationType</span></span>
<span data-ttu-id="85f7d-121">Typ agregacji zapytania</span><span class="sxs-lookup"><span data-stu-id="85f7d-121">The aggregation type of the query</span></span>

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

### <span data-ttu-id="85f7d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f7d-122">-DefaultProfile</span></span>
<span data-ttu-id="85f7d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="85f7d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85f7d-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="85f7d-124">-DetailedOutput</span></span>
<span data-ttu-id="85f7d-125">Wskazuje, że to polecenie cmdlet wyświetla szczegółowe dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="85f7d-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="85f7d-126">Domyślnie dane wyjściowe są podsumowywane.</span><span class="sxs-lookup"><span data-stu-id="85f7d-126">By default, output is summarized.</span></span>

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

### <span data-ttu-id="85f7d-127">- EndTime</span><span class="sxs-lookup"><span data-stu-id="85f7d-127">-EndTime</span></span>
<span data-ttu-id="85f7d-128">Określa czas zakończenia kwerendy w czasie lokalnym.</span><span class="sxs-lookup"><span data-stu-id="85f7d-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="85f7d-129">Wartością domyślną jest bieżąca godzina.</span><span class="sxs-lookup"><span data-stu-id="85f7d-129">The default is the current time.</span></span>

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

### <span data-ttu-id="85f7d-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="85f7d-130">-MetricFilter</span></span>
<span data-ttu-id="85f7d-131">Określa metrykę filtru wymiarów metrycznych, dla których mają być kwerendowane metryki.</span><span class="sxs-lookup"><span data-stu-id="85f7d-131">Specifies the metric dimension filter to query metrics for.</span></span>

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

### <span data-ttu-id="85f7d-132">-MetricName</span><span class="sxs-lookup"><span data-stu-id="85f7d-132">-MetricName</span></span>
<span data-ttu-id="85f7d-133">Określa tablicę nazw metryk.</span><span class="sxs-lookup"><span data-stu-id="85f7d-133">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="85f7d-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="85f7d-134">-MetricNamespace</span></span>
<span data-ttu-id="85f7d-135">Określa metrykę przestrzeni nazw, dla których mają być kwerendy.</span><span class="sxs-lookup"><span data-stu-id="85f7d-135">Specifies the metric namespace to query metrics for.</span></span>

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

### <span data-ttu-id="85f7d-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="85f7d-136">-OrderBy</span></span>
<span data-ttu-id="85f7d-137">Określa agregację do użycia w wynikach sortowania i kierunek sortowania (przykład: suma asc).</span><span class="sxs-lookup"><span data-stu-id="85f7d-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

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

### <span data-ttu-id="85f7d-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85f7d-138">-ResourceId</span></span>
<span data-ttu-id="85f7d-139">Określa identyfikator zasobu metryki.</span><span class="sxs-lookup"><span data-stu-id="85f7d-139">Specifies the resource ID of the metric.</span></span>

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

### <span data-ttu-id="85f7d-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="85f7d-140">-ResultType</span></span>
<span data-ttu-id="85f7d-141">Określa typ wyniku do zwrócenia (metadane lub dane).</span><span class="sxs-lookup"><span data-stu-id="85f7d-141">Specifies the result type to be returned (metadata or data).</span></span>

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

### <span data-ttu-id="85f7d-142">— StartTime</span><span class="sxs-lookup"><span data-stu-id="85f7d-142">-StartTime</span></span>
<span data-ttu-id="85f7d-143">Określa czas rozpoczęcia zapytania w czasie lokalnym.</span><span class="sxs-lookup"><span data-stu-id="85f7d-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="85f7d-144">Wartością domyślną jest bieżący czas lokalny minus jedna godzina.</span><span class="sxs-lookup"><span data-stu-id="85f7d-144">The default is the current local time minus one hour.</span></span>

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

### <span data-ttu-id="85f7d-145">- TimeGrain</span><span class="sxs-lookup"><span data-stu-id="85f7d-145">-TimeGrain</span></span>
<span data-ttu-id="85f7d-146">Określa grain czasu metryki jako obiekt **TimeSpan** w formacie gg:mm:ss.</span><span class="sxs-lookup"><span data-stu-id="85f7d-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

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

### <span data-ttu-id="85f7d-147">— Na górze</span><span class="sxs-lookup"><span data-stu-id="85f7d-147">-Top</span></span>
<span data-ttu-id="85f7d-148">Określa maksymalną liczbę rekordów do pobrania (wartość domyślna: 10), które mają zostać określone przy $filter.</span><span class="sxs-lookup"><span data-stu-id="85f7d-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

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

### <span data-ttu-id="85f7d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85f7d-149">CommonParameters</span></span>
<span data-ttu-id="85f7d-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85f7d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85f7d-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85f7d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85f7d-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85f7d-152">INPUTS</span></span>

### <span data-ttu-id="85f7d-153">System.String</span><span class="sxs-lookup"><span data-stu-id="85f7d-153">System.String</span></span>

### <span data-ttu-id="85f7d-154">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="85f7d-154">System.TimeSpan</span></span>

### <span data-ttu-id="85f7d-155">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="85f7d-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="85f7d-156">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="85f7d-156">System.DateTime</span></span>

### <span data-ttu-id="85f7d-157">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="85f7d-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="85f7d-158">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="85f7d-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="85f7d-159">System.String[]</span><span class="sxs-lookup"><span data-stu-id="85f7d-159">System.String[]</span></span>

### <span data-ttu-id="85f7d-160">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="85f7d-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="85f7d-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="85f7d-161">OUTPUTS</span></span>

### <span data-ttu-id="85f7d-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span><span class="sxs-lookup"><span data-stu-id="85f7d-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="85f7d-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="85f7d-163">NOTES</span></span>

<span data-ttu-id="85f7d-164">Więcej informacji o obsługiwanych metrykach można znaleźć na stronie: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="85f7d-164">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="85f7d-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85f7d-165">RELATED LINKS</span></span>

<span data-ttu-id="85f7d-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="85f7d-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


