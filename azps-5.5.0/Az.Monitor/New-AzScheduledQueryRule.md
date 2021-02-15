---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 5a896bedd7e0dd6e220fb4b8dae2cc2e87ae0fcb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184939"
---
# <span data-ttu-id="511b1-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="511b1-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="511b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="511b1-102">SYNOPSIS</span></span>
<span data-ttu-id="511b1-103">Tworzy regułę alertu dziennika (typ reguły zaplanowanego zapytania)</span><span class="sxs-lookup"><span data-stu-id="511b1-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="511b1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="511b1-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="511b1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="511b1-105">DESCRIPTION</span></span>
<span data-ttu-id="511b1-106">Tworzy regułę alertu dziennika (typ reguły zaplanowanego zapytania)</span><span class="sxs-lookup"><span data-stu-id="511b1-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="511b1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="511b1-107">EXAMPLES</span></span>

### <span data-ttu-id="511b1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="511b1-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="511b1-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="511b1-109">PARAMETERS</span></span>

### <span data-ttu-id="511b1-110">— Akcja</span><span class="sxs-lookup"><span data-stu-id="511b1-110">-Action</span></span>
<span data-ttu-id="511b1-111">Zaplanowana reguła kwerendy ostrzegawca</span><span class="sxs-lookup"><span data-stu-id="511b1-111">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="511b1-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="511b1-112">-AsJob</span></span>
<span data-ttu-id="511b1-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="511b1-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="511b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="511b1-114">-DefaultProfile</span></span>
<span data-ttu-id="511b1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="511b1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="511b1-116">— Opis</span><span class="sxs-lookup"><span data-stu-id="511b1-116">-Description</span></span>
<span data-ttu-id="511b1-117">Opis tego alertu</span><span class="sxs-lookup"><span data-stu-id="511b1-117">The description for this alert</span></span>

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

### <span data-ttu-id="511b1-118">— włączone</span><span class="sxs-lookup"><span data-stu-id="511b1-118">-Enabled</span></span>
<span data-ttu-id="511b1-119">Stan alertu platformy Azure — prawidłowe wartości — $true, $false</span><span class="sxs-lookup"><span data-stu-id="511b1-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="511b1-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="511b1-120">-Location</span></span>
<span data-ttu-id="511b1-121">Lokalizacja tego alertu</span><span class="sxs-lookup"><span data-stu-id="511b1-121">The location for this alert</span></span>

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

### <span data-ttu-id="511b1-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="511b1-122">-Name</span></span>
<span data-ttu-id="511b1-123">Nazwa alertu</span><span class="sxs-lookup"><span data-stu-id="511b1-123">The alert name</span></span>

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

### <span data-ttu-id="511b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="511b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="511b1-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="511b1-125">The resource group name</span></span>

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

### <span data-ttu-id="511b1-126">— Planowanie</span><span class="sxs-lookup"><span data-stu-id="511b1-126">-Schedule</span></span>
<span data-ttu-id="511b1-127">Harmonogram reguł kwerend planowanych</span><span class="sxs-lookup"><span data-stu-id="511b1-127">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="511b1-128">— Źródło</span><span class="sxs-lookup"><span data-stu-id="511b1-128">-Source</span></span>
<span data-ttu-id="511b1-129">Źródło reguł kwerendy zaplanowanej</span><span class="sxs-lookup"><span data-stu-id="511b1-129">The scheduled query rule source</span></span>

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

### <span data-ttu-id="511b1-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="511b1-130">-Tag</span></span>
<span data-ttu-id="511b1-131">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="511b1-131">Resource tags</span></span>

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

### <span data-ttu-id="511b1-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="511b1-132">-Confirm</span></span>
<span data-ttu-id="511b1-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="511b1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="511b1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="511b1-134">-WhatIf</span></span>
<span data-ttu-id="511b1-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="511b1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="511b1-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="511b1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="511b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="511b1-137">CommonParameters</span></span>
<span data-ttu-id="511b1-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="511b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="511b1-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="511b1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="511b1-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="511b1-140">INPUTS</span></span>

### <span data-ttu-id="511b1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="511b1-141">System.String</span></span>

## <span data-ttu-id="511b1-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="511b1-142">OUTPUTS</span></span>

### <span data-ttu-id="511b1-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="511b1-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="511b1-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="511b1-144">NOTES</span></span>

## <span data-ttu-id="511b1-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="511b1-145">RELATED LINKS</span></span>
