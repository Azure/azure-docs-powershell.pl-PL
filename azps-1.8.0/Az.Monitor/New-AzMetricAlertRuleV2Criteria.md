---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 16687824216fa0014d59b78a96d22a4da8a19fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867263"
---
# <span data-ttu-id="d7475-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d7475-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="d7475-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7475-102">SYNOPSIS</span></span>
<span data-ttu-id="d7475-103">Tworzy obiekt Local kryteria, za pomocą którego można utworzyć nowy Alert metryki</span><span class="sxs-lookup"><span data-stu-id="d7475-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="d7475-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7475-104">SYNTAX</span></span>

### <span data-ttu-id="d7475-105">StaticThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7475-105">StaticThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7475-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7475-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 -DynamicThreshold <String> [-Sensitivity <String>] [-FailingPeriod <Int32>] [-TotalPeriod <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7475-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d7475-107">DESCRIPTION</span></span>
<span data-ttu-id="d7475-108">Polecenie cmdlet **New-AzMetricAlertRuleV2Criteria** tworzy obiekt Local Metric kryteriów, który ma być wykorzystywany jako wejściowy polecenie cmdlet Add-AzMetricAlertRuleV2, który tworzy nową regułę alertu metryki.</span><span class="sxs-lookup"><span data-stu-id="d7475-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="d7475-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7475-109">EXAMPLES</span></span>

### <span data-ttu-id="d7475-110">Przykład 1. Tworzenie prostych kryteriów alertów metrycznych</span><span class="sxs-lookup"><span data-stu-id="d7475-110">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 5
Dimensions           :
AdditionalProperties :
```

<span data-ttu-id="d7475-111">To polecenie tworzy proste kryteria alertu metryki, które mogą być używane w regule alertu metryki</span><span class="sxs-lookup"><span data-stu-id="d7475-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="d7475-112">Przykład 2: tworzenie bardziej złożonych kryteriów alertów metrycznych</span><span class="sxs-lookup"><span data-stu-id="d7475-112">Example 2: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 2
Dimensions           : {availabilityResult/name}
AdditionalProperties :
```

<span data-ttu-id="d7475-113">Ten zestaw poleceń tworzy bardziej złożone kryteria alertów metryki, które zawierają zaznaczenie wymiarów.</span><span class="sxs-lookup"><span data-stu-id="d7475-113">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="d7475-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7475-114">PARAMETERS</span></span>

### <span data-ttu-id="d7475-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7475-115">-DefaultProfile</span></span>
<span data-ttu-id="d7475-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7475-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7475-117">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d7475-117">-DimensionSelection</span></span>
<span data-ttu-id="d7475-118">Lista warunków wymiaru</span><span class="sxs-lookup"><span data-stu-id="d7475-118">List of dimension conditions</span></span>

```yaml
Type: PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7475-119">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="d7475-119">-DynamicThreshold</span></span>
<span data-ttu-id="d7475-120">Próg dynamiczny dla warunku reguły</span><span class="sxs-lookup"><span data-stu-id="d7475-120">The Dynamic Threshold for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7475-121">-FailingPeriod</span><span class="sxs-lookup"><span data-stu-id="d7475-121">-FailingPeriod</span></span>
<span data-ttu-id="d7475-122">Okres niepowodzeń reguły</span><span class="sxs-lookup"><span data-stu-id="d7475-122">The Failing Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7475-123">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="d7475-123">-IgnoreDataBefore</span></span>
<span data-ttu-id="d7475-124">Parametr IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="d7475-124">The IgnoreDataBefore parameter</span></span>

```yaml
Type: DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7475-125">-Metricname</span><span class="sxs-lookup"><span data-stu-id="d7475-125">-MetricName</span></span>
<span data-ttu-id="d7475-126">Nazwa metryki dla reguły</span><span class="sxs-lookup"><span data-stu-id="d7475-126">The metric name for rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7475-127">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="d7475-127">-MetricNamespace</span></span>
<span data-ttu-id="d7475-128">Obszar nazw metryki</span><span class="sxs-lookup"><span data-stu-id="d7475-128">The Namespace of the metric</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7475-129">-Operator</span><span class="sxs-lookup"><span data-stu-id="d7475-129">-Operator</span></span>
<span data-ttu-id="d7475-130">Operator warunku reguły</span><span class="sxs-lookup"><span data-stu-id="d7475-130">The rule condition operator</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7475-131">-Czułość</span><span class="sxs-lookup"><span data-stu-id="d7475-131">-Sensitivity</span></span>
<span data-ttu-id="d7475-132">Czułość na warunek reguły</span><span class="sxs-lookup"><span data-stu-id="d7475-132">The sensitivity for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7475-133">-Próg</span><span class="sxs-lookup"><span data-stu-id="d7475-133">-Threshold</span></span>
<span data-ttu-id="d7475-134">Próg warunku reguły</span><span class="sxs-lookup"><span data-stu-id="d7475-134">The threshold for rule condition</span></span>

```yaml
Type: Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7475-135">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="d7475-135">-TimeAggregation</span></span>
<span data-ttu-id="d7475-136">Operacja agregacji używana do rzutowania wielu wartości metrycznych w interwale okien</span><span class="sxs-lookup"><span data-stu-id="d7475-136">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7475-137">-TotalPeriod</span><span class="sxs-lookup"><span data-stu-id="d7475-137">-TotalPeriod</span></span>
<span data-ttu-id="d7475-138">Całkowity okres dla warunku reguły</span><span class="sxs-lookup"><span data-stu-id="d7475-138">The Total Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7475-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7475-139">CommonParameters</span></span>
<span data-ttu-id="d7475-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7475-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d7475-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7475-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7475-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7475-142">INPUTS</span></span>

### <span data-ttu-id="d7475-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="d7475-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="d7475-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7475-144">OUTPUTS</span></span>

### <span data-ttu-id="d7475-145">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="d7475-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria</span></span>

## <span data-ttu-id="d7475-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7475-146">NOTES</span></span>

## <span data-ttu-id="d7475-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7475-147">RELATED LINKS</span></span>
