---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: f13408e23dcf8f1db9de2e19fc05d899b712a783
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381236"
---
# <span data-ttu-id="7d32f-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="7d32f-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="7d32f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d32f-102">SYNOPSIS</span></span>
<span data-ttu-id="7d32f-103">Ustawianie dziennej ilości danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="7d32f-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="7d32f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d32f-104">SYNTAX</span></span>

### <span data-ttu-id="7d32f-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7d32f-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d32f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d32f-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d32f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d32f-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d32f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7d32f-108">DESCRIPTION</span></span>
<span data-ttu-id="7d32f-109">Ustawianie dziennej ilości danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="7d32f-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="7d32f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d32f-110">EXAMPLES</span></span>

### <span data-ttu-id="7d32f-111">Przykład 1 Ustawianie codziennego wolumenu danych dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="7d32f-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="7d32f-112">Ustaw dzienną ilość danych od Cap do 400 GB i Zatrzymaj powiadomienie o wysyłaniu po trafieniu zasobu "Testuj" w grupie "test".</span><span class="sxs-lookup"><span data-stu-id="7d32f-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="7d32f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d32f-113">PARAMETERS</span></span>

### <span data-ttu-id="7d32f-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7d32f-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="7d32f-115">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7d32f-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="7d32f-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="7d32f-116">-DailyCapGB</span></span>
<span data-ttu-id="7d32f-117">Dzienna Cap.</span><span class="sxs-lookup"><span data-stu-id="7d32f-117">Daily Cap.</span></span>

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

### <span data-ttu-id="7d32f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d32f-118">-DefaultProfile</span></span>
<span data-ttu-id="7d32f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d32f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d32f-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="7d32f-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="7d32f-121">Zatrzymaj Wysyłanie powiadomienia, gdy trafisz na koniec.</span><span class="sxs-lookup"><span data-stu-id="7d32f-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="7d32f-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7d32f-122">-Name</span></span>
<span data-ttu-id="7d32f-123">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7d32f-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="7d32f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d32f-124">-ResourceGroupName</span></span>
<span data-ttu-id="7d32f-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7d32f-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="7d32f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d32f-126">-ResourceId</span></span>
<span data-ttu-id="7d32f-127">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7d32f-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="7d32f-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d32f-128">-Confirm</span></span>
<span data-ttu-id="7d32f-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d32f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d32f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d32f-130">-WhatIf</span></span>
<span data-ttu-id="7d32f-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d32f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d32f-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7d32f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d32f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d32f-133">CommonParameters</span></span>
<span data-ttu-id="7d32f-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d32f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d32f-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d32f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d32f-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d32f-136">INPUTS</span></span>

### <span data-ttu-id="7d32f-137">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7d32f-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="7d32f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7d32f-138">System.String</span></span>

## <span data-ttu-id="7d32f-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d32f-139">OUTPUTS</span></span>

### <span data-ttu-id="7d32f-140">Microsoft. Azure. Commands. ApplicationInsights. models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="7d32f-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="7d32f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d32f-141">NOTES</span></span>

## <span data-ttu-id="7d32f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d32f-142">RELATED LINKS</span></span>
