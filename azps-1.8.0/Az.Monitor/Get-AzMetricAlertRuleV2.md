---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
ms.openlocfilehash: f792452202a33b23bde2153ba781456d7c8c7094
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867300"
---
# <span data-ttu-id="4a873-101">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4a873-101">Get-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="4a873-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a873-102">SYNOPSIS</span></span>
<span data-ttu-id="4a873-103">Pobiera reguły alertów metryki w wersji 2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="4a873-103">Gets V2 (non-classic) metric alert rules</span></span>

## <span data-ttu-id="4a873-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a873-104">SYNTAX</span></span>

### <span data-ttu-id="4a873-105">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a873-105">ByResourceGroupName</span></span>
```
Get-AzMetricAlertRuleV2 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a873-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="4a873-106">ByRuleName</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a873-107">ByRuleId</span><span class="sxs-lookup"><span data-stu-id="4a873-107">ByRuleId</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a873-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4a873-108">DESCRIPTION</span></span>
<span data-ttu-id="4a873-109">Polecenie cmdlet **Get-AzMetricAlertRuleV2** pobiera regułę alertu o nazwie lub identyfikatorze URI albo wszystkie reguły alertów metryki z określonej grupy zasobów lub abonamentu.</span><span class="sxs-lookup"><span data-stu-id="4a873-109">The **Get-AzMetricAlertRuleV2** cmdlet gets a metric alert rule by its name or URI, or all metric alert rules from a specified resource group or subscription.</span></span>

## <span data-ttu-id="4a873-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a873-110">EXAMPLES</span></span>
### <span data-ttu-id="4a873-111">Przykład 1: pobieranie wszystkich reguł alertów metrycznych w bieżącym abonamentzie</span><span class="sxs-lookup"><span data-stu-id="4a873-111">Example 1: Get all metric alert rules in current subscription</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : metricResourceGroup
Description          : fdafda
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/microsoft.insights/metricAlerts/Rule1
Name                 : Rule1
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}

Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : SampleResourceGroup
Description          : Testing 1 minute granuarity
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/Microsoft.Compute/virtualMachines/SCCMDemo4}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:01:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/Rule2
Name                 : Rule2
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}

```

<span data-ttu-id="4a873-112">To polecenie pobiera wszystkie reguły alertów metrycznych w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4a873-112">This command gets all the metric alert rules in the current subscription.</span></span>


### <span data-ttu-id="4a873-113">Przykład 2: pobieranie wszystkich reguł alertów metrycznych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="4a873-113">Example 2: Get all metric alert rules in a resource group</span></span>

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/pr
                       oviders/microsoft.insights/actiongroups/emails}
ResourceGroup        : metricAlertsRG
Description          : Test Classic VM alert - CPU Usage
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Micr
                       osoft.ClassicCompute/virtualMachines/VM1}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.ClassicCompute/virtualMachines
TargetResourceRegion : southcentralus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/micro
                       soft.insights/metricAlerts/Test%20Classic%20VM%20alert%20-%20CPU%20Usage
Name                 : Test Classic VM alert - CPU Usage
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}

```
<span data-ttu-id="4a873-114">To polecenie pobiera wszystkie reguły alertów metrycznych z grupy zasobów o nazwie metricAlertsRG.</span><span class="sxs-lookup"><span data-stu-id="4a873-114">This command gets all the metric alert rules in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="4a873-115">Przykład 3: uzyskiwanie reguły alertu metryki według nazwy</span><span class="sxs-lookup"><span data-stu-id="4a873-115">Example 3: Get a metric alert rule by name</span></span>

```powershell
PS C:\> Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG -Name PS3182019

Criteria             : {metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
ResourceGroup        : metricAlertsRG
Description          : This is description 
Severity             : 1
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="4a873-116">To polecenie pobiera regułę alertu metryki o nazwie PS3182019 w grupie zasobów o nazwie metricAlertsRG.</span><span class="sxs-lookup"><span data-stu-id="4a873-116">This command gets the metric alert rule named PS3182019 in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="4a873-117">Przykład 4: uzyskiwanie reguły alertu metryki przez ruleID</span><span class="sxs-lookup"><span data-stu-id="4a873-117">Example 4: Get a metric alert rule by ruleID</span></span>

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/emails}
ResourceGroup        : SampleResourceGroup
Description          : Test Description
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : 
TargetResourceRegion : 
AutoMitigate         : 
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
Name                 : MyMetricAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : 
```

<span data-ttu-id="4a873-118">To polecenie pobiera regułę alertu metryki o danym IDENTYFIKATORze zasobu.</span><span class="sxs-lookup"><span data-stu-id="4a873-118">This command gets the metric alert rule with the given resource ID.</span></span>

## <span data-ttu-id="4a873-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a873-119">PARAMETERS</span></span>

### <span data-ttu-id="4a873-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a873-120">-DefaultProfile</span></span>
<span data-ttu-id="4a873-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a873-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a873-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4a873-122">-Name</span></span>
<span data-ttu-id="4a873-123">Nazwa reguły alertu metryki</span><span class="sxs-lookup"><span data-stu-id="4a873-123">The Name of metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a873-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a873-124">-ResourceGroupName</span></span>
<span data-ttu-id="4a873-125">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a873-125">The ResourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByRuleName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a873-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a873-126">-ResourceId</span></span>
<span data-ttu-id="4a873-127">Identyfikator reguły alertu metryki</span><span class="sxs-lookup"><span data-stu-id="4a873-127">The Rule Id of metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: ByRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a873-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a873-128">CommonParameters</span></span>
<span data-ttu-id="4a873-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a873-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4a873-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a873-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a873-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a873-131">INPUTS</span></span>

### <span data-ttu-id="4a873-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4a873-132">System.String</span></span>

## <span data-ttu-id="4a873-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a873-133">OUTPUTS</span></span>

### <span data-ttu-id="4a873-134">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4a873-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="4a873-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a873-135">NOTES</span></span>

## <span data-ttu-id="4a873-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a873-136">RELATED LINKS</span></span>