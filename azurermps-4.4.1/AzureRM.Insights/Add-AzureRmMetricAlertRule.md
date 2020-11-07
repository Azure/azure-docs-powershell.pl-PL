---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 9a215195ada1d804d2c139ed748eb844df46eed5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719301"
---
# <span data-ttu-id="5d8ae-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="5d8ae-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="5d8ae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="5d8ae-103">Umożliwia dodanie lub zaktualizowanie reguły alertu opartego na metrykach.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d8ae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d8ae-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d8ae-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5d8ae-105">DESCRIPTION</span></span>
<span data-ttu-id="5d8ae-106">Polecenie cmdlet **Add-AzureRmMetricAlertRule** umożliwia dodanie lub zaktualizowanie reguły alertu opartego na metrykach.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="5d8ae-107">Dodana reguła jest skojarzona z grupą zasobów i ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-107">The added rule is associated with a resource group and has a name.</span></span>

## <span data-ttu-id="5d8ae-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d8ae-108">EXAMPLES</span></span>

### <span data-ttu-id="5d8ae-109">Przykład 1: Dodawanie reguły alertu metryki do witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="5d8ae-109">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="5d8ae-110">To polecenie umożliwia utworzenie reguły alertu metryki dla witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-110">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="5d8ae-111">Przykład 2: wyłączanie reguły</span><span class="sxs-lookup"><span data-stu-id="5d8ae-111">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="5d8ae-112">To polecenie wyłącza regułę.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-112">This command disables a rule.</span></span>
<span data-ttu-id="5d8ae-113">Jeśli reguła nie istnieje, zostanie ona wyłączona.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-113">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="5d8ae-114">Jeśli reguła już istnieje, to po prostu jej wyłączenie.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-114">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="5d8ae-115">Przykład 3: Dodawanie reguły za pomocą akcji</span><span class="sxs-lookup"><span data-stu-id="5d8ae-115">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="5d8ae-116">To polecenie umożliwia utworzenie reguły alertu metryki dla witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-116">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="5d8ae-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d8ae-117">PARAMETERS</span></span>

### <span data-ttu-id="5d8ae-118">-Akcje</span><span class="sxs-lookup"><span data-stu-id="5d8ae-118">-Actions</span></span>
<span data-ttu-id="5d8ae-119">Określa listę akcji rozdzielonych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-119">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="5d8ae-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="5d8ae-120">-Description</span></span>
<span data-ttu-id="5d8ae-121">Określa opis reguły.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-121">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="5d8ae-122">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="5d8ae-122">-DisableRule</span></span>
<span data-ttu-id="5d8ae-123">Wyłącza regułę.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-123">Disables the rule.</span></span>
<span data-ttu-id="5d8ae-124">Jeśli ten parametr nie jest określony, reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-124">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="5d8ae-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5d8ae-125">-Location</span></span>
<span data-ttu-id="5d8ae-126">Określa lokalizację, w której zdefiniowana jest reguła.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="5d8ae-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="5d8ae-127">-MetricName</span></span>
<span data-ttu-id="5d8ae-128">Określa nazwę metryki monitorowanej przez regułę.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-128">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="5d8ae-129">Ten parametr można określić tylko dla reguł opartych na metrykach.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-129">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="5d8ae-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5d8ae-130">-Name</span></span>
<span data-ttu-id="5d8ae-131">Określa nazwę reguły.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-131">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="5d8ae-132">-Operator</span><span class="sxs-lookup"><span data-stu-id="5d8ae-132">-Operator</span></span>
<span data-ttu-id="5d8ae-133">Określa operator relacyjny warunku reguły.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-133">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="5d8ae-134">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5d8ae-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5d8ae-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="5d8ae-135">GreaterThan</span></span>
- <span data-ttu-id="5d8ae-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="5d8ae-136">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="5d8ae-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="5d8ae-137">LessThan</span></span>
- <span data-ttu-id="5d8ae-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="5d8ae-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="5d8ae-139">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5d8ae-139">-ResourceGroup</span></span>
<span data-ttu-id="5d8ae-140">Określa nazwę grupy zasobów dla reguły.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-140">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="5d8ae-141">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="5d8ae-141">-TargetResourceId</span></span>
<span data-ttu-id="5d8ae-142">Określa identyfikator zasobu monitorującego regułę.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-142">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="5d8ae-143">Uwaga: nie można zaktualizować tej właściwości dla istniejącej reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-143">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="5d8ae-144">-Próg</span><span class="sxs-lookup"><span data-stu-id="5d8ae-144">-Threshold</span></span>
<span data-ttu-id="5d8ae-145">Określa próg reguły.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-145">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="5d8ae-146">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="5d8ae-146">-TimeAggregationOperator</span></span>
<span data-ttu-id="5d8ae-147">Określa operator agregacji, który ma zostać zastosowany do przedziału czasu podczas szacowania reguły.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-147">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="5d8ae-148">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="5d8ae-148">-WindowSize</span></span>
<span data-ttu-id="5d8ae-149">Określa rozmiar okna czasu dla reguły w celu obliczenia danych.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-149">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="5d8ae-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d8ae-150">-DefaultProfile</span></span>
<span data-ttu-id="5d8ae-151">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d8ae-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d8ae-152">CommonParameters</span></span>
<span data-ttu-id="5d8ae-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d8ae-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d8ae-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d8ae-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d8ae-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d8ae-155">INPUTS</span></span>

## <span data-ttu-id="5d8ae-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d8ae-156">OUTPUTS</span></span>

### <span data-ttu-id="5d8ae-157">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5d8ae-157">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="5d8ae-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d8ae-158">NOTES</span></span>

## <span data-ttu-id="5d8ae-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d8ae-159">RELATED LINKS</span></span>

[<span data-ttu-id="5d8ae-160">Dodaj-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="5d8ae-160">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="5d8ae-161">Dodaj-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="5d8ae-161">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="5d8ae-162">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="5d8ae-162">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="5d8ae-163">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="5d8ae-163">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="5d8ae-164">Nowe — AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="5d8ae-164">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="5d8ae-165">Nowe — AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="5d8ae-165">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="5d8ae-166">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="5d8ae-166">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


