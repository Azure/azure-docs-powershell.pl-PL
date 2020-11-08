---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 25854c3432f0ea28ee5eb267013992fce977b06a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053985"
---
# <span data-ttu-id="a05b1-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a05b1-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="a05b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a05b1-102">SYNOPSIS</span></span>
<span data-ttu-id="a05b1-103">Dodaje lub aktualizuje regułę alertu opartą na metryce w wersji 2 (nieklasycznej).</span><span class="sxs-lookup"><span data-stu-id="a05b1-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="a05b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a05b1-104">SYNTAX</span></span>

### <span data-ttu-id="a05b1-105">CreateAlertByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a05b1-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-DisableRule] [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a05b1-106">CreateAlertByResourceIdAndActionGroup</span><span class="sxs-lookup"><span data-stu-id="a05b1-106">CreateAlertByResourceIdAndActionGroup</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a05b1-107">CreateAlertByResourceIdAndActionGroupId</span><span class="sxs-lookup"><span data-stu-id="a05b1-107">CreateAlertByResourceIdAndActionGroupId</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroupId <String[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a05b1-108">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="a05b1-108">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-DisableRule] [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a05b1-109">CreateAlertByScopesAndActionGroup</span><span class="sxs-lookup"><span data-stu-id="a05b1-109">CreateAlertByScopesAndActionGroup</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a05b1-110">CreateAlertByScopesAndActionGroupId</span><span class="sxs-lookup"><span data-stu-id="a05b1-110">CreateAlertByScopesAndActionGroupId</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroupId <String[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a05b1-111">Opis</span><span class="sxs-lookup"><span data-stu-id="a05b1-111">DESCRIPTION</span></span>
<span data-ttu-id="a05b1-112">Dodaje lub aktualizuje **regułę alertu opartą na metryce w wersji 2 (nieklasycznej)**.</span><span class="sxs-lookup"><span data-stu-id="a05b1-112">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="a05b1-113">Dodana reguła jest skojarzona z grupą zasobów i ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="a05b1-113">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="a05b1-114">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="a05b1-114">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="a05b1-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a05b1-115">EXAMPLES</span></span>

### <span data-ttu-id="a05b1-116">Przykład 1: Dodawanie reguły alertu metryki do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a05b1-116">Example 1: Add a metric alert rule to a virtual machine</span></span>

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

<span data-ttu-id="a05b1-117">To polecenie umożliwia utworzenie reguły alertu metryki dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a05b1-117">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="a05b1-118">$condition jest wyjściem polecenia cmdlet New-AzMetricAlertRuleV2Criteria, a $act jest wyjściem polecenia cmdlet New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="a05b1-118">$condition is the output of New-AzMetricAlertRuleV2Criteria cmdlet and $act is the output of New-AzActionGroup cmdlet</span></span>

### <span data-ttu-id="a05b1-119">Przykład 2: Dodawanie reguły alertu metryki dla wszystkich maszyn wirtualnych w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a05b1-119">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
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

<span data-ttu-id="a05b1-120">To polecenie tworzy regułę alertu metryki dla wszystkich maszyn wirtualnych w subskrypcji, które znajdują się na Wschodzie.</span><span class="sxs-lookup"><span data-stu-id="a05b1-120">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="a05b1-121">Przykład 3: wyłączanie reguły alertu metryki</span><span class="sxs-lookup"><span data-stu-id="a05b1-121">Example 3: Disable a metric alert rule</span></span>
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

<span data-ttu-id="a05b1-122">To polecenie wyłącza regułę alertu o metryce.</span><span class="sxs-lookup"><span data-stu-id="a05b1-122">This command disables a metric alert rule.</span></span> <span data-ttu-id="a05b1-123">Oto dane wyjściowe Get-AzMetricAlertRuleV2 do Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a05b1-123">Here, we are piping output of Get-AzMetricAlertRuleV2 to Add-AzMetricAlertRuleV2</span></span> 

### <span data-ttu-id="a05b1-124">Przykład 4: Dodawanie reguły alertu metryki z wymiarami</span><span class="sxs-lookup"><span data-stu-id="a05b1-124">Example 4: Add a metric alert rule with dimensions</span></span>

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

<span data-ttu-id="a05b1-125">Aby utworzyć bardziej złożoną regułę alertu metryki, taką jak te, które obejmują Wybieranie wartości wymiaru lub mających wiele kryteriów, można użyć poleceń cmdlet pomocnik New-AzMetricAlertRuleV2DimensionSelection i New-AzMetricAlertRuleV2Criteria.</span><span class="sxs-lookup"><span data-stu-id="a05b1-125">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets New-AzMetricAlertRuleV2DimensionSelection and New-AzMetricAlertRuleV2Criteria.</span></span>

<span data-ttu-id="a05b1-126">Powyżej zestaw poleceń cmdlet utworzy regułę alertu metryki z wymiarami.</span><span class="sxs-lookup"><span data-stu-id="a05b1-126">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="a05b1-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a05b1-127">PARAMETERS</span></span>

### <span data-ttu-id="a05b1-128">-Action</span><span class="sxs-lookup"><span data-stu-id="a05b1-128">-ActionGroup</span></span>
<span data-ttu-id="a05b1-129">Grupa akcji dla reguły</span><span class="sxs-lookup"><span data-stu-id="a05b1-129">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: CreateAlertByResourceIdAndActionGroup, CreateAlertByScopesAndActionGroup
Aliases: Actions

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a05b1-130">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="a05b1-130">-ActionGroupId</span></span>
<span data-ttu-id="a05b1-131">Identyfikator grupy akcji dla reguły</span><span class="sxs-lookup"><span data-stu-id="a05b1-131">The Action Group id for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByResourceIdAndActionGroupId, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a05b1-132">-Warunek</span><span class="sxs-lookup"><span data-stu-id="a05b1-132">-Condition</span></span>
<span data-ttu-id="a05b1-133">Warunek reguły</span><span class="sxs-lookup"><span data-stu-id="a05b1-133">The condition for rule</span></span>

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

### <span data-ttu-id="a05b1-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05b1-134">-DefaultProfile</span></span>
<span data-ttu-id="a05b1-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a05b1-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a05b1-136">— Opis</span><span class="sxs-lookup"><span data-stu-id="a05b1-136">-Description</span></span>
<span data-ttu-id="a05b1-137">Opis reguły alertu metryki</span><span class="sxs-lookup"><span data-stu-id="a05b1-137">The description of the metric alert rule</span></span>

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

### <span data-ttu-id="a05b1-138">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="a05b1-138">-DisableRule</span></span>
<span data-ttu-id="a05b1-139">Flaga Wyłącz regułę (stan)</span><span class="sxs-lookup"><span data-stu-id="a05b1-139">The disable rule (status) flag</span></span>

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

### <span data-ttu-id="a05b1-140">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="a05b1-140">-Frequency</span></span>
<span data-ttu-id="a05b1-141">Częstotliwość obliczania dla reguły</span><span class="sxs-lookup"><span data-stu-id="a05b1-141">The evaluation frequency for rule</span></span>

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

### <span data-ttu-id="a05b1-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a05b1-142">-Name</span></span>
<span data-ttu-id="a05b1-143">Nazwa reguły alertu metryki</span><span class="sxs-lookup"><span data-stu-id="a05b1-143">The name of metric alert rule</span></span>

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

### <span data-ttu-id="a05b1-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a05b1-144">-ResourceGroupName</span></span>
<span data-ttu-id="a05b1-145">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a05b1-145">The Resource Group Name</span></span>

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

### <span data-ttu-id="a05b1-146">— Ważność</span><span class="sxs-lookup"><span data-stu-id="a05b1-146">-Severity</span></span>
<span data-ttu-id="a05b1-147">Ważność reguły alertu metryki</span><span class="sxs-lookup"><span data-stu-id="a05b1-147">The severity for the metric alert rule</span></span>

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

### <span data-ttu-id="a05b1-148">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a05b1-148">-TargetResourceId</span></span>
<span data-ttu-id="a05b1-149">Identyfikator zasobu docelowego dla reguły</span><span class="sxs-lookup"><span data-stu-id="a05b1-149">The target resource id for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByResourceId, CreateAlertByResourceIdAndActionGroup, CreateAlertByResourceIdAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a05b1-150">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="a05b1-150">-TargetResourceRegion</span></span>
<span data-ttu-id="a05b1-151">Docelowy region zasobów dla reguły</span><span class="sxs-lookup"><span data-stu-id="a05b1-151">The target resource region for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a05b1-152">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="a05b1-152">-TargetResourceScope</span></span>
<span data-ttu-id="a05b1-153">Zakres zasobów docelowych dla reguły</span><span class="sxs-lookup"><span data-stu-id="a05b1-153">The target resource scope for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a05b1-154">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="a05b1-154">-TargetResourceType</span></span>
<span data-ttu-id="a05b1-155">Typ zasobu docelowego dla reguły</span><span class="sxs-lookup"><span data-stu-id="a05b1-155">The target resource type for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a05b1-156">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="a05b1-156">-WindowSize</span></span>
<span data-ttu-id="a05b1-157">Rozmiar okna reguły</span><span class="sxs-lookup"><span data-stu-id="a05b1-157">The window size for rule</span></span>

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

### <span data-ttu-id="a05b1-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a05b1-158">-Confirm</span></span>
<span data-ttu-id="a05b1-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a05b1-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a05b1-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a05b1-160">-WhatIf</span></span>
<span data-ttu-id="a05b1-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a05b1-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a05b1-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a05b1-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a05b1-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05b1-163">CommonParameters</span></span>
<span data-ttu-id="a05b1-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a05b1-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05b1-165">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a05b1-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05b1-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a05b1-166">INPUTS</span></span>

### <span data-ttu-id="a05b1-167">System. String</span><span class="sxs-lookup"><span data-stu-id="a05b1-167">System.String</span></span>

### <span data-ttu-id="a05b1-168">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="a05b1-168">System.TimeSpan</span></span>

### <span data-ttu-id="a05b1-169">System. String []</span><span class="sxs-lookup"><span data-stu-id="a05b1-169">System.String[]</span></span>

### <span data-ttu-id="a05b1-170">System. Collections. Generic. list "1 [[Microsoft. Azure. polecenia. info............ w. OutputClasses. IPSMultiMetricCriteria, Microsoft. Azure. PowerShell. cmdlets. Monitor, Version = 1.0.1.0</span><span class="sxs-lookup"><span data-stu-id="a05b1-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a05b1-171">Microsoft. Azure. Management. Monitor. MODELES. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="a05b1-171">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="a05b1-172">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a05b1-172">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a05b1-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a05b1-173">System.Int32</span></span>

## <span data-ttu-id="a05b1-174">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a05b1-174">OUTPUTS</span></span>

### <span data-ttu-id="a05b1-175">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a05b1-175">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="a05b1-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a05b1-176">NOTES</span></span>

## <span data-ttu-id="a05b1-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a05b1-177">RELATED LINKS</span></span>
