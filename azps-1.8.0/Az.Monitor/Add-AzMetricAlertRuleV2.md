---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 17be83253d452b4c347154f8c0e392277287d0b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867360"
---
# <span data-ttu-id="65b33-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="65b33-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="65b33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65b33-102">SYNOPSIS</span></span>
<span data-ttu-id="65b33-103">Dodaje lub aktualizuje regułę alertu opartą na metryce w wersji 2 (nieklasycznej).</span><span class="sxs-lookup"><span data-stu-id="65b33-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="65b33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65b33-104">SYNTAX</span></span>

### <span data-ttu-id="65b33-105">CreateAlertByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="65b33-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b33-106">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="65b33-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65b33-107">Opis</span><span class="sxs-lookup"><span data-stu-id="65b33-107">DESCRIPTION</span></span>
<span data-ttu-id="65b33-108">Dodaje lub aktualizuje **regułę alertu opartą na metryce w wersji 2 (nieklasycznej)**.</span><span class="sxs-lookup"><span data-stu-id="65b33-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="65b33-109">Dodana reguła jest skojarzona z grupą zasobów i ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="65b33-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="65b33-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="65b33-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="65b33-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65b33-111">EXAMPLES</span></span>

### <span data-ttu-id="65b33-112">Przykład 1: Dodawanie reguły alertu metryki do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="65b33-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

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

<span data-ttu-id="65b33-113">To polecenie umożliwia utworzenie reguły alertu metryki dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="65b33-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="65b33-114">$condition jest wyjściem polecenia cmdlet New-AzMetricAlertRuleV2Criteria, a $act jest wyjściem polecenia cmdlet New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="65b33-114">$condition is the output of New-AzMetricAlertRuleV2Criteria cmdlet and $act is the output of New-AzActionGroup cmdlet</span></span>

### <span data-ttu-id="65b33-115">Przykład 2: Dodawanie reguły alertu metryki dla wszystkich maszyn wirtualnych w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="65b33-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
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

<span data-ttu-id="65b33-116">To polecenie tworzy regułę alertu metryki dla wszystkich maszyn wirtualnych w subskrypcji, które znajdują się na Wschodzie.</span><span class="sxs-lookup"><span data-stu-id="65b33-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="65b33-117">Przykład 3: wyłączanie reguły alertu metryki</span><span class="sxs-lookup"><span data-stu-id="65b33-117">Example 3: Disable a metric alert rule</span></span>
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

<span data-ttu-id="65b33-118">To polecenie wyłącza regułę alertu o metryce.</span><span class="sxs-lookup"><span data-stu-id="65b33-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="65b33-119">Oto dane wyjściowe Get-AzMetricAlertRuleV2 do Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="65b33-119">Here, we are piping output of Get-AzMetricAlertRuleV2 to Add-AzMetricAlertRuleV2</span></span> 

### <span data-ttu-id="65b33-120">Przykład 4: Dodawanie reguły alertu metryki z wymiarami</span><span class="sxs-lookup"><span data-stu-id="65b33-120">Example 4: Add a metric alert rule with dimensions</span></span>

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

<span data-ttu-id="65b33-121">Aby utworzyć bardziej złożoną regułę alertu metryki, taką jak te, które obejmują Wybieranie wartości wymiaru lub mających wiele kryteriów, można użyć poleceń cmdlet pomocnik New-AzMetricAlertRuleV2DimensionSelection i New-AzMetricAlertRuleV2Criteria.</span><span class="sxs-lookup"><span data-stu-id="65b33-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets New-AzMetricAlertRuleV2DimensionSelection and New-AzMetricAlertRuleV2Criteria.</span></span>

<span data-ttu-id="65b33-122">Powyżej zestaw poleceń cmdlet utworzy regułę alertu metryki z wymiarami.</span><span class="sxs-lookup"><span data-stu-id="65b33-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>
## <span data-ttu-id="65b33-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65b33-123">PARAMETERS</span></span>

### <span data-ttu-id="65b33-124">-Action</span><span class="sxs-lookup"><span data-stu-id="65b33-124">-ActionGroup</span></span>
<span data-ttu-id="65b33-125">Grupa akcji dla reguły</span><span class="sxs-lookup"><span data-stu-id="65b33-125">The Action Group for rule</span></span>

```yaml
Type: ActivityLogAlertActionGroup[]
Parameter Sets: (All)
Aliases: Actions

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65b33-126">-Warunek</span><span class="sxs-lookup"><span data-stu-id="65b33-126">-Condition</span></span>
<span data-ttu-id="65b33-127">Warunek reguły</span><span class="sxs-lookup"><span data-stu-id="65b33-127">The condition for rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria]
Parameter Sets: (All)
Aliases: Criteria

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65b33-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65b33-128">-Confirm</span></span>
<span data-ttu-id="65b33-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65b33-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b33-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b33-130">-DefaultProfile</span></span>
<span data-ttu-id="65b33-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65b33-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65b33-132">— Opis</span><span class="sxs-lookup"><span data-stu-id="65b33-132">-Description</span></span>
<span data-ttu-id="65b33-133">Opis reguły alertu metryki</span><span class="sxs-lookup"><span data-stu-id="65b33-133">The description of the metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b33-134">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="65b33-134">-DisableRule</span></span>
<span data-ttu-id="65b33-135">Flaga Wyłącz regułę (stan)</span><span class="sxs-lookup"><span data-stu-id="65b33-135">The disable rule (status) flag</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b33-136">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="65b33-136">-Frequency</span></span>
<span data-ttu-id="65b33-137">Częstotliwość obliczania dla reguły</span><span class="sxs-lookup"><span data-stu-id="65b33-137">The evaluation frequency for rule</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: EvaluationFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b33-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65b33-138">-Name</span></span>
<span data-ttu-id="65b33-139">Nazwa reguły alertu metryki</span><span class="sxs-lookup"><span data-stu-id="65b33-139">The name of metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b33-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b33-140">-ResourceGroupName</span></span>
<span data-ttu-id="65b33-141">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="65b33-141">The Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b33-142">— Ważność</span><span class="sxs-lookup"><span data-stu-id="65b33-142">-Severity</span></span>
<span data-ttu-id="65b33-143">Ważność reguły alertu metryki</span><span class="sxs-lookup"><span data-stu-id="65b33-143">The severity for the metric alert rule</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b33-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="65b33-144">-TargetResourceId</span></span>
<span data-ttu-id="65b33-145">Identyfikator zasobu docelowego dla reguły</span><span class="sxs-lookup"><span data-stu-id="65b33-145">The target resource id for rule</span></span>

```yaml
Type: String
Parameter Sets: CreateAlertByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b33-146">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="65b33-146">-TargetResourceRegion</span></span>
<span data-ttu-id="65b33-147">Docelowy region zasobów dla reguły</span><span class="sxs-lookup"><span data-stu-id="65b33-147">The target resource region for rule</span></span>

```yaml
Type: String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b33-148">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="65b33-148">-TargetResourceScope</span></span>
<span data-ttu-id="65b33-149">Zakres zasobów docelowych dla reguły</span><span class="sxs-lookup"><span data-stu-id="65b33-149">The target resource scope for rule</span></span>

```yaml
Type: String[]
Parameter Sets: CreateAlertByScopes
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b33-150">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="65b33-150">-TargetResourceType</span></span>
<span data-ttu-id="65b33-151">Typ zasobu docelowego dla reguły</span><span class="sxs-lookup"><span data-stu-id="65b33-151">The target resource type for rule</span></span>

```yaml
Type: String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b33-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65b33-152">-WhatIf</span></span>
<span data-ttu-id="65b33-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65b33-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65b33-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65b33-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b33-155">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="65b33-155">-WindowSize</span></span>
<span data-ttu-id="65b33-156">Rozmiar okna reguły</span><span class="sxs-lookup"><span data-stu-id="65b33-156">The window size for rule</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b33-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b33-157">CommonParameters</span></span>
<span data-ttu-id="65b33-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65b33-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="65b33-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65b33-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b33-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65b33-160">INPUTS</span></span>

### <span data-ttu-id="65b33-161">System. String</span><span class="sxs-lookup"><span data-stu-id="65b33-161">System.String</span></span>

### <span data-ttu-id="65b33-162">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="65b33-162">System.TimeSpan</span></span>

### <span data-ttu-id="65b33-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="65b33-163">System.String[]</span></span>

### <span data-ttu-id="65b33-164">System. Collections. Generic. list "1 [[Microsoft. Azure. polecenia. info............ w. OutputClasses. PSMetricCriteria, Microsoft. Azure. PowerShell. cmdlets. Monitor, Version = 1.0.1.0</span><span class="sxs-lookup"><span data-stu-id="65b33-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="65b33-165">Microsoft. Azure. Management. Monitor. MODELES. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="65b33-165">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="65b33-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="65b33-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="65b33-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="65b33-167">System.Int32</span></span>

## <span data-ttu-id="65b33-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65b33-168">OUTPUTS</span></span>

### <span data-ttu-id="65b33-169">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="65b33-169">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="65b33-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65b33-170">NOTES</span></span>

## <span data-ttu-id="65b33-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65b33-171">RELATED LINKS</span></span>
