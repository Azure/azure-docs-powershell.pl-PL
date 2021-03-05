---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 8b1658ef2ff2779243d42461f4b94964017a6847
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985909"
---
# <span data-ttu-id="2a103-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2a103-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="2a103-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a103-102">SYNOPSIS</span></span>
<span data-ttu-id="2a103-103">Aktualizuje regułę alertu dziennika</span><span class="sxs-lookup"><span data-stu-id="2a103-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="2a103-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2a103-104">SYNTAX</span></span>

### <span data-ttu-id="2a103-105">ByRuleName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="2a103-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a103-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2a103-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a103-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a103-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a103-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2a103-108">DESCRIPTION</span></span>
<span data-ttu-id="2a103-109">Aktualizuje regułę alertu dziennika, a to polecenie obsługuje aktualizowanie tylko właściwości "Włączone".</span><span class="sxs-lookup"><span data-stu-id="2a103-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="2a103-110">Aby zaktualizować inne właściwości, [zobacz polecenie Set-AzScheduledQueryRule.](https://docs.microsoft.com/powershell/module/az.monitor/set-azscheduledqueryrule)</span><span class="sxs-lookup"><span data-stu-id="2a103-110">To update other properties, see [Set-AzScheduledQueryRule](https://docs.microsoft.com/powershell/module/az.monitor/set-azscheduledqueryrule) command.</span></span>

## <span data-ttu-id="2a103-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2a103-111">EXAMPLES</span></span>

### <span data-ttu-id="2a103-112">Przykład 1. Aktualizowanie według nazwy reguły</span><span class="sxs-lookup"><span data-stu-id="2a103-112">Example 1: Update by rule name</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:49:15 PM
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

### <span data-ttu-id="2a103-113">Przykład 2. Aktualizowanie według obiektu wejściowego</span><span class="sxs-lookup"><span data-stu-id="2a103-113">Example 2: Update by input object</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -InputObject $sqr -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:50:18 PM
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

### <span data-ttu-id="2a103-114">Przykład 3. Aktualizacja według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="2a103-114">Example 3: Update by resource Id</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceId /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1 -Enabled $true

Description       : description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:51:14 PM
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

## <span data-ttu-id="2a103-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a103-115">PARAMETERS</span></span>

### <span data-ttu-id="2a103-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a103-116">-DefaultProfile</span></span>
<span data-ttu-id="2a103-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a103-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a103-118">— włączone</span><span class="sxs-lookup"><span data-stu-id="2a103-118">-Enabled</span></span>
<span data-ttu-id="2a103-119">Stan alertu platformy Azure — prawidłowe wartości — $true, $false</span><span class="sxs-lookup"><span data-stu-id="2a103-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="2a103-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a103-120">-InputObject</span></span>
<span data-ttu-id="2a103-121">Zasób reguła kwerendy zaplanowanej</span><span class="sxs-lookup"><span data-stu-id="2a103-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="2a103-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2a103-122">-Name</span></span>
<span data-ttu-id="2a103-123">Nazwa alertu</span><span class="sxs-lookup"><span data-stu-id="2a103-123">The alert name</span></span>

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

### <span data-ttu-id="2a103-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a103-124">-ResourceGroupName</span></span>
<span data-ttu-id="2a103-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2a103-125">The resource group name</span></span>

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

### <span data-ttu-id="2a103-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a103-126">-ResourceId</span></span>
<span data-ttu-id="2a103-127">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="2a103-127">The resource Id</span></span>

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

### <span data-ttu-id="2a103-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a103-128">-Confirm</span></span>
<span data-ttu-id="2a103-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2a103-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a103-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a103-130">-WhatIf</span></span>
<span data-ttu-id="2a103-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a103-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a103-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2a103-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a103-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a103-133">CommonParameters</span></span>
<span data-ttu-id="2a103-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a103-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a103-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a103-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a103-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a103-136">INPUTS</span></span>

### <span data-ttu-id="2a103-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="2a103-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="2a103-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2a103-138">System.String</span></span>

## <span data-ttu-id="2a103-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a103-139">OUTPUTS</span></span>

### <span data-ttu-id="2a103-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="2a103-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="2a103-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2a103-141">NOTES</span></span>

## <span data-ttu-id="2a103-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a103-142">RELATED LINKS</span></span>
