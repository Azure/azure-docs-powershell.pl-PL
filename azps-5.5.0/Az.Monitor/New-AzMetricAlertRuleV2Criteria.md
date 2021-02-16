---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 0158f274ea485262b05fa1a336a2ce071fc64930
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190138"
---
# <span data-ttu-id="8387f-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="8387f-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="8387f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8387f-102">SYNOPSIS</span></span>
<span data-ttu-id="8387f-103">Tworzy obiekt kryteriów lokalnych, za pomocą których można utworzyć nowy alert metryczny.</span><span class="sxs-lookup"><span data-stu-id="8387f-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="8387f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8387f-104">SYNTAX</span></span>

### <span data-ttu-id="8387f-105">StaticThresholdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8387f-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8387f-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8387f-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8387f-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="8387f-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8387f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8387f-108">DESCRIPTION</span></span>
<span data-ttu-id="8387f-109">Polecenie cmdlet **New-AzMetricAlertRuleV2Criteria** tworzy lokalny obiekt kryteriów metrycznych, który ma być używany jako polecenie cmdlet [Add-AzMetricAlertRuleV2,](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) co tworzy nową metryczną regułę alertu.</span><span class="sxs-lookup"><span data-stu-id="8387f-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="8387f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8387f-110">EXAMPLES</span></span>

### <span data-ttu-id="8387f-111">Przykład 1. Tworzenie prostych kryteriów alertów metrycznych</span><span class="sxs-lookup"><span data-stu-id="8387f-111">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="8387f-112">To polecenie tworzy proste kryteria alertów metrycznych, które mogą być używane w metryce alertu</span><span class="sxs-lookup"><span data-stu-id="8387f-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="8387f-113">Przykład 2. Tworzenie dynamicznych kryteriów alertów metrycznych</span><span class="sxs-lookup"><span data-stu-id="8387f-113">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="8387f-114">To polecenie tworzy kryteria alertu dynamicznego metryczna, które mogą być używane w metryce alertu</span><span class="sxs-lookup"><span data-stu-id="8387f-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="8387f-115">Przykład 3. Tworzenie bardziej złożonych kryteriów alertów metrycznych</span><span class="sxs-lookup"><span data-stu-id="8387f-115">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="8387f-116">Ten zestaw poleceń tworzy bardziej złożone kryteria metrycznych alertów, które obejmują wybór wymiarów</span><span class="sxs-lookup"><span data-stu-id="8387f-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="8387f-117">Przykład 4. Tworzenie kryteriów dostępności testów sieci Web</span><span class="sxs-lookup"><span data-stu-id="8387f-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="8387f-118">To polecenie tworzy kryteria dostępności testów sieci Web, które mogą być używane w metryczna reguła alertu</span><span class="sxs-lookup"><span data-stu-id="8387f-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="8387f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8387f-119">PARAMETERS</span></span>

### <span data-ttu-id="8387f-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="8387f-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="8387f-121">Identyfikator zasobu szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8387f-121">The Application Insights resource Id.</span></span>

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

### <span data-ttu-id="8387f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8387f-122">-DefaultProfile</span></span>
<span data-ttu-id="8387f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8387f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8387f-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="8387f-124">-DimensionSelection</span></span>
<span data-ttu-id="8387f-125">Lista warunków wymiaru</span><span class="sxs-lookup"><span data-stu-id="8387f-125">List of dimension conditions</span></span>

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

### <span data-ttu-id="8387f-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="8387f-126">-DynamicThreshold</span></span>
<span data-ttu-id="8387f-127">Parametr przełącznika do używania dynamicznego typu progowego</span><span class="sxs-lookup"><span data-stu-id="8387f-127">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="8387f-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="8387f-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="8387f-129">Łączna liczba zbadanych punktów</span><span class="sxs-lookup"><span data-stu-id="8387f-129">The Total number of examined points</span></span>

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

### <span data-ttu-id="8387f-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="8387f-130">-FailedLocationCount</span></span>
<span data-ttu-id="8387f-131">Minimalna liczba lokalizacji, w których nie można podnieść alertu.</span><span class="sxs-lookup"><span data-stu-id="8387f-131">The minimum number of failed locations to raise an alert.</span></span>

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

### <span data-ttu-id="8387f-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="8387f-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="8387f-133">Parametr IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="8387f-133">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="8387f-134">-MetricName</span><span class="sxs-lookup"><span data-stu-id="8387f-134">-MetricName</span></span>
<span data-ttu-id="8387f-135">Nazwa metryki reguły</span><span class="sxs-lookup"><span data-stu-id="8387f-135">The metric name for rule</span></span>

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

### <span data-ttu-id="8387f-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="8387f-136">-MetricNamespace</span></span>
<span data-ttu-id="8387f-137">Przestrzeń nazw metryki</span><span class="sxs-lookup"><span data-stu-id="8387f-137">The Namespace of the metric</span></span>

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

### <span data-ttu-id="8387f-138">-Operator</span><span class="sxs-lookup"><span data-stu-id="8387f-138">-Operator</span></span>
<span data-ttu-id="8387f-139">Operator warunku reguły</span><span class="sxs-lookup"><span data-stu-id="8387f-139">The rule condition operator</span></span>

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

### <span data-ttu-id="8387f-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="8387f-140">-SkipMetricValidation</span></span>
<span data-ttu-id="8387f-141">Umożliwia utworzenie reguły alertu na metryki niestandardowej, która nie została jeszcze pominięta, co powoduje pominięcie sprawdzania poprawności metryki</span><span class="sxs-lookup"><span data-stu-id="8387f-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

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

### <span data-ttu-id="8387f-142">— próg</span><span class="sxs-lookup"><span data-stu-id="8387f-142">-Threshold</span></span>
<span data-ttu-id="8387f-143">Próg warunku reguły</span><span class="sxs-lookup"><span data-stu-id="8387f-143">The threshold for rule condition</span></span>

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

### <span data-ttu-id="8387f-144">- ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="8387f-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="8387f-145">Czułość warunku reguły</span><span class="sxs-lookup"><span data-stu-id="8387f-145">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="8387f-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="8387f-146">-TimeAggregation</span></span>
<span data-ttu-id="8387f-147">Operacja agregacji używana do rzutowania wielu metrycznych wartości w interwale okna</span><span class="sxs-lookup"><span data-stu-id="8387f-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

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

### <span data-ttu-id="8387f-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="8387f-148">-ViolationCount</span></span>
<span data-ttu-id="8387f-149">Minimalna liczba naruszeń wymaganych w wybranym oknie czasu wyszukiwania wymaganym do podnieść alert</span><span class="sxs-lookup"><span data-stu-id="8387f-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="8387f-150">— WebTest</span><span class="sxs-lookup"><span data-stu-id="8387f-150">-WebTest</span></span>
<span data-ttu-id="8387f-151">Switch parameter for using availability criteria Type</span><span class="sxs-lookup"><span data-stu-id="8387f-151">Switch parameter for using availability criteria Type</span></span>

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

### <span data-ttu-id="8387f-152">-WebTestId</span><span class="sxs-lookup"><span data-stu-id="8387f-152">-WebTestId</span></span>
<span data-ttu-id="8387f-153">Identyfikator testu sieci Web szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8387f-153">The Application Insights web test Id.</span></span>

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

### <span data-ttu-id="8387f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8387f-154">CommonParameters</span></span>
<span data-ttu-id="8387f-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8387f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8387f-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8387f-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8387f-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8387f-157">INPUTS</span></span>

### <span data-ttu-id="8387f-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span><span class="sxs-lookup"><span data-stu-id="8387f-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="8387f-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8387f-159">OUTPUTS</span></span>

### <span data-ttu-id="8387f-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="8387f-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="8387f-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8387f-161">NOTES</span></span>

## <span data-ttu-id="8387f-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8387f-162">RELATED LINKS</span></span>
