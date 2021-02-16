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
# New-AzMetricAlertRuleV2Criteria

## SYNOPSIS
Tworzy obiekt kryteriów lokalnych, za pomocą których można utworzyć nowy alert metryczny.

## SKŁADNIA

### StaticThresholdParameterSet (domyślne)
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DynamicThresholdParameterSet
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WebtestParameterSet
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **New-AzMetricAlertRuleV2Criteria** tworzy lokalny obiekt kryteriów metrycznych, który ma być używany jako polecenie cmdlet [Add-AzMetricAlertRuleV2,](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) co tworzy nową metryczną regułę alertu.

## PRZYKŁADY

### Przykład 1. Tworzenie prostych kryteriów alertów metrycznych

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

To polecenie tworzy proste kryteria alertów metrycznych, które mogą być używane w metryce alertu

### Przykład 2. Tworzenie dynamicznych kryteriów alertów metrycznych

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

To polecenie tworzy kryteria alertu dynamicznego metryczna, które mogą być używane w metryce alertu

### Przykład 3. Tworzenie bardziej złożonych kryteriów alertów metrycznych

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

Ten zestaw poleceń tworzy bardziej złożone kryteria metrycznych alertów, które obejmują wybór wymiarów

### Przykład 4. Tworzenie kryteriów dostępności testów sieci Web

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

To polecenie tworzy kryteria dostępności testów sieci Web, które mogą być używane w metryczna reguła alertu

## PARAMETERS

### -ApplicationInsightsId
Identyfikator zasobu szczegółowych informacji aplikacji.

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### -DimensionSelection
Lista warunków wymiaru

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

### -DynamicThreshold
Parametr przełącznika do używania dynamicznego typu progowego

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

### -ExaminedAggregatedPointCount
Łączna liczba zbadanych punktów

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

### -FailedLocationCount
Minimalna liczba lokalizacji, w których nie można podnieść alertu.

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

### -IgnoreDataBefore
Parametr IgnoreDataBefore

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

### -MetricName
Nazwa metryki reguły

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

### -MetricNamespace
Przestrzeń nazw metryki

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

### -Operator
Operator warunku reguły

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

### -SkipMetricValidation
Umożliwia utworzenie reguły alertu na metryki niestandardowej, która nie została jeszcze pominięta, co powoduje pominięcie sprawdzania poprawności metryki

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

### — próg
Próg warunku reguły

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

### - ThresholdSensitivity
Czułość warunku reguły

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

### -TimeAggregation
Operacja agregacji używana do rzutowania wielu metrycznych wartości w interwale okna

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

### -ViolationCount
Minimalna liczba naruszeń wymaganych w wybranym oknie czasu wyszukiwania wymaganym do podnieść alert

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

### — WebTest
Switch parameter for using availability criteria Type

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

### -WebTestId
Identyfikator testu sieci Web szczegółowych informacji aplikacji.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]

## OUTPUTS

### Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria

## NOTATKI

## LINKI POKREWNE
