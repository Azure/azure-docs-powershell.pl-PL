---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
ms.openlocfilehash: ed5649ead1c0e043ed3d97cb957d6b405967f450
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867367"
---
# <span data-ttu-id="70335-101">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="70335-101">Add-AzMetricAlertRule</span></span>

## <span data-ttu-id="70335-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70335-102">SYNOPSIS</span></span>
<span data-ttu-id="70335-103">Umożliwia dodanie lub zaktualizowanie reguły alertu opartego na metrykach.</span><span class="sxs-lookup"><span data-stu-id="70335-103">Adds or updates a metric-based alert rule.</span></span>

## <span data-ttu-id="70335-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70335-104">SYNTAX</span></span>

```
Add-AzMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70335-105">Opis</span><span class="sxs-lookup"><span data-stu-id="70335-105">DESCRIPTION</span></span>
<span data-ttu-id="70335-106">Polecenie cmdlet **Add-AzMetricAlertRule** umożliwia dodanie lub zaktualizowanie reguły alertu opartego na metrykach.</span><span class="sxs-lookup"><span data-stu-id="70335-106">The **Add-AzMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="70335-107">Dodana reguła jest skojarzona z grupą zasobów i ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="70335-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="70335-108">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="70335-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="70335-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70335-109">EXAMPLES</span></span>

### <span data-ttu-id="70335-110">Przykład 1: Dodawanie reguły alertu metryki do witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="70335-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="70335-111">To polecenie umożliwia utworzenie reguły alertu metryki dla witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="70335-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="70335-112">Przykład 2: wyłączanie reguły</span><span class="sxs-lookup"><span data-stu-id="70335-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="70335-113">To polecenie wyłącza regułę.</span><span class="sxs-lookup"><span data-stu-id="70335-113">This command disables a rule.</span></span>
<span data-ttu-id="70335-114">Jeśli reguła nie istnieje, zostanie ona wyłączona.</span><span class="sxs-lookup"><span data-stu-id="70335-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="70335-115">Jeśli reguła już istnieje, to po prostu jej wyłączenie.</span><span class="sxs-lookup"><span data-stu-id="70335-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="70335-116">Przykład 3: Dodawanie reguły za pomocą akcji</span><span class="sxs-lookup"><span data-stu-id="70335-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="70335-117">To polecenie umożliwia utworzenie reguły alertu metryki dla witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="70335-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="70335-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70335-118">PARAMETERS</span></span>

### <span data-ttu-id="70335-119">-Action</span><span class="sxs-lookup"><span data-stu-id="70335-119">-Action</span></span>
<span data-ttu-id="70335-120">Określa listę akcji rozdzielonych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="70335-120">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="70335-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70335-121">-DefaultProfile</span></span>
<span data-ttu-id="70335-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="70335-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70335-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="70335-123">-Description</span></span>
<span data-ttu-id="70335-124">Określa opis reguły.</span><span class="sxs-lookup"><span data-stu-id="70335-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="70335-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="70335-125">-DisableRule</span></span>
<span data-ttu-id="70335-126">Wyłącza regułę.</span><span class="sxs-lookup"><span data-stu-id="70335-126">Disables the rule.</span></span>
<span data-ttu-id="70335-127">Jeśli ten parametr nie jest określony, reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="70335-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="70335-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="70335-128">-Location</span></span>
<span data-ttu-id="70335-129">Określa lokalizację, w której zdefiniowana jest reguła.</span><span class="sxs-lookup"><span data-stu-id="70335-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="70335-130">-Metricname</span><span class="sxs-lookup"><span data-stu-id="70335-130">-MetricName</span></span>
<span data-ttu-id="70335-131">Określa nazwę metryki monitorowanej przez regułę.</span><span class="sxs-lookup"><span data-stu-id="70335-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="70335-132">Ten parametr można określić tylko dla reguł opartych na metrykach.</span><span class="sxs-lookup"><span data-stu-id="70335-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="70335-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70335-133">-Name</span></span>
<span data-ttu-id="70335-134">Określa nazwę reguły.</span><span class="sxs-lookup"><span data-stu-id="70335-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="70335-135">-Operator</span><span class="sxs-lookup"><span data-stu-id="70335-135">-Operator</span></span>
<span data-ttu-id="70335-136">Określa operator relacyjny warunku reguły.</span><span class="sxs-lookup"><span data-stu-id="70335-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="70335-137">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="70335-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="70335-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="70335-138">GreaterThan</span></span>
- <span data-ttu-id="70335-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="70335-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="70335-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="70335-140">LessThan</span></span>
- <span data-ttu-id="70335-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="70335-141">LessThanOrEqual</span></span>

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

### <span data-ttu-id="70335-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70335-142">-ResourceGroupName</span></span>
<span data-ttu-id="70335-143">Określa nazwę grupy zasobów dla reguły.</span><span class="sxs-lookup"><span data-stu-id="70335-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="70335-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="70335-144">-TargetResourceId</span></span>
<span data-ttu-id="70335-145">Określa identyfikator zasobu monitorującego regułę.</span><span class="sxs-lookup"><span data-stu-id="70335-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="70335-146">Uwaga: nie można zaktualizować tej właściwości dla istniejącej reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="70335-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="70335-147">-Próg</span><span class="sxs-lookup"><span data-stu-id="70335-147">-Threshold</span></span>
<span data-ttu-id="70335-148">Określa próg reguły.</span><span class="sxs-lookup"><span data-stu-id="70335-148">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="70335-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="70335-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="70335-150">Określa operator agregacji, który ma zostać zastosowany do przedziału czasu podczas szacowania reguły.</span><span class="sxs-lookup"><span data-stu-id="70335-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="70335-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="70335-151">-WindowSize</span></span>
<span data-ttu-id="70335-152">Określa rozmiar okna czasu dla reguły w celu obliczenia danych.</span><span class="sxs-lookup"><span data-stu-id="70335-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="70335-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70335-153">-Confirm</span></span>
<span data-ttu-id="70335-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70335-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70335-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70335-155">-WhatIf</span></span>
<span data-ttu-id="70335-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70335-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70335-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="70335-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70335-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70335-158">CommonParameters</span></span>
<span data-ttu-id="70335-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70335-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70335-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70335-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70335-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70335-161">INPUTS</span></span>

### <span data-ttu-id="70335-162">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="70335-162">System.TimeSpan</span></span>

### <span data-ttu-id="70335-163">Microsoft. Azure. Management. Monitor. Management. models. ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="70335-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="70335-164">System. Double</span><span class="sxs-lookup"><span data-stu-id="70335-164">System.Double</span></span>

### <span data-ttu-id="70335-165">System. String</span><span class="sxs-lookup"><span data-stu-id="70335-165">System.String</span></span>

### <span data-ttu-id="70335-166">System. Nullable ' 1 [[Microsoft. Azure. Management. Monitor. Management. MODELES. TimeAggregationOperator, Microsoft. Azure. PowerShell. cmdlets. Monitor, wersja = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="70335-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="70335-167">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="70335-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="70335-168">System. Collections. Generic. list "1 [[Microsoft. Azure. Management. Monitor. Management.. RuleAction; Microsoft. Azure. PowerShell. cmdlets.</span><span class="sxs-lookup"><span data-stu-id="70335-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="70335-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70335-169">OUTPUTS</span></span>

### <span data-ttu-id="70335-170">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="70335-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="70335-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70335-171">NOTES</span></span>

## <span data-ttu-id="70335-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70335-172">RELATED LINKS</span></span>

[<span data-ttu-id="70335-173">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="70335-173">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="70335-174">Dodaj-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="70335-174">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="70335-175">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="70335-175">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="70335-176">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="70335-176">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

[<span data-ttu-id="70335-177">Nowe — AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="70335-177">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="70335-178">Nowe — AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="70335-178">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

[<span data-ttu-id="70335-179">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="70335-179">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


