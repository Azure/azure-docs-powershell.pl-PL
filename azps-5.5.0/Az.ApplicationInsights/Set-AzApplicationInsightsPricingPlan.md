---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: d9ddfdb43db8e94d0dc65606f6c5f86f05db31d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182243"
---
# <span data-ttu-id="7db20-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="7db20-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="7db20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7db20-102">SYNOPSIS</span></span>
<span data-ttu-id="7db20-103">Ustawianie planu cenowego i dziennych informacji o ilości danych dla zasobu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="7db20-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="7db20-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7db20-104">SYNTAX</span></span>

### <span data-ttu-id="7db20-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7db20-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db20-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7db20-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db20-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7db20-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7db20-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7db20-108">DESCRIPTION</span></span>
<span data-ttu-id="7db20-109">Ustaw plan cenowy i dzienne informacje o ilości danych dla zasobu szczegółowych informacji o aplikacjach.</span><span class="sxs-lookup"><span data-stu-id="7db20-109">Set pricing plan and daily data volume information for an application insights resource.</span></span>
<span data-ttu-id="7db20-110">To polecenie cmdlet nie umożliwia ustawienia planu cen szczegółowych informacji o aplikacjach utworzonego po kwietniu 2018 r.: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span><span class="sxs-lookup"><span data-stu-id="7db20-110">Pricing plan of application insights created after April 2018 cannot be set by this cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span></span>

## <span data-ttu-id="7db20-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7db20-111">EXAMPLES</span></span>

### <span data-ttu-id="7db20-112">Przykład 1. Ustawianie planu cenowego i dziennych informacji o ilości danych dla zasobu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="7db20-112">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="7db20-113">Ustaw plan cenowy na "Podstawowy", ustaw dzienny limit ilości danych na 400 GB na dzień i zatrzymaj wysyłanie powiadomień po przecięcie limitu "test" zasobu w grupie zasobów "grupa testowa"</span><span class="sxs-lookup"><span data-stu-id="7db20-113">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="7db20-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7db20-114">PARAMETERS</span></span>

### <span data-ttu-id="7db20-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7db20-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="7db20-116">Obiekt składnika Szczegółowe informacje o aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7db20-116">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7db20-117">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="7db20-117">-DailyCapGB</span></span>
<span data-ttu-id="7db20-118">Dzienny limit.</span><span class="sxs-lookup"><span data-stu-id="7db20-118">Daily Cap.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7db20-119">-DefaultProfile</span></span>
<span data-ttu-id="7db20-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7db20-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7db20-121">-DisableNotificationWhenCap</span><span class="sxs-lookup"><span data-stu-id="7db20-121">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="7db20-122">Zatrzymanie wysyłania powiadomień po przecięcie limitu.</span><span class="sxs-lookup"><span data-stu-id="7db20-122">Stop send notification when hit cap.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db20-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7db20-123">-Name</span></span>
<span data-ttu-id="7db20-124">Nazwa składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7db20-124">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db20-125">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="7db20-125">-PricingPlan</span></span>
<span data-ttu-id="7db20-126">Nazwa planu cenowego.</span><span class="sxs-lookup"><span data-stu-id="7db20-126">Pricing plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db20-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7db20-127">-ResourceGroupName</span></span>
<span data-ttu-id="7db20-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7db20-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db20-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7db20-129">-ResourceId</span></span>
<span data-ttu-id="7db20-130">Identyfikator składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7db20-130">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7db20-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7db20-131">-Confirm</span></span>
<span data-ttu-id="7db20-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7db20-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7db20-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7db20-133">-WhatIf</span></span>
<span data-ttu-id="7db20-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7db20-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7db20-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7db20-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7db20-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db20-136">CommonParameters</span></span>
<span data-ttu-id="7db20-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7db20-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db20-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7db20-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db20-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7db20-139">INPUTS</span></span>

### <span data-ttu-id="7db20-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7db20-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="7db20-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7db20-141">System.String</span></span>

## <span data-ttu-id="7db20-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7db20-142">OUTPUTS</span></span>

### <span data-ttu-id="7db20-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="7db20-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="7db20-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7db20-144">NOTES</span></span>

## <span data-ttu-id="7db20-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7db20-145">RELATED LINKS</span></span>
