---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178659"
---
# <span data-ttu-id="4f61b-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="4f61b-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="4f61b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f61b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f61b-103">Odrzuć zagregowany alert iot</span><span class="sxs-lookup"><span data-stu-id="4f61b-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="4f61b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4f61b-104">SYNTAX</span></span>

### <span data-ttu-id="4f61b-105">SolutionLevelResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="4f61b-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f61b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4f61b-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f61b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f61b-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f61b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4f61b-108">DESCRIPTION</span></span>
<span data-ttu-id="4f61b-109">Polecenie Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet odrzuca określony alert agregowany na urządzeniach centrum iot.</span><span class="sxs-lookup"><span data-stu-id="4f61b-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="4f61b-110">Nazwa alertów agregowanych to kombinacja typu alertu i daty zagregowanej alertu, oddzielona przecinkiem "/".</span><span class="sxs-lookup"><span data-stu-id="4f61b-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="4f61b-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4f61b-111">EXAMPLES</span></span>

### <span data-ttu-id="4f61b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4f61b-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="4f61b-113">Odrzuć zagregowany alert "IoT_SucessfulLocalLogin/2020-03-15" (nazwa połączona z typem alertu i zagregowaną datą) z rozwiązania zabezpieczeń IoT "MySolutionName" w grupie zasobów "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="4f61b-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="4f61b-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4f61b-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="4f61b-115">Odrzuć zagregowany alert o identyfikatorze zasobu "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span><span class="sxs-lookup"><span data-stu-id="4f61b-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="4f61b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f61b-116">PARAMETERS</span></span>

### <span data-ttu-id="4f61b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f61b-117">-DefaultProfile</span></span>
<span data-ttu-id="4f61b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f61b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f61b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f61b-119">-InputObject</span></span>
<span data-ttu-id="4f61b-120">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="4f61b-120">Input Object.</span></span>

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

### <span data-ttu-id="4f61b-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4f61b-121">-Name</span></span>
<span data-ttu-id="4f61b-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="4f61b-122">Resource name.</span></span>

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

### <span data-ttu-id="4f61b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f61b-123">-PassThru</span></span>
<span data-ttu-id="4f61b-124">Sprawdź, czy operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="4f61b-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="4f61b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f61b-125">-ResourceGroupName</span></span>
<span data-ttu-id="4f61b-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4f61b-126">Resource group name.</span></span>

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

### <span data-ttu-id="4f61b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f61b-127">-ResourceId</span></span>
<span data-ttu-id="4f61b-128">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="4f61b-128">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="4f61b-129">—SolutionName</span><span class="sxs-lookup"><span data-stu-id="4f61b-129">-SolutionName</span></span>
<span data-ttu-id="4f61b-130">Nazwa rozwiązania</span><span class="sxs-lookup"><span data-stu-id="4f61b-130">Solution name</span></span>

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

### <span data-ttu-id="4f61b-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4f61b-131">-Confirm</span></span>
<span data-ttu-id="4f61b-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4f61b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f61b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f61b-133">-WhatIf</span></span>
<span data-ttu-id="4f61b-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f61b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f61b-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4f61b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f61b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f61b-136">CommonParameters</span></span>
<span data-ttu-id="4f61b-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f61b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f61b-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f61b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f61b-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f61b-139">INPUTS</span></span>

### <span data-ttu-id="4f61b-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="4f61b-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="4f61b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4f61b-141">System.String</span></span>

## <span data-ttu-id="4f61b-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4f61b-142">OUTPUTS</span></span>

### <span data-ttu-id="4f61b-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4f61b-143">System.Boolean</span></span>

## <span data-ttu-id="4f61b-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4f61b-144">NOTES</span></span>

## <span data-ttu-id="4f61b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f61b-145">RELATED LINKS</span></span>
