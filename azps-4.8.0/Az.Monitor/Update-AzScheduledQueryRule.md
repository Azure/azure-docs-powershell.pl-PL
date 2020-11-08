---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 1e591f9c6d631ab6b8c3a5246eb4e45655de841e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062649"
---
# <span data-ttu-id="ea79d-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ea79d-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="ea79d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea79d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea79d-103">Aktualizowanie reguły alertów dziennika</span><span class="sxs-lookup"><span data-stu-id="ea79d-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="ea79d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea79d-104">SYNTAX</span></span>

### <span data-ttu-id="ea79d-105">ByRuleName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ea79d-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea79d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ea79d-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea79d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ea79d-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea79d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ea79d-108">DESCRIPTION</span></span>
<span data-ttu-id="ea79d-109">Aktualizuje regułę alertu dziennika, aktualizowanie tylko właściwości "Enabled" jest obsługiwane przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="ea79d-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="ea79d-110">Aby zaktualizować inne właściwości, zobacz polecenie "Set-AzScheduledQueryRule".</span><span class="sxs-lookup"><span data-stu-id="ea79d-110">To update other properties, see "Set-AzScheduledQueryRule" command.</span></span>

## <span data-ttu-id="ea79d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea79d-111">EXAMPLES</span></span>

### <span data-ttu-id="ea79d-112">Przykład 1: Aktualizacja według nazwy reguły</span><span class="sxs-lookup"><span data-stu-id="ea79d-112">Example 1: Update by rule name</span></span>
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

### <span data-ttu-id="ea79d-113">Przykład 2: aktualizowanie według obiektu wejścia</span><span class="sxs-lookup"><span data-stu-id="ea79d-113">Example 2: Update by input object</span></span>
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

### <span data-ttu-id="ea79d-114">Przykład 3: aktualizowanie według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="ea79d-114">Example 3: Update by resource Id</span></span>
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

## <span data-ttu-id="ea79d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea79d-115">PARAMETERS</span></span>

### <span data-ttu-id="ea79d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea79d-116">-DefaultProfile</span></span>
<span data-ttu-id="ea79d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea79d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea79d-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="ea79d-118">-Enabled</span></span>
<span data-ttu-id="ea79d-119">Stan alertu na platformie Azure — prawidłowe wartości — $true, $false</span><span class="sxs-lookup"><span data-stu-id="ea79d-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="ea79d-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ea79d-120">-InputObject</span></span>
<span data-ttu-id="ea79d-121">Zasób reguły zaplanowanego zapytania</span><span class="sxs-lookup"><span data-stu-id="ea79d-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="ea79d-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea79d-122">-Name</span></span>
<span data-ttu-id="ea79d-123">Nazwa alertu</span><span class="sxs-lookup"><span data-stu-id="ea79d-123">The alert name</span></span>

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

### <span data-ttu-id="ea79d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea79d-124">-ResourceGroupName</span></span>
<span data-ttu-id="ea79d-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ea79d-125">The resource group name</span></span>

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

### <span data-ttu-id="ea79d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea79d-126">-ResourceId</span></span>
<span data-ttu-id="ea79d-127">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="ea79d-127">The resource Id</span></span>

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

### <span data-ttu-id="ea79d-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea79d-128">-Confirm</span></span>
<span data-ttu-id="ea79d-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea79d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea79d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea79d-130">-WhatIf</span></span>
<span data-ttu-id="ea79d-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea79d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea79d-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea79d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea79d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea79d-133">CommonParameters</span></span>
<span data-ttu-id="ea79d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea79d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea79d-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea79d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea79d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea79d-136">INPUTS</span></span>

### <span data-ttu-id="ea79d-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="ea79d-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="ea79d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ea79d-138">System.String</span></span>

## <span data-ttu-id="ea79d-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea79d-139">OUTPUTS</span></span>

### <span data-ttu-id="ea79d-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="ea79d-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="ea79d-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea79d-141">NOTES</span></span>

## <span data-ttu-id="ea79d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea79d-142">RELATED LINKS</span></span>
