---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: ff9a54852d84d7c1183e81cb8b597279f357ebe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965738"
---
# <span data-ttu-id="0ebc0-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="0ebc0-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="0ebc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ebc0-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebc0-103">Tworzy rozwiązanie do analizy dziennika.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="0ebc0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0ebc0-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0ebc0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0ebc0-105">DESCRIPTION</span></span>
<span data-ttu-id="0ebc0-106">Tworzy rozwiązanie do analizy dziennika.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="0ebc0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0ebc0-107">EXAMPLES</span></span>

### <span data-ttu-id="0ebc0-108">Przykład 1. Tworzenie rozwiązania do analizy dzienników monitorów dla obszaru roboczego analizy dziennika</span><span class="sxs-lookup"><span data-stu-id="0ebc0-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="0ebc0-109">To polecenie tworzy rozwiązanie do analizy dzienników monitorów dla obszaru roboczego analizy dziennika.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="0ebc0-110">Najczęściej używane typy:</span><span class="sxs-lookup"><span data-stu-id="0ebc0-110">Commonly used types are:</span></span>

| <span data-ttu-id="0ebc0-111">Typ</span><span class="sxs-lookup"><span data-stu-id="0ebc0-111">Type</span></span> | <span data-ttu-id="0ebc0-112">Opis</span><span class="sxs-lookup"><span data-stu-id="0ebc0-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="0ebc0-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="0ebc0-113">SecurityCenterFree</span></span> |  <span data-ttu-id="0ebc0-114">Azure Security Center — wersja bezpłatna</span><span class="sxs-lookup"><span data-stu-id="0ebc0-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="0ebc0-115">Zabezpieczenia</span><span class="sxs-lookup"><span data-stu-id="0ebc0-115">Security</span></span> | <span data-ttu-id="0ebc0-116">Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="0ebc0-116">Azure Security Center</span></span> |
| <span data-ttu-id="0ebc0-117">Aktualizacje</span><span class="sxs-lookup"><span data-stu-id="0ebc0-117">Updates</span></span> | <span data-ttu-id="0ebc0-118">Zarządzanie aktualizacjami</span><span class="sxs-lookup"><span data-stu-id="0ebc0-118">Update Management</span></span> |
| <span data-ttu-id="0ebc0-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="0ebc0-119">ContainerInsights</span></span> | <span data-ttu-id="0ebc0-120">Azure Monitor for Containers</span><span class="sxs-lookup"><span data-stu-id="0ebc0-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="0ebc0-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="0ebc0-121">ServiceMap</span></span> | <span data-ttu-id="0ebc0-122">Mapa usługi</span><span class="sxs-lookup"><span data-stu-id="0ebc0-122">Service Map</span></span> |
| <span data-ttu-id="0ebc0-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="0ebc0-123">AzureActivity</span></span> | <span data-ttu-id="0ebc0-124">Analiza dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="0ebc0-124">Activity log analytics</span></span> |
| <span data-ttu-id="0ebc0-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="0ebc0-125">ChangeTracking</span></span> | <span data-ttu-id="0ebc0-126">Śledzenie zmian i spis</span><span class="sxs-lookup"><span data-stu-id="0ebc0-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="0ebc0-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="0ebc0-127">VMInsights</span></span> | <span data-ttu-id="0ebc0-128">Azure Monitor dla maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="0ebc0-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="0ebc0-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="0ebc0-129">SecurityInsights</span></span> | <span data-ttu-id="0ebc0-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="0ebc0-130">Azure Sentinel</span></span> |
| <span data-ttu-id="0ebc0-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="0ebc0-131">NetworkMonitoring</span></span> | <span data-ttu-id="0ebc0-132">Monitor wydajności sieci</span><span class="sxs-lookup"><span data-stu-id="0ebc0-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="0ebc0-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="0ebc0-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="0ebc0-134">Ocena luk w zabezpieczeniach języka SQL</span><span class="sxs-lookup"><span data-stu-id="0ebc0-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="0ebc0-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="0ebc0-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="0ebc0-136">Zaawansowana ochrona przed zagrożeniami w języku SQL</span><span class="sxs-lookup"><span data-stu-id="0ebc0-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="0ebc0-137">Ochrona przed złośliwym oprogramowaniem</span><span class="sxs-lookup"><span data-stu-id="0ebc0-137">AntiMalware</span></span> | <span data-ttu-id="0ebc0-138">Ocena oprogramowania w celu ochrony przed złośliwym oprogramowaniem</span><span class="sxs-lookup"><span data-stu-id="0ebc0-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="0ebc0-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="0ebc0-139">AzureAutomation</span></span> | <span data-ttu-id="0ebc0-140">Pracownik hybrydowy automatyzacji</span><span class="sxs-lookup"><span data-stu-id="0ebc0-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="0ebc0-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="0ebc0-141">LogicAppsManagement</span></span> | <span data-ttu-id="0ebc0-142">Zarządzanie aplikacjami logic</span><span class="sxs-lookup"><span data-stu-id="0ebc0-142">Logic Apps Management</span></span> |
| <span data-ttu-id="0ebc0-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="0ebc0-143">SQLDataClassification</span></span> | <span data-ttu-id="0ebc0-144">Klasyfikacja & odnajdowania danych SQL</span><span class="sxs-lookup"><span data-stu-id="0ebc0-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="0ebc0-145">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ebc0-145">PARAMETERS</span></span>

### <span data-ttu-id="0ebc0-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebc0-146">-DefaultProfile</span></span>
<span data-ttu-id="0ebc0-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebc0-148">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0ebc0-148">-Location</span></span>
<span data-ttu-id="0ebc0-149">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-149">Resource location.</span></span>
<span data-ttu-id="0ebc0-150">Musi być taki sam jak obszar roboczy analityczny dziennika.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-150">Must be the same as the log analytic workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebc0-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ebc0-151">-ResourceGroupName</span></span>
<span data-ttu-id="0ebc0-152">Nazwa grupy zasobów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-152">The name of the resource group to get.</span></span>
<span data-ttu-id="0ebc0-153">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-153">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebc0-154">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ebc0-154">-SubscriptionId</span></span>
<span data-ttu-id="0ebc0-155">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0ebc0-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebc0-157">— Tag</span><span class="sxs-lookup"><span data-stu-id="0ebc0-157">-Tag</span></span>
<span data-ttu-id="0ebc0-158">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="0ebc0-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebc0-159">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="0ebc0-159">-Type</span></span>
<span data-ttu-id="0ebc0-160">Typ rozwiązania do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-160">Type of the solution to be created.</span></span>
<span data-ttu-id="0ebc0-161">Na przykład "Kontener".</span><span class="sxs-lookup"><span data-stu-id="0ebc0-161">For example "Container".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebc0-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="0ebc0-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="0ebc0-163">Identyfikator zasobu Azure dla obszaru roboczego, w którym rozwiązanie zostanie wdrożone/włączone.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebc0-164">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0ebc0-164">-Confirm</span></span>
<span data-ttu-id="0ebc0-165">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ebc0-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ebc0-166">-WhatIf</span></span>
<span data-ttu-id="0ebc0-167">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ebc0-168">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ebc0-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebc0-169">CommonParameters</span></span>
<span data-ttu-id="0ebc0-170">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebc0-171">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ebc0-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebc0-172">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ebc0-172">INPUTS</span></span>

## <span data-ttu-id="0ebc0-173">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ebc0-173">OUTPUTS</span></span>

### <span data-ttu-id="0ebc0-174">Microsoft.Azure.PowerShell.Cmdlet.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="0ebc0-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="0ebc0-175">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0ebc0-175">NOTES</span></span>

<span data-ttu-id="0ebc0-176">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0ebc0-176">ALIASES</span></span>

## <span data-ttu-id="0ebc0-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ebc0-177">RELATED LINKS</span></span>



[<span data-ttu-id="0ebc0-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0ebc0-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

