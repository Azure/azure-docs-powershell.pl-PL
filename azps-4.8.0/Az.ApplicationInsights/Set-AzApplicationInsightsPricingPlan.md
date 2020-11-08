---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: e044d8a086833ad94ed01267adf08469941a32a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222694"
---
# <span data-ttu-id="bb360-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="bb360-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="bb360-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb360-102">SYNOPSIS</span></span>
<span data-ttu-id="bb360-103">Ustawianie planu cennika i informacji o wolumenach codziennego przesyłania danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="bb360-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="bb360-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb360-104">SYNTAX</span></span>

### <span data-ttu-id="bb360-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bb360-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb360-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb360-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb360-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb360-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb360-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bb360-108">DESCRIPTION</span></span>
<span data-ttu-id="bb360-109">Ustawianie planu cennika i informacji o wolumenach codziennego przesyłania danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="bb360-109">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="bb360-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb360-110">EXAMPLES</span></span>

### <span data-ttu-id="bb360-111">Przykład 1 Ustawianie planu cennika i informacji o dziennym woluminie danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="bb360-111">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="bb360-112">Ustaw plan cenowy na "podstawowy", ustaw codzienne ilości danych od Cap do 400 GB na dzień i Zatrzymaj Wysyłanie powiadomienia o wysyłaniu dla zasobu "Testuj" w grupie "test".</span><span class="sxs-lookup"><span data-stu-id="bb360-112">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="bb360-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb360-113">PARAMETERS</span></span>

### <span data-ttu-id="bb360-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="bb360-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="bb360-115">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="bb360-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="bb360-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="bb360-116">-DailyCapGB</span></span>
<span data-ttu-id="bb360-117">Dzienna Cap.</span><span class="sxs-lookup"><span data-stu-id="bb360-117">Daily Cap.</span></span>

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

### <span data-ttu-id="bb360-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb360-118">-DefaultProfile</span></span>
<span data-ttu-id="bb360-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb360-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb360-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="bb360-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="bb360-121">Zatrzymaj Wysyłanie powiadomienia, gdy trafisz na koniec.</span><span class="sxs-lookup"><span data-stu-id="bb360-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="bb360-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bb360-122">-Name</span></span>
<span data-ttu-id="bb360-123">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="bb360-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="bb360-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="bb360-124">-PricingPlan</span></span>
<span data-ttu-id="bb360-125">Nazwa planu cennika.</span><span class="sxs-lookup"><span data-stu-id="bb360-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="bb360-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb360-126">-ResourceGroupName</span></span>
<span data-ttu-id="bb360-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bb360-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="bb360-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb360-128">-ResourceId</span></span>
<span data-ttu-id="bb360-129">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="bb360-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="bb360-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb360-130">-Confirm</span></span>
<span data-ttu-id="bb360-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb360-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb360-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb360-132">-WhatIf</span></span>
<span data-ttu-id="bb360-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb360-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb360-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bb360-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb360-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb360-135">CommonParameters</span></span>
<span data-ttu-id="bb360-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb360-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb360-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb360-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb360-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb360-138">INPUTS</span></span>

### <span data-ttu-id="bb360-139">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="bb360-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="bb360-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bb360-140">System.String</span></span>

## <span data-ttu-id="bb360-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb360-141">OUTPUTS</span></span>

### <span data-ttu-id="bb360-142">Microsoft. Azure. Commands. ApplicationInsights. models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="bb360-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="bb360-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb360-143">NOTES</span></span>

## <span data-ttu-id="bb360-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb360-144">RELATED LINKS</span></span>
