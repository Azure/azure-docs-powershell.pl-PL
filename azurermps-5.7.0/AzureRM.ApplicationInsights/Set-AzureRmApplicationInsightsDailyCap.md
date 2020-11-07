---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
ms.openlocfilehash: 12e8e4f76f623391e6046f4f8b0bd424e7b9334d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716861"
---
# <span data-ttu-id="9479c-101">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="9479c-101">Set-AzureRmApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="9479c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9479c-102">SYNOPSIS</span></span>
<span data-ttu-id="9479c-103">Ustawianie dziennej ilości danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="9479c-103">Set daily data volume cap for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9479c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9479c-104">SYNTAX</span></span>

### <span data-ttu-id="9479c-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9479c-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9479c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9479c-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9479c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9479c-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9479c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9479c-108">DESCRIPTION</span></span>
<span data-ttu-id="9479c-109">Ustawianie dziennej ilości danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="9479c-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="9479c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9479c-110">EXAMPLES</span></span>

### <span data-ttu-id="9479c-111">Przykład 1 Ustawianie codziennego wolumenu danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="9479c-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="9479c-112">Ustaw codzienne dane volumen Cap na 400 zł i Zatrzymaj powiadomienie o wysyłaniu po trafieniu zasobu "Testuj" w grupie "test" w grupie zasób.</span><span class="sxs-lookup"><span data-stu-id="9479c-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="9479c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9479c-113">PARAMETERS</span></span>

### <span data-ttu-id="9479c-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9479c-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="9479c-115">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9479c-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="9479c-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9479c-116">-Confirm</span></span>
<span data-ttu-id="9479c-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9479c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9479c-118">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="9479c-118">-DailyCapGB</span></span>
<span data-ttu-id="9479c-119">Dzienna Cap.</span><span class="sxs-lookup"><span data-stu-id="9479c-119">Daily Cap.</span></span>

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

### <span data-ttu-id="9479c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9479c-120">-DefaultProfile</span></span>
<span data-ttu-id="9479c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9479c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9479c-122">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="9479c-122">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="9479c-123">Zatrzymaj Wysyłanie powiadomienia, gdy trafisz na koniec.</span><span class="sxs-lookup"><span data-stu-id="9479c-123">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="9479c-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9479c-124">-Name</span></span>
<span data-ttu-id="9479c-125">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9479c-125">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="9479c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9479c-126">-ResourceGroupName</span></span>
<span data-ttu-id="9479c-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9479c-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="9479c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9479c-128">-ResourceId</span></span>
<span data-ttu-id="9479c-129">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9479c-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="9479c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9479c-130">-WhatIf</span></span>
<span data-ttu-id="9479c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9479c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9479c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9479c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9479c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9479c-133">CommonParameters</span></span>
<span data-ttu-id="9479c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9479c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9479c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9479c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9479c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9479c-136">INPUTS</span></span>

### <span data-ttu-id="9479c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9479c-137">System.String</span></span>
<span data-ttu-id="9479c-138">System. Double. Boolean</span><span class="sxs-lookup"><span data-stu-id="9479c-138">System.Double System.Boolean</span></span>

## <span data-ttu-id="9479c-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9479c-139">OUTPUTS</span></span>

### <span data-ttu-id="9479c-140">Microsoft. Azure. Commands. ApplicationInsights. models. PSPricingTier</span><span class="sxs-lookup"><span data-stu-id="9479c-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingTier</span></span>

## <span data-ttu-id="9479c-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9479c-141">NOTES</span></span>

## <span data-ttu-id="9479c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9479c-142">RELATED LINKS</span></span>

