---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 0158f274ea485262b05fa1a336a2ce071fc64930
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233328"
---
# <span data-ttu-id="7e958-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="7e958-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="7e958-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e958-102">SYNOPSIS</span></span>
<span data-ttu-id="7e958-103">Tworzy obiekt Local kryteria, za pomocą którego można utworzyć nowy Alert metryki</span><span class="sxs-lookup"><span data-stu-id="7e958-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="7e958-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e958-104">SYNTAX</span></span>

### <span data-ttu-id="7e958-105">StaticThresholdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7e958-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e958-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e958-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e958-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e958-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e958-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7e958-108">DESCRIPTION</span></span>
<span data-ttu-id="7e958-109">Polecenie cmdlet **New-AzMetricAlertRuleV2Criteria** tworzy obiekt Local Metric kryteriów, który ma być wykorzystywany jako wejściowy polecenie cmdlet [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) , które tworzy nową regułę alertu metryki.</span><span class="sxs-lookup"><span data-stu-id="7e958-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="7e958-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e958-110">EXAMPLES</span></span>

### <span data-ttu-id="7e958-111">Przykład 1. Tworzenie prostych kryteriów alertów metrycznych</span><span class="sxs-lookup"><span data-stu-id="7e958-111">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="7e958-112">To polecenie tworzy proste kryteria alertu metryki, które mogą być używane w regule alertu metryki</span><span class="sxs-lookup"><span data-stu-id="7e958-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="7e958-113">Przykład 2: Tworzenie kryteriów dynamicznego alertu metrycznego</span><span class="sxs-lookup"><span data-stu-id="7e958-113">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="7e958-114">To polecenie tworzy dynamiczne kryteria alertów metrycznych, które mogą być używane w regule alertu metryki</span><span class="sxs-lookup"><span data-stu-id="7e958-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="7e958-115">Przykład 3: tworzenie bardziej złożonych kryteriów alertów metrycznych</span><span class="sxs-lookup"><span data-stu-id="7e958-115">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="7e958-116">Ten zestaw poleceń tworzy bardziej złożone kryteria alertów metryki, które zawierają zaznaczenie wymiarów.</span><span class="sxs-lookup"><span data-stu-id="7e958-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="7e958-117">Przykład 4: Tworzenie kryteriów dostępności WebTest</span><span class="sxs-lookup"><span data-stu-id="7e958-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="7e958-118">To polecenie tworzy kryteria dostępności WebTest, których można użyć w regule alertu metryki</span><span class="sxs-lookup"><span data-stu-id="7e958-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="7e958-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e958-119">PARAMETERS</span></span>

### <span data-ttu-id="7e958-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="7e958-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="7e958-121">Identyfikator zasobu usługi Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7e958-121">The Application Insights resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases: componentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e958-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e958-122">-DefaultProfile</span></span>
<span data-ttu-id="7e958-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e958-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e958-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7e958-124">-DimensionSelection</span></span>
<span data-ttu-id="7e958-125">Lista warunków wymiaru</span><span class="sxs-lookup"><span data-stu-id="7e958-125">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e958-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="7e958-126">-DynamicThreshold</span></span>
<span data-ttu-id="7e958-127">Parametr Switch umożliwiający używanie typu progu dynamicznego</span><span class="sxs-lookup"><span data-stu-id="7e958-127">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="7e958-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="7e958-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="7e958-129">Łączna liczba punktów badanych</span><span class="sxs-lookup"><span data-stu-id="7e958-129">The Total number of examined points</span></span>

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

### <span data-ttu-id="7e958-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="7e958-130">-FailedLocationCount</span></span>
<span data-ttu-id="7e958-131">Minimalna liczba nieudanych lokalizacji, dla których ma zostać poddany alert.</span><span class="sxs-lookup"><span data-stu-id="7e958-131">The minimum number of failed locations to raise an alert.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WebtestParameterSet
Aliases: AlertLocationThreshold

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e958-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="7e958-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="7e958-133">Parametr IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="7e958-133">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="7e958-134">-Metricname</span><span class="sxs-lookup"><span data-stu-id="7e958-134">-MetricName</span></span>
<span data-ttu-id="7e958-135">Nazwa metryki dla reguły</span><span class="sxs-lookup"><span data-stu-id="7e958-135">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e958-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="7e958-136">-MetricNamespace</span></span>
<span data-ttu-id="7e958-137">Obszar nazw metryki</span><span class="sxs-lookup"><span data-stu-id="7e958-137">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e958-138">-Operator</span><span class="sxs-lookup"><span data-stu-id="7e958-138">-Operator</span></span>
<span data-ttu-id="7e958-139">Operator warunku reguły</span><span class="sxs-lookup"><span data-stu-id="7e958-139">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e958-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="7e958-140">-SkipMetricValidation</span></span>
<span data-ttu-id="7e958-141">Umożliwia utworzenie reguły alertu na niestandardową metryki, która nie jest jeszcze emitowana, powodując Pominięcie sprawdzania poprawności metryki.</span><span class="sxs-lookup"><span data-stu-id="7e958-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e958-142">-Próg</span><span class="sxs-lookup"><span data-stu-id="7e958-142">-Threshold</span></span>
<span data-ttu-id="7e958-143">Próg warunku reguły</span><span class="sxs-lookup"><span data-stu-id="7e958-143">The threshold for rule condition</span></span>

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

### <span data-ttu-id="7e958-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="7e958-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="7e958-145">Czułość na warunek reguły</span><span class="sxs-lookup"><span data-stu-id="7e958-145">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="7e958-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="7e958-146">-TimeAggregation</span></span>
<span data-ttu-id="7e958-147">Operacja agregacji używana do rzutowania wielu wartości metrycznych w interwale okien</span><span class="sxs-lookup"><span data-stu-id="7e958-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e958-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="7e958-148">-ViolationCount</span></span>
<span data-ttu-id="7e958-149">Minimalna liczba nieprawidłowych naruszeń w wybranym przedziale czasu lookback wymaganym do podniesienia poziomu alertu</span><span class="sxs-lookup"><span data-stu-id="7e958-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="7e958-150">-WebTest</span><span class="sxs-lookup"><span data-stu-id="7e958-150">-WebTest</span></span>
<span data-ttu-id="7e958-151">Parametr przełącznika umożliwiający używanie kryteriów dostępności typu</span><span class="sxs-lookup"><span data-stu-id="7e958-151">Switch parameter for using availability criteria Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebtestParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e958-152">-WebTestId</span><span class="sxs-lookup"><span data-stu-id="7e958-152">-WebTestId</span></span>
<span data-ttu-id="7e958-153">Identyfikator testu w sieci Web usługi Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7e958-153">The Application Insights web test Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e958-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e958-154">CommonParameters</span></span>
<span data-ttu-id="7e958-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e958-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e958-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e958-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e958-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e958-157">INPUTS</span></span>

### <span data-ttu-id="7e958-158">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="7e958-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="7e958-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e958-159">OUTPUTS</span></span>

### <span data-ttu-id="7e958-160">Microsoft. Azure. Commands. Insights. OutputClasses. IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="7e958-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="7e958-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e958-161">NOTES</span></span>

## <span data-ttu-id="7e958-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e958-162">RELATED LINKS</span></span>
