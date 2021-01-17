---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: d9ddfdb43db8e94d0dc65606f6c5f86f05db31d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353422"
---
# <span data-ttu-id="3f11e-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="3f11e-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="3f11e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f11e-102">SYNOPSIS</span></span>
<span data-ttu-id="3f11e-103">Ustawianie planu cennika i informacji o wolumenach codziennego przesyłania danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="3f11e-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="3f11e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f11e-104">SYNTAX</span></span>

### <span data-ttu-id="3f11e-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3f11e-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f11e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f11e-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f11e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f11e-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f11e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3f11e-108">DESCRIPTION</span></span>
<span data-ttu-id="3f11e-109">Konfigurowanie planu cennika i informacji o wolumenach codziennego przesyłania danych dla zasobu usługi Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3f11e-109">Set pricing plan and daily data volume information for an application insights resource.</span></span>
<span data-ttu-id="3f11e-110">Ten aplet polecenia cmdlet nie może ustawić planu taryfowego dotyczącego usługi Application Insights utworzonego po 2018 kwietnia: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span><span class="sxs-lookup"><span data-stu-id="3f11e-110">Pricing plan of application insights created after April 2018 cannot be set by this cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span></span>

## <span data-ttu-id="3f11e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f11e-111">EXAMPLES</span></span>

### <span data-ttu-id="3f11e-112">Przykład 1 Ustawianie planu cennika i informacji o dziennym woluminie danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="3f11e-112">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="3f11e-113">Ustaw plan cenowy na "podstawowy", ustaw codzienne ilości danych od Cap do 400 GB na dzień i Zatrzymaj Wysyłanie powiadomienia o wysyłaniu dla zasobu "Testuj" w grupie "test".</span><span class="sxs-lookup"><span data-stu-id="3f11e-113">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="3f11e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f11e-114">PARAMETERS</span></span>

### <span data-ttu-id="3f11e-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3f11e-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="3f11e-116">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3f11e-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="3f11e-117">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="3f11e-117">-DailyCapGB</span></span>
<span data-ttu-id="3f11e-118">Dzienna Cap.</span><span class="sxs-lookup"><span data-stu-id="3f11e-118">Daily Cap.</span></span>

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

### <span data-ttu-id="3f11e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f11e-119">-DefaultProfile</span></span>
<span data-ttu-id="3f11e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f11e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f11e-121">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="3f11e-121">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="3f11e-122">Zatrzymaj Wysyłanie powiadomienia, gdy trafisz na koniec.</span><span class="sxs-lookup"><span data-stu-id="3f11e-122">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="3f11e-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3f11e-123">-Name</span></span>
<span data-ttu-id="3f11e-124">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3f11e-124">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="3f11e-125">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="3f11e-125">-PricingPlan</span></span>
<span data-ttu-id="3f11e-126">Nazwa planu cennika.</span><span class="sxs-lookup"><span data-stu-id="3f11e-126">Pricing plan name.</span></span>

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

### <span data-ttu-id="3f11e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f11e-127">-ResourceGroupName</span></span>
<span data-ttu-id="3f11e-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3f11e-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="3f11e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f11e-129">-ResourceId</span></span>
<span data-ttu-id="3f11e-130">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3f11e-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="3f11e-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3f11e-131">-Confirm</span></span>
<span data-ttu-id="3f11e-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f11e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f11e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f11e-133">-WhatIf</span></span>
<span data-ttu-id="3f11e-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f11e-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f11e-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3f11e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f11e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f11e-136">CommonParameters</span></span>
<span data-ttu-id="3f11e-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f11e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f11e-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f11e-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f11e-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f11e-139">INPUTS</span></span>

### <span data-ttu-id="3f11e-140">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3f11e-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="3f11e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3f11e-141">System.String</span></span>

## <span data-ttu-id="3f11e-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f11e-142">OUTPUTS</span></span>

### <span data-ttu-id="3f11e-143">Microsoft. Azure. Commands. ApplicationInsights. models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="3f11e-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="3f11e-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f11e-144">NOTES</span></span>

## <span data-ttu-id="3f11e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f11e-145">RELATED LINKS</span></span>
