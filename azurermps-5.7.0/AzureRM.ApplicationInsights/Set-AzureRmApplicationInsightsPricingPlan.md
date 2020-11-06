---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
ms.openlocfilehash: 4785abb883c262273d8d3b0798067e76092511fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551792"
---
# <span data-ttu-id="e4591-101">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="e4591-101">Set-AzureRmApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="e4591-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4591-102">SYNOPSIS</span></span>
<span data-ttu-id="e4591-103">Ustawianie planu cennika i informacji o wolumenach codziennego przesyłania danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="e4591-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4591-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4591-104">SYNTAX</span></span>

### <span data-ttu-id="e4591-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e4591-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4591-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4591-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4591-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4591-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4591-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e4591-108">DESCRIPTION</span></span>
<span data-ttu-id="e4591-109">Ustawianie planu cennika i informacji o wolumenach codziennego przesyłania danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="e4591-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="e4591-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4591-110">EXAMPLES</span></span>

### <span data-ttu-id="e4591-111">Przykład 1 Ustawianie planu cennika i informacji o dziennym woluminie danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="e4591-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="e4591-112">Ustaw plan cenowy na "podstawowy", ustaw codzienne dane volumen Cap na dzień i Zatrzymaj powiadomienie o wysyłaniu po trafieniu zasobu "Testuj" w grupie "test".</span><span class="sxs-lookup"><span data-stu-id="e4591-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="e4591-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4591-113">PARAMETERS</span></span>

### <span data-ttu-id="e4591-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e4591-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="e4591-115">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e4591-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4591-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4591-116">-Confirm</span></span>
<span data-ttu-id="e4591-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4591-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4591-118">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="e4591-118">-DailyCapGB</span></span>
<span data-ttu-id="e4591-119">Dzienna Cap.</span><span class="sxs-lookup"><span data-stu-id="e4591-119">Daily Cap.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4591-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4591-120">-DefaultProfile</span></span>
<span data-ttu-id="e4591-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4591-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4591-122">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="e4591-122">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="e4591-123">Zatrzymaj Wysyłanie powiadomienia, gdy trafisz na koniec.</span><span class="sxs-lookup"><span data-stu-id="e4591-123">Stop send notification when hit cap.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4591-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4591-124">-Name</span></span>
<span data-ttu-id="e4591-125">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e4591-125">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4591-126">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="e4591-126">-PricingPlan</span></span>
<span data-ttu-id="e4591-127">Nazwa planu cennika.</span><span class="sxs-lookup"><span data-stu-id="e4591-127">Pricing plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4591-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4591-128">-ResourceGroupName</span></span>
<span data-ttu-id="e4591-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4591-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4591-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4591-130">-ResourceId</span></span>
<span data-ttu-id="e4591-131">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e4591-131">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4591-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4591-132">-WhatIf</span></span>
<span data-ttu-id="e4591-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4591-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4591-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4591-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4591-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4591-135">CommonParameters</span></span>
<span data-ttu-id="e4591-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4591-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4591-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4591-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4591-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4591-138">INPUTS</span></span>

### <span data-ttu-id="e4591-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e4591-139">System.String</span></span>
<span data-ttu-id="e4591-140">System. Double. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4591-140">System.Double System.Boolean</span></span>

## <span data-ttu-id="e4591-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4591-141">OUTPUTS</span></span>

### <span data-ttu-id="e4591-142">Microsoft. Azure. Commands. ApplicationInsights. models. PSPricingTier</span><span class="sxs-lookup"><span data-stu-id="e4591-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingTier</span></span>

## <span data-ttu-id="e4591-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4591-143">NOTES</span></span>

## <span data-ttu-id="e4591-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4591-144">RELATED LINKS</span></span>

