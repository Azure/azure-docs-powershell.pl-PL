---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 41ce3c066651cb2bc6ea13ddd0a7a3bb15d28879
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503295"
---
# <span data-ttu-id="e5535-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="e5535-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="e5535-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5535-102">SYNOPSIS</span></span>
<span data-ttu-id="e5535-103">Tworzy obiekt typu akcja alertu</span><span class="sxs-lookup"><span data-stu-id="e5535-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="e5535-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5535-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5535-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e5535-105">DESCRIPTION</span></span>
<span data-ttu-id="e5535-106">Tworzy obiekt typu akcja powiadamiania o tym, że obiekt ma zostać przekazany do polecenia, które umożliwia utworzenie reguły alertu dziennika</span><span class="sxs-lookup"><span data-stu-id="e5535-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="e5535-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5535-107">EXAMPLES</span></span>

### <span data-ttu-id="e5535-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e5535-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="e5535-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5535-109">PARAMETERS</span></span>

### <span data-ttu-id="e5535-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="e5535-110">-AznsAction</span></span>
<span data-ttu-id="e5535-111">Szczegóły akcji AzNS</span><span class="sxs-lookup"><span data-stu-id="e5535-111">The AzNS action details</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5535-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5535-112">-DefaultProfile</span></span>
<span data-ttu-id="e5535-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5535-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5535-114">— Ważność</span><span class="sxs-lookup"><span data-stu-id="e5535-114">-Severity</span></span>
<span data-ttu-id="e5535-115">Ważność tego alertu</span><span class="sxs-lookup"><span data-stu-id="e5535-115">The severity for this alert</span></span>

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

### <span data-ttu-id="e5535-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="e5535-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="e5535-117">Czas trwania (w minutach), dla którego alert powinien być ograniczany</span><span class="sxs-lookup"><span data-stu-id="e5535-117">The duration in minutes for which alert should be throttled</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5535-118">-Trigger</span><span class="sxs-lookup"><span data-stu-id="e5535-118">-Trigger</span></span>
<span data-ttu-id="e5535-119">Warunek wyzwalacza alertu</span><span class="sxs-lookup"><span data-stu-id="e5535-119">The alert trigger condition</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5535-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5535-120">CommonParameters</span></span>
<span data-ttu-id="e5535-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5535-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5535-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5535-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5535-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5535-123">INPUTS</span></span>

### <span data-ttu-id="e5535-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e5535-124">None</span></span>

## <span data-ttu-id="e5535-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5535-125">OUTPUTS</span></span>

### <span data-ttu-id="e5535-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="e5535-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="e5535-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5535-127">NOTES</span></span>

## <span data-ttu-id="e5535-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5535-128">RELATED LINKS</span></span>
