---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 9ca873736ad86eaac17dd2795ad61716197ceaba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184970"
---
# <span data-ttu-id="9a8bc-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="9a8bc-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="9a8bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a8bc-102">SYNOPSIS</span></span>
<span data-ttu-id="9a8bc-103">Pobiera definicje metryk.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-103">Gets metric definitions.</span></span>

## <span data-ttu-id="9a8bc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9a8bc-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a8bc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9a8bc-105">DESCRIPTION</span></span>
<span data-ttu-id="9a8bc-106">Polecenie **cmdlet Get-AzMetricDefinition** pobiera definicje metryk.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="9a8bc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9a8bc-107">EXAMPLES</span></span>

### <span data-ttu-id="9a8bc-108">Przykład 1. Uzyskiwanie definicji metrycznych dla zasobu</span><span class="sxs-lookup"><span data-stu-id="9a8bc-108">Example 1: Get metric definitions for a resource</span></span>
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

<span data-ttu-id="9a8bc-109">To polecenie pobiera definicje metryk dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="9a8bc-110">Przykład 2. Uzyskiwanie definicji metrycznych ze szczegółowymi danymi wyjściowym</span><span class="sxs-lookup"><span data-stu-id="9a8bc-110">Example 2: Get metric definitions with detailed output</span></span>
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

<span data-ttu-id="9a8bc-111">To polecenie pobiera definicje metryk dla witryny sieci Web 2.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="9a8bc-112">Dane wyjściowe są szczegółowe.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-112">The output is detailed.</span></span>

### <span data-ttu-id="9a8bc-113">Przykład 3. Uzyskiwanie definicji metrycznych według nazwy</span><span class="sxs-lookup"><span data-stu-id="9a8bc-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricName "BytesSent,CpuTime"
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

<span data-ttu-id="9a8bc-114">To polecenie pobiera definicje metryk BytesSent i CpuTime.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="9a8bc-115">Dane wyjściowe są szczegółowe.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-115">The output is detailed.</span></span>

## <span data-ttu-id="9a8bc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a8bc-116">PARAMETERS</span></span>

### <span data-ttu-id="9a8bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a8bc-117">-DefaultProfile</span></span>
<span data-ttu-id="9a8bc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9a8bc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a8bc-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="9a8bc-119">-DetailedOutput</span></span>
<span data-ttu-id="9a8bc-120">Oznacza, że ta operacja uwzględniała szczegółowe dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="9a8bc-121">Jeśli nie określisz tego parametru, dane wyjściowe będą podsumowywane.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="9a8bc-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="9a8bc-122">-MetricName</span></span>
<span data-ttu-id="9a8bc-123">Określa tablicę nazw metryk.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-123">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="9a8bc-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="9a8bc-124">-MetricNamespace</span></span>
<span data-ttu-id="9a8bc-125">Określa metryczna przestrzeń nazw, dla których mają być kwerendne definicje metryk.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-125">Specifies the metric namespace to query metric definitions for.</span></span>

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

### <span data-ttu-id="9a8bc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a8bc-126">-ResourceId</span></span>
<span data-ttu-id="9a8bc-127">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="9a8bc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a8bc-128">CommonParameters</span></span>
<span data-ttu-id="9a8bc-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a8bc-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a8bc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a8bc-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a8bc-131">INPUTS</span></span>

### <span data-ttu-id="9a8bc-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9a8bc-132">System.String</span></span>

### <span data-ttu-id="9a8bc-133">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9a8bc-133">System.String[]</span></span>

## <span data-ttu-id="9a8bc-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a8bc-134">OUTPUTS</span></span>

### <span data-ttu-id="9a8bc-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="9a8bc-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="9a8bc-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9a8bc-136">NOTES</span></span>

<span data-ttu-id="9a8bc-137">Więcej informacji o obsługiwanych metrykach można znaleźć na stronie: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="9a8bc-137">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="9a8bc-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a8bc-138">RELATED LINKS</span></span>

<span data-ttu-id="9a8bc-139">[Get-AzMetric](./Get-AzMetric.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="9a8bc-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


