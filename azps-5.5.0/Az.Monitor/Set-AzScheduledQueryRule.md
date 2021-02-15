---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: 0351d6920c4af7f781ef27f4dfbc36a13e0c50cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190082"
---
# <span data-ttu-id="b6b24-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b6b24-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="b6b24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6b24-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b24-103">Aktualizuje regułę alertu dziennika</span><span class="sxs-lookup"><span data-stu-id="b6b24-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="b6b24-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b6b24-104">SYNTAX</span></span>

### <span data-ttu-id="b6b24-105">ByRuleName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="b6b24-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6b24-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b6b24-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6b24-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6b24-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6b24-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b6b24-108">DESCRIPTION</span></span>
<span data-ttu-id="b6b24-109">Aktualizuje regułę alertu dziennika semantyką PUT</span><span class="sxs-lookup"><span data-stu-id="b6b24-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="b6b24-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b6b24-110">EXAMPLES</span></span>

### <span data-ttu-id="b6b24-111">Przykład 1. Ustawianie według nazwy reguły</span><span class="sxs-lookup"><span data-stu-id="b6b24-111">Example 1: Set by rule name</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "log alert description" -Schedule $schedule -Source $source

Description       : log alert description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:45:04 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="b6b24-112">Przykład 2. Ustawianie według obiektu input</span><span class="sxs-lookup"><span data-stu-id="b6b24-112">Example 2: Set by Input Object</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -InputObject $sqr -Description "changed description"

Description       : changed description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:46:38 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="b6b24-113">Przykład 3. Ustawianie według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="b6b24-113">Example 3: Set by resource Id</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "change description again" -Schedule $schedule -Source $source

Description       : change description again
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:47:59 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="b6b24-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6b24-114">PARAMETERS</span></span>

### <span data-ttu-id="b6b24-115">— akcja</span><span class="sxs-lookup"><span data-stu-id="b6b24-115">-Action</span></span>
<span data-ttu-id="b6b24-116">Zaplanowane działanie alertu reguły kwerendy</span><span class="sxs-lookup"><span data-stu-id="b6b24-116">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b24-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b6b24-117">-AsJob</span></span>
<span data-ttu-id="b6b24-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b6b24-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6b24-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b24-119">-DefaultProfile</span></span>
<span data-ttu-id="b6b24-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b24-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6b24-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="b6b24-121">-Description</span></span>
<span data-ttu-id="b6b24-122">Opis tego alertu</span><span class="sxs-lookup"><span data-stu-id="b6b24-122">The description for this alert</span></span>

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

### <span data-ttu-id="b6b24-123">— włączone</span><span class="sxs-lookup"><span data-stu-id="b6b24-123">-Enabled</span></span>
<span data-ttu-id="b6b24-124">Stan alertu platformy Azure — prawidłowe wartości — $true, $false</span><span class="sxs-lookup"><span data-stu-id="b6b24-124">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b24-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6b24-125">-InputObject</span></span>
<span data-ttu-id="b6b24-126">Zasób reguły kwerendy zaplanowanej</span><span class="sxs-lookup"><span data-stu-id="b6b24-126">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="b6b24-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b6b24-127">-Location</span></span>
<span data-ttu-id="b6b24-128">Lokalizacja tego alertu</span><span class="sxs-lookup"><span data-stu-id="b6b24-128">The location for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b24-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b6b24-129">-Name</span></span>
<span data-ttu-id="b6b24-130">Nazwa alertu</span><span class="sxs-lookup"><span data-stu-id="b6b24-130">The alert name</span></span>

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

### <span data-ttu-id="b6b24-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6b24-131">-ResourceGroupName</span></span>
<span data-ttu-id="b6b24-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b6b24-132">The resource group name</span></span>

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

### <span data-ttu-id="b6b24-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6b24-133">-ResourceId</span></span>
<span data-ttu-id="b6b24-134">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="b6b24-134">The resource Id</span></span>

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

### <span data-ttu-id="b6b24-135">— Planowanie</span><span class="sxs-lookup"><span data-stu-id="b6b24-135">-Schedule</span></span>
<span data-ttu-id="b6b24-136">Harmonogram reguł kwerend planowanych</span><span class="sxs-lookup"><span data-stu-id="b6b24-136">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b24-137">— Źródło</span><span class="sxs-lookup"><span data-stu-id="b6b24-137">-Source</span></span>
<span data-ttu-id="b6b24-138">Źródło reguł kwerendy zaplanowanej</span><span class="sxs-lookup"><span data-stu-id="b6b24-138">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b24-139">— Tag</span><span class="sxs-lookup"><span data-stu-id="b6b24-139">-Tag</span></span>
<span data-ttu-id="b6b24-140">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="b6b24-140">Resource tags</span></span>

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

### <span data-ttu-id="b6b24-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6b24-141">-Confirm</span></span>
<span data-ttu-id="b6b24-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b6b24-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6b24-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6b24-143">-WhatIf</span></span>
<span data-ttu-id="b6b24-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6b24-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6b24-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b6b24-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6b24-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b24-146">CommonParameters</span></span>
<span data-ttu-id="b6b24-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6b24-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b24-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6b24-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b24-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6b24-149">INPUTS</span></span>

### <span data-ttu-id="b6b24-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="b6b24-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="b6b24-151">System.String</span><span class="sxs-lookup"><span data-stu-id="b6b24-151">System.String</span></span>

### <span data-ttu-id="b6b24-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="b6b24-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="b6b24-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="b6b24-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="b6b24-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="b6b24-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="b6b24-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6b24-155">OUTPUTS</span></span>

### <span data-ttu-id="b6b24-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="b6b24-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="b6b24-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b6b24-157">NOTES</span></span>

## <span data-ttu-id="b6b24-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6b24-158">RELATED LINKS</span></span>
