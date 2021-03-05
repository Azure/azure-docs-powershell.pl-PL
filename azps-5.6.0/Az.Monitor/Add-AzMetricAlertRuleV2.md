---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: f679b674de8ed2f860278cb3a384f73ed17e5f54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980266"
---
# <span data-ttu-id="0b0d8-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0b0d8-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="0b0d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b0d8-102">SYNOPSIS</span></span>
<span data-ttu-id="0b0d8-103">Dodaje lub aktualizuje regułę alertów W2 (nieistnieczną) opartą na metryki.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="0b0d8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0b0d8-104">SYNTAX</span></span>

### <span data-ttu-id="0b0d8-105">CreateAlertByResourceId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0b0d8-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b0d8-106">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="0b0d8-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b0d8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0b0d8-107">DESCRIPTION</span></span>
<span data-ttu-id="0b0d8-108">Dodaje lub aktualizuje regułę alertu opartą na metryce **(nieistnieczną) V2.**</span><span class="sxs-lookup"><span data-stu-id="0b0d8-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="0b0d8-109">Dodana reguła jest skojarzona z grupą zasobów i ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="0b0d8-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, czyli może wymagać potwierdzenia od użytkownika przed utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="0b0d8-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0b0d8-111">EXAMPLES</span></span>

### <span data-ttu-id="0b0d8-112">Przykład 1. Dodawanie reguły alertu metryczne do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0b0d8-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name PS3182019 -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1", "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="0b0d8-113">To polecenie tworzy regułę alertu metryczne dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="0b0d8-114">$condition wynik polecenia cmdlet [New-AzMetricAlertRuleV2Criteria,](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) a $act wynik polecenia cmdlet [New-AzActionGroup](https://docs.microsoft.com/powershell/module/az.monitor/new-azactiongroup)</span><span class="sxs-lookup"><span data-stu-id="0b0d8-114">$condition is the output of [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet and $act is the output of [New-AzActionGroup](https://docs.microsoft.com/powershell/module/az.monitor/new-azactiongroup) cmdlet</span></span>

### <span data-ttu-id="0b0d8-115">Przykład 2. Dodawanie reguły alertu metryki dla wszystkich maszyn wirtualnych w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0b0d8-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name AllVM -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/AllVM
Name                 : AllVM
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="0b0d8-116">To polecenie tworzy regułę alertu metryki dla wszystkich maszyn wirtualnych w subskrypcji, które znajdują się we wschód</span><span class="sxs-lookup"><span data-stu-id="0b0d8-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="0b0d8-117">Przykład 3. Wyłączanie reguły alertu metryczne</span><span class="sxs-lookup"><span data-stu-id="0b0d8-117">Example 3: Disable a metric alert rule</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest  -Name TestAlertRule | Add-AzMetricAlertRuleV2 -DisableRule
Description          : This new Metric alert rule was created from Powershell version: 1.0.1
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo1}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/TestAlertRule
Name                 : TestAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="0b0d8-118">To polecenie wyłącza regułę alertu metryczne.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="0b0d8-119">W tym miejscu przedstawiamy dane wyjściowe funkcji [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricalertrulev2) do dodatku [AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2)</span><span class="sxs-lookup"><span data-stu-id="0b0d8-119">Here, we are piping output of [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricalertrulev2) to [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2)</span></span> 

### <span data-ttu-id="0b0d8-120">Przykład 4. Dodawanie metryczna reguła alertu o wymiarach</span><span class="sxs-lookup"><span data-stu-id="0b0d8-120">Example 4: Add a metric alert rule with dimensions</span></span>

```powershell
PS C:\>$act = New-AzActionGroup -ActionGroupId "/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo"
PS C:\>$dim1 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest"
PS C:\>$dim2 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/location" -ValuesToInclude "*"
PS C:\>$criteria = New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -DimensionSelection $dim1,$dim2 -TimeAggregation Average -Operator GreaterThan -Threshold 2
PS C:\>Add-AzMetricAlertRuleV2 -Name AlertWithDim -ResourceGroupName alertstest -WindowSize 00:05:00 -Frequency 00:05:00 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction" -Condition $criteria -ActionGroup $act -DisableRule -Severity 4
Description          : This new Metric alert rule was created from Powershell version: 1.0.0
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/AlertWithDim
Name                 : AlertWithDim
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="0b0d8-121">Aby utworzyć bardziej złożoną metryczną regułę alertów, na przykład tę, która obejmuje wybieranie wartości wymiaru lub wiele kryteriów, można użyć polecenia cmdlet pomocnika [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) i [New-AzMetricAlertRuleV2Criteria.](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria)</span><span class="sxs-lookup"><span data-stu-id="0b0d8-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) and [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria).</span></span>

<span data-ttu-id="0b0d8-122">Powyższy zestaw cmdlet spowoduje utworzenie metryczna reguła alertu o wymiarach.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="0b0d8-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b0d8-123">PARAMETERS</span></span>

### <span data-ttu-id="0b0d8-124">- ActionGroup</span><span class="sxs-lookup"><span data-stu-id="0b0d8-124">-ActionGroup</span></span>
<span data-ttu-id="0b0d8-125">Grupa akcji reguły</span><span class="sxs-lookup"><span data-stu-id="0b0d8-125">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0d8-126">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="0b0d8-126">-ActionGroupId</span></span>
<span data-ttu-id="0b0d8-127">Identyfikator grupy akcji reguły</span><span class="sxs-lookup"><span data-stu-id="0b0d8-127">The Action Group id for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0d8-128">— Warunek</span><span class="sxs-lookup"><span data-stu-id="0b0d8-128">-Condition</span></span>
<span data-ttu-id="0b0d8-129">Warunek reguły</span><span class="sxs-lookup"><span data-stu-id="0b0d8-129">The condition for rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]
Parameter Sets: (All)
Aliases: Criteria

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0d8-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b0d8-130">-DefaultProfile</span></span>
<span data-ttu-id="0b0d8-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b0d8-132">— Opis</span><span class="sxs-lookup"><span data-stu-id="0b0d8-132">-Description</span></span>
<span data-ttu-id="0b0d8-133">Opis reguły alertów metrycznych</span><span class="sxs-lookup"><span data-stu-id="0b0d8-133">The description of the metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0d8-134">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="0b0d8-134">-DisableRule</span></span>
<span data-ttu-id="0b0d8-135">Flaga wyłącz regułę (stan)</span><span class="sxs-lookup"><span data-stu-id="0b0d8-135">The disable rule (status) flag</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0d8-136">— Częstość</span><span class="sxs-lookup"><span data-stu-id="0b0d8-136">-Frequency</span></span>
<span data-ttu-id="0b0d8-137">Częstotliwość oceny reguły</span><span class="sxs-lookup"><span data-stu-id="0b0d8-137">The evaluation frequency for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: EvaluationFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0d8-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0b0d8-138">-Name</span></span>
<span data-ttu-id="0b0d8-139">Nazwa reguły alertu metryczne</span><span class="sxs-lookup"><span data-stu-id="0b0d8-139">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0d8-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b0d8-140">-ResourceGroupName</span></span>
<span data-ttu-id="0b0d8-141">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0b0d8-141">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0d8-142">— Ważność</span><span class="sxs-lookup"><span data-stu-id="0b0d8-142">-Severity</span></span>
<span data-ttu-id="0b0d8-143">Ważność reguły alertu metryki</span><span class="sxs-lookup"><span data-stu-id="0b0d8-143">The severity for the metric alert rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0d8-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="0b0d8-144">-TargetResourceId</span></span>
<span data-ttu-id="0b0d8-145">Identyfikator zasobu docelowego reguły</span><span class="sxs-lookup"><span data-stu-id="0b0d8-145">The target resource id for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0d8-146">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="0b0d8-146">-TargetResourceRegion</span></span>
<span data-ttu-id="0b0d8-147">Docelowy region zasobów reguły</span><span class="sxs-lookup"><span data-stu-id="0b0d8-147">The target resource region for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0d8-148">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="0b0d8-148">-TargetResourceScope</span></span>
<span data-ttu-id="0b0d8-149">Docelowy zakres zasobów dla reguły</span><span class="sxs-lookup"><span data-stu-id="0b0d8-149">The target resource scope for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByScopes
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0d8-150">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="0b0d8-150">-TargetResourceType</span></span>
<span data-ttu-id="0b0d8-151">Typ zasobu docelowego reguły</span><span class="sxs-lookup"><span data-stu-id="0b0d8-151">The target resource type for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0d8-152">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="0b0d8-152">-WindowSize</span></span>
<span data-ttu-id="0b0d8-153">Rozmiar okna reguły</span><span class="sxs-lookup"><span data-stu-id="0b0d8-153">The window size for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0d8-154">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b0d8-154">-Confirm</span></span>
<span data-ttu-id="0b0d8-155">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b0d8-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b0d8-156">-WhatIf</span></span>
<span data-ttu-id="0b0d8-157">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b0d8-158">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b0d8-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b0d8-159">CommonParameters</span></span>
<span data-ttu-id="0b0d8-160">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b0d8-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b0d8-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b0d8-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b0d8-162">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b0d8-162">INPUTS</span></span>

### <span data-ttu-id="0b0d8-163">System.String</span><span class="sxs-lookup"><span data-stu-id="0b0d8-163">System.String</span></span>

### <span data-ttu-id="0b0d8-164">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="0b0d8-164">System.TimeSpan</span></span>

### <span data-ttu-id="0b0d8-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0b0d8-165">System.String[]</span></span>

### <span data-ttu-id="0b0d8-166">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="0b0d8-166">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0b0d8-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span><span class="sxs-lookup"><span data-stu-id="0b0d8-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="0b0d8-168">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="0b0d8-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0b0d8-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0b0d8-169">System.Int32</span></span>

## <span data-ttu-id="0b0d8-170">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b0d8-170">OUTPUTS</span></span>

### <span data-ttu-id="0b0d8-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0b0d8-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="0b0d8-172">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0b0d8-172">NOTES</span></span>

## <span data-ttu-id="0b0d8-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b0d8-173">RELATED LINKS</span></span>
