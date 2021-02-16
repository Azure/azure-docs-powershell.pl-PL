---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187387"
---
# <span data-ttu-id="d9db5-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d9db5-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="d9db5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9db5-102">SYNOPSIS</span></span>
<span data-ttu-id="d9db5-103">Tworzy obiekt wyzwalacza metryki typu Log.</span><span class="sxs-lookup"><span data-stu-id="d9db5-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="d9db5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9db5-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9db5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9db5-105">DESCRIPTION</span></span>
<span data-ttu-id="d9db5-106">Tworzy obiekt wyzwalacza metryki typu Log i jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d9db5-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="d9db5-107">Jest to warunek wyzwalacza reguły zapytania metryki, który może być używany, gdy trzeba województwo typu miary metryki alertu.</span><span class="sxs-lookup"><span data-stu-id="d9db5-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="d9db5-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9db5-108">EXAMPLES</span></span>

### <span data-ttu-id="d9db5-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d9db5-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="d9db5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9db5-110">PARAMETERS</span></span>

### <span data-ttu-id="d9db5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9db5-111">-DefaultProfile</span></span>
<span data-ttu-id="d9db5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9db5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9db5-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="d9db5-113">-MetricColumn</span></span>
<span data-ttu-id="d9db5-114">Kolumna, w której jest agregowana wartość metryki.</span><span class="sxs-lookup"><span data-stu-id="d9db5-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="d9db5-115">Dane wejściowe nie są sprawdzane poprawność.</span><span class="sxs-lookup"><span data-stu-id="d9db5-115">The input is not validated.</span></span> <span data-ttu-id="d9db5-116">Najpierw zostanie sprawdzona, kiedy New-AzScheduledQueryRule ostatecznie zostanie wywołana.</span><span class="sxs-lookup"><span data-stu-id="d9db5-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="d9db5-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="d9db5-117">-MetricTriggerType</span></span>
<span data-ttu-id="d9db5-118">Metryczny typ wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="d9db5-118">The metric trigger type.</span></span>
<span data-ttu-id="d9db5-119">Dane wejściowe nie są sprawdzane poprawność.</span><span class="sxs-lookup"><span data-stu-id="d9db5-119">The input is not validated.</span></span> <span data-ttu-id="d9db5-120">Najpierw zostanie sprawdzona, kiedy New-AzScheduledQueryRule ostatecznie zostanie wywołana.</span><span class="sxs-lookup"><span data-stu-id="d9db5-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="d9db5-121">— próg</span><span class="sxs-lookup"><span data-stu-id="d9db5-121">-Threshold</span></span>
<span data-ttu-id="d9db5-122">Wartość progowa metryki: Kolejne, Suma.</span><span class="sxs-lookup"><span data-stu-id="d9db5-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="d9db5-123">Dane wejściowe nie są sprawdzane poprawność.</span><span class="sxs-lookup"><span data-stu-id="d9db5-123">The input is not validated.</span></span> <span data-ttu-id="d9db5-124">Najpierw zostanie sprawdzona, kiedy New-AzScheduledQueryRule ostatecznie zostanie wywołana.</span><span class="sxs-lookup"><span data-stu-id="d9db5-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="d9db5-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="d9db5-125">-ThresholdOperator</span></span>
<span data-ttu-id="d9db5-126">Operator progu metryki: GreaterThan, LessThan, Equal.</span><span class="sxs-lookup"><span data-stu-id="d9db5-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="d9db5-127">Dane wejściowe nie są sprawdzane poprawność.</span><span class="sxs-lookup"><span data-stu-id="d9db5-127">The input is not validated.</span></span> <span data-ttu-id="d9db5-128">Najpierw zostanie sprawdzona, kiedy New-AzScheduledQueryRule ostatecznie zostanie wywołana.</span><span class="sxs-lookup"><span data-stu-id="d9db5-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="d9db5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9db5-129">CommonParameters</span></span>
<span data-ttu-id="d9db5-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9db5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9db5-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9db5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9db5-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9db5-132">INPUTS</span></span>

### <span data-ttu-id="d9db5-133">Brak</span><span class="sxs-lookup"><span data-stu-id="d9db5-133">None</span></span>

## <span data-ttu-id="d9db5-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d9db5-134">OUTPUTS</span></span>

### <span data-ttu-id="d9db5-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d9db5-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="d9db5-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9db5-136">NOTES</span></span>

## <span data-ttu-id="d9db5-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9db5-137">RELATED LINKS</span></span>
