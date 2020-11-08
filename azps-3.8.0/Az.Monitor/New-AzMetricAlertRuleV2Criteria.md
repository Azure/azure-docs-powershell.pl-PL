---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 6e50269e98a942d425f914eed5cc0a75938d0e9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049375"
---
# <span data-ttu-id="ba262-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="ba262-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="ba262-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba262-102">SYNOPSIS</span></span>
<span data-ttu-id="ba262-103">Tworzy obiekt Local kryteria, za pomocą którego można utworzyć nowy Alert metryki</span><span class="sxs-lookup"><span data-stu-id="ba262-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="ba262-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba262-104">SYNTAX</span></span>

### <span data-ttu-id="ba262-105">StaticThresholdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ba262-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba262-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba262-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 [-ThresholdSensitivity <String>] [-ViolationCount <Int32>] [-ExaminedAggregatedPointCount <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba262-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ba262-107">DESCRIPTION</span></span>
<span data-ttu-id="ba262-108">Polecenie cmdlet **New-AzMetricAlertRuleV2Criteria** tworzy obiekt Local Metric kryteriów, który ma być wykorzystywany jako wejściowy polecenie cmdlet Add-AzMetricAlertRuleV2, który tworzy nową regułę alertu metryki.</span><span class="sxs-lookup"><span data-stu-id="ba262-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="ba262-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba262-109">EXAMPLES</span></span>

### <span data-ttu-id="ba262-110">Przykład 1. Tworzenie prostych kryteriów alertów metrycznych</span><span class="sxs-lookup"><span data-stu-id="ba262-110">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 5
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="ba262-111">To polecenie tworzy proste kryteria alertu metryki, które mogą być używane w regule alertu metryki</span><span class="sxs-lookup"><span data-stu-id="ba262-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="ba262-112">Przykład 2: Tworzenie kryteriów dynamicznego alertu metrycznego</span><span class="sxs-lookup"><span data-stu-id="ba262-112">Example 2: Create a dynamic metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -Dynamic -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -ThresholdSensitivity Medium -ViolationCount 2 -ExaminedAggregatedPointCount 4
CriterionType        : DynamicThresholdCriterion
OperatorProperty     : GreaterThan
AlertSensitivity     : Medium
FailingPeriods       : Microsoft.Azure.Management.Monitor.Models.DynamicThresholdFailingPeriods
IgnoreDataBefore     :
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="ba262-113">To polecenie tworzy dynamiczne kryteria alertów metrycznych, które mogą być używane w regule alertu metryki</span><span class="sxs-lookup"><span data-stu-id="ba262-113">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="ba262-114">Przykład 3: tworzenie bardziej złożonych kryteriów alertów metrycznych</span><span class="sxs-lookup"><span data-stu-id="ba262-114">Example 3: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 2
AdditionalProperties :
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
TimeAggregation      : Average
Dimensions           : {availabilityResult/name}
```

<span data-ttu-id="ba262-115">Ten zestaw poleceń tworzy bardziej złożone kryteria alertów metryki, które zawierają zaznaczenie wymiarów.</span><span class="sxs-lookup"><span data-stu-id="ba262-115">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="ba262-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba262-116">PARAMETERS</span></span>

### <span data-ttu-id="ba262-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba262-117">-DefaultProfile</span></span>
<span data-ttu-id="ba262-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba262-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba262-119">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="ba262-119">-DimensionSelection</span></span>
<span data-ttu-id="ba262-120">Lista warunków wymiaru</span><span class="sxs-lookup"><span data-stu-id="ba262-120">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-121">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="ba262-121">-DynamicThreshold</span></span>
<span data-ttu-id="ba262-122">Parametr Switch umożliwiający używanie typu progu dynamicznego</span><span class="sxs-lookup"><span data-stu-id="ba262-122">Switch parameter for using Dynamic Threshold Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-123">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="ba262-123">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="ba262-124">Łączna liczba punktów badanych</span><span class="sxs-lookup"><span data-stu-id="ba262-124">The Total number of examined points</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: TotalPeriod, NumberOfExaminedAggregatedPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-125">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="ba262-125">-IgnoreDataBefore</span></span>
<span data-ttu-id="ba262-126">Parametr IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="ba262-126">The IgnoreDataBefore parameter</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="ba262-127">-MetricName</span></span>
<span data-ttu-id="ba262-128">Nazwa metryki dla reguły</span><span class="sxs-lookup"><span data-stu-id="ba262-128">The metric name for rule</span></span>

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

### <span data-ttu-id="ba262-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="ba262-129">-MetricNamespace</span></span>
<span data-ttu-id="ba262-130">Obszar nazw metryki</span><span class="sxs-lookup"><span data-stu-id="ba262-130">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-131">-Operator</span><span class="sxs-lookup"><span data-stu-id="ba262-131">-Operator</span></span>
<span data-ttu-id="ba262-132">Operator warunku reguły</span><span class="sxs-lookup"><span data-stu-id="ba262-132">The rule condition operator</span></span>

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

### <span data-ttu-id="ba262-133">-Próg</span><span class="sxs-lookup"><span data-stu-id="ba262-133">-Threshold</span></span>
<span data-ttu-id="ba262-134">Próg warunku reguły</span><span class="sxs-lookup"><span data-stu-id="ba262-134">The threshold for rule condition</span></span>

```yaml
Type: System.Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-135">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="ba262-135">-ThresholdSensitivity</span></span>
<span data-ttu-id="ba262-136">Czułość na warunek reguły</span><span class="sxs-lookup"><span data-stu-id="ba262-136">The sensitivity for rule condition</span></span>

```yaml
Type: System.String
Parameter Sets: DynamicThresholdParameterSet
Aliases: Sensitivity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-137">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="ba262-137">-TimeAggregation</span></span>
<span data-ttu-id="ba262-138">Operacja agregacji używana do rzutowania wielu wartości metrycznych w interwale okien</span><span class="sxs-lookup"><span data-stu-id="ba262-138">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

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

### <span data-ttu-id="ba262-139">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="ba262-139">-ViolationCount</span></span>
<span data-ttu-id="ba262-140">Minimalna liczba nieprawidłowych naruszeń w wybranym przedziale czasu lookback wymaganym do podniesienia poziomu alertu</span><span class="sxs-lookup"><span data-stu-id="ba262-140">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: FailingPeriod, NumberOfViolations

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba262-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba262-141">CommonParameters</span></span>
<span data-ttu-id="ba262-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba262-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba262-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba262-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba262-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba262-144">INPUTS</span></span>

### <span data-ttu-id="ba262-145">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="ba262-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="ba262-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba262-146">OUTPUTS</span></span>

### <span data-ttu-id="ba262-147">Microsoft. Azure. Commands. Insights. OutputClasses. IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="ba262-147">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="ba262-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba262-148">NOTES</span></span>

## <span data-ttu-id="ba262-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba262-149">RELATED LINKS</span></span>
