---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: e30ae2389d7f597cd667b9d29ab76087a55315cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867299"
---
# <span data-ttu-id="def92-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="def92-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="def92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="def92-102">SYNOPSIS</span></span>
<span data-ttu-id="def92-103">Pobiera definicje metryk.</span><span class="sxs-lookup"><span data-stu-id="def92-103">Gets metric definitions.</span></span>

## <span data-ttu-id="def92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="def92-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="def92-105">Opis</span><span class="sxs-lookup"><span data-stu-id="def92-105">DESCRIPTION</span></span>
<span data-ttu-id="def92-106">Polecenie cmdlet **Get-AzMetricDefinition** umożliwia pobieranie definicji metryk.</span><span class="sxs-lookup"><span data-stu-id="def92-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="def92-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="def92-107">EXAMPLES</span></span>

### <span data-ttu-id="def92-108">Przykład 1: uzyskiwanie definicji metryk dla zasobu</span><span class="sxs-lookup"><span data-stu-id="def92-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
Name                   : CpuTime
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Seconds
Name                   : Requests
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="def92-109">To polecenie pobiera definicje metryk dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="def92-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="def92-110">Przykład 2: uzyskiwanie definicji metryk ze szczegółowym wyjściem</span><span class="sxs-lookup"><span data-stu-id="def92-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : Requests
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="def92-111">To polecenie pobiera definicje metryk dla website2.</span><span class="sxs-lookup"><span data-stu-id="def92-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="def92-112">Wynik jest szczegółowy.</span><span class="sxs-lookup"><span data-stu-id="def92-112">The output is detailed.</span></span>

### <span data-ttu-id="def92-113">Przykład 3: uzyskiwanie definicji metryk według nazw</span><span class="sxs-lookup"><span data-stu-id="def92-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricNames "BytesSent,CpuTime"
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : BytesSent
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Bytes
```

<span data-ttu-id="def92-114">To polecenie pobiera definicje metryk BytesSent i CpuTime.</span><span class="sxs-lookup"><span data-stu-id="def92-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="def92-115">Wynik jest szczegółowy.</span><span class="sxs-lookup"><span data-stu-id="def92-115">The output is detailed.</span></span>

## <span data-ttu-id="def92-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="def92-116">PARAMETERS</span></span>

### <span data-ttu-id="def92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="def92-117">-DefaultProfile</span></span>
<span data-ttu-id="def92-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="def92-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="def92-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="def92-119">-DetailedOutput</span></span>
<span data-ttu-id="def92-120">Wskazuje, że ta operacja zawiera szczegółowe dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="def92-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="def92-121">Jeśli ten parametr nie zostanie określony, dane wyjściowe zostaną podsumowane.</span><span class="sxs-lookup"><span data-stu-id="def92-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="def92-122">-Metricname</span><span class="sxs-lookup"><span data-stu-id="def92-122">-MetricName</span></span>
<span data-ttu-id="def92-123">Określa tablicę nazw metryk.</span><span class="sxs-lookup"><span data-stu-id="def92-123">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="def92-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="def92-124">-MetricNamespace</span></span>
<span data-ttu-id="def92-125">Określa obszar nazw metryki służący do wyszukiwania definicji metryki.</span><span class="sxs-lookup"><span data-stu-id="def92-125">Specifies the metric namespace to query metric definitions for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="def92-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="def92-126">-ResourceId</span></span>
<span data-ttu-id="def92-127">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="def92-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="def92-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def92-128">CommonParameters</span></span>
<span data-ttu-id="def92-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="def92-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def92-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="def92-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def92-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="def92-131">INPUTS</span></span>

### <span data-ttu-id="def92-132">System. String</span><span class="sxs-lookup"><span data-stu-id="def92-132">System.String</span></span>

### <span data-ttu-id="def92-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="def92-133">System.String[]</span></span>

## <span data-ttu-id="def92-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="def92-134">OUTPUTS</span></span>

### <span data-ttu-id="def92-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="def92-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="def92-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="def92-136">NOTES</span></span>

## <span data-ttu-id="def92-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="def92-137">RELATED LINKS</span></span>

<span data-ttu-id="def92-138">[Get-AzMetric](./Get-AzMetric.md) 
 [Nowe — AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="def92-138">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>

