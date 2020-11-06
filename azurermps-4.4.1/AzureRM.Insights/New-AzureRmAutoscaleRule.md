---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: e6f157e199dedf6a7587f607cdd275183ec67c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553299"
---
# <span data-ttu-id="7b1a9-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="7b1a9-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="7b1a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b1a9-102">SYNOPSIS</span></span>
<span data-ttu-id="7b1a9-103">Umożliwia utworzenie reguły skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b1a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b1a9-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b1a9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7b1a9-105">DESCRIPTION</span></span>
<span data-ttu-id="7b1a9-106">Polecenie cmdlet **New-AzureRmAutoscaleRule** umożliwia utworzenie reguły skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="7b1a9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b1a9-107">EXAMPLES</span></span>

### <span data-ttu-id="7b1a9-108">Przykład 1. Tworzenie reguły</span><span class="sxs-lookup"><span data-stu-id="7b1a9-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="7b1a9-109">To polecenie powoduje utworzenie reguły.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-109">This command creates a rule.</span></span>

### <span data-ttu-id="7b1a9-110">Przykład 2: tworzenie dwóch reguł</span><span class="sxs-lookup"><span data-stu-id="7b1a9-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="7b1a9-111">Pierwsze polecenie tworzy regułę dla metryki Request, a następnie zapisuje ją w zmiennej $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="7b1a9-112">Drugie polecenie tworzy drugą regułę dla metryki Request, a następnie zapisuje ją w zmiennej $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="7b1a9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b1a9-113">PARAMETERS</span></span>

### <span data-ttu-id="7b1a9-114">-Metricname</span><span class="sxs-lookup"><span data-stu-id="7b1a9-114">-MetricName</span></span>
<span data-ttu-id="7b1a9-115">Określa nazwę metryki.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-115">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="7b1a9-116">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="7b1a9-116">-MetricResourceId</span></span>
<span data-ttu-id="7b1a9-117">Określa identyfikator zasobu metryki.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-117">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="7b1a9-118">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="7b1a9-118">-MetricStatistic</span></span>
<span data-ttu-id="7b1a9-119">Określa statystykę metryki.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-119">Specifies the metric statistic.</span></span>
<span data-ttu-id="7b1a9-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7b1a9-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b1a9-121">Ze</span><span class="sxs-lookup"><span data-stu-id="7b1a9-121">Average</span></span>
- <span data-ttu-id="7b1a9-122">Wznowion</span><span class="sxs-lookup"><span data-stu-id="7b1a9-122">Min</span></span>
- <span data-ttu-id="7b1a9-123">Liczba</span><span class="sxs-lookup"><span data-stu-id="7b1a9-123">Max</span></span>
- <span data-ttu-id="7b1a9-124">Zryczałtowanej</span><span class="sxs-lookup"><span data-stu-id="7b1a9-124">Sum</span></span>

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

### <span data-ttu-id="7b1a9-125">-Operator</span><span class="sxs-lookup"><span data-stu-id="7b1a9-125">-Operator</span></span>
<span data-ttu-id="7b1a9-126">Określa operator.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-126">Specifies the operator.</span></span>
<span data-ttu-id="7b1a9-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7b1a9-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b1a9-128">Wystawc</span><span class="sxs-lookup"><span data-stu-id="7b1a9-128">Equals</span></span>
- <span data-ttu-id="7b1a9-129">NotEquals</span><span class="sxs-lookup"><span data-stu-id="7b1a9-129">NotEquals</span></span>
- <span data-ttu-id="7b1a9-130">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="7b1a9-130">GreaterThan</span></span>
- <span data-ttu-id="7b1a9-131">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="7b1a9-131">GreaterThanOrEqual</span></span>
- <span data-ttu-id="7b1a9-132">LessThan</span><span class="sxs-lookup"><span data-stu-id="7b1a9-132">LessThan</span></span>
- <span data-ttu-id="7b1a9-133">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="7b1a9-133">LessThanOrEqual</span></span>

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

### <span data-ttu-id="7b1a9-134">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="7b1a9-134">-ScaleActionCooldown</span></span>
<span data-ttu-id="7b1a9-135">Umożliwia określenie akcji Autoskalowanie cooldown czasu.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-135">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="7b1a9-136">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="7b1a9-136">-ScaleActionDirection</span></span>
<span data-ttu-id="7b1a9-137">Określa kierunek działania skali.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-137">Specifies the scale action direction.</span></span>
<span data-ttu-id="7b1a9-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7b1a9-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b1a9-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7b1a9-139">None</span></span>
- <span data-ttu-id="7b1a9-140">Dwyżek</span><span class="sxs-lookup"><span data-stu-id="7b1a9-140">Increase</span></span>
- <span data-ttu-id="7b1a9-141">Zmniejsz</span><span class="sxs-lookup"><span data-stu-id="7b1a9-141">Decrease</span></span>

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

### <span data-ttu-id="7b1a9-142">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="7b1a9-142">-ScaleActionScaleType</span></span>
<span data-ttu-id="7b1a9-143">Określa typ skali.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-143">Specifies the scale type.</span></span>
<span data-ttu-id="7b1a9-144">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7b1a9-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b1a9-145">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="7b1a9-145">ChangeSize</span></span>
- <span data-ttu-id="7b1a9-146">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="7b1a9-146">ChangeCount</span></span>
- <span data-ttu-id="7b1a9-147">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="7b1a9-147">PercentChangeCount</span></span>
- <span data-ttu-id="7b1a9-148">ExactCount</span><span class="sxs-lookup"><span data-stu-id="7b1a9-148">ExactCount</span></span>

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

### <span data-ttu-id="7b1a9-149">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="7b1a9-149">-ScaleActionValue</span></span>
<span data-ttu-id="7b1a9-150">Określa wartość akcji.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-150">Specifies the action value.</span></span>

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

### <span data-ttu-id="7b1a9-151">-Próg</span><span class="sxs-lookup"><span data-stu-id="7b1a9-151">-Threshold</span></span>
<span data-ttu-id="7b1a9-152">Określa próg wartości metryki.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-152">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="7b1a9-153">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="7b1a9-153">-TimeAggregationOperator</span></span>
<span data-ttu-id="7b1a9-154">Określa operator agregacji czasu.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-154">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="7b1a9-155">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7b1a9-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b1a9-156">Ze</span><span class="sxs-lookup"><span data-stu-id="7b1a9-156">Average</span></span>
- <span data-ttu-id="7b1a9-157">Najmniejszy</span><span class="sxs-lookup"><span data-stu-id="7b1a9-157">Minimum</span></span>
- <span data-ttu-id="7b1a9-158">Maksymalna</span><span class="sxs-lookup"><span data-stu-id="7b1a9-158">Maximum</span></span>
- <span data-ttu-id="7b1a9-159">Końcu</span><span class="sxs-lookup"><span data-stu-id="7b1a9-159">Last</span></span>
- <span data-ttu-id="7b1a9-160">Suma, liczba</span><span class="sxs-lookup"><span data-stu-id="7b1a9-160">Total, Count</span></span>

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

### <span data-ttu-id="7b1a9-161">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="7b1a9-161">-TimeGrain</span></span>
<span data-ttu-id="7b1a9-162">Określa ziarno czasu.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-162">Specifies the time grain.</span></span>

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

### <span data-ttu-id="7b1a9-163">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="7b1a9-163">-TimeWindow</span></span>
<span data-ttu-id="7b1a9-164">Określa okno czasu.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-164">Specifies the time window.</span></span>

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

### <span data-ttu-id="7b1a9-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b1a9-165">-DefaultProfile</span></span>
<span data-ttu-id="7b1a9-166">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b1a9-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b1a9-167">CommonParameters</span></span>
<span data-ttu-id="7b1a9-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b1a9-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b1a9-169">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b1a9-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b1a9-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b1a9-170">INPUTS</span></span>

## <span data-ttu-id="7b1a9-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b1a9-171">OUTPUTS</span></span>

### <span data-ttu-id="7b1a9-172">Microsoft. Azure. Management. Monitor. Management. models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="7b1a9-172">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="7b1a9-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b1a9-173">NOTES</span></span>

## <span data-ttu-id="7b1a9-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b1a9-174">RELATED LINKS</span></span>

[<span data-ttu-id="7b1a9-175">Dodaj-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7b1a9-175">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="7b1a9-176">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="7b1a9-176">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="7b1a9-177">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7b1a9-177">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="7b1a9-178">Nowe — AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="7b1a9-178">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="7b1a9-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7b1a9-179">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


