---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: 5addf4bae7024d86b6a517a40a4033992047fe08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546604"
---
# <span data-ttu-id="7eb11-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="7eb11-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="7eb11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7eb11-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb11-103">Umożliwia utworzenie reguły skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="7eb11-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eb11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7eb11-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7eb11-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7eb11-105">DESCRIPTION</span></span>
<span data-ttu-id="7eb11-106">Polecenie cmdlet **New-AzureRmAutoscaleRule** umożliwia utworzenie reguły skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="7eb11-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="7eb11-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7eb11-107">EXAMPLES</span></span>

### <span data-ttu-id="7eb11-108">Przykład 1. Tworzenie reguły</span><span class="sxs-lookup"><span data-stu-id="7eb11-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="7eb11-109">To polecenie powoduje utworzenie reguły.</span><span class="sxs-lookup"><span data-stu-id="7eb11-109">This command creates a rule.</span></span>

### <span data-ttu-id="7eb11-110">Przykład 2: tworzenie dwóch reguł</span><span class="sxs-lookup"><span data-stu-id="7eb11-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="7eb11-111">Pierwsze polecenie tworzy regułę dla metryki Request, a następnie zapisuje ją w zmiennej $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="7eb11-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="7eb11-112">Drugie polecenie tworzy drugą regułę dla metryki Request, a następnie zapisuje ją w zmiennej $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="7eb11-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="7eb11-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7eb11-113">PARAMETERS</span></span>

### <span data-ttu-id="7eb11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb11-114">-DefaultProfile</span></span>
<span data-ttu-id="7eb11-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7eb11-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb11-116">-Metricname</span><span class="sxs-lookup"><span data-stu-id="7eb11-116">-MetricName</span></span>
<span data-ttu-id="7eb11-117">Określa nazwę metryki.</span><span class="sxs-lookup"><span data-stu-id="7eb11-117">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="7eb11-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="7eb11-118">-MetricResourceId</span></span>
<span data-ttu-id="7eb11-119">Określa identyfikator zasobu metryki.</span><span class="sxs-lookup"><span data-stu-id="7eb11-119">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="7eb11-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="7eb11-120">-MetricStatistic</span></span>
<span data-ttu-id="7eb11-121">Określa statystykę metryki.</span><span class="sxs-lookup"><span data-stu-id="7eb11-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="7eb11-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7eb11-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7eb11-123">Ze</span><span class="sxs-lookup"><span data-stu-id="7eb11-123">Average</span></span>
- <span data-ttu-id="7eb11-124">Wznowion</span><span class="sxs-lookup"><span data-stu-id="7eb11-124">Min</span></span>
- <span data-ttu-id="7eb11-125">Liczba</span><span class="sxs-lookup"><span data-stu-id="7eb11-125">Max</span></span>
- <span data-ttu-id="7eb11-126">Zryczałtowanej</span><span class="sxs-lookup"><span data-stu-id="7eb11-126">Sum</span></span>

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

### <span data-ttu-id="7eb11-127">-Operator</span><span class="sxs-lookup"><span data-stu-id="7eb11-127">-Operator</span></span>
<span data-ttu-id="7eb11-128">Określa operator.</span><span class="sxs-lookup"><span data-stu-id="7eb11-128">Specifies the operator.</span></span>
<span data-ttu-id="7eb11-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7eb11-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7eb11-130">Wystawc</span><span class="sxs-lookup"><span data-stu-id="7eb11-130">Equals</span></span>
- <span data-ttu-id="7eb11-131">NotEquals</span><span class="sxs-lookup"><span data-stu-id="7eb11-131">NotEquals</span></span>
- <span data-ttu-id="7eb11-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="7eb11-132">GreaterThan</span></span>
- <span data-ttu-id="7eb11-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="7eb11-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="7eb11-134">LessThan</span><span class="sxs-lookup"><span data-stu-id="7eb11-134">LessThan</span></span>
- <span data-ttu-id="7eb11-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="7eb11-135">LessThanOrEqual</span></span>

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

### <span data-ttu-id="7eb11-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="7eb11-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="7eb11-137">Umożliwia określenie akcji Autoskalowanie cooldown czasu.</span><span class="sxs-lookup"><span data-stu-id="7eb11-137">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="7eb11-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="7eb11-138">-ScaleActionDirection</span></span>
<span data-ttu-id="7eb11-139">Określa kierunek działania skali.</span><span class="sxs-lookup"><span data-stu-id="7eb11-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="7eb11-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7eb11-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7eb11-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7eb11-141">None</span></span>
- <span data-ttu-id="7eb11-142">Dwyżek</span><span class="sxs-lookup"><span data-stu-id="7eb11-142">Increase</span></span>
- <span data-ttu-id="7eb11-143">Zmniejsz</span><span class="sxs-lookup"><span data-stu-id="7eb11-143">Decrease</span></span>

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

### <span data-ttu-id="7eb11-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="7eb11-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="7eb11-145">Określa typ skali.</span><span class="sxs-lookup"><span data-stu-id="7eb11-145">Specifies the scale type.</span></span>
<span data-ttu-id="7eb11-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7eb11-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7eb11-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="7eb11-147">ChangeSize</span></span>
- <span data-ttu-id="7eb11-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="7eb11-148">ChangeCount</span></span>
- <span data-ttu-id="7eb11-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="7eb11-149">PercentChangeCount</span></span>
- <span data-ttu-id="7eb11-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="7eb11-150">ExactCount</span></span>

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

### <span data-ttu-id="7eb11-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="7eb11-151">-ScaleActionValue</span></span>
<span data-ttu-id="7eb11-152">Określa wartość akcji.</span><span class="sxs-lookup"><span data-stu-id="7eb11-152">Specifies the action value.</span></span>

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

### <span data-ttu-id="7eb11-153">-Próg</span><span class="sxs-lookup"><span data-stu-id="7eb11-153">-Threshold</span></span>
<span data-ttu-id="7eb11-154">Określa próg wartości metryki.</span><span class="sxs-lookup"><span data-stu-id="7eb11-154">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="7eb11-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="7eb11-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="7eb11-156">Określa operator agregacji czasu.</span><span class="sxs-lookup"><span data-stu-id="7eb11-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="7eb11-157">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7eb11-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7eb11-158">Ze</span><span class="sxs-lookup"><span data-stu-id="7eb11-158">Average</span></span>
- <span data-ttu-id="7eb11-159">Najmniejszy</span><span class="sxs-lookup"><span data-stu-id="7eb11-159">Minimum</span></span>
- <span data-ttu-id="7eb11-160">Maksymalna</span><span class="sxs-lookup"><span data-stu-id="7eb11-160">Maximum</span></span>
- <span data-ttu-id="7eb11-161">Końcu</span><span class="sxs-lookup"><span data-stu-id="7eb11-161">Last</span></span>
- <span data-ttu-id="7eb11-162">Suma, liczba</span><span class="sxs-lookup"><span data-stu-id="7eb11-162">Total, Count</span></span>

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

### <span data-ttu-id="7eb11-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="7eb11-163">-TimeGrain</span></span>
<span data-ttu-id="7eb11-164">Określa ziarno czasu.</span><span class="sxs-lookup"><span data-stu-id="7eb11-164">Specifies the time grain.</span></span>

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

### <span data-ttu-id="7eb11-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="7eb11-165">-TimeWindow</span></span>
<span data-ttu-id="7eb11-166">Określa okno czasu.</span><span class="sxs-lookup"><span data-stu-id="7eb11-166">Specifies the time window.</span></span>

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

### <span data-ttu-id="7eb11-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb11-167">CommonParameters</span></span>
<span data-ttu-id="7eb11-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eb11-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb11-169">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eb11-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb11-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7eb11-170">INPUTS</span></span>

### <span data-ttu-id="7eb11-171">System. String</span><span class="sxs-lookup"><span data-stu-id="7eb11-171">System.String</span></span>

### <span data-ttu-id="7eb11-172">Microsoft. Azure. Management. Monitor. Management. models. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="7eb11-172">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="7eb11-173">Microsoft. Azure. Management. Monitor. Management. models. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="7eb11-173">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="7eb11-174">System. Double</span><span class="sxs-lookup"><span data-stu-id="7eb11-174">System.Double</span></span>

### <span data-ttu-id="7eb11-175">Microsoft. Azure. Management. Monitor. Management. models. TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="7eb11-175">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="7eb11-176">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="7eb11-176">System.TimeSpan</span></span>

### <span data-ttu-id="7eb11-177">Microsoft. Azure. Management. Monitor. Management. models. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="7eb11-177">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="7eb11-178">Microsoft. Azure. Management. Monitor. Management. models. Scale.</span><span class="sxs-lookup"><span data-stu-id="7eb11-178">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="7eb11-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7eb11-179">OUTPUTS</span></span>

### <span data-ttu-id="7eb11-180">Microsoft. Azure. Management. Monitor. Management. models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="7eb11-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="7eb11-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7eb11-181">NOTES</span></span>

## <span data-ttu-id="7eb11-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7eb11-182">RELATED LINKS</span></span>

[<span data-ttu-id="7eb11-183">Dodaj-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7eb11-183">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="7eb11-184">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="7eb11-184">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="7eb11-185">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7eb11-185">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="7eb11-186">Nowe — AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="7eb11-186">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="7eb11-187">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7eb11-187">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


