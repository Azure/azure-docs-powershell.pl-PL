---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: 08d84c1f5e71c18a47e48bda1e39ce37ed0cb026
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717196"
---
# <span data-ttu-id="ad9d8-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="ad9d8-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="ad9d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad9d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ad9d8-103">Umożliwia dodanie lub zaktualizowanie reguły alertu WebTest.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad9d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad9d8-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad9d8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad9d8-105">DESCRIPTION</span></span>
<span data-ttu-id="ad9d8-106">Polecenie cmdlet **Add-AzureRmWebtestAlertRule** umożliwia dodanie lub zaktualizowanie reguły alertu o typie Metryka, zdarzenie lub WebTest.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="ad9d8-107">Dodana reguła jest skojarzona z grupą zasobów i ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="ad9d8-108">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="ad9d8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad9d8-109">EXAMPLES</span></span>

### <span data-ttu-id="ad9d8-110">Przykład 1: Dodawanie reguły alertu WebTest</span><span class="sxs-lookup"><span data-stu-id="ad9d8-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="ad9d8-111">To polecenie umożliwia dodanie lub zaktualizowanie reguły alertu WebTest.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="ad9d8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad9d8-112">PARAMETERS</span></span>

### <span data-ttu-id="ad9d8-113">-Action</span><span class="sxs-lookup"><span data-stu-id="ad9d8-113">-Action</span></span>
<span data-ttu-id="ad9d8-114">Określa listę akcji rozdzielonych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="ad9d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad9d8-115">-DefaultProfile</span></span>
<span data-ttu-id="ad9d8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ad9d8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad9d8-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="ad9d8-117">-Description</span></span>
<span data-ttu-id="ad9d8-118">Określa opis reguły.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="ad9d8-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="ad9d8-119">-DisableRule</span></span>
<span data-ttu-id="ad9d8-120">Wyłącza regułę.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-120">Disables the rule.</span></span>
<span data-ttu-id="ad9d8-121">Jeśli ten parametr nie jest określony, reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="ad9d8-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="ad9d8-122">-FailedLocationCount</span></span>
<span data-ttu-id="ad9d8-123">Określa liczbę niepomyślnych lokalizacji reguł WebTest.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="ad9d8-124">Jest to podobne do progu w innych typach reguł.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-124">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="ad9d8-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ad9d8-125">-Location</span></span>
<span data-ttu-id="ad9d8-126">Określa lokalizację, w której zdefiniowana jest reguła.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="ad9d8-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="ad9d8-127">-MetricName</span></span>
<span data-ttu-id="ad9d8-128">Określa nazwę metryki.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="ad9d8-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="ad9d8-129">-MetricNamespace</span></span>
<span data-ttu-id="ad9d8-130">Określa obszar nazw metryki dla reguły.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="ad9d8-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad9d8-131">-Name</span></span>
<span data-ttu-id="ad9d8-132">Określa nazwę reguły.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="ad9d8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad9d8-133">-ResourceGroupName</span></span>
<span data-ttu-id="ad9d8-134">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ad9d8-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="ad9d8-135">-TargetResourceUri</span></span>
<span data-ttu-id="ad9d8-136">Określa identyfikator zasobu WebTest.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="ad9d8-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="ad9d8-137">-WindowSize</span></span>
<span data-ttu-id="ad9d8-138">Określa rozmiar okna czasu dla reguły w celu obliczenia danych.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="ad9d8-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad9d8-139">-Confirm</span></span>
<span data-ttu-id="ad9d8-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad9d8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad9d8-141">-WhatIf</span></span>
<span data-ttu-id="ad9d8-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad9d8-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad9d8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad9d8-144">CommonParameters</span></span>
<span data-ttu-id="ad9d8-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad9d8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad9d8-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad9d8-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad9d8-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad9d8-147">INPUTS</span></span>

### <span data-ttu-id="ad9d8-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ad9d8-148">System.String</span></span>

### <span data-ttu-id="ad9d8-149">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="ad9d8-149">System.TimeSpan</span></span>

### <span data-ttu-id="ad9d8-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ad9d8-150">System.Int32</span></span>

### <span data-ttu-id="ad9d8-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ad9d8-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ad9d8-152">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Monitor. Management. model. RuleAction; Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ad9d8-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ad9d8-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad9d8-153">OUTPUTS</span></span>

### <span data-ttu-id="ad9d8-154">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ad9d8-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="ad9d8-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad9d8-155">NOTES</span></span>

## <span data-ttu-id="ad9d8-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad9d8-156">RELATED LINKS</span></span>

[<span data-ttu-id="ad9d8-157">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ad9d8-157">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ad9d8-158">Dodaj-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="ad9d8-158">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="ad9d8-159">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="ad9d8-159">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="ad9d8-160">Nowe — AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="ad9d8-160">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


