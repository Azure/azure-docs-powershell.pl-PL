---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: 24ad63f1422a829a0cef3ed0c4907ea5687b6151
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992650"
---
# <span data-ttu-id="fadad-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fadad-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="fadad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fadad-102">SYNOPSIS</span></span>
<span data-ttu-id="fadad-103">Usuwa regułę alertu dziennika</span><span class="sxs-lookup"><span data-stu-id="fadad-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="fadad-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fadad-104">SYNTAX</span></span>

### <span data-ttu-id="fadad-105">ByRuleName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="fadad-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fadad-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fadad-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fadad-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fadad-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fadad-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fadad-108">DESCRIPTION</span></span>
<span data-ttu-id="fadad-109">Usuwa regułę alertu dziennika</span><span class="sxs-lookup"><span data-stu-id="fadad-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="fadad-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fadad-110">EXAMPLES</span></span>

### <span data-ttu-id="fadad-111">Przykład 1. Usuwanie według nazwy reguły</span><span class="sxs-lookup"><span data-stu-id="fadad-111">Example 1: Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="fadad-112">Przykład 2. Usuwanie obiektu wejściowego</span><span class="sxs-lookup"><span data-stu-id="fadad-112">Example 2: Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="fadad-113">Przykład 3. Usuwanie według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="fadad-113">Example 3: Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="fadad-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fadad-114">PARAMETERS</span></span>

### <span data-ttu-id="fadad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fadad-115">-DefaultProfile</span></span>
<span data-ttu-id="fadad-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fadad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fadad-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fadad-117">-InputObject</span></span>
<span data-ttu-id="fadad-118">Zasób reguła kwerendy zaplanowanej</span><span class="sxs-lookup"><span data-stu-id="fadad-118">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fadad-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fadad-119">-Name</span></span>
<span data-ttu-id="fadad-120">Nazwa alertu</span><span class="sxs-lookup"><span data-stu-id="fadad-120">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadad-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fadad-121">-PassThru</span></span>
<span data-ttu-id="fadad-122">Zwraca wartość wskazującą sukces lub porażkę.</span><span class="sxs-lookup"><span data-stu-id="fadad-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="fadad-123">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="fadad-123">This cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadad-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fadad-124">-ResourceGroupName</span></span>
<span data-ttu-id="fadad-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fadad-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadad-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fadad-126">-ResourceId</span></span>
<span data-ttu-id="fadad-127">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="fadad-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fadad-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fadad-128">-Confirm</span></span>
<span data-ttu-id="fadad-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fadad-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadad-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fadad-130">-WhatIf</span></span>
<span data-ttu-id="fadad-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fadad-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fadad-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fadad-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadad-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fadad-133">CommonParameters</span></span>
<span data-ttu-id="fadad-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fadad-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fadad-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fadad-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fadad-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fadad-136">INPUTS</span></span>

### <span data-ttu-id="fadad-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="fadad-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="fadad-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fadad-138">System.String</span></span>

## <span data-ttu-id="fadad-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fadad-139">OUTPUTS</span></span>

### <span data-ttu-id="fadad-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fadad-140">System.Boolean</span></span>

## <span data-ttu-id="fadad-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fadad-141">NOTES</span></span>

## <span data-ttu-id="fadad-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fadad-142">RELATED LINKS</span></span>
