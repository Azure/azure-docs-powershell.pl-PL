---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 5cee29c5141a9fa5cce1af93f7c3ec1de487ffec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382636"
---
# <span data-ttu-id="9deae-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="9deae-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="9deae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9deae-102">SYNOPSIS</span></span>
<span data-ttu-id="9deae-103">Pobiera zaplanowane zasoby zapytań</span><span class="sxs-lookup"><span data-stu-id="9deae-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="9deae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9deae-104">SYNTAX</span></span>

### <span data-ttu-id="9deae-105">BySubscriptionOrResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9deae-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9deae-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="9deae-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9deae-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9deae-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9deae-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9deae-108">DESCRIPTION</span></span>
<span data-ttu-id="9deae-109">Pobiera zaplanowane zasoby zapytań</span><span class="sxs-lookup"><span data-stu-id="9deae-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="9deae-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9deae-110">EXAMPLES</span></span>

### <span data-ttu-id="9deae-111">Przykład 1: Lista według abonamentu lub grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9deae-111">Example 1: List by subscription or resource group</span></span>
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

### <span data-ttu-id="9deae-112">Przykład 2: Uzyskaj według nazwy reguły</span><span class="sxs-lookup"><span data-stu-id="9deae-112">Example 2: Get by rule name</span></span>
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

### <span data-ttu-id="9deae-113">Przykład 3: uzyskiwanie według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="9deae-113">Example 3: Get by resource Id</span></span>
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

## <span data-ttu-id="9deae-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9deae-114">PARAMETERS</span></span>

### <span data-ttu-id="9deae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9deae-115">-DefaultProfile</span></span>
<span data-ttu-id="9deae-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9deae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9deae-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9deae-117">-Name</span></span>
<span data-ttu-id="9deae-118">Nazwa reguły alertu</span><span class="sxs-lookup"><span data-stu-id="9deae-118">The alert rule name</span></span>

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

### <span data-ttu-id="9deae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9deae-119">-ResourceGroupName</span></span>
<span data-ttu-id="9deae-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9deae-120">The resource group name</span></span>

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

### <span data-ttu-id="9deae-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9deae-121">-ResourceId</span></span>
<span data-ttu-id="9deae-122">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="9deae-122">The resource Id</span></span>

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

### <span data-ttu-id="9deae-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9deae-123">CommonParameters</span></span>
<span data-ttu-id="9deae-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9deae-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9deae-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9deae-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9deae-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9deae-126">INPUTS</span></span>

### <span data-ttu-id="9deae-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9deae-127">None</span></span>

## <span data-ttu-id="9deae-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9deae-128">OUTPUTS</span></span>

### <span data-ttu-id="9deae-129">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="9deae-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="9deae-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9deae-130">NOTES</span></span>

## <span data-ttu-id="9deae-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9deae-131">RELATED LINKS</span></span>
