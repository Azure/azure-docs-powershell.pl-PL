---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220765"
---
# <span data-ttu-id="56e10-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="56e10-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="56e10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56e10-102">SYNOPSIS</span></span>
<span data-ttu-id="56e10-103">Tworzy obiekt typu wyzwalacz metryki dziennika.</span><span class="sxs-lookup"><span data-stu-id="56e10-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="56e10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56e10-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56e10-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56e10-105">DESCRIPTION</span></span>
<span data-ttu-id="56e10-106">Tworzy obiekt typu wyzwalacz metryki dziennika i jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="56e10-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="56e10-107">Jest to warunek wyzwalania reguły kwerendy metryki, który ma być stosowany, gdy trzeba podać typ wpisu metryki.</span><span class="sxs-lookup"><span data-stu-id="56e10-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="56e10-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56e10-108">EXAMPLES</span></span>

### <span data-ttu-id="56e10-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="56e10-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="56e10-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56e10-110">PARAMETERS</span></span>

### <span data-ttu-id="56e10-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e10-111">-DefaultProfile</span></span>
<span data-ttu-id="56e10-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56e10-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56e10-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="56e10-113">-MetricColumn</span></span>
<span data-ttu-id="56e10-114">Kolumna, w której jest agregowana wartość metryki.</span><span class="sxs-lookup"><span data-stu-id="56e10-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="56e10-115">Dane wejściowe nie są sprawdzane.</span><span class="sxs-lookup"><span data-stu-id="56e10-115">The input is not validated.</span></span> <span data-ttu-id="56e10-116">Zostanie ona najpierw sprawdzona, gdy New-AzScheduledQueryRule jest po pewnym czasie wywoływana.</span><span class="sxs-lookup"><span data-stu-id="56e10-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="56e10-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="56e10-117">-MetricTriggerType</span></span>
<span data-ttu-id="56e10-118">Typ wyzwalacza metryki.</span><span class="sxs-lookup"><span data-stu-id="56e10-118">The metric trigger type.</span></span>
<span data-ttu-id="56e10-119">Dane wejściowe nie są sprawdzane.</span><span class="sxs-lookup"><span data-stu-id="56e10-119">The input is not validated.</span></span> <span data-ttu-id="56e10-120">Zostanie ona najpierw sprawdzona, gdy New-AzScheduledQueryRule jest po pewnym czasie wywoływana.</span><span class="sxs-lookup"><span data-stu-id="56e10-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="56e10-121">-Próg</span><span class="sxs-lookup"><span data-stu-id="56e10-121">-Threshold</span></span>
<span data-ttu-id="56e10-122">Wartość progowa metryki: kolejno, suma.</span><span class="sxs-lookup"><span data-stu-id="56e10-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="56e10-123">Dane wejściowe nie są sprawdzane.</span><span class="sxs-lookup"><span data-stu-id="56e10-123">The input is not validated.</span></span> <span data-ttu-id="56e10-124">Zostanie ona najpierw sprawdzona, gdy New-AzScheduledQueryRule jest po pewnym czasie wywoływana.</span><span class="sxs-lookup"><span data-stu-id="56e10-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="56e10-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="56e10-125">-ThresholdOperator</span></span>
<span data-ttu-id="56e10-126">Operator progu metrycznego: GreaterThan, LessThan, równe.</span><span class="sxs-lookup"><span data-stu-id="56e10-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="56e10-127">Dane wejściowe nie są sprawdzane.</span><span class="sxs-lookup"><span data-stu-id="56e10-127">The input is not validated.</span></span> <span data-ttu-id="56e10-128">Zostanie ona najpierw sprawdzona, gdy New-AzScheduledQueryRule jest po pewnym czasie wywoływana.</span><span class="sxs-lookup"><span data-stu-id="56e10-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="56e10-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e10-129">CommonParameters</span></span>
<span data-ttu-id="56e10-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e10-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e10-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56e10-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e10-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56e10-132">INPUTS</span></span>

### <span data-ttu-id="56e10-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="56e10-133">None</span></span>

## <span data-ttu-id="56e10-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56e10-134">OUTPUTS</span></span>

### <span data-ttu-id="56e10-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="56e10-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="56e10-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56e10-136">NOTES</span></span>

## <span data-ttu-id="56e10-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56e10-137">RELATED LINKS</span></span>
