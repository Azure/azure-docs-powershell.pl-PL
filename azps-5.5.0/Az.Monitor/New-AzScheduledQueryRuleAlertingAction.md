---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 41ce3c066651cb2bc6ea13ddd0a7a3bb15d28879
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184931"
---
# <span data-ttu-id="3a536-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="3a536-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="3a536-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a536-102">SYNOPSIS</span></span>
<span data-ttu-id="3a536-103">Tworzy obiekt typu Akcja alertu</span><span class="sxs-lookup"><span data-stu-id="3a536-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="3a536-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3a536-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a536-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3a536-105">DESCRIPTION</span></span>
<span data-ttu-id="3a536-106">Tworzy obiekt typu Akcja alertu Ten obiekt ma zostać przekazany do polecenia tworzącego regułę alertu dziennika.</span><span class="sxs-lookup"><span data-stu-id="3a536-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="3a536-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3a536-107">EXAMPLES</span></span>

### <span data-ttu-id="3a536-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3a536-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="3a536-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a536-109">PARAMETERS</span></span>

### <span data-ttu-id="3a536-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="3a536-110">-AznsAction</span></span>
<span data-ttu-id="3a536-111">Szczegóły akcji AzNS</span><span class="sxs-lookup"><span data-stu-id="3a536-111">The AzNS action details</span></span>

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

### <span data-ttu-id="3a536-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a536-112">-DefaultProfile</span></span>
<span data-ttu-id="3a536-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a536-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a536-114">— Ważność</span><span class="sxs-lookup"><span data-stu-id="3a536-114">-Severity</span></span>
<span data-ttu-id="3a536-115">Ważność tego alertu</span><span class="sxs-lookup"><span data-stu-id="3a536-115">The severity for this alert</span></span>

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

### <span data-ttu-id="3a536-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="3a536-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="3a536-117">Czas trwania (w minutach), dla którego należy ograniczać alerty</span><span class="sxs-lookup"><span data-stu-id="3a536-117">The duration in minutes for which alert should be throttled</span></span>

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

### <span data-ttu-id="3a536-118">— Wyzwalacz</span><span class="sxs-lookup"><span data-stu-id="3a536-118">-Trigger</span></span>
<span data-ttu-id="3a536-119">Warunek wyzwalacza alertu</span><span class="sxs-lookup"><span data-stu-id="3a536-119">The alert trigger condition</span></span>

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

### <span data-ttu-id="3a536-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a536-120">CommonParameters</span></span>
<span data-ttu-id="3a536-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a536-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a536-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a536-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a536-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a536-123">INPUTS</span></span>

### <span data-ttu-id="3a536-124">Brak</span><span class="sxs-lookup"><span data-stu-id="3a536-124">None</span></span>

## <span data-ttu-id="3a536-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3a536-125">OUTPUTS</span></span>

### <span data-ttu-id="3a536-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="3a536-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="3a536-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3a536-127">NOTES</span></span>

## <span data-ttu-id="3a536-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a536-128">RELATED LINKS</span></span>
