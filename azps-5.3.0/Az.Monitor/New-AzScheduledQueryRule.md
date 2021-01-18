---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 5a896bedd7e0dd6e220fb4b8dae2cc2e87ae0fcb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503305"
---
# <span data-ttu-id="a39bf-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a39bf-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="a39bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a39bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a39bf-103">Tworzy regułę alertu dziennika (zaplanowany typ reguły kwerendy)</span><span class="sxs-lookup"><span data-stu-id="a39bf-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="a39bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a39bf-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a39bf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a39bf-105">DESCRIPTION</span></span>
<span data-ttu-id="a39bf-106">Tworzy regułę alertu dziennika (zaplanowany typ reguły kwerendy)</span><span class="sxs-lookup"><span data-stu-id="a39bf-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="a39bf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a39bf-107">EXAMPLES</span></span>

### <span data-ttu-id="a39bf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a39bf-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="a39bf-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a39bf-109">PARAMETERS</span></span>

### <span data-ttu-id="a39bf-110">-Action</span><span class="sxs-lookup"><span data-stu-id="a39bf-110">-Action</span></span>
<span data-ttu-id="a39bf-111">Akcja zaplanowanego alertu dotyczącego reguły kwerendy</span><span class="sxs-lookup"><span data-stu-id="a39bf-111">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="a39bf-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a39bf-112">-AsJob</span></span>
<span data-ttu-id="a39bf-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a39bf-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a39bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39bf-114">-DefaultProfile</span></span>
<span data-ttu-id="a39bf-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a39bf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a39bf-116">— Opis</span><span class="sxs-lookup"><span data-stu-id="a39bf-116">-Description</span></span>
<span data-ttu-id="a39bf-117">Opis tego alertu</span><span class="sxs-lookup"><span data-stu-id="a39bf-117">The description for this alert</span></span>

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

### <span data-ttu-id="a39bf-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="a39bf-118">-Enabled</span></span>
<span data-ttu-id="a39bf-119">Stan alertu na platformie Azure — prawidłowe wartości — $true, $false</span><span class="sxs-lookup"><span data-stu-id="a39bf-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="a39bf-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a39bf-120">-Location</span></span>
<span data-ttu-id="a39bf-121">Lokalizacja tego alertu</span><span class="sxs-lookup"><span data-stu-id="a39bf-121">The location for this alert</span></span>

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

### <span data-ttu-id="a39bf-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a39bf-122">-Name</span></span>
<span data-ttu-id="a39bf-123">Nazwa alertu</span><span class="sxs-lookup"><span data-stu-id="a39bf-123">The alert name</span></span>

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

### <span data-ttu-id="a39bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a39bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="a39bf-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a39bf-125">The resource group name</span></span>

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

### <span data-ttu-id="a39bf-126">-Schedule</span><span class="sxs-lookup"><span data-stu-id="a39bf-126">-Schedule</span></span>
<span data-ttu-id="a39bf-127">Harmonogram reguły zaplanowanego zapytania</span><span class="sxs-lookup"><span data-stu-id="a39bf-127">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="a39bf-128">-Source</span><span class="sxs-lookup"><span data-stu-id="a39bf-128">-Source</span></span>
<span data-ttu-id="a39bf-129">Źródło zaplanowanej reguły kwerend</span><span class="sxs-lookup"><span data-stu-id="a39bf-129">The scheduled query rule source</span></span>

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

### <span data-ttu-id="a39bf-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a39bf-130">-Tag</span></span>
<span data-ttu-id="a39bf-131">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="a39bf-131">Resource tags</span></span>

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

### <span data-ttu-id="a39bf-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a39bf-132">-Confirm</span></span>
<span data-ttu-id="a39bf-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a39bf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a39bf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a39bf-134">-WhatIf</span></span>
<span data-ttu-id="a39bf-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a39bf-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a39bf-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a39bf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a39bf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a39bf-137">CommonParameters</span></span>
<span data-ttu-id="a39bf-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a39bf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a39bf-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a39bf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a39bf-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a39bf-140">INPUTS</span></span>

### <span data-ttu-id="a39bf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a39bf-141">System.String</span></span>

## <span data-ttu-id="a39bf-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a39bf-142">OUTPUTS</span></span>

### <span data-ttu-id="a39bf-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="a39bf-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="a39bf-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a39bf-144">NOTES</span></span>

## <span data-ttu-id="a39bf-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a39bf-145">RELATED LINKS</span></span>
