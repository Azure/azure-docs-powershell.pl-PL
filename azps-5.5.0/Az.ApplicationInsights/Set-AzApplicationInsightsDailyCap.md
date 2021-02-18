---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: f13408e23dcf8f1db9de2e19fc05d899b712a783
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201242"
---
# <span data-ttu-id="25461-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="25461-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="25461-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25461-102">SYNOPSIS</span></span>
<span data-ttu-id="25461-103">Ustawianie dziennego limitu ilości danych dla zasobu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="25461-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="25461-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="25461-104">SYNTAX</span></span>

### <span data-ttu-id="25461-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="25461-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25461-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25461-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25461-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25461-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25461-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="25461-108">DESCRIPTION</span></span>
<span data-ttu-id="25461-109">Ustawianie dziennego limitu ilości danych dla zasobu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="25461-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="25461-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="25461-110">EXAMPLES</span></span>

### <span data-ttu-id="25461-111">Przykład 1. Ustawianie dziennego limitu liczby danych dla zasobu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="25461-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="25461-112">Ustawianie dziennego limitu woluminu danych na 400 GB na dzień i zatrzymywanie wysyłania powiadomień po przecięcie limitu "test" zasobu w grupie zasobów "grupa testowa"</span><span class="sxs-lookup"><span data-stu-id="25461-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="25461-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25461-113">PARAMETERS</span></span>

### <span data-ttu-id="25461-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="25461-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="25461-115">Obiekt składnika Szczegółowe informacje o aplikacji.</span><span class="sxs-lookup"><span data-stu-id="25461-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="25461-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="25461-116">-DailyCapGB</span></span>
<span data-ttu-id="25461-117">Dzienny limit.</span><span class="sxs-lookup"><span data-stu-id="25461-117">Daily Cap.</span></span>

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

### <span data-ttu-id="25461-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25461-118">-DefaultProfile</span></span>
<span data-ttu-id="25461-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="25461-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25461-120">-DisableNotificationWhenCap</span><span class="sxs-lookup"><span data-stu-id="25461-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="25461-121">Zatrzymanie wysyłania powiadomień po przecięcie limitu.</span><span class="sxs-lookup"><span data-stu-id="25461-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="25461-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="25461-122">-Name</span></span>
<span data-ttu-id="25461-123">Nazwa składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="25461-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="25461-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25461-124">-ResourceGroupName</span></span>
<span data-ttu-id="25461-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25461-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="25461-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25461-126">-ResourceId</span></span>
<span data-ttu-id="25461-127">Identyfikator składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="25461-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="25461-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25461-128">-Confirm</span></span>
<span data-ttu-id="25461-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="25461-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25461-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25461-130">-WhatIf</span></span>
<span data-ttu-id="25461-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25461-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25461-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="25461-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25461-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25461-133">CommonParameters</span></span>
<span data-ttu-id="25461-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25461-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25461-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25461-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25461-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25461-136">INPUTS</span></span>

### <span data-ttu-id="25461-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="25461-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="25461-138">System.String</span><span class="sxs-lookup"><span data-stu-id="25461-138">System.String</span></span>

## <span data-ttu-id="25461-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25461-139">OUTPUTS</span></span>

### <span data-ttu-id="25461-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="25461-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="25461-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="25461-141">NOTES</span></span>

## <span data-ttu-id="25461-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25461-142">RELATED LINKS</span></span>
