---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 49863fd8102aef7b0175328edc0b4523f13921d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961818"
---
# <span data-ttu-id="ec56b-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ec56b-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="ec56b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec56b-102">SYNOPSIS</span></span>
<span data-ttu-id="ec56b-103">Tworzy regułę alertu dziennika (typ reguły zaplanowanego zapytania)</span><span class="sxs-lookup"><span data-stu-id="ec56b-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="ec56b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ec56b-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec56b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ec56b-105">DESCRIPTION</span></span>
<span data-ttu-id="ec56b-106">Tworzy regułę alertu dziennika (typ reguły zaplanowanego zapytania)</span><span class="sxs-lookup"><span data-stu-id="ec56b-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="ec56b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ec56b-107">EXAMPLES</span></span>

### <span data-ttu-id="ec56b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ec56b-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="ec56b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec56b-109">PARAMETERS</span></span>

### <span data-ttu-id="ec56b-110">— Akcja</span><span class="sxs-lookup"><span data-stu-id="ec56b-110">-Action</span></span>
<span data-ttu-id="ec56b-111">Zaplanowana reguła kwerendy ostrzegawca</span><span class="sxs-lookup"><span data-stu-id="ec56b-111">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec56b-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ec56b-112">-AsJob</span></span>
<span data-ttu-id="ec56b-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ec56b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec56b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec56b-114">-DefaultProfile</span></span>
<span data-ttu-id="ec56b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec56b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec56b-116">— Opis</span><span class="sxs-lookup"><span data-stu-id="ec56b-116">-Description</span></span>
<span data-ttu-id="ec56b-117">Opis tego alertu</span><span class="sxs-lookup"><span data-stu-id="ec56b-117">The description for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec56b-118">— włączone</span><span class="sxs-lookup"><span data-stu-id="ec56b-118">-Enabled</span></span>
<span data-ttu-id="ec56b-119">Stan alertu platformy Azure — prawidłowe wartości — $true, $false</span><span class="sxs-lookup"><span data-stu-id="ec56b-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec56b-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ec56b-120">-Location</span></span>
<span data-ttu-id="ec56b-121">Lokalizacja tego alertu</span><span class="sxs-lookup"><span data-stu-id="ec56b-121">The location for this alert</span></span>

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

### <span data-ttu-id="ec56b-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ec56b-122">-Name</span></span>
<span data-ttu-id="ec56b-123">Nazwa alertu</span><span class="sxs-lookup"><span data-stu-id="ec56b-123">The alert name</span></span>

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

### <span data-ttu-id="ec56b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec56b-124">-ResourceGroupName</span></span>
<span data-ttu-id="ec56b-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ec56b-125">The resource group name</span></span>

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

### <span data-ttu-id="ec56b-126">— Planowanie</span><span class="sxs-lookup"><span data-stu-id="ec56b-126">-Schedule</span></span>
<span data-ttu-id="ec56b-127">Harmonogram reguł kwerend planowanych</span><span class="sxs-lookup"><span data-stu-id="ec56b-127">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec56b-128">— Źródło</span><span class="sxs-lookup"><span data-stu-id="ec56b-128">-Source</span></span>
<span data-ttu-id="ec56b-129">Źródło reguł kwerendy zaplanowanej</span><span class="sxs-lookup"><span data-stu-id="ec56b-129">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec56b-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="ec56b-130">-Tag</span></span>
<span data-ttu-id="ec56b-131">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="ec56b-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec56b-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ec56b-132">-Confirm</span></span>
<span data-ttu-id="ec56b-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ec56b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec56b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec56b-134">-WhatIf</span></span>
<span data-ttu-id="ec56b-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec56b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec56b-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ec56b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec56b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec56b-137">CommonParameters</span></span>
<span data-ttu-id="ec56b-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec56b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec56b-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec56b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec56b-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec56b-140">INPUTS</span></span>

### <span data-ttu-id="ec56b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ec56b-141">System.String</span></span>

## <span data-ttu-id="ec56b-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec56b-142">OUTPUTS</span></span>

### <span data-ttu-id="ec56b-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="ec56b-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="ec56b-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ec56b-144">NOTES</span></span>

## <span data-ttu-id="ec56b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec56b-145">RELATED LINKS</span></span>
