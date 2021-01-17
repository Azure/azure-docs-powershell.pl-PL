---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: d9ddfdb43db8e94d0dc65606f6c5f86f05db31d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381222"
---
# <span data-ttu-id="8c2eb-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="8c2eb-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="8c2eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c2eb-102">SYNOPSIS</span></span>
<span data-ttu-id="8c2eb-103">Ustawianie planu cennika i informacji o wolumenach codziennego przesyłania danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="8c2eb-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="8c2eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c2eb-104">SYNTAX</span></span>

### <span data-ttu-id="8c2eb-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c2eb-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c2eb-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c2eb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c2eb-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c2eb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8c2eb-108">DESCRIPTION</span></span>
<span data-ttu-id="8c2eb-109">Konfigurowanie planu cennika i informacji o wolumenach codziennego przesyłania danych dla zasobu usługi Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-109">Set pricing plan and daily data volume information for an application insights resource.</span></span>
<span data-ttu-id="8c2eb-110">Ten aplet polecenia cmdlet nie może ustawić planu taryfowego dotyczącego usługi Application Insights utworzonego po 2018 kwietnia: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span><span class="sxs-lookup"><span data-stu-id="8c2eb-110">Pricing plan of application insights created after April 2018 cannot be set by this cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span></span>

## <span data-ttu-id="8c2eb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c2eb-111">EXAMPLES</span></span>

### <span data-ttu-id="8c2eb-112">Przykład 1 Ustawianie planu cennika i informacji o dziennym woluminie danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="8c2eb-112">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="8c2eb-113">Ustaw plan cenowy na "podstawowy", ustaw codzienne ilości danych od Cap do 400 GB na dzień i Zatrzymaj Wysyłanie powiadomienia o wysyłaniu dla zasobu "Testuj" w grupie "test".</span><span class="sxs-lookup"><span data-stu-id="8c2eb-113">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="8c2eb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c2eb-114">PARAMETERS</span></span>

### <span data-ttu-id="8c2eb-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8c2eb-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8c2eb-116">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="8c2eb-117">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="8c2eb-117">-DailyCapGB</span></span>
<span data-ttu-id="8c2eb-118">Dzienna Cap.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-118">Daily Cap.</span></span>

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

### <span data-ttu-id="8c2eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c2eb-119">-DefaultProfile</span></span>
<span data-ttu-id="8c2eb-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c2eb-121">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="8c2eb-121">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="8c2eb-122">Zatrzymaj Wysyłanie powiadomienia, gdy trafisz na koniec.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-122">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="8c2eb-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c2eb-123">-Name</span></span>
<span data-ttu-id="8c2eb-124">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-124">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="8c2eb-125">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="8c2eb-125">-PricingPlan</span></span>
<span data-ttu-id="8c2eb-126">Nazwa planu cennika.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-126">Pricing plan name.</span></span>

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

### <span data-ttu-id="8c2eb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c2eb-127">-ResourceGroupName</span></span>
<span data-ttu-id="8c2eb-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="8c2eb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c2eb-129">-ResourceId</span></span>
<span data-ttu-id="8c2eb-130">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="8c2eb-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c2eb-131">-Confirm</span></span>
<span data-ttu-id="8c2eb-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c2eb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c2eb-133">-WhatIf</span></span>
<span data-ttu-id="8c2eb-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c2eb-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c2eb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c2eb-136">CommonParameters</span></span>
<span data-ttu-id="8c2eb-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c2eb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c2eb-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c2eb-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c2eb-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c2eb-139">INPUTS</span></span>

### <span data-ttu-id="8c2eb-140">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8c2eb-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="8c2eb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8c2eb-141">System.String</span></span>

## <span data-ttu-id="8c2eb-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c2eb-142">OUTPUTS</span></span>

### <span data-ttu-id="8c2eb-143">Microsoft. Azure. Commands. ApplicationInsights. models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="8c2eb-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="8c2eb-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c2eb-144">NOTES</span></span>

## <span data-ttu-id="8c2eb-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c2eb-145">RELATED LINKS</span></span>
