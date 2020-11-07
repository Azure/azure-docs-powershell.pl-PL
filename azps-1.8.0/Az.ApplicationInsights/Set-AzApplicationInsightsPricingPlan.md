---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: 33b55c70d88daf8493012945f49794c25e62b474
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710620"
---
# <span data-ttu-id="c1496-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="c1496-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="c1496-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1496-102">SYNOPSIS</span></span>
<span data-ttu-id="c1496-103">Ustawianie planu cennika i informacji o wolumenach codziennego przesyłania danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="c1496-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="c1496-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1496-104">SYNTAX</span></span>

### <span data-ttu-id="c1496-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c1496-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1496-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1496-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1496-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1496-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1496-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c1496-108">DESCRIPTION</span></span>
<span data-ttu-id="c1496-109">Ustawianie planu cennika i informacji o wolumenach codziennego przesyłania danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="c1496-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="c1496-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1496-110">EXAMPLES</span></span>

### <span data-ttu-id="c1496-111">Przykład 1 Ustawianie planu cennika i informacji o dziennym woluminie danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="c1496-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="c1496-112">Ustaw plan cenowy na "podstawowy", ustaw codzienne dane volumen Cap na dzień i Zatrzymaj powiadomienie o wysyłaniu po trafieniu zasobu "Testuj" w grupie "test".</span><span class="sxs-lookup"><span data-stu-id="c1496-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="c1496-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1496-113">PARAMETERS</span></span>

### <span data-ttu-id="c1496-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c1496-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c1496-115">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c1496-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c1496-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="c1496-116">-DailyCapGB</span></span>
<span data-ttu-id="c1496-117">Dzienna Cap.</span><span class="sxs-lookup"><span data-stu-id="c1496-117">Daily Cap.</span></span>

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

### <span data-ttu-id="c1496-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1496-118">-DefaultProfile</span></span>
<span data-ttu-id="c1496-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1496-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1496-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="c1496-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="c1496-121">Zatrzymaj Wysyłanie powiadomienia, gdy trafisz na koniec.</span><span class="sxs-lookup"><span data-stu-id="c1496-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="c1496-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c1496-122">-Name</span></span>
<span data-ttu-id="c1496-123">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c1496-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="c1496-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="c1496-124">-PricingPlan</span></span>
<span data-ttu-id="c1496-125">Nazwa planu cennika.</span><span class="sxs-lookup"><span data-stu-id="c1496-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="c1496-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1496-126">-ResourceGroupName</span></span>
<span data-ttu-id="c1496-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c1496-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="c1496-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1496-128">-ResourceId</span></span>
<span data-ttu-id="c1496-129">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c1496-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c1496-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1496-130">-Confirm</span></span>
<span data-ttu-id="c1496-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1496-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1496-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1496-132">-WhatIf</span></span>
<span data-ttu-id="c1496-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1496-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1496-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c1496-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1496-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1496-135">CommonParameters</span></span>
<span data-ttu-id="c1496-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1496-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1496-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1496-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1496-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1496-138">INPUTS</span></span>

### <span data-ttu-id="c1496-139">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c1496-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="c1496-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c1496-140">System.String</span></span>

## <span data-ttu-id="c1496-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1496-141">OUTPUTS</span></span>

### <span data-ttu-id="c1496-142">Microsoft. Azure. Commands. ApplicationInsights. models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="c1496-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="c1496-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1496-143">NOTES</span></span>

## <span data-ttu-id="c1496-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1496-144">RELATED LINKS</span></span>