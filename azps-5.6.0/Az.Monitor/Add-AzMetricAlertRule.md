---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
ms.openlocfilehash: a38dbb3e608390369a31d9376923328d9550cbd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980273"
---
# <span data-ttu-id="f5203-101">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="f5203-101">Add-AzMetricAlertRule</span></span>

## <span data-ttu-id="f5203-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5203-102">SYNOPSIS</span></span>
<span data-ttu-id="f5203-103">Dodaje lub aktualizuje regułę alertów opartą na metrykach.</span><span class="sxs-lookup"><span data-stu-id="f5203-103">Adds or updates a metric-based alert rule.</span></span>

## <span data-ttu-id="f5203-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f5203-104">SYNTAX</span></span>

```
Add-AzMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5203-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f5203-105">DESCRIPTION</span></span>
<span data-ttu-id="f5203-106">Polecenie **cmdlet Add-AzMetricAlertRule** dodaje lub aktualizuje regułę alertu opartą na metryki.</span><span class="sxs-lookup"><span data-stu-id="f5203-106">The **Add-AzMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="f5203-107">Dodana reguła jest skojarzona z grupą zasobów i ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="f5203-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="f5203-108">To polecenie cmdlet implementuje wzorzec ShouldProcess, czyli może wymagać potwierdzenia od użytkownika przed utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="f5203-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f5203-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f5203-109">EXAMPLES</span></span>

### <span data-ttu-id="f5203-110">Przykład 1. Dodawanie reguły alertu metryczne do witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="f5203-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="f5203-111">To polecenie tworzy regułę alertu metryczne dla witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f5203-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="f5203-112">Przykład 2. Wyłączanie reguły</span><span class="sxs-lookup"><span data-stu-id="f5203-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="f5203-113">To polecenie wyłącza regułę.</span><span class="sxs-lookup"><span data-stu-id="f5203-113">This command disables a rule.</span></span>
<span data-ttu-id="f5203-114">Jeśli reguła nie istnieje, zostanie wyłączona.</span><span class="sxs-lookup"><span data-stu-id="f5203-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="f5203-115">Jeśli reguła istnieje, zostanie ona po prostu zablokowana.</span><span class="sxs-lookup"><span data-stu-id="f5203-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="f5203-116">Przykład 3. Dodawanie reguły z akcjami</span><span class="sxs-lookup"><span data-stu-id="f5203-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="f5203-117">To polecenie tworzy regułę alertu metryczne dla witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f5203-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="f5203-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5203-118">PARAMETERS</span></span>

### <span data-ttu-id="f5203-119">— Akcja</span><span class="sxs-lookup"><span data-stu-id="f5203-119">-Action</span></span>
<span data-ttu-id="f5203-120">Określa rozdzieloną przecinkami listę akcji.</span><span class="sxs-lookup"><span data-stu-id="f5203-120">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5203-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5203-121">-DefaultProfile</span></span>
<span data-ttu-id="f5203-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f5203-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5203-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="f5203-123">-Description</span></span>
<span data-ttu-id="f5203-124">Określa opis reguły.</span><span class="sxs-lookup"><span data-stu-id="f5203-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="f5203-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="f5203-125">-DisableRule</span></span>
<span data-ttu-id="f5203-126">Wyłącza regułę.</span><span class="sxs-lookup"><span data-stu-id="f5203-126">Disables the rule.</span></span>
<span data-ttu-id="f5203-127">Jeśli nie określisz tego parametru, reguła zostanie włączona.</span><span class="sxs-lookup"><span data-stu-id="f5203-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="f5203-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f5203-128">-Location</span></span>
<span data-ttu-id="f5203-129">Określa lokalizację, w której jest zdefiniowana reguła.</span><span class="sxs-lookup"><span data-stu-id="f5203-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="f5203-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="f5203-130">-MetricName</span></span>
<span data-ttu-id="f5203-131">Określa nazwę metryki, która jest monitorowana przez regułę.</span><span class="sxs-lookup"><span data-stu-id="f5203-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="f5203-132">Określ ten parametr tylko dla reguł opartych na metrykach.</span><span class="sxs-lookup"><span data-stu-id="f5203-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="f5203-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f5203-133">-Name</span></span>
<span data-ttu-id="f5203-134">Określa nazwę reguły.</span><span class="sxs-lookup"><span data-stu-id="f5203-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="f5203-135">-Operator</span><span class="sxs-lookup"><span data-stu-id="f5203-135">-Operator</span></span>
<span data-ttu-id="f5203-136">Określa operator relacyjnych warunku reguły.</span><span class="sxs-lookup"><span data-stu-id="f5203-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="f5203-137">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f5203-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f5203-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="f5203-138">GreaterThan</span></span>
- <span data-ttu-id="f5203-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="f5203-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="f5203-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="f5203-140">LessThan</span></span>
- <span data-ttu-id="f5203-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="f5203-141">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5203-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5203-142">-ResourceGroupName</span></span>
<span data-ttu-id="f5203-143">Określa nazwę grupy zasobów reguły.</span><span class="sxs-lookup"><span data-stu-id="f5203-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="f5203-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f5203-144">-TargetResourceId</span></span>
<span data-ttu-id="f5203-145">Określa identyfikator zasobu, który jest monitorowyny przez regułę.</span><span class="sxs-lookup"><span data-stu-id="f5203-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="f5203-146">UWAGA: Tej właściwości nie można zaktualizować dla istniejącej reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="f5203-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="f5203-147">— próg</span><span class="sxs-lookup"><span data-stu-id="f5203-147">-Threshold</span></span>
<span data-ttu-id="f5203-148">Określa próg reguły.</span><span class="sxs-lookup"><span data-stu-id="f5203-148">Specifies the threshold of the rule.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5203-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="f5203-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="f5203-150">Określa operator agregacji do zastosowania w oknie czasowym podczas oceny reguły.</span><span class="sxs-lookup"><span data-stu-id="f5203-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator]
Parameter Sets: (All)
Aliases:
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5203-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="f5203-151">-WindowSize</span></span>
<span data-ttu-id="f5203-152">Określa rozmiar okna czasowego reguły obliczania danych.</span><span class="sxs-lookup"><span data-stu-id="f5203-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="f5203-153">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f5203-153">-Confirm</span></span>
<span data-ttu-id="f5203-154">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f5203-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5203-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5203-155">-WhatIf</span></span>
<span data-ttu-id="f5203-156">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5203-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5203-157">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f5203-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5203-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5203-158">CommonParameters</span></span>
<span data-ttu-id="f5203-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5203-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5203-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5203-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5203-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5203-161">INPUTS</span></span>

### <span data-ttu-id="f5203-162">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="f5203-162">System.TimeSpan</span></span>

### <span data-ttu-id="f5203-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="f5203-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="f5203-164">System.Double</span><span class="sxs-lookup"><span data-stu-id="f5203-164">System.Double</span></span>

### <span data-ttu-id="f5203-165">System.String</span><span class="sxs-lookup"><span data-stu-id="f5203-165">System.String</span></span>

### <span data-ttu-id="f5203-166">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlet.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f5203-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f5203-167">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="f5203-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f5203-168">System.Collections.generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlet.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f5203-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f5203-169">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5203-169">OUTPUTS</span></span>

### <span data-ttu-id="f5203-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f5203-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="f5203-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f5203-171">NOTES</span></span>

## <span data-ttu-id="f5203-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5203-172">RELATED LINKS</span></span>

[<span data-ttu-id="f5203-173">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f5203-173">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="f5203-174">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="f5203-174">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="f5203-175">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="f5203-175">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="f5203-176">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="f5203-176">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

[<span data-ttu-id="f5203-177">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="f5203-177">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="f5203-178">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="f5203-178">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

[<span data-ttu-id="f5203-179">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="f5203-179">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


