---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: cd4e374909fa58f036a0f67cd7a89bb968defd71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203462"
---
# <span data-ttu-id="26b36-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="26b36-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="26b36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26b36-102">SYNOPSIS</span></span>
<span data-ttu-id="26b36-103">Tworzy regułę skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="26b36-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="26b36-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="26b36-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26b36-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="26b36-105">DESCRIPTION</span></span>
<span data-ttu-id="26b36-106">Polecenie **cmdlet New-AzAutoscaleRule** tworzy regułę skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="26b36-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="26b36-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="26b36-107">EXAMPLES</span></span>

### <span data-ttu-id="26b36-108">Przykład 1. Tworzenie reguły</span><span class="sxs-lookup"><span data-stu-id="26b36-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="26b36-109">To polecenie tworzy regułę.</span><span class="sxs-lookup"><span data-stu-id="26b36-109">This command creates a rule.</span></span>

### <span data-ttu-id="26b36-110">Przykład 2. Tworzenie dwóch reguł</span><span class="sxs-lookup"><span data-stu-id="26b36-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="26b36-111">Pierwsze polecenie tworzy regułę dla metryki Żądania, a następnie przechowuje ją w zmiennej $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="26b36-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="26b36-112">Drugie polecenie tworzy drugą regułę dla metryki Żądania, a następnie przechowuje ją w zmiennej $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="26b36-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="26b36-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="26b36-113">Example 3</span></span>

<span data-ttu-id="26b36-114">Tworzy regułę skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="26b36-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="26b36-115">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="26b36-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="26b36-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26b36-116">PARAMETERS</span></span>

### <span data-ttu-id="26b36-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b36-117">-DefaultProfile</span></span>
<span data-ttu-id="26b36-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="26b36-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26b36-119">-MetricName</span><span class="sxs-lookup"><span data-stu-id="26b36-119">-MetricName</span></span>
<span data-ttu-id="26b36-120">Określa nazwę metryki.</span><span class="sxs-lookup"><span data-stu-id="26b36-120">Specifies the name of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b36-121">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="26b36-121">-MetricResourceId</span></span>
<span data-ttu-id="26b36-122">Określa metryyczny identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="26b36-122">Specifies the metric resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b36-123">- MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="26b36-123">-MetricStatistic</span></span>
<span data-ttu-id="26b36-124">Określa statystykę metryki.</span><span class="sxs-lookup"><span data-stu-id="26b36-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="26b36-125">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="26b36-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26b36-126">Średnia</span><span class="sxs-lookup"><span data-stu-id="26b36-126">Average</span></span>
- <span data-ttu-id="26b36-127">Minimum</span><span class="sxs-lookup"><span data-stu-id="26b36-127">Min</span></span>
- <span data-ttu-id="26b36-128">Maksimum</span><span class="sxs-lookup"><span data-stu-id="26b36-128">Max</span></span>
- <span data-ttu-id="26b36-129">Suma</span><span class="sxs-lookup"><span data-stu-id="26b36-129">Sum</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType
Parameter Sets: (All)
Aliases:
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b36-130">-Operator</span><span class="sxs-lookup"><span data-stu-id="26b36-130">-Operator</span></span>
<span data-ttu-id="26b36-131">Określa operator.</span><span class="sxs-lookup"><span data-stu-id="26b36-131">Specifies the operator.</span></span>
<span data-ttu-id="26b36-132">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="26b36-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26b36-133">Równa się</span><span class="sxs-lookup"><span data-stu-id="26b36-133">Equals</span></span>
- <span data-ttu-id="26b36-134">Nierówne</span><span class="sxs-lookup"><span data-stu-id="26b36-134">NotEquals</span></span>
- <span data-ttu-id="26b36-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="26b36-135">GreaterThan</span></span>
- <span data-ttu-id="26b36-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="26b36-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="26b36-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="26b36-137">LessThan</span></span>
- <span data-ttu-id="26b36-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="26b36-138">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType
Parameter Sets: (All)
Aliases:
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b36-139">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="26b36-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="26b36-140">Określa czas odnowienia akcji autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="26b36-140">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b36-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="26b36-141">-ScaleActionDirection</span></span>
<span data-ttu-id="26b36-142">Określa kierunek akcji skalowania.</span><span class="sxs-lookup"><span data-stu-id="26b36-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="26b36-143">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="26b36-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26b36-144">Brak</span><span class="sxs-lookup"><span data-stu-id="26b36-144">None</span></span>
- <span data-ttu-id="26b36-145">Zwiększ</span><span class="sxs-lookup"><span data-stu-id="26b36-145">Increase</span></span>
- <span data-ttu-id="26b36-146">Zmniejszanie</span><span class="sxs-lookup"><span data-stu-id="26b36-146">Decrease</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection
Parameter Sets: (All)
Aliases:
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b36-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="26b36-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="26b36-148">Określa typ skali.</span><span class="sxs-lookup"><span data-stu-id="26b36-148">Specifies the scale type.</span></span>
<span data-ttu-id="26b36-149">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="26b36-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26b36-150">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="26b36-150">ChangeSize</span></span>
- <span data-ttu-id="26b36-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="26b36-151">ChangeCount</span></span>
- <span data-ttu-id="26b36-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="26b36-152">PercentChangeCount</span></span>
- <span data-ttu-id="26b36-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="26b36-153">ExactCount</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleType
Parameter Sets: (All)
Aliases:
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b36-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="26b36-154">-ScaleActionValue</span></span>
<span data-ttu-id="26b36-155">Określa wartość akcji.</span><span class="sxs-lookup"><span data-stu-id="26b36-155">Specifies the action value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b36-156">— próg</span><span class="sxs-lookup"><span data-stu-id="26b36-156">-Threshold</span></span>
<span data-ttu-id="26b36-157">Określa próg wartości metryczne.</span><span class="sxs-lookup"><span data-stu-id="26b36-157">Specifies the threshold of the metric value.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b36-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="26b36-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="26b36-159">Określa operator agregacji czasu.</span><span class="sxs-lookup"><span data-stu-id="26b36-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="26b36-160">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="26b36-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26b36-161">Średnia</span><span class="sxs-lookup"><span data-stu-id="26b36-161">Average</span></span>
- <span data-ttu-id="26b36-162">Minimum</span><span class="sxs-lookup"><span data-stu-id="26b36-162">Minimum</span></span>
- <span data-ttu-id="26b36-163">Maksimum</span><span class="sxs-lookup"><span data-stu-id="26b36-163">Maximum</span></span>
- <span data-ttu-id="26b36-164">Ostatnie</span><span class="sxs-lookup"><span data-stu-id="26b36-164">Last</span></span>
- <span data-ttu-id="26b36-165">Suma, Licznik</span><span class="sxs-lookup"><span data-stu-id="26b36-165">Total, Count</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType
Parameter Sets: (All)
Aliases:
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b36-166">- TimeGrain</span><span class="sxs-lookup"><span data-stu-id="26b36-166">-TimeGrain</span></span>
<span data-ttu-id="26b36-167">Określa wielkość czasu.</span><span class="sxs-lookup"><span data-stu-id="26b36-167">Specifies the time grain.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b36-168">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="26b36-168">-TimeWindow</span></span>
<span data-ttu-id="26b36-169">Określa okres.</span><span class="sxs-lookup"><span data-stu-id="26b36-169">Specifies the time window.</span></span>

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

### <span data-ttu-id="26b36-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b36-170">CommonParameters</span></span>
<span data-ttu-id="26b36-171">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b36-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b36-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26b36-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b36-173">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26b36-173">INPUTS</span></span>

### <span data-ttu-id="26b36-174">System.String</span><span class="sxs-lookup"><span data-stu-id="26b36-174">System.String</span></span>

### <span data-ttu-id="26b36-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="26b36-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="26b36-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="26b36-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="26b36-177">System.Double</span><span class="sxs-lookup"><span data-stu-id="26b36-177">System.Double</span></span>

### <span data-ttu-id="26b36-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="26b36-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="26b36-179">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="26b36-179">System.TimeSpan</span></span>

### <span data-ttu-id="26b36-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="26b36-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="26b36-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span><span class="sxs-lookup"><span data-stu-id="26b36-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="26b36-182">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26b36-182">OUTPUTS</span></span>

### <span data-ttu-id="26b36-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span><span class="sxs-lookup"><span data-stu-id="26b36-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="26b36-184">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="26b36-184">NOTES</span></span>

## <span data-ttu-id="26b36-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26b36-185">RELATED LINKS</span></span>

[<span data-ttu-id="26b36-186">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="26b36-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="26b36-187">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="26b36-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="26b36-188">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="26b36-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="26b36-189">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="26b36-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="26b36-190">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="26b36-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


