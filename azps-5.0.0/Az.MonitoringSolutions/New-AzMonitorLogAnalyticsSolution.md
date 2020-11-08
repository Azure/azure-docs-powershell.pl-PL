---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233875"
---
# <span data-ttu-id="ea12d-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="ea12d-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="ea12d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea12d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea12d-103">Tworzy rozwiązanie dziennika.</span><span class="sxs-lookup"><span data-stu-id="ea12d-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="ea12d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea12d-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea12d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ea12d-105">DESCRIPTION</span></span>
<span data-ttu-id="ea12d-106">Tworzy rozwiązanie dziennika.</span><span class="sxs-lookup"><span data-stu-id="ea12d-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="ea12d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea12d-107">EXAMPLES</span></span>

### <span data-ttu-id="ea12d-108">Przykład 1: Tworzenie rozwiązania analizy dzienników monitora dla obszaru roboczego Analiza dzienników</span><span class="sxs-lookup"><span data-stu-id="ea12d-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="ea12d-109">To polecenie tworzy rozwiązanie analizy dzienników dla obszaru roboczego Analiza dzienników.</span><span class="sxs-lookup"><span data-stu-id="ea12d-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="ea12d-110">Najczęściej używane typy to:</span><span class="sxs-lookup"><span data-stu-id="ea12d-110">Commonly used types are:</span></span>

| <span data-ttu-id="ea12d-111">Wpisywać</span><span class="sxs-lookup"><span data-stu-id="ea12d-111">Type</span></span> | <span data-ttu-id="ea12d-112">Opis</span><span class="sxs-lookup"><span data-stu-id="ea12d-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="ea12d-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="ea12d-113">SecurityCenterFree</span></span> |  <span data-ttu-id="ea12d-114">Usługa Azure Security Center — bezpłatna wersja</span><span class="sxs-lookup"><span data-stu-id="ea12d-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="ea12d-115">Zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="ea12d-115">Security</span></span> | <span data-ttu-id="ea12d-116">Usługa Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="ea12d-116">Azure Security Center</span></span> |
| <span data-ttu-id="ea12d-117">Aktualizacje</span><span class="sxs-lookup"><span data-stu-id="ea12d-117">Updates</span></span> | <span data-ttu-id="ea12d-118">Zarządzanie aktualizacją</span><span class="sxs-lookup"><span data-stu-id="ea12d-118">Update Management</span></span> |
| <span data-ttu-id="ea12d-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="ea12d-119">ContainerInsights</span></span> | <span data-ttu-id="ea12d-120">Monitor Azure dla kontenerów</span><span class="sxs-lookup"><span data-stu-id="ea12d-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="ea12d-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="ea12d-121">ServiceMap</span></span> | <span data-ttu-id="ea12d-122">Mapa usługi</span><span class="sxs-lookup"><span data-stu-id="ea12d-122">Service Map</span></span> |
| <span data-ttu-id="ea12d-123">Usługa Azure</span><span class="sxs-lookup"><span data-stu-id="ea12d-123">AzureActivity</span></span> | <span data-ttu-id="ea12d-124">Analiza dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="ea12d-124">Activity log analytics</span></span> |
| <span data-ttu-id="ea12d-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="ea12d-125">ChangeTracking</span></span> | <span data-ttu-id="ea12d-126">Śledzenie zmian i stan zapasów</span><span class="sxs-lookup"><span data-stu-id="ea12d-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="ea12d-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="ea12d-127">VMInsights</span></span> | <span data-ttu-id="ea12d-128">Monitor Azure dla maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="ea12d-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="ea12d-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="ea12d-129">SecurityInsights</span></span> | <span data-ttu-id="ea12d-130">Azure — wskaźnik</span><span class="sxs-lookup"><span data-stu-id="ea12d-130">Azure Sentinel</span></span> |
| <span data-ttu-id="ea12d-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="ea12d-131">NetworkMonitoring</span></span> | <span data-ttu-id="ea12d-132">Monitor wydajności sieci</span><span class="sxs-lookup"><span data-stu-id="ea12d-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="ea12d-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="ea12d-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="ea12d-134">Ocena luki w zabezpieczeniach SQL</span><span class="sxs-lookup"><span data-stu-id="ea12d-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="ea12d-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ea12d-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="ea12d-136">Zaawansowana ochrona przed zagrożeniami SQL</span><span class="sxs-lookup"><span data-stu-id="ea12d-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="ea12d-137">Przed złośliwym oprogramowaniem</span><span class="sxs-lookup"><span data-stu-id="ea12d-137">AntiMalware</span></span> | <span data-ttu-id="ea12d-138">Ocena ochrony przed złośliwym oprogramowaniem</span><span class="sxs-lookup"><span data-stu-id="ea12d-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="ea12d-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="ea12d-139">AzureAutomation</span></span> | <span data-ttu-id="ea12d-140">Hybrydowy proces automatyzacji</span><span class="sxs-lookup"><span data-stu-id="ea12d-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="ea12d-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="ea12d-141">LogicAppsManagement</span></span> | <span data-ttu-id="ea12d-142">Zarządzanie aplikacjami logicznymi</span><span class="sxs-lookup"><span data-stu-id="ea12d-142">Logic Apps Management</span></span> |
| <span data-ttu-id="ea12d-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="ea12d-143">SQLDataClassification</span></span> | <span data-ttu-id="ea12d-144">Funkcja wykrywania danych SQL & Klasyfikacja</span><span class="sxs-lookup"><span data-stu-id="ea12d-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="ea12d-145">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea12d-145">PARAMETERS</span></span>

### <span data-ttu-id="ea12d-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea12d-146">-DefaultProfile</span></span>
<span data-ttu-id="ea12d-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea12d-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea12d-148">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ea12d-148">-Location</span></span>
<span data-ttu-id="ea12d-149">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ea12d-149">Resource location.</span></span>
<span data-ttu-id="ea12d-150">Musi być taki sam jak obszar roboczy analityczny dziennik.</span><span class="sxs-lookup"><span data-stu-id="ea12d-150">Must be the same as the log analytic workspace.</span></span>

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

### <span data-ttu-id="ea12d-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea12d-151">-ResourceGroupName</span></span>
<span data-ttu-id="ea12d-152">Nazwa grupy zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="ea12d-152">The name of the resource group to get.</span></span>
<span data-ttu-id="ea12d-153">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="ea12d-153">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ea12d-154">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ea12d-154">-SubscriptionId</span></span>
<span data-ttu-id="ea12d-155">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ea12d-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ea12d-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ea12d-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ea12d-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="ea12d-157">-Tag</span></span>
<span data-ttu-id="ea12d-158">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="ea12d-158">Resource tags</span></span>

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

### <span data-ttu-id="ea12d-159">-Type</span><span class="sxs-lookup"><span data-stu-id="ea12d-159">-Type</span></span>
<span data-ttu-id="ea12d-160">Typ rozwiązania, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="ea12d-160">Type of the solution to be created.</span></span>
<span data-ttu-id="ea12d-161">Na przykład "kontener".</span><span class="sxs-lookup"><span data-stu-id="ea12d-161">For example "Container".</span></span>

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

### <span data-ttu-id="ea12d-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="ea12d-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="ea12d-163">Identyfikator zasobu platformy Azure dla obszaru roboczego, w którym zostanie wdrożone/włączone rozwiązanie.</span><span class="sxs-lookup"><span data-stu-id="ea12d-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

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

### <span data-ttu-id="ea12d-164">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea12d-164">-Confirm</span></span>
<span data-ttu-id="ea12d-165">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea12d-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea12d-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea12d-166">-WhatIf</span></span>
<span data-ttu-id="ea12d-167">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea12d-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea12d-168">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea12d-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea12d-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea12d-169">CommonParameters</span></span>
<span data-ttu-id="ea12d-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea12d-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea12d-171">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea12d-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea12d-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea12d-172">INPUTS</span></span>

## <span data-ttu-id="ea12d-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea12d-173">OUTPUTS</span></span>

### <span data-ttu-id="ea12d-174">Microsoft. Azure. PowerShell. polecenia. MonitoringSolutions. models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="ea12d-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="ea12d-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea12d-175">NOTES</span></span>

<span data-ttu-id="ea12d-176">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ea12d-176">ALIASES</span></span>

## <span data-ttu-id="ea12d-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea12d-177">RELATED LINKS</span></span>



[<span data-ttu-id="ea12d-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ea12d-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

