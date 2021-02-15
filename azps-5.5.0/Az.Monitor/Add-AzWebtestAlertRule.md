---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: 043bb0e0b3c5fac61407eaca3d20c82ebe483037
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203545"
---
# <span data-ttu-id="d07ad-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="d07ad-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="d07ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d07ad-102">SYNOPSIS</span></span>
<span data-ttu-id="d07ad-103">Dodaje lub aktualizuje regułę alertu testu sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d07ad-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="d07ad-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d07ad-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d07ad-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d07ad-105">DESCRIPTION</span></span>
<span data-ttu-id="d07ad-106">Polecenie **cmdlet Add-AzWebtestAlertRule** dodaje lub aktualizuje regułę alertu o typie metryki, zdarzenia lub testu sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d07ad-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="d07ad-107">Dodana reguła jest skojarzona z grupą zasobów i ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="d07ad-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="d07ad-108">To polecenie cmdlet implementuje wzorzec ShouldProcess, czyli może wymagać potwierdzenia od użytkownika przed utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="d07ad-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="d07ad-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d07ad-109">EXAMPLES</span></span>

### <span data-ttu-id="d07ad-110">Przykład 1. Dodawanie reguły alertu testu sieci Web</span><span class="sxs-lookup"><span data-stu-id="d07ad-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="d07ad-111">To polecenie dodaje lub aktualizuje regułę alertu testu sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d07ad-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="d07ad-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d07ad-112">PARAMETERS</span></span>

### <span data-ttu-id="d07ad-113">— akcja</span><span class="sxs-lookup"><span data-stu-id="d07ad-113">-Action</span></span>
<span data-ttu-id="d07ad-114">Określa rozdzieloną przecinkami listę akcji.</span><span class="sxs-lookup"><span data-stu-id="d07ad-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="d07ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d07ad-115">-DefaultProfile</span></span>
<span data-ttu-id="d07ad-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d07ad-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d07ad-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="d07ad-117">-Description</span></span>
<span data-ttu-id="d07ad-118">Określa opis reguły.</span><span class="sxs-lookup"><span data-stu-id="d07ad-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="d07ad-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="d07ad-119">-DisableRule</span></span>
<span data-ttu-id="d07ad-120">Wyłącza regułę.</span><span class="sxs-lookup"><span data-stu-id="d07ad-120">Disables the rule.</span></span>
<span data-ttu-id="d07ad-121">Jeśli nie określisz tego parametru, reguła zostanie włączona.</span><span class="sxs-lookup"><span data-stu-id="d07ad-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="d07ad-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="d07ad-122">-FailedLocationCount</span></span>
<span data-ttu-id="d07ad-123">Określa liczbę lokalizacji, dla których nie powiodło się, dla reguł testów sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d07ad-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="d07ad-124">Jest to podobne do progu w innych typach reguł.</span><span class="sxs-lookup"><span data-stu-id="d07ad-124">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="d07ad-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d07ad-125">-Location</span></span>
<span data-ttu-id="d07ad-126">Określa lokalizację, w której jest zdefiniowana reguła.</span><span class="sxs-lookup"><span data-stu-id="d07ad-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="d07ad-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="d07ad-127">-MetricName</span></span>
<span data-ttu-id="d07ad-128">Określa nazwę metryki.</span><span class="sxs-lookup"><span data-stu-id="d07ad-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="d07ad-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="d07ad-129">-MetricNamespace</span></span>
<span data-ttu-id="d07ad-130">Określa metryczna przestrzeń nazw reguły.</span><span class="sxs-lookup"><span data-stu-id="d07ad-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="d07ad-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d07ad-131">-Name</span></span>
<span data-ttu-id="d07ad-132">Określa nazwę reguły.</span><span class="sxs-lookup"><span data-stu-id="d07ad-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="d07ad-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d07ad-133">-ResourceGroupName</span></span>
<span data-ttu-id="d07ad-134">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d07ad-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d07ad-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="d07ad-135">-TargetResourceUri</span></span>
<span data-ttu-id="d07ad-136">Określa identyfikator zasobu testu sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d07ad-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="d07ad-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="d07ad-137">-WindowSize</span></span>
<span data-ttu-id="d07ad-138">Określa rozmiar okna czasowego reguły obliczania danych.</span><span class="sxs-lookup"><span data-stu-id="d07ad-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="d07ad-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d07ad-139">-Confirm</span></span>
<span data-ttu-id="d07ad-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d07ad-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d07ad-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d07ad-141">-WhatIf</span></span>
<span data-ttu-id="d07ad-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d07ad-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d07ad-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d07ad-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d07ad-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d07ad-144">CommonParameters</span></span>
<span data-ttu-id="d07ad-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d07ad-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d07ad-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d07ad-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d07ad-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d07ad-147">INPUTS</span></span>

### <span data-ttu-id="d07ad-148">System.String</span><span class="sxs-lookup"><span data-stu-id="d07ad-148">System.String</span></span>

### <span data-ttu-id="d07ad-149">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="d07ad-149">System.TimeSpan</span></span>

### <span data-ttu-id="d07ad-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d07ad-150">System.Int32</span></span>

### <span data-ttu-id="d07ad-151">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="d07ad-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d07ad-152">System.Collections.generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlet.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="d07ad-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d07ad-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d07ad-153">OUTPUTS</span></span>

### <span data-ttu-id="d07ad-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d07ad-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="d07ad-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d07ad-155">NOTES</span></span>

## <span data-ttu-id="d07ad-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d07ad-156">RELATED LINKS</span></span>

[<span data-ttu-id="d07ad-157">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d07ad-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="d07ad-158">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="d07ad-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="d07ad-159">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="d07ad-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="d07ad-160">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="d07ad-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


