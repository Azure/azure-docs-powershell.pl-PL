---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: ac588fe9a82209cfd56c08f750fcd35945bc8af1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891137"
---
# <span data-ttu-id="6c013-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="6c013-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="6c013-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c013-102">SYNOPSIS</span></span>
<span data-ttu-id="6c013-103">Umożliwia utworzenie reguły skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="6c013-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="6c013-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c013-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c013-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6c013-105">DESCRIPTION</span></span>
<span data-ttu-id="6c013-106">Polecenie cmdlet **New-AzAutoscaleRule** umożliwia utworzenie reguły skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="6c013-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="6c013-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c013-107">EXAMPLES</span></span>

### <span data-ttu-id="6c013-108">Przykład 1. Tworzenie reguły</span><span class="sxs-lookup"><span data-stu-id="6c013-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="6c013-109">To polecenie powoduje utworzenie reguły.</span><span class="sxs-lookup"><span data-stu-id="6c013-109">This command creates a rule.</span></span>

### <span data-ttu-id="6c013-110">Przykład 2: tworzenie dwóch reguł</span><span class="sxs-lookup"><span data-stu-id="6c013-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="6c013-111">Pierwsze polecenie tworzy regułę dla metryki Request, a następnie zapisuje ją w zmiennej $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="6c013-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="6c013-112">Drugie polecenie tworzy drugą regułę dla metryki Request, a następnie zapisuje ją w zmiennej $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="6c013-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="6c013-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c013-113">PARAMETERS</span></span>

### <span data-ttu-id="6c013-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c013-114">-DefaultProfile</span></span>
<span data-ttu-id="6c013-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6c013-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c013-116">-Metricname</span><span class="sxs-lookup"><span data-stu-id="6c013-116">-MetricName</span></span>
<span data-ttu-id="6c013-117">Określa nazwę metryki.</span><span class="sxs-lookup"><span data-stu-id="6c013-117">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="6c013-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="6c013-118">-MetricResourceId</span></span>
<span data-ttu-id="6c013-119">Określa identyfikator zasobu metryki.</span><span class="sxs-lookup"><span data-stu-id="6c013-119">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="6c013-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="6c013-120">-MetricStatistic</span></span>
<span data-ttu-id="6c013-121">Określa statystykę metryki.</span><span class="sxs-lookup"><span data-stu-id="6c013-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="6c013-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6c013-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6c013-123">Ze</span><span class="sxs-lookup"><span data-stu-id="6c013-123">Average</span></span>
- <span data-ttu-id="6c013-124">Wznowion</span><span class="sxs-lookup"><span data-stu-id="6c013-124">Min</span></span>
- <span data-ttu-id="6c013-125">Liczba</span><span class="sxs-lookup"><span data-stu-id="6c013-125">Max</span></span>
- <span data-ttu-id="6c013-126">Zryczałtowanej</span><span class="sxs-lookup"><span data-stu-id="6c013-126">Sum</span></span>

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

### <span data-ttu-id="6c013-127">-Operator</span><span class="sxs-lookup"><span data-stu-id="6c013-127">-Operator</span></span>
<span data-ttu-id="6c013-128">Określa operator.</span><span class="sxs-lookup"><span data-stu-id="6c013-128">Specifies the operator.</span></span>
<span data-ttu-id="6c013-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6c013-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6c013-130">Wystawc</span><span class="sxs-lookup"><span data-stu-id="6c013-130">Equals</span></span>
- <span data-ttu-id="6c013-131">NotEquals</span><span class="sxs-lookup"><span data-stu-id="6c013-131">NotEquals</span></span>
- <span data-ttu-id="6c013-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="6c013-132">GreaterThan</span></span>
- <span data-ttu-id="6c013-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="6c013-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="6c013-134">LessThan</span><span class="sxs-lookup"><span data-stu-id="6c013-134">LessThan</span></span>
- <span data-ttu-id="6c013-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="6c013-135">LessThanOrEqual</span></span>

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

### <span data-ttu-id="6c013-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="6c013-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="6c013-137">Umożliwia określenie akcji Autoskalowanie cooldown czasu.</span><span class="sxs-lookup"><span data-stu-id="6c013-137">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="6c013-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="6c013-138">-ScaleActionDirection</span></span>
<span data-ttu-id="6c013-139">Określa kierunek działania skali.</span><span class="sxs-lookup"><span data-stu-id="6c013-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="6c013-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6c013-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6c013-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6c013-141">None</span></span>
- <span data-ttu-id="6c013-142">Dwyżek</span><span class="sxs-lookup"><span data-stu-id="6c013-142">Increase</span></span>
- <span data-ttu-id="6c013-143">Zmniejsz</span><span class="sxs-lookup"><span data-stu-id="6c013-143">Decrease</span></span>

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

### <span data-ttu-id="6c013-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="6c013-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="6c013-145">Określa typ skali.</span><span class="sxs-lookup"><span data-stu-id="6c013-145">Specifies the scale type.</span></span>
<span data-ttu-id="6c013-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6c013-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6c013-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="6c013-147">ChangeSize</span></span>
- <span data-ttu-id="6c013-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="6c013-148">ChangeCount</span></span>
- <span data-ttu-id="6c013-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="6c013-149">PercentChangeCount</span></span>
- <span data-ttu-id="6c013-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="6c013-150">ExactCount</span></span>

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

### <span data-ttu-id="6c013-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="6c013-151">-ScaleActionValue</span></span>
<span data-ttu-id="6c013-152">Określa wartość akcji.</span><span class="sxs-lookup"><span data-stu-id="6c013-152">Specifies the action value.</span></span>

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

### <span data-ttu-id="6c013-153">-Próg</span><span class="sxs-lookup"><span data-stu-id="6c013-153">-Threshold</span></span>
<span data-ttu-id="6c013-154">Określa próg wartości metryki.</span><span class="sxs-lookup"><span data-stu-id="6c013-154">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="6c013-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="6c013-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="6c013-156">Określa operator agregacji czasu.</span><span class="sxs-lookup"><span data-stu-id="6c013-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="6c013-157">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6c013-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6c013-158">Ze</span><span class="sxs-lookup"><span data-stu-id="6c013-158">Average</span></span>
- <span data-ttu-id="6c013-159">Najmniejszy</span><span class="sxs-lookup"><span data-stu-id="6c013-159">Minimum</span></span>
- <span data-ttu-id="6c013-160">Maksymalna</span><span class="sxs-lookup"><span data-stu-id="6c013-160">Maximum</span></span>
- <span data-ttu-id="6c013-161">Końcu</span><span class="sxs-lookup"><span data-stu-id="6c013-161">Last</span></span>
- <span data-ttu-id="6c013-162">Suma, liczba</span><span class="sxs-lookup"><span data-stu-id="6c013-162">Total, Count</span></span>

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

### <span data-ttu-id="6c013-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="6c013-163">-TimeGrain</span></span>
<span data-ttu-id="6c013-164">Określa ziarno czasu.</span><span class="sxs-lookup"><span data-stu-id="6c013-164">Specifies the time grain.</span></span>

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

### <span data-ttu-id="6c013-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="6c013-165">-TimeWindow</span></span>
<span data-ttu-id="6c013-166">Określa okno czasu.</span><span class="sxs-lookup"><span data-stu-id="6c013-166">Specifies the time window.</span></span>

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

### <span data-ttu-id="6c013-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c013-167">CommonParameters</span></span>
<span data-ttu-id="6c013-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c013-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c013-169">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c013-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c013-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c013-170">INPUTS</span></span>

### <span data-ttu-id="6c013-171">System. String</span><span class="sxs-lookup"><span data-stu-id="6c013-171">System.String</span></span>

### <span data-ttu-id="6c013-172">Microsoft. Azure. Management. Monitor. Management. models. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="6c013-172">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="6c013-173">Microsoft. Azure. Management. Monitor. Management. models. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="6c013-173">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="6c013-174">System. Double</span><span class="sxs-lookup"><span data-stu-id="6c013-174">System.Double</span></span>

### <span data-ttu-id="6c013-175">Microsoft. Azure. Management. Monitor. Management. models. TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="6c013-175">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="6c013-176">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="6c013-176">System.TimeSpan</span></span>

### <span data-ttu-id="6c013-177">Microsoft. Azure. Management. Monitor. Management. models. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="6c013-177">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="6c013-178">Microsoft. Azure. Management. Monitor. Management. models. Scale.</span><span class="sxs-lookup"><span data-stu-id="6c013-178">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="6c013-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c013-179">OUTPUTS</span></span>

### <span data-ttu-id="6c013-180">Microsoft. Azure. Management. Monitor. Management. models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="6c013-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="6c013-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c013-181">NOTES</span></span>

## <span data-ttu-id="6c013-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c013-182">RELATED LINKS</span></span>

[<span data-ttu-id="6c013-183">Dodaj-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="6c013-183">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="6c013-184">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="6c013-184">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="6c013-185">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="6c013-185">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="6c013-186">Nowe — AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="6c013-186">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="6c013-187">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="6c013-187">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


