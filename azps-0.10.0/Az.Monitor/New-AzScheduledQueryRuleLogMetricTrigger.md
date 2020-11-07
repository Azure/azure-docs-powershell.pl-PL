---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c5fb336d7ba105469506bb0a80a5b69036e5474b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891117"
---
# <span data-ttu-id="7dd2f-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7dd2f-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="7dd2f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7dd2f-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd2f-103">Tworzy obiekt typu wyzwalacz metryki dziennika</span><span class="sxs-lookup"><span data-stu-id="7dd2f-103">Creates an object of type Log Metric Trigger</span></span>

## <span data-ttu-id="7dd2f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7dd2f-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7dd2f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7dd2f-105">DESCRIPTION</span></span>
<span data-ttu-id="7dd2f-106">Tworzy obiekt typu wyzwalacz metryki dziennika i jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7dd2f-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="7dd2f-107">Jest to warunek wyzwalania reguły kwerendy metryki, który ma być stosowany, gdy trzeba podać typ wpisu metryki.</span><span class="sxs-lookup"><span data-stu-id="7dd2f-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="7dd2f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7dd2f-108">EXAMPLES</span></span>

### <span data-ttu-id="7dd2f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7dd2f-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="7dd2f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7dd2f-110">PARAMETERS</span></span>

### <span data-ttu-id="7dd2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd2f-111">-DefaultProfile</span></span>
<span data-ttu-id="7dd2f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd2f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dd2f-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="7dd2f-113">-MetricColumn</span></span>
<span data-ttu-id="7dd2f-114">Kolumna, w której jest agregowana wartość metryki</span><span class="sxs-lookup"><span data-stu-id="7dd2f-114">Column on which metric value is being aggregated</span></span>

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

### <span data-ttu-id="7dd2f-115">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="7dd2f-115">-MetricTriggerType</span></span>
<span data-ttu-id="7dd2f-116">Typ wyzwalacza metryki</span><span class="sxs-lookup"><span data-stu-id="7dd2f-116">The metric trigger type</span></span>

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

### <span data-ttu-id="7dd2f-117">-Próg</span><span class="sxs-lookup"><span data-stu-id="7dd2f-117">-Threshold</span></span>
<span data-ttu-id="7dd2f-118">Wartość progowa metryki</span><span class="sxs-lookup"><span data-stu-id="7dd2f-118">The metric threshold value</span></span>

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

### <span data-ttu-id="7dd2f-119">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="7dd2f-119">-ThresholdOperator</span></span>
<span data-ttu-id="7dd2f-120">Operator progu metrycznego: GreaterThan, LessThan, równy</span><span class="sxs-lookup"><span data-stu-id="7dd2f-120">The metric threshold operator : GreaterThan, LessThan, Equal</span></span>

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

### <span data-ttu-id="7dd2f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd2f-121">CommonParameters</span></span>
<span data-ttu-id="7dd2f-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dd2f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd2f-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7dd2f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd2f-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dd2f-124">INPUTS</span></span>

### <span data-ttu-id="7dd2f-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7dd2f-125">None</span></span>

## <span data-ttu-id="7dd2f-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7dd2f-126">OUTPUTS</span></span>

### <span data-ttu-id="7dd2f-127">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7dd2f-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="7dd2f-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7dd2f-128">NOTES</span></span>

## <span data-ttu-id="7dd2f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7dd2f-129">RELATED LINKS</span></span>
