---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: 63ade199b63e57cc72e965002942773f47214494
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716734"
---
# <span data-ttu-id="48c6c-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="48c6c-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="48c6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="48c6c-103">Pobiera wartości metryki zasobu.</span><span class="sxs-lookup"><span data-stu-id="48c6c-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48c6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48c6c-104">SYNTAX</span></span>

### <span data-ttu-id="48c6c-105">GetWithDefaultParameters</span><span class="sxs-lookup"><span data-stu-id="48c6c-105">GetWithDefaultParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48c6c-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="48c6c-106">GetWithFullParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48c6c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="48c6c-107">DESCRIPTION</span></span>
<span data-ttu-id="48c6c-108">Polecenie cmdlet **Get-AzureRmMetric** pobiera wartości metryk dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="48c6c-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="48c6c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48c6c-109">EXAMPLES</span></span>

### <span data-ttu-id="48c6c-110">Przykład 1: uzyskiwanie metryki z podsumowaniem wyników</span><span class="sxs-lookup"><span data-stu-id="48c6c-110">Example 1: Get a metric with summarized output</span></span>
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

<span data-ttu-id="48c6c-111">To polecenie pobiera wartości metryczne dla website3 z ziarnem czasowym o wartości 1 minuta.</span><span class="sxs-lookup"><span data-stu-id="48c6c-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="48c6c-112">Przykład 2: uzyskiwanie metryki ze szczegółowym wyjściem</span><span class="sxs-lookup"><span data-stu-id="48c6c-112">Example 2: Get a metric with detailed output</span></span>
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

<span data-ttu-id="48c6c-113">To polecenie pobiera wartości metryczne dla website3 z ziarnem czasowym o wartości 1 minuta.</span><span class="sxs-lookup"><span data-stu-id="48c6c-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="48c6c-114">Wynik jest szczegółowy.</span><span class="sxs-lookup"><span data-stu-id="48c6c-114">The output is detailed.</span></span>

### <span data-ttu-id="48c6c-115">Przykład 3: uzyskiwanie szczegółowych danych wyjściowych dla określonej metryki</span><span class="sxs-lookup"><span data-stu-id="48c6c-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput -MetricNames "Requests"
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

<span data-ttu-id="48c6c-116">To polecenie pobiera szczegółowe dane wyjściowe metryki żądań.</span><span class="sxs-lookup"><span data-stu-id="48c6c-116">This command gets detailed output for the Requests metric.</span></span>

## <span data-ttu-id="48c6c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48c6c-117">PARAMETERS</span></span>

### <span data-ttu-id="48c6c-118">-Agregacja</span><span class="sxs-lookup"><span data-stu-id="48c6c-118">-AggregationType</span></span>
<span data-ttu-id="48c6c-119">Typ agregacji zapytania</span><span class="sxs-lookup"><span data-stu-id="48c6c-119">The aggregation type of the query</span></span>

```yaml
Type: AggregationType
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48c6c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c6c-120">-DefaultProfile</span></span>
<span data-ttu-id="48c6c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48c6c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c6c-122">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="48c6c-122">-DetailedOutput</span></span>
<span data-ttu-id="48c6c-123">Wskazuje, że w tym poleceniu cmdlet są wyświetlane szczegółowe dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="48c6c-123">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="48c6c-124">Domyślnie dane wyjściowe są sumowane.</span><span class="sxs-lookup"><span data-stu-id="48c6c-124">By default, output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48c6c-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="48c6c-125">-EndTime</span></span>
<span data-ttu-id="48c6c-126">Określa godzinę zakończenia kwerendy w czasie lokalnym.</span><span class="sxs-lookup"><span data-stu-id="48c6c-126">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="48c6c-127">Wartością domyślną jest bieżąca godzina.</span><span class="sxs-lookup"><span data-stu-id="48c6c-127">The default is the current time.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48c6c-128">-Metricname</span><span class="sxs-lookup"><span data-stu-id="48c6c-128">-MetricName</span></span>
<span data-ttu-id="48c6c-129">Określa tablicę nazw metryk.</span><span class="sxs-lookup"><span data-stu-id="48c6c-129">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False (GetWithDefaultParameters), True (GetAzureRmAMetricFullParamGroup)
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: GetWithFullParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48c6c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48c6c-130">-ResourceId</span></span>
<span data-ttu-id="48c6c-131">Określa identyfikator zasobu metryki.</span><span class="sxs-lookup"><span data-stu-id="48c6c-131">Specifies the resource ID of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48c6c-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="48c6c-132">-StartTime</span></span>
<span data-ttu-id="48c6c-133">Określa godzinę rozpoczęcia kwerendy w czasie lokalnym.</span><span class="sxs-lookup"><span data-stu-id="48c6c-133">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="48c6c-134">Domyślnie jest to bieżący czas lokalny minus jedna godzina.</span><span class="sxs-lookup"><span data-stu-id="48c6c-134">The default is the current local time minus one hour.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48c6c-135">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="48c6c-135">-TimeGrain</span></span>
<span data-ttu-id="48c6c-136">Określa ziarno czasu metryki jako obiektu **TimeSpan** w formacie gg: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="48c6c-136">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48c6c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c6c-137">CommonParameters</span></span>
<span data-ttu-id="48c6c-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48c6c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c6c-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48c6c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c6c-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48c6c-140">INPUTS</span></span>

### <span data-ttu-id="48c6c-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="48c6c-141">None</span></span>
<span data-ttu-id="48c6c-142">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="48c6c-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="48c6c-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48c6c-143">OUTPUTS</span></span>

### <span data-ttu-id="48c6c-144">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric []</span><span class="sxs-lookup"><span data-stu-id="48c6c-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric[]</span></span>

## <span data-ttu-id="48c6c-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48c6c-145">NOTES</span></span>

## <span data-ttu-id="48c6c-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48c6c-146">RELATED LINKS</span></span>

[<span data-ttu-id="48c6c-147">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="48c6c-147">Get-AzureRmMetricDefinition</span></span>](./Get-AzureRmMetricDefinition.md)


