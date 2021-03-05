---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: c698c91f8b4115fb811ebcda41eaf43662f0bf08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986623"
---
# <span data-ttu-id="09e8c-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="09e8c-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="09e8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="09e8c-103">Odrzuć zagregowany alert iot</span><span class="sxs-lookup"><span data-stu-id="09e8c-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="09e8c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="09e8c-104">SYNTAX</span></span>

### <span data-ttu-id="09e8c-105">SolutionLevelResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="09e8c-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09e8c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="09e8c-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09e8c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="09e8c-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09e8c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="09e8c-108">DESCRIPTION</span></span>
<span data-ttu-id="09e8c-109">Polecenie Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet odrzuca określony alert agregowany na urządzeniach centrum iot.</span><span class="sxs-lookup"><span data-stu-id="09e8c-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="09e8c-110">Nazwa alertów agregowanych to kombinacja typu alertu i daty zagregowanej alertu oddzielona przecinkiem "/".</span><span class="sxs-lookup"><span data-stu-id="09e8c-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="09e8c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="09e8c-111">EXAMPLES</span></span>

### <span data-ttu-id="09e8c-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="09e8c-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="09e8c-113">Odrzuć zagregowany alert "IoT_SucessfulLocalLogin/2020-03-15" (nazwa połączona z typem alertu i zagregowaną datą) z rozwiązania zabezpieczeń IoT "MySolutionName" w grupie zasobów "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="09e8c-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="09e8c-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="09e8c-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="09e8c-115">Odrzuć zagregowany alert o identyfikatorze zasobu "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span><span class="sxs-lookup"><span data-stu-id="09e8c-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="09e8c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09e8c-116">PARAMETERS</span></span>

### <span data-ttu-id="09e8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09e8c-117">-DefaultProfile</span></span>
<span data-ttu-id="09e8c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="09e8c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09e8c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09e8c-119">-InputObject</span></span>
<span data-ttu-id="09e8c-120">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="09e8c-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="09e8c-121">-Name</span></span>
<span data-ttu-id="09e8c-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="09e8c-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09e8c-123">-PassThru</span></span>
<span data-ttu-id="09e8c-124">Sprawdź, czy operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="09e8c-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="09e8c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09e8c-125">-ResourceGroupName</span></span>
<span data-ttu-id="09e8c-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="09e8c-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09e8c-127">-ResourceId</span></span>
<span data-ttu-id="09e8c-128">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="09e8c-128">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-129">—SolutionName</span><span class="sxs-lookup"><span data-stu-id="09e8c-129">-SolutionName</span></span>
<span data-ttu-id="09e8c-130">Nazwa rozwiązania</span><span class="sxs-lookup"><span data-stu-id="09e8c-130">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09e8c-131">-Confirm</span></span>
<span data-ttu-id="09e8c-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="09e8c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09e8c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09e8c-133">-WhatIf</span></span>
<span data-ttu-id="09e8c-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09e8c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09e8c-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="09e8c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09e8c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e8c-136">CommonParameters</span></span>
<span data-ttu-id="09e8c-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09e8c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e8c-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09e8c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e8c-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09e8c-139">INPUTS</span></span>

### <span data-ttu-id="09e8c-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="09e8c-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="09e8c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="09e8c-141">System.String</span></span>

## <span data-ttu-id="09e8c-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09e8c-142">OUTPUTS</span></span>

### <span data-ttu-id="09e8c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="09e8c-143">System.Boolean</span></span>

## <span data-ttu-id="09e8c-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="09e8c-144">NOTES</span></span>

## <span data-ttu-id="09e8c-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09e8c-145">RELATED LINKS</span></span>
