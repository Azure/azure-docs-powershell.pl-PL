---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 11A521DF-E77C-4D6F-A2D9-1C2CF8972F57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
ms.openlocfilehash: 38644018ac9ae19d1c413123ca071f564d336fa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553874"
---
# <span data-ttu-id="6b419-101">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="6b419-101">Add-AzureRmLogAlertRule</span></span>

## <span data-ttu-id="6b419-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b419-102">SYNOPSIS</span></span>
<span data-ttu-id="6b419-103">Dodanie lub zastąpienie reguły alertu dziennika.</span><span class="sxs-lookup"><span data-stu-id="6b419-103">Adds or replaces a log alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b419-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b419-104">SYNTAX</span></span>

```
Add-AzureRmLogAlertRule [-TargetResourceGroup <String>] [-TargetResourceId <String>] [-Level <String>]
 -OperationName <String> [-TargetResourceProvider <String>] [-Status <String>] [-SubStatus <String>]
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b419-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6b419-105">DESCRIPTION</span></span>
<span data-ttu-id="6b419-106">Polecenie cmdlet **Add-AzureRmLogAlertRule** umożliwia dodanie lub zastąpienie reguły alertu zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="6b419-106">The **Add-AzureRmLogAlertRule** cmdlet adds or replaces an event alert rule.</span></span>
<span data-ttu-id="6b419-107">Dodana reguła jest skojarzona z grupą zasobów i ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="6b419-107">The added rule is associated with a resource group and has a name.</span></span>

<span data-ttu-id="6b419-108">Ogłoszono we wcześniejszych wersjach: **polecenie cmdlet Add-AzureRMLogAlertRule jest przestarzałe w przyszłej wersji.**</span><span class="sxs-lookup"><span data-stu-id="6b419-108">As announced in previous releases: **Add-AzureRMLogAlertRule cmdlet will be deprecated in a future release.**</span></span> <span data-ttu-id="6b419-109">Po pierwszym dniu 2017 przy użyciu tego polecenia cmdlet nie będzie już żadnego skutku, ponieważ ta funkcja jest przenoszony do alertów dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="6b419-109">After October 1st 2017 using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="6b419-110">Aby uzyskać **_https://aka.ms/migratemealerts_** więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="6b419-110">Please see **_https://aka.ms/migratemealerts_** for more information.</span></span>

## <span data-ttu-id="6b419-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b419-111">EXAMPLES</span></span>

### <span data-ttu-id="6b419-112">Przykład 1: Dodawanie reguły alertu dziennika</span><span class="sxs-lookup"><span data-stu-id="6b419-112">Example 1: Add a log alert rule</span></span>
```
PS C:\>Add-AzureRmLogAlertRule -Name "logRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -OperationName "Create" -TargetResourceId "/subscriptions/abbfb07c-6c93-40be-bc9b-4f0deba32f4c/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/misitiooeltuyo" -Description "My log rule"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="6b419-113">To polecenie umożliwia dodanie lub zaktualizowanie reguły alertu opartego na zdarzeniu.</span><span class="sxs-lookup"><span data-stu-id="6b419-113">This command adds or updates an event-based alert rule.</span></span>

## <span data-ttu-id="6b419-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b419-114">PARAMETERS</span></span>

### <span data-ttu-id="6b419-115">-Akcje</span><span class="sxs-lookup"><span data-stu-id="6b419-115">-Actions</span></span>
<span data-ttu-id="6b419-116">Określa listę akcji rozdzielonych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="6b419-116">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="6b419-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="6b419-117">-Description</span></span>
<span data-ttu-id="6b419-118">Określa opis reguły.</span><span class="sxs-lookup"><span data-stu-id="6b419-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="6b419-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="6b419-119">-DisableRule</span></span>
<span data-ttu-id="6b419-120">Wyłącza regułę.</span><span class="sxs-lookup"><span data-stu-id="6b419-120">Disables a rule.</span></span>
<span data-ttu-id="6b419-121">Jeśli ten parametr nie jest określony, reguła jest włączona.</span><span class="sxs-lookup"><span data-stu-id="6b419-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="6b419-122">-Level</span><span class="sxs-lookup"><span data-stu-id="6b419-122">-Level</span></span>
<span data-ttu-id="6b419-123">Określa poziom zdarzenia monitorującego regułę.</span><span class="sxs-lookup"><span data-stu-id="6b419-123">Specifies the level of the event the rule is monitoring.</span></span>
<span data-ttu-id="6b419-124">Ten parametr można określić tylko dla reguł opartych na zdarzeniach.</span><span class="sxs-lookup"><span data-stu-id="6b419-124">Specify this parameter only for event-based rules.</span></span>

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

### <span data-ttu-id="6b419-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6b419-125">-Location</span></span>
<span data-ttu-id="6b419-126">Określa lokalizację reguły.</span><span class="sxs-lookup"><span data-stu-id="6b419-126">Specifies the location for the rule.</span></span>

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

### <span data-ttu-id="6b419-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6b419-127">-Name</span></span>
<span data-ttu-id="6b419-128">Określa nazwę reguły.</span><span class="sxs-lookup"><span data-stu-id="6b419-128">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="6b419-129">-OperationName</span><span class="sxs-lookup"><span data-stu-id="6b419-129">-OperationName</span></span>
<span data-ttu-id="6b419-130">Określa nazwę operacji.</span><span class="sxs-lookup"><span data-stu-id="6b419-130">Specifies the name of the operation.</span></span>

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

### <span data-ttu-id="6b419-131">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6b419-131">-ResourceGroup</span></span>
<span data-ttu-id="6b419-132">Określa nazwę grupy zasobów dla reguły.</span><span class="sxs-lookup"><span data-stu-id="6b419-132">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="6b419-133">-Status</span><span class="sxs-lookup"><span data-stu-id="6b419-133">-Status</span></span>
<span data-ttu-id="6b419-134">Określa stan.</span><span class="sxs-lookup"><span data-stu-id="6b419-134">Specifies the status.</span></span>

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

### <span data-ttu-id="6b419-135">-Status</span><span class="sxs-lookup"><span data-stu-id="6b419-135">-SubStatus</span></span>
<span data-ttu-id="6b419-136">Określa podstan.</span><span class="sxs-lookup"><span data-stu-id="6b419-136">Specifies the substatus.</span></span>

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

### <span data-ttu-id="6b419-137">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6b419-137">-TargetResourceGroup</span></span>
<span data-ttu-id="6b419-138">Określa grupę zasobów zasobu, którym podlega monitorowanie reguły.</span><span class="sxs-lookup"><span data-stu-id="6b419-138">Specifies the resource group of the resource the rule is monitoring.</span></span>

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

### <span data-ttu-id="6b419-139">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6b419-139">-TargetResourceId</span></span>
<span data-ttu-id="6b419-140">Określa identyfikator zasobu monitorującego regułę.</span><span class="sxs-lookup"><span data-stu-id="6b419-140">Specifies the ID of the resource the rule is monitoring.</span></span>

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

### <span data-ttu-id="6b419-141">-TargetResourceProvider</span><span class="sxs-lookup"><span data-stu-id="6b419-141">-TargetResourceProvider</span></span>
<span data-ttu-id="6b419-142">Określa dostawcę zasobów dla zasobu, którym podlega monitorowanie reguły.</span><span class="sxs-lookup"><span data-stu-id="6b419-142">Specifies the resource provider of the resource the rule is monitoring.</span></span>

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

### <span data-ttu-id="6b419-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b419-143">-DefaultProfile</span></span>
<span data-ttu-id="6b419-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b419-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b419-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b419-145">CommonParameters</span></span>
<span data-ttu-id="6b419-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b419-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b419-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b419-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b419-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b419-148">INPUTS</span></span>

## <span data-ttu-id="6b419-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b419-149">OUTPUTS</span></span>

### <span data-ttu-id="6b419-150">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6b419-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="6b419-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b419-151">NOTES</span></span>

## <span data-ttu-id="6b419-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b419-152">RELATED LINKS</span></span>

[<span data-ttu-id="6b419-153">Dodaj-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="6b419-153">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="6b419-154">Dodaj-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="6b419-154">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="6b419-155">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="6b419-155">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="6b419-156">Nowe — AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="6b419-156">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="6b419-157">Nowe — AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="6b419-157">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


