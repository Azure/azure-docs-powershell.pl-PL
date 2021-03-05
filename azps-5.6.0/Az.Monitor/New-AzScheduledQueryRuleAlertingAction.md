---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 0394aa7c2db880bbb10c8d68c9d502560c1035bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961809"
---
# <span data-ttu-id="9fd0a-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="9fd0a-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="9fd0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fd0a-102">SYNOPSIS</span></span>
<span data-ttu-id="9fd0a-103">Tworzy obiekt typu Akcja alertu</span><span class="sxs-lookup"><span data-stu-id="9fd0a-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="9fd0a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9fd0a-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fd0a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9fd0a-105">DESCRIPTION</span></span>
<span data-ttu-id="9fd0a-106">Tworzy obiekt typu Akcja alertu Ten obiekt ma zostać przekazany do polecenia tworzącego regułę alertu dziennika.</span><span class="sxs-lookup"><span data-stu-id="9fd0a-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="9fd0a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9fd0a-107">EXAMPLES</span></span>

### <span data-ttu-id="9fd0a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9fd0a-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="9fd0a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fd0a-109">PARAMETERS</span></span>

### <span data-ttu-id="9fd0a-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="9fd0a-110">-AznsAction</span></span>
<span data-ttu-id="9fd0a-111">Szczegóły akcji AzNS</span><span class="sxs-lookup"><span data-stu-id="9fd0a-111">The AzNS action details</span></span>

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

### <span data-ttu-id="9fd0a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fd0a-112">-DefaultProfile</span></span>
<span data-ttu-id="9fd0a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fd0a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fd0a-114">— Ważność</span><span class="sxs-lookup"><span data-stu-id="9fd0a-114">-Severity</span></span>
<span data-ttu-id="9fd0a-115">Ważność tego alertu</span><span class="sxs-lookup"><span data-stu-id="9fd0a-115">The severity for this alert</span></span>

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

### <span data-ttu-id="9fd0a-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="9fd0a-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="9fd0a-117">Czas trwania (w minutach), dla którego należy ograniczać alerty</span><span class="sxs-lookup"><span data-stu-id="9fd0a-117">The duration in minutes for which alert should be throttled</span></span>

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

### <span data-ttu-id="9fd0a-118">— Wyzwalacz</span><span class="sxs-lookup"><span data-stu-id="9fd0a-118">-Trigger</span></span>
<span data-ttu-id="9fd0a-119">Warunek wyzwalacza alertu</span><span class="sxs-lookup"><span data-stu-id="9fd0a-119">The alert trigger condition</span></span>

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

### <span data-ttu-id="9fd0a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fd0a-120">CommonParameters</span></span>
<span data-ttu-id="9fd0a-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fd0a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fd0a-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9fd0a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fd0a-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fd0a-123">INPUTS</span></span>

### <span data-ttu-id="9fd0a-124">Brak</span><span class="sxs-lookup"><span data-stu-id="9fd0a-124">None</span></span>

## <span data-ttu-id="9fd0a-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fd0a-125">OUTPUTS</span></span>

### <span data-ttu-id="9fd0a-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="9fd0a-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="9fd0a-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9fd0a-127">NOTES</span></span>

## <span data-ttu-id="9fd0a-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fd0a-128">RELATED LINKS</span></span>
