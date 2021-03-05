---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: 0270c9bf6d543455772095a6d0fe3f0f1a55a416
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978426"
---
# <span data-ttu-id="a1211-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a1211-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="a1211-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1211-102">SYNOPSIS</span></span>
<span data-ttu-id="a1211-103">Tworzy obiekt wyzwalacza metryki typu Log.</span><span class="sxs-lookup"><span data-stu-id="a1211-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="a1211-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a1211-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1211-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a1211-105">DESCRIPTION</span></span>
<span data-ttu-id="a1211-106">Tworzy obiekt wyzwalacza metryki typu log i jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a1211-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="a1211-107">Jest to warunek wyzwalacza reguły zapytania metryczne, który może być używany, gdy trzeba województwo typu miary metryki alertu.</span><span class="sxs-lookup"><span data-stu-id="a1211-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="a1211-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a1211-108">EXAMPLES</span></span>

### <span data-ttu-id="a1211-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a1211-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="a1211-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1211-110">PARAMETERS</span></span>

### <span data-ttu-id="a1211-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1211-111">-DefaultProfile</span></span>
<span data-ttu-id="a1211-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1211-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1211-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="a1211-113">-MetricColumn</span></span>
<span data-ttu-id="a1211-114">Kolumna, w której jest agregowana wartość metryki.</span><span class="sxs-lookup"><span data-stu-id="a1211-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="a1211-115">Dane wejściowe nie są sprawdzane poprawność.</span><span class="sxs-lookup"><span data-stu-id="a1211-115">The input is not validated.</span></span> <span data-ttu-id="a1211-116">Najpierw zostanie sprawdzona, kiedy New-AzScheduledQueryRule ostatecznie zostanie wywołana.</span><span class="sxs-lookup"><span data-stu-id="a1211-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="a1211-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="a1211-117">-MetricTriggerType</span></span>
<span data-ttu-id="a1211-118">Typ wyzwalacza metryki.</span><span class="sxs-lookup"><span data-stu-id="a1211-118">The metric trigger type.</span></span>
<span data-ttu-id="a1211-119">Dane wejściowe nie są sprawdzane poprawność.</span><span class="sxs-lookup"><span data-stu-id="a1211-119">The input is not validated.</span></span> <span data-ttu-id="a1211-120">Najpierw zostanie sprawdzona, kiedy New-AzScheduledQueryRule ostatecznie zostanie wywołana.</span><span class="sxs-lookup"><span data-stu-id="a1211-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="a1211-121">— próg</span><span class="sxs-lookup"><span data-stu-id="a1211-121">-Threshold</span></span>
<span data-ttu-id="a1211-122">Wartość progowa metryki: Kolejna, Suma.</span><span class="sxs-lookup"><span data-stu-id="a1211-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="a1211-123">Dane wejściowe nie są sprawdzane poprawność.</span><span class="sxs-lookup"><span data-stu-id="a1211-123">The input is not validated.</span></span> <span data-ttu-id="a1211-124">Najpierw zostanie sprawdzona, kiedy New-AzScheduledQueryRule ostatecznie zostanie wywołana.</span><span class="sxs-lookup"><span data-stu-id="a1211-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1211-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="a1211-125">-ThresholdOperator</span></span>
<span data-ttu-id="a1211-126">Operator progu metryki: GreaterThan, LessThan, Equal.</span><span class="sxs-lookup"><span data-stu-id="a1211-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="a1211-127">Dane wejściowe nie są sprawdzane poprawność.</span><span class="sxs-lookup"><span data-stu-id="a1211-127">The input is not validated.</span></span> <span data-ttu-id="a1211-128">Najpierw zostanie sprawdzona, kiedy New-AzScheduledQueryRule ostatecznie zostanie wywołana.</span><span class="sxs-lookup"><span data-stu-id="a1211-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="a1211-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1211-129">CommonParameters</span></span>
<span data-ttu-id="a1211-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1211-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1211-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1211-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1211-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1211-132">INPUTS</span></span>

### <span data-ttu-id="a1211-133">Brak</span><span class="sxs-lookup"><span data-stu-id="a1211-133">None</span></span>

## <span data-ttu-id="a1211-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1211-134">OUTPUTS</span></span>

### <span data-ttu-id="a1211-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a1211-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="a1211-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a1211-136">NOTES</span></span>

## <span data-ttu-id="a1211-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1211-137">RELATED LINKS</span></span>
