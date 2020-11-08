---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 0fffbc11291fcf3cd7d3989e211bcbb0d202ea9b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063454"
---
# <span data-ttu-id="cc98e-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="cc98e-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="cc98e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc98e-102">SYNOPSIS</span></span>
<span data-ttu-id="cc98e-103">Tworzenie obiektu typu warunek wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="cc98e-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="cc98e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc98e-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc98e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cc98e-105">DESCRIPTION</span></span>
<span data-ttu-id="cc98e-106">Tworzy obiekt typu warunek wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="cc98e-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="cc98e-107">Ten obiekt ma zostać przekazany do polecenia, które służy do tworzenia obiektu akcji alertu</span><span class="sxs-lookup"><span data-stu-id="cc98e-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="cc98e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc98e-108">EXAMPLES</span></span>

### <span data-ttu-id="cc98e-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cc98e-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="cc98e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc98e-110">PARAMETERS</span></span>

### <span data-ttu-id="cc98e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc98e-111">-DefaultProfile</span></span>
<span data-ttu-id="cc98e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc98e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc98e-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="cc98e-113">-MetricTrigger</span></span>
<span data-ttu-id="cc98e-114">Warunek wyzwalania dla reguły zapytania metryki</span><span class="sxs-lookup"><span data-stu-id="cc98e-114">Trigger condition for metric query rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc98e-115">-Próg</span><span class="sxs-lookup"><span data-stu-id="cc98e-115">-Threshold</span></span>
<span data-ttu-id="cc98e-116">Próg, powyżej którego zostanie wyzwolony alert</span><span class="sxs-lookup"><span data-stu-id="cc98e-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="cc98e-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="cc98e-117">-ThresholdOperator</span></span>
<span data-ttu-id="cc98e-118">Operator progu: GreaterThan, LessThan lub równe</span><span class="sxs-lookup"><span data-stu-id="cc98e-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="cc98e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc98e-119">CommonParameters</span></span>
<span data-ttu-id="cc98e-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc98e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc98e-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc98e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc98e-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc98e-122">INPUTS</span></span>

### <span data-ttu-id="cc98e-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cc98e-123">None</span></span>

## <span data-ttu-id="cc98e-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc98e-124">OUTPUTS</span></span>

### <span data-ttu-id="cc98e-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="cc98e-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="cc98e-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc98e-126">NOTES</span></span>

## <span data-ttu-id="cc98e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc98e-127">RELATED LINKS</span></span>
