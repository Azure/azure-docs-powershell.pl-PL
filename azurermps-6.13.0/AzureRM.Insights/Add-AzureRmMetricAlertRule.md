---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 155a34133b9fa03c1f056fd65a0ec202fc0aed72
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716952"
---
# <span data-ttu-id="13447-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="13447-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="13447-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13447-102">SYNOPSIS</span></span>
<span data-ttu-id="13447-103">Umożliwia dodanie lub zaktualizowanie reguły alertu opartego na metrykach.</span><span class="sxs-lookup"><span data-stu-id="13447-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13447-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13447-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13447-105">Opis</span><span class="sxs-lookup"><span data-stu-id="13447-105">DESCRIPTION</span></span>
<span data-ttu-id="13447-106">Polecenie cmdlet **Add-AzureRmMetricAlertRule** umożliwia dodanie lub zaktualizowanie reguły alertu opartego na metrykach.</span><span class="sxs-lookup"><span data-stu-id="13447-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="13447-107">Dodana reguła jest skojarzona z grupą zasobów i ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="13447-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="13447-108">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="13447-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="13447-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13447-109">EXAMPLES</span></span>

### <span data-ttu-id="13447-110">Przykład 1: Dodawanie reguły alertu metryki do witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="13447-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="13447-111">To polecenie umożliwia utworzenie reguły alertu metryki dla witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="13447-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="13447-112">Przykład 2: wyłączanie reguły</span><span class="sxs-lookup"><span data-stu-id="13447-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="13447-113">To polecenie wyłącza regułę.</span><span class="sxs-lookup"><span data-stu-id="13447-113">This command disables a rule.</span></span>
<span data-ttu-id="13447-114">Jeśli reguła nie istnieje, zostanie ona wyłączona.</span><span class="sxs-lookup"><span data-stu-id="13447-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="13447-115">Jeśli reguła już istnieje, to po prostu jej wyłączenie.</span><span class="sxs-lookup"><span data-stu-id="13447-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="13447-116">Przykład 3: Dodawanie reguły za pomocą akcji</span><span class="sxs-lookup"><span data-stu-id="13447-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="13447-117">To polecenie umożliwia utworzenie reguły alertu metryki dla witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="13447-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="13447-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13447-118">PARAMETERS</span></span>

### <span data-ttu-id="13447-119">-Action</span><span class="sxs-lookup"><span data-stu-id="13447-119">-Action</span></span>
<span data-ttu-id="13447-120">Określa listę akcji rozdzielonych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="13447-120">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="13447-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13447-121">-DefaultProfile</span></span>
<span data-ttu-id="13447-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="13447-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13447-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="13447-123">-Description</span></span>
<span data-ttu-id="13447-124">Określa opis reguły.</span><span class="sxs-lookup"><span data-stu-id="13447-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="13447-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="13447-125">-DisableRule</span></span>
<span data-ttu-id="13447-126">Wyłącza regułę.</span><span class="sxs-lookup"><span data-stu-id="13447-126">Disables the rule.</span></span>
<span data-ttu-id="13447-127">Jeśli ten parametr nie jest określony, reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="13447-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="13447-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="13447-128">-Location</span></span>
<span data-ttu-id="13447-129">Określa lokalizację, w której zdefiniowana jest reguła.</span><span class="sxs-lookup"><span data-stu-id="13447-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="13447-130">-Metricname</span><span class="sxs-lookup"><span data-stu-id="13447-130">-MetricName</span></span>
<span data-ttu-id="13447-131">Określa nazwę metryki monitorowanej przez regułę.</span><span class="sxs-lookup"><span data-stu-id="13447-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="13447-132">Ten parametr można określić tylko dla reguł opartych na metrykach.</span><span class="sxs-lookup"><span data-stu-id="13447-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="13447-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13447-133">-Name</span></span>
<span data-ttu-id="13447-134">Określa nazwę reguły.</span><span class="sxs-lookup"><span data-stu-id="13447-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="13447-135">-Operator</span><span class="sxs-lookup"><span data-stu-id="13447-135">-Operator</span></span>
<span data-ttu-id="13447-136">Określa operator relacyjny warunku reguły.</span><span class="sxs-lookup"><span data-stu-id="13447-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="13447-137">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="13447-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="13447-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="13447-138">GreaterThan</span></span>
- <span data-ttu-id="13447-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="13447-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="13447-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="13447-140">LessThan</span></span>
- <span data-ttu-id="13447-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="13447-141">LessThanOrEqual</span></span>

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

### <span data-ttu-id="13447-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13447-142">-ResourceGroupName</span></span>
<span data-ttu-id="13447-143">Określa nazwę grupy zasobów dla reguły.</span><span class="sxs-lookup"><span data-stu-id="13447-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="13447-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="13447-144">-TargetResourceId</span></span>
<span data-ttu-id="13447-145">Określa identyfikator zasobu monitorującego regułę.</span><span class="sxs-lookup"><span data-stu-id="13447-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="13447-146">Uwaga: nie można zaktualizować tej właściwości dla istniejącej reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="13447-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="13447-147">-Próg</span><span class="sxs-lookup"><span data-stu-id="13447-147">-Threshold</span></span>
<span data-ttu-id="13447-148">Określa próg reguły.</span><span class="sxs-lookup"><span data-stu-id="13447-148">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="13447-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="13447-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="13447-150">Określa operator agregacji, który ma zostać zastosowany do przedziału czasu podczas szacowania reguły.</span><span class="sxs-lookup"><span data-stu-id="13447-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="13447-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="13447-151">-WindowSize</span></span>
<span data-ttu-id="13447-152">Określa rozmiar okna czasu dla reguły w celu obliczenia danych.</span><span class="sxs-lookup"><span data-stu-id="13447-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="13447-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13447-153">-Confirm</span></span>
<span data-ttu-id="13447-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13447-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13447-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13447-155">-WhatIf</span></span>
<span data-ttu-id="13447-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13447-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13447-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13447-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13447-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13447-158">CommonParameters</span></span>
<span data-ttu-id="13447-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13447-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13447-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13447-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13447-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13447-161">INPUTS</span></span>

### <span data-ttu-id="13447-162">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="13447-162">System.TimeSpan</span></span>

### <span data-ttu-id="13447-163">Microsoft. Azure. Management. Monitor. Management. models. ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="13447-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="13447-164">System. Double</span><span class="sxs-lookup"><span data-stu-id="13447-164">System.Double</span></span>

### <span data-ttu-id="13447-165">System. String</span><span class="sxs-lookup"><span data-stu-id="13447-165">System.String</span></span>

### <span data-ttu-id="13447-166">System. Nullable ' 1 [[Microsoft. Azure. Management. Monitor. Management. MODELES. TimeAggregationOperator, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="13447-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="13447-167">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="13447-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="13447-168">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Monitor. Management. model. RuleAction; Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="13447-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="13447-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13447-169">OUTPUTS</span></span>

### <span data-ttu-id="13447-170">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="13447-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="13447-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13447-171">NOTES</span></span>

## <span data-ttu-id="13447-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13447-172">RELATED LINKS</span></span>

[<span data-ttu-id="13447-173">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="13447-173">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="13447-174">Dodaj-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="13447-174">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="13447-175">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="13447-175">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="13447-176">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="13447-176">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="13447-177">Nowe — AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="13447-177">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="13447-178">Nowe — AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="13447-178">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="13447-179">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="13447-179">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


