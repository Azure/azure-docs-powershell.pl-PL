---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: 52b3d39aef4c117fe8b26bb35f1bf50143e5fec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553869"
---
# <span data-ttu-id="bf1bd-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="bf1bd-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="bf1bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="bf1bd-103">Umożliwia dodanie lub zaktualizowanie reguły alertu WebTest.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf1bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf1bd-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf1bd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bf1bd-105">DESCRIPTION</span></span>
<span data-ttu-id="bf1bd-106">Polecenie cmdlet **Add-AzureRmWebtestAlertRule** umożliwia dodanie lub zaktualizowanie reguły alertu o typie Metryka, zdarzenie lub WebTest.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="bf1bd-107">Dodana reguła jest skojarzona z grupą zasobów i ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-107">The added rule is associated to a resource group and has a name.</span></span>

## <span data-ttu-id="bf1bd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf1bd-108">EXAMPLES</span></span>

### <span data-ttu-id="bf1bd-109">Przykład 1: Dodawanie reguły alertu WebTest</span><span class="sxs-lookup"><span data-stu-id="bf1bd-109">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="bf1bd-110">To polecenie umożliwia dodanie lub zaktualizowanie reguły alertu WebTest.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-110">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="bf1bd-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf1bd-111">PARAMETERS</span></span>

### <span data-ttu-id="bf1bd-112">-Akcje</span><span class="sxs-lookup"><span data-stu-id="bf1bd-112">-Actions</span></span>
<span data-ttu-id="bf1bd-113">Określa listę akcji rozdzielonych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-113">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="bf1bd-114">— Opis</span><span class="sxs-lookup"><span data-stu-id="bf1bd-114">-Description</span></span>
<span data-ttu-id="bf1bd-115">Określa opis reguły.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-115">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="bf1bd-116">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="bf1bd-116">-DisableRule</span></span>
<span data-ttu-id="bf1bd-117">Wyłącza regułę.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-117">Disables the rule.</span></span>
<span data-ttu-id="bf1bd-118">Jeśli ten parametr nie jest określony, reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-118">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="bf1bd-119">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="bf1bd-119">-FailedLocationCount</span></span>
<span data-ttu-id="bf1bd-120">Określa liczbę niepomyślnych lokalizacji reguł WebTest.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-120">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="bf1bd-121">Jest to podobne do progu w innych typach reguł.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-121">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="bf1bd-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bf1bd-122">-Location</span></span>
<span data-ttu-id="bf1bd-123">Określa lokalizację, w której zdefiniowana jest reguła.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-123">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="bf1bd-124">-Metricname</span><span class="sxs-lookup"><span data-stu-id="bf1bd-124">-MetricName</span></span>
<span data-ttu-id="bf1bd-125">Określa nazwę metryki.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-125">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="bf1bd-126">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="bf1bd-126">-MetricNamespace</span></span>
<span data-ttu-id="bf1bd-127">Określa obszar nazw metryki dla reguły.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-127">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="bf1bd-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf1bd-128">-Name</span></span>
<span data-ttu-id="bf1bd-129">Określa nazwę reguły.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-129">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="bf1bd-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bf1bd-130">-ResourceGroup</span></span>
<span data-ttu-id="bf1bd-131">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bf1bd-132">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="bf1bd-132">-TargetResourceUri</span></span>
<span data-ttu-id="bf1bd-133">Określa identyfikator zasobu WebTest.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-133">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="bf1bd-134">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="bf1bd-134">-WindowSize</span></span>
<span data-ttu-id="bf1bd-135">Określa rozmiar okna czasu dla reguły w celu obliczenia danych.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-135">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="bf1bd-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf1bd-136">-DefaultProfile</span></span>
<span data-ttu-id="bf1bd-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf1bd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf1bd-138">CommonParameters</span></span>
<span data-ttu-id="bf1bd-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf1bd-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf1bd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf1bd-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf1bd-141">INPUTS</span></span>

## <span data-ttu-id="bf1bd-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf1bd-142">OUTPUTS</span></span>

### <span data-ttu-id="bf1bd-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bf1bd-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="bf1bd-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf1bd-144">NOTES</span></span>

## <span data-ttu-id="bf1bd-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf1bd-145">RELATED LINKS</span></span>

[<span data-ttu-id="bf1bd-146">Dodaj-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="bf1bd-146">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="bf1bd-147">Dodaj-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="bf1bd-147">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="bf1bd-148">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="bf1bd-148">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="bf1bd-149">Nowe — AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="bf1bd-149">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


