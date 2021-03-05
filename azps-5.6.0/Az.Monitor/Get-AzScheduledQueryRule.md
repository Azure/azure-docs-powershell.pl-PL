---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 98590e23035810317bf4290513a1c0030b0fcac0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979930"
---
# <span data-ttu-id="deadd-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="deadd-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="deadd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deadd-102">SYNOPSIS</span></span>
<span data-ttu-id="deadd-103">Pobiera zasoby dotyczące zapytań planowanych</span><span class="sxs-lookup"><span data-stu-id="deadd-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="deadd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="deadd-104">SYNTAX</span></span>

### <span data-ttu-id="deadd-105">BySubscriptionOrResourceGroup (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="deadd-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="deadd-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="deadd-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="deadd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="deadd-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="deadd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="deadd-108">DESCRIPTION</span></span>
<span data-ttu-id="deadd-109">Pobiera zasoby dotyczące zapytań planowanych</span><span class="sxs-lookup"><span data-stu-id="deadd-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="deadd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="deadd-110">EXAMPLES</span></span>

### <span data-ttu-id="deadd-111">Przykład 1. Lista według subskrypcji lub grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="deadd-111">Example 1: List by subscription or resource group</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup"

Description       : description 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}

Description       : description 2
Enabled           : true
LastUpdatedTime   : 15-Apr-19 6:57:00 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.Action
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule2
Name              : LogAlertRule2
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="deadd-112">Przykład 2. Uzyskiwanie według nazwy reguły</span><span class="sxs-lookup"><span data-stu-id="deadd-112">Example 2: Get by rule name</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
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

### <span data-ttu-id="deadd-113">Przykład 3. Uzyskiwanie według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="deadd-113">Example 3: Get by resource Id</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
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

## <span data-ttu-id="deadd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="deadd-114">PARAMETERS</span></span>

### <span data-ttu-id="deadd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deadd-115">-DefaultProfile</span></span>
<span data-ttu-id="deadd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="deadd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deadd-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="deadd-117">-Name</span></span>
<span data-ttu-id="deadd-118">Nazwa reguły alertu</span><span class="sxs-lookup"><span data-stu-id="deadd-118">The alert rule name</span></span>

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

### <span data-ttu-id="deadd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deadd-119">-ResourceGroupName</span></span>
<span data-ttu-id="deadd-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="deadd-120">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="deadd-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="deadd-121">-ResourceId</span></span>
<span data-ttu-id="deadd-122">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="deadd-122">The resource Id</span></span>

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

### <span data-ttu-id="deadd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deadd-123">CommonParameters</span></span>
<span data-ttu-id="deadd-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deadd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deadd-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="deadd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deadd-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="deadd-126">INPUTS</span></span>

### <span data-ttu-id="deadd-127">Brak</span><span class="sxs-lookup"><span data-stu-id="deadd-127">None</span></span>

## <span data-ttu-id="deadd-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="deadd-128">OUTPUTS</span></span>

### <span data-ttu-id="deadd-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="deadd-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="deadd-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="deadd-130">NOTES</span></span>

## <span data-ttu-id="deadd-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="deadd-131">RELATED LINKS</span></span>
