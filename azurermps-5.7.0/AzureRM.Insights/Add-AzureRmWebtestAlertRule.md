---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: da395b66cb4d63593c097f214701365370e06b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544300"
---
# <span data-ttu-id="e42eb-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e42eb-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="e42eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e42eb-102">SYNOPSIS</span></span>
<span data-ttu-id="e42eb-103">Umożliwia dodanie lub zaktualizowanie reguły alertu WebTest.</span><span class="sxs-lookup"><span data-stu-id="e42eb-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e42eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e42eb-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e42eb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e42eb-105">DESCRIPTION</span></span>
<span data-ttu-id="e42eb-106">Polecenie cmdlet **Add-AzureRmWebtestAlertRule** umożliwia dodanie lub zaktualizowanie reguły alertu o typie Metryka, zdarzenie lub WebTest.</span><span class="sxs-lookup"><span data-stu-id="e42eb-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="e42eb-107">Dodana reguła jest skojarzona z grupą zasobów i ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="e42eb-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="e42eb-108">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="e42eb-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e42eb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e42eb-109">EXAMPLES</span></span>

### <span data-ttu-id="e42eb-110">Przykład 1: Dodawanie reguły alertu WebTest</span><span class="sxs-lookup"><span data-stu-id="e42eb-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="e42eb-111">To polecenie umożliwia dodanie lub zaktualizowanie reguły alertu WebTest.</span><span class="sxs-lookup"><span data-stu-id="e42eb-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="e42eb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e42eb-112">PARAMETERS</span></span>

### <span data-ttu-id="e42eb-113">-Action</span><span class="sxs-lookup"><span data-stu-id="e42eb-113">-Action</span></span>
<span data-ttu-id="e42eb-114">Określa listę akcji rozdzielonych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="e42eb-114">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42eb-115">-DefaultProfile</span></span>
<span data-ttu-id="e42eb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e42eb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42eb-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="e42eb-117">-Description</span></span>
<span data-ttu-id="e42eb-118">Określa opis reguły.</span><span class="sxs-lookup"><span data-stu-id="e42eb-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="e42eb-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="e42eb-119">-DisableRule</span></span>
<span data-ttu-id="e42eb-120">Wyłącza regułę.</span><span class="sxs-lookup"><span data-stu-id="e42eb-120">Disables the rule.</span></span>
<span data-ttu-id="e42eb-121">Jeśli ten parametr nie jest określony, reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="e42eb-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="e42eb-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="e42eb-122">-FailedLocationCount</span></span>
<span data-ttu-id="e42eb-123">Określa liczbę niepomyślnych lokalizacji reguł WebTest.</span><span class="sxs-lookup"><span data-stu-id="e42eb-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="e42eb-124">Jest to podobne do progu w innych typach reguł.</span><span class="sxs-lookup"><span data-stu-id="e42eb-124">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="e42eb-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e42eb-125">-Location</span></span>
<span data-ttu-id="e42eb-126">Określa lokalizację, w której zdefiniowana jest reguła.</span><span class="sxs-lookup"><span data-stu-id="e42eb-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="e42eb-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="e42eb-127">-MetricName</span></span>
<span data-ttu-id="e42eb-128">Określa nazwę metryki.</span><span class="sxs-lookup"><span data-stu-id="e42eb-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="e42eb-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="e42eb-129">-MetricNamespace</span></span>
<span data-ttu-id="e42eb-130">Określa obszar nazw metryki dla reguły.</span><span class="sxs-lookup"><span data-stu-id="e42eb-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="e42eb-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e42eb-131">-Name</span></span>
<span data-ttu-id="e42eb-132">Określa nazwę reguły.</span><span class="sxs-lookup"><span data-stu-id="e42eb-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="e42eb-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e42eb-133">-ResourceGroupName</span></span>
<span data-ttu-id="e42eb-134">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e42eb-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e42eb-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="e42eb-135">-TargetResourceUri</span></span>
<span data-ttu-id="e42eb-136">Określa identyfikator zasobu WebTest.</span><span class="sxs-lookup"><span data-stu-id="e42eb-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="e42eb-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="e42eb-137">-WindowSize</span></span>
<span data-ttu-id="e42eb-138">Określa rozmiar okna czasu dla reguły w celu obliczenia danych.</span><span class="sxs-lookup"><span data-stu-id="e42eb-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="e42eb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42eb-139">CommonParameters</span></span>
<span data-ttu-id="e42eb-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e42eb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42eb-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e42eb-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42eb-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e42eb-142">INPUTS</span></span>

### <span data-ttu-id="e42eb-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e42eb-143">None</span></span>
<span data-ttu-id="e42eb-144">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e42eb-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e42eb-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e42eb-145">OUTPUTS</span></span>

### <span data-ttu-id="e42eb-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e42eb-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="e42eb-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e42eb-147">NOTES</span></span>

## <span data-ttu-id="e42eb-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e42eb-148">RELATED LINKS</span></span>

[<span data-ttu-id="e42eb-149">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e42eb-149">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e42eb-150">Dodaj-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e42eb-150">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="e42eb-151">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="e42eb-151">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="e42eb-152">Nowe — AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e42eb-152">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


