---
ms.openlocfilehash: 3848f7fb8e298d137c747405f32a0776c1a8f029
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048635"
---
## <a name="200---may-2019"></a><span data-ttu-id="aef7a-101">2.0.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="aef7a-101">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aef7a-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aef7a-102">Az.Accounts</span></span>
* <span data-ttu-id="aef7a-103">Aktualizacja biblioteki uwierzytelniania w celu rozwiązania problemów z usługą ADFS dotyczących uwierzytelniania nazwy użytkownika i hasła</span><span class="sxs-lookup"><span data-stu-id="aef7a-103">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="aef7a-104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-104">Az.CognitiveServices</span></span>
* <span data-ttu-id="aef7a-105">Dla usług wyszukiwania Bing wyświetlane jest tylko zrzeczenie odpowiedzialności usługi Bing.</span><span class="sxs-lookup"><span data-stu-id="aef7a-105">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="aef7a-106">Naprawiono błąd polegający na niepomyślnym tworzeniu konta.</span><span class="sxs-lookup"><span data-stu-id="aef7a-106">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aef7a-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aef7a-107">Az.Compute</span></span>
* <span data-ttu-id="aef7a-108">Funkcja Grupa umieszczania w pobliżu.</span><span class="sxs-lookup"><span data-stu-id="aef7a-108">Proximity placement group feature.</span></span>
    - <span data-ttu-id="aef7a-109">Dodano następujące nowe polecenia cmdlet:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="aef7a-109">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="aef7a-110">Do następujących poleceń cmdlet dodano nowy parametr ProximityPlacementGroupId:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="aef7a-110">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="aef7a-111">Do polecenia New-AzGalleryImageVersion dodano parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="aef7a-111">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="aef7a-112">Właściwość TargetRegion polecenia New-AzGalleryImageVersion może zawierać parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="aef7a-112">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="aef7a-113">Do poleceń Stop-AzVM i Stop-AzVmss dodano parametr przełącznika SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="aef7a-113">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="aef7a-114">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="aef7a-114">Breaking changes</span></span>
    - <span data-ttu-id="aef7a-115">Polecenie Set-AzVMBootDiagnostics zamieniono na polecenie Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="aef7a-115">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="aef7a-116">Polecenie Export-AzLogAnalyticThrottledRequests zamieniono na polecenie Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="aef7a-116">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="aef7a-117">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="aef7a-117">Az.DeploymentManager</span></span>
* <span data-ttu-id="aef7a-118">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="aef7a-118">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="aef7a-119">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="aef7a-119">Az.Dns</span></span>
* <span data-ttu-id="aef7a-120">Automatyczne delegowanie serwera nazw systemu DNS</span><span class="sxs-lookup"><span data-stu-id="aef7a-120">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="aef7a-121">Polecenie cmdlet tworzenia strefy DNS akceptuje nazwę strefy nadrzędnej jako dodatkowy parametr opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="aef7a-121">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="aef7a-122">Dodaje rekordy serwera nazw w strefie nadrzędnej dla nowo utworzonej strefy podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="aef7a-122">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="aef7a-123">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="aef7a-123">Az.FrontDoor</span></span>
* <span data-ttu-id="aef7a-124">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="aef7a-124">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="aef7a-125">Zmiana nazw poleceń cmdlet zapory aplikacji internetowej w celu dołączenia ciągu „Waf”</span><span class="sxs-lookup"><span data-stu-id="aef7a-125">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="aef7a-126">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="aef7a-126">Az.HDInsight</span></span>
* <span data-ttu-id="aef7a-127">Usunięto dwa polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="aef7a-127">Removed two cmdlets:</span></span>
    - <span data-ttu-id="aef7a-128">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="aef7a-128">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="aef7a-129">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="aef7a-129">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="aef7a-130">Dodano nowe polecenie cmdlet Set-AzHDInsightGatewayCredential w celu zastąpienia polecenia Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="aef7a-130">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="aef7a-131">Zaktualizowano polecenie cmdlet Get-AzHDInsightJobOutput, aby rozróżnić rolę czytelnika i rolę operatora usługi HDInsight:</span><span class="sxs-lookup"><span data-stu-id="aef7a-131">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="aef7a-132">Użytkownicy z rolą czytelnika muszą jawnie określić parametr „DefaultStorageAccountKey” — w przeciwnym razie wystąpi błąd.</span><span class="sxs-lookup"><span data-stu-id="aef7a-132">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="aef7a-133">Nie będzie to miało wpływu na użytkowników z rolą operatora usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="aef7a-133">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="aef7a-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="aef7a-134">Az.Monitor</span></span>
* <span data-ttu-id="aef7a-135">Nowe polecenia cmdlet dla interfejsu API SQR (Scheduled Query Rule, reguła zaplanowanego zapytania)</span><span class="sxs-lookup"><span data-stu-id="aef7a-135">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="aef7a-136">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="aef7a-136">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="aef7a-137">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="aef7a-137">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="aef7a-138">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="aef7a-138">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="aef7a-139">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="aef7a-139">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="aef7a-140">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="aef7a-140">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="aef7a-141">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="aef7a-141">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="aef7a-142">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="aef7a-142">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="aef7a-143">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="aef7a-143">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="aef7a-144">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="aef7a-144">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="aef7a-145">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="aef7a-145">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="aef7a-146">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="aef7a-146">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="aef7a-147">[Więcej](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) informacji na temat interfejsu API SQR</span><span class="sxs-lookup"><span data-stu-id="aef7a-147">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="aef7a-148">Zaktualizowano plik Az.Monitor.md w celu uwzględnienia poleceń cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="aef7a-148">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aef7a-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aef7a-149">Az.Network</span></span>
* <span data-ttu-id="aef7a-150">Dodano obsługę dla zasobu usługi NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="aef7a-150">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="aef7a-151">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="aef7a-151">New cmdlets</span></span>
        - <span data-ttu-id="aef7a-152">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="aef7a-152">New-AzNatGateway</span></span>
        - <span data-ttu-id="aef7a-153">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="aef7a-153">Get-AzNatGateway</span></span>
        - <span data-ttu-id="aef7a-154">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="aef7a-154">Set-AzNatGateway</span></span>
        - <span data-ttu-id="aef7a-155">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="aef7a-155">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="aef7a-156">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="aef7a-156">Updated cmdlets</span></span>
        - <span data-ttu-id="aef7a-157">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="aef7a-157">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="aef7a-158">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="aef7a-158">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="aef7a-159">Zaktualizowano poniższe polecenia dla funkcji: Ustawianie/usuwanie tras niestandardowych dla bramy Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="aef7a-159">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="aef7a-160">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="aef7a-160">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="aef7a-161">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="aef7a-161">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="aef7a-162">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="aef7a-162">Az.PolicyInsights</span></span>
* <span data-ttu-id="aef7a-163">Obsługa zapytań dotyczących szczegółów oceny zasad.</span><span class="sxs-lookup"><span data-stu-id="aef7a-163">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="aef7a-164">Dodano parametr „-Expand” do polecenia Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="aef7a-164">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="aef7a-165">Obsługa polecenia „-Expand PolicyEvaluationDetails”.</span><span class="sxs-lookup"><span data-stu-id="aef7a-165">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aef7a-166">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-166">Az.RecoveryServices</span></span>
* <span data-ttu-id="aef7a-167">Obsługa odzyskiwania lokacji między subskrypcjami z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="aef7a-167">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="aef7a-168">Oznaczanie nadchodzących zmian powodujących niezgodność dla usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="aef7a-168">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="aef7a-169">Poprawka zakończenia planu akcji dla planu odzyskiwania usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="aef7a-169">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="aef7a-170">Poprawka aktualizacji mapowania sieci usługi Azure Site Recovery z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="aef7a-170">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="aef7a-171">Poprawka aktualizacji kierunku ochrony usługi Azure Site Recovery z platformy Azure na platformę Azure dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="aef7a-171">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="aef7a-172">Inne drobne poprawki.</span><span class="sxs-lookup"><span data-stu-id="aef7a-172">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="aef7a-173">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="aef7a-173">Az.Relay</span></span>
* <span data-ttu-id="aef7a-174">Poprawiono błędy pisowni w komunikatach przeznaczonych dla klientów</span><span class="sxs-lookup"><span data-stu-id="aef7a-174">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="aef7a-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aef7a-175">Az.ServiceBus</span></span>
* <span data-ttu-id="aef7a-176">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="aef7a-176">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aef7a-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aef7a-177">Az.Storage</span></span>
* <span data-ttu-id="aef7a-178">Uaktualnienie biblioteki klienta usługi Storage do wersji 10.0.1 (przestrzeń nazw wszystkich obiektów tego zestawu SDK została zmieniona z „Microsoft.WindowsAzure.Storage.*” na „Microsoft.Azure.Storage.*”)</span><span class="sxs-lookup"><span data-stu-id="aef7a-178">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="aef7a-179">Uaktualnienie do wersji Microsoft.Azure.Management.Storage 11.0.0 w celu obsługi nowego interfejsu API w wersji 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="aef7a-179">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="aef7a-180">Domyślny rodzaj konta magazynu w poleceniu Utwórz konto magazynu został zmieniony ze „Storage” na „StorageV2”</span><span class="sxs-lookup"><span data-stu-id="aef7a-180">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="aef7a-181">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aef7a-181">New-AzStorageAccount</span></span>
* <span data-ttu-id="aef7a-182">Zmiana wyjściowego parametru Sku.Name polecenia cmdlet konta magazynu w celu wyrównania z wejściowym parametrem SkuName przez dodanie znaku „-”, na przykład zmiana „StandardLRS” na „Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="aef7a-182">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="aef7a-183">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aef7a-183">New-AzStorageAccount</span></span>
    - <span data-ttu-id="aef7a-184">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aef7a-184">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="aef7a-185">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aef7a-185">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aef7a-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aef7a-186">Az.Websites</span></span>
* <span data-ttu-id="aef7a-187">Właściwość „Kind” będzie teraz ustawiona dla obiektów PSSite zwracanych przez polecenie Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="aef7a-187">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="aef7a-188">Polecenia Get-AzWebApp\*Metrics i Get-AzAppServicePlanMetrics oznaczono jako przestarzałe</span><span class="sxs-lookup"><span data-stu-id="aef7a-188">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="aef7a-189">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="aef7a-189">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="aef7a-190">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="aef7a-190">Highlights since the last major release</span></span>
* <span data-ttu-id="aef7a-191">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="aef7a-191">General availability of `Az` module</span></span>
* <span data-ttu-id="aef7a-192">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="aef7a-192">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="aef7a-193">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="aef7a-193">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="aef7a-194">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="aef7a-194">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="aef7a-195">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="aef7a-195">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="aef7a-196">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aef7a-196">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="aef7a-197">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="aef7a-197">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="aef7a-198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aef7a-198">Az.Accounts</span></span>
* <span data-ttu-id="aef7a-199">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="aef7a-199">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="aef7a-200">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="aef7a-200">Az.Batch</span></span>
* <span data-ttu-id="aef7a-201">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="aef7a-202">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="aef7a-202">Az.Cdn</span></span>
* <span data-ttu-id="aef7a-203">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="aef7a-204">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-204">Az.CognitiveServices</span></span>
* <span data-ttu-id="aef7a-205">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aef7a-206">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aef7a-206">Az.Compute</span></span>
* <span data-ttu-id="aef7a-207">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="aef7a-207">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="aef7a-208">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aef7a-209">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="aef7a-209">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aef7a-210">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aef7a-210">Az.DataFactory</span></span>
* <span data-ttu-id="aef7a-211">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="aef7a-211">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aef7a-212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aef7a-212">Az.DataLakeStore</span></span>
* <span data-ttu-id="aef7a-213">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-213">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="aef7a-214">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="aef7a-214">Az.EventGrid</span></span>
* <span data-ttu-id="aef7a-215">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="aef7a-215">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="aef7a-216">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="aef7a-216">Az.EventHub</span></span>
* <span data-ttu-id="aef7a-217">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="aef7a-217">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="aef7a-218">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="aef7a-218">Az.HDInsight</span></span>
* <span data-ttu-id="aef7a-219">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="aef7a-220">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="aef7a-220">Az.IotHub</span></span>
* <span data-ttu-id="aef7a-221">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-221">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="aef7a-222">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aef7a-222">Az.KeyVault</span></span>
* <span data-ttu-id="aef7a-223">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-223">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aef7a-224">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="aef7a-224">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="aef7a-225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="aef7a-225">Az.MachineLearning</span></span>
* <span data-ttu-id="aef7a-226">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-226">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="aef7a-227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="aef7a-227">Az.Media</span></span>
* <span data-ttu-id="aef7a-228">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-228">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="aef7a-229">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="aef7a-229">Az.Monitor</span></span>
  * <span data-ttu-id="aef7a-230">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="aef7a-230">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="aef7a-231">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="aef7a-231">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="aef7a-232">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="aef7a-232">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="aef7a-233">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="aef7a-233">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="aef7a-234">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="aef7a-234">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="aef7a-235">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="aef7a-235">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="aef7a-236">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="aef7a-236">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aef7a-237">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aef7a-237">Az.Network</span></span>
* <span data-ttu-id="aef7a-238">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aef7a-239">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="aef7a-239">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="aef7a-240">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="aef7a-240">Az.NotificationHubs</span></span>
* <span data-ttu-id="aef7a-241">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-241">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="aef7a-242">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aef7a-242">Az.OperationalInsights</span></span>
* <span data-ttu-id="aef7a-243">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="aef7a-244">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="aef7a-244">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="aef7a-245">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aef7a-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="aef7a-247">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-247">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aef7a-248">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="aef7a-248">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="aef7a-249">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="aef7a-249">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="aef7a-250">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="aef7a-250">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="aef7a-251">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="aef7a-251">Az.RedisCache</span></span>
* <span data-ttu-id="aef7a-252">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="aef7a-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aef7a-253">Az.Resources</span></span>
* <span data-ttu-id="aef7a-254">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="aef7a-254">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="aef7a-255">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aef7a-255">Az.Sql</span></span>
* <span data-ttu-id="aef7a-256">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="aef7a-256">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="aef7a-257">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aef7a-258">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="aef7a-258">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="aef7a-259">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="aef7a-259">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="aef7a-260">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="aef7a-260">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="aef7a-261">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="aef7a-261">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="aef7a-262">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="aef7a-262">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aef7a-263">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aef7a-263">Az.Websites</span></span>
* <span data-ttu-id="aef7a-264">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="aef7a-264">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="aef7a-265">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="aef7a-265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aef7a-266">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="aef7a-266">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="aef7a-267">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="aef7a-267">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="aef7a-268">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="aef7a-268">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="aef7a-269">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="aef7a-269">Highlights since the last major release</span></span>
* <span data-ttu-id="aef7a-270">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="aef7a-270">General availability of `Az` module</span></span>
* <span data-ttu-id="aef7a-271">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="aef7a-271">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="aef7a-272">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="aef7a-272">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="aef7a-273">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="aef7a-273">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="aef7a-274">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="aef7a-274">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="aef7a-275">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aef7a-275">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="aef7a-276">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="aef7a-276">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="aef7a-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aef7a-277">Az.Accounts</span></span>
* <span data-ttu-id="aef7a-278">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="aef7a-278">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="aef7a-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-279">Az.AnalysisServices</span></span>
* <span data-ttu-id="aef7a-280">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="aef7a-280">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="aef7a-281">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="aef7a-281">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aef7a-282">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aef7a-282">Az.Automation</span></span>
* <span data-ttu-id="aef7a-283">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="aef7a-283">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="aef7a-284">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="aef7a-284">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="aef7a-285">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="aef7a-285">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aef7a-286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aef7a-286">Az.Compute</span></span>
* <span data-ttu-id="aef7a-287">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="aef7a-287">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="aef7a-288">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="aef7a-288">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="aef7a-289">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="aef7a-289">Az.ContainerInstance</span></span>
* <span data-ttu-id="aef7a-290">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="aef7a-290">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aef7a-291">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aef7a-291">Az.DataFactory</span></span>
* <span data-ttu-id="aef7a-292">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="aef7a-292">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="aef7a-293">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="aef7a-293">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="aef7a-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aef7a-294">Az.Resources</span></span>
* <span data-ttu-id="aef7a-295">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="aef7a-295">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="aef7a-296">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="aef7a-296">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="aef7a-297">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="aef7a-297">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="aef7a-298">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="aef7a-298">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="aef7a-299">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="aef7a-299">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="aef7a-300">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="aef7a-300">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="aef7a-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aef7a-301">Az.Sql</span></span>
* <span data-ttu-id="aef7a-302">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="aef7a-302">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aef7a-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aef7a-303">Az.Storage</span></span>
* <span data-ttu-id="aef7a-304">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="aef7a-304">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="aef7a-305">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="aef7a-305">New-AzStorageContext</span></span>
* <span data-ttu-id="aef7a-306">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="aef7a-306">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="aef7a-307">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="aef7a-307">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="aef7a-308">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="aef7a-308">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="aef7a-309">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aef7a-309">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="aef7a-310">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aef7a-310">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="aef7a-311">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="aef7a-311">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="aef7a-312">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="aef7a-312">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="aef7a-313">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="aef7a-313">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="aef7a-314">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="aef7a-314">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="aef7a-315">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="aef7a-315">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="aef7a-316">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="aef7a-316">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="aef7a-317">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="aef7a-317">Highlights since the last major release</span></span>
* <span data-ttu-id="aef7a-318">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="aef7a-318">General availability of `Az` module</span></span>
* <span data-ttu-id="aef7a-319">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="aef7a-319">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="aef7a-320">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="aef7a-320">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="aef7a-321">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="aef7a-321">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="aef7a-322">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="aef7a-322">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="aef7a-323">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aef7a-323">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="aef7a-324">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="aef7a-324">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aef7a-325">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aef7a-325">Az.Automation</span></span>
* <span data-ttu-id="aef7a-326">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="aef7a-326">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="aef7a-327">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="aef7a-327">Dynamic grouping</span></span>
    * <span data-ttu-id="aef7a-328">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="aef7a-328">Pre-Post script</span></span>
    * <span data-ttu-id="aef7a-329">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="aef7a-329">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aef7a-330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aef7a-330">Az.Compute</span></span>
* <span data-ttu-id="aef7a-331">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="aef7a-331">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="aef7a-332">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="aef7a-332">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="aef7a-333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aef7a-333">Az.KeyVault</span></span>
* <span data-ttu-id="aef7a-334">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="aef7a-334">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aef7a-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aef7a-335">Az.Network</span></span>
* <span data-ttu-id="aef7a-336">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="aef7a-336">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="aef7a-337">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="aef7a-337">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aef7a-338">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-338">Az.RecoveryServices</span></span>
* <span data-ttu-id="aef7a-339">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="aef7a-339">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="aef7a-340">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="aef7a-340">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="aef7a-341">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aef7a-341">Az.Resources</span></span>
* <span data-ttu-id="aef7a-342">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aef7a-342">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="aef7a-343">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="aef7a-343">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="aef7a-344">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aef7a-344">Az.Sql</span></span>
* <span data-ttu-id="aef7a-345">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="aef7a-345">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aef7a-346">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aef7a-346">Az.Storage</span></span>
* <span data-ttu-id="aef7a-347">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="aef7a-347">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="aef7a-348">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="aef7a-348">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="aef7a-349">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="aef7a-349">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="aef7a-350">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="aef7a-350">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="aef7a-351">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="aef7a-351">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="aef7a-352">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="aef7a-352">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="aef7a-353">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="aef7a-353">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aef7a-354">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aef7a-354">Az.Websites</span></span>
* <span data-ttu-id="aef7a-355">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="aef7a-355">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="aef7a-356">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="aef7a-356">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aef7a-357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aef7a-357">Az.Accounts</span></span>
* <span data-ttu-id="aef7a-358">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="aef7a-358">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="aef7a-359">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="aef7a-359">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aef7a-360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aef7a-360">Az.Automation</span></span>
* <span data-ttu-id="aef7a-361">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="aef7a-361">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="aef7a-362">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="aef7a-362">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="aef7a-363">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="aef7a-363">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="aef7a-364">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="aef7a-364">Az.Cdn</span></span>
* <span data-ttu-id="aef7a-365">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="aef7a-365">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aef7a-366">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aef7a-366">Az.Compute</span></span>
* <span data-ttu-id="aef7a-367">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="aef7a-367">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aef7a-368">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aef7a-368">Az.DataFactory</span></span>
* <span data-ttu-id="aef7a-369">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="aef7a-369">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="aef7a-370">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="aef7a-370">Az.LogicApp</span></span>
* <span data-ttu-id="aef7a-371">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="aef7a-371">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aef7a-372">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aef7a-372">Az.Network</span></span>
* <span data-ttu-id="aef7a-373">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="aef7a-373">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aef7a-374">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-374">Az.RecoveryServices</span></span>
* <span data-ttu-id="aef7a-375">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="aef7a-375">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="aef7a-376">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="aef7a-376">SDK Update</span></span>
* <span data-ttu-id="aef7a-377">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="aef7a-377">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="aef7a-378">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="aef7a-378">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="aef7a-379">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aef7a-379">Az.Resources</span></span>
* <span data-ttu-id="aef7a-380">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="aef7a-380">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="aef7a-381">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="aef7a-381">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="aef7a-382">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="aef7a-382">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="aef7a-383">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="aef7a-383">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="aef7a-384">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="aef7a-384">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="aef7a-385">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="aef7a-385">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="aef7a-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aef7a-386">Az.Sql</span></span>
* <span data-ttu-id="aef7a-387">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="aef7a-387">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="aef7a-388">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="aef7a-388">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aef7a-389">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aef7a-389">Az.Storage</span></span>
* <span data-ttu-id="aef7a-390">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aef7a-390">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="aef7a-391">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="aef7a-391">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="aef7a-392">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-392">Az.AnalysisServices</span></span>
* <span data-ttu-id="aef7a-393">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="aef7a-393">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aef7a-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aef7a-394">Az.Automation</span></span>
* <span data-ttu-id="aef7a-395">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="aef7a-395">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="aef7a-396">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="aef7a-396">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="aef7a-397">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="aef7a-397">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="aef7a-398">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-398">Az.CognitiveServices</span></span>
* <span data-ttu-id="aef7a-399">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="aef7a-399">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aef7a-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aef7a-400">Az.Compute</span></span>
* <span data-ttu-id="aef7a-401">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="aef7a-401">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="aef7a-402">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="aef7a-402">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="aef7a-403">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="aef7a-403">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="aef7a-404">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="aef7a-404">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aef7a-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aef7a-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="aef7a-406">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="aef7a-406">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="aef7a-407">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="aef7a-407">Az.EventHub</span></span>
* <span data-ttu-id="aef7a-408">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="aef7a-408">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="aef7a-409">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aef7a-409">Az.KeyVault</span></span>
* <span data-ttu-id="aef7a-410">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aef7a-410">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="aef7a-411">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="aef7a-411">Az.LogicApp</span></span>
* <span data-ttu-id="aef7a-412">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="aef7a-412">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="aef7a-413">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="aef7a-413">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="aef7a-414">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="aef7a-414">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="aef7a-415">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aef7a-415">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="aef7a-416">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aef7a-416">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="aef7a-417">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aef7a-417">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="aef7a-418">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aef7a-418">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="aef7a-419">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="aef7a-419">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="aef7a-420">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aef7a-420">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="aef7a-421">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aef7a-421">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="aef7a-422">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aef7a-422">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="aef7a-423">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aef7a-423">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="aef7a-424">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="aef7a-424">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="aef7a-425">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="aef7a-425">Az.Monitor</span></span>
* <span data-ttu-id="aef7a-426">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="aef7a-426">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aef7a-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aef7a-427">Az.Network</span></span>
* <span data-ttu-id="aef7a-428">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="aef7a-428">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="aef7a-429">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aef7a-429">Az.OperationalInsights</span></span>
* <span data-ttu-id="aef7a-430">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="aef7a-430">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="aef7a-431">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="aef7a-431">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="aef7a-432">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="aef7a-432">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="aef7a-433">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aef7a-433">Az.Resources</span></span>
* <span data-ttu-id="aef7a-434">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="aef7a-434">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="aef7a-435">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="aef7a-435">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="aef7a-436">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="aef7a-436">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="aef7a-437">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="aef7a-437">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="aef7a-438">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aef7a-438">Az.Sql</span></span>
* <span data-ttu-id="aef7a-439">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="aef7a-439">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="aef7a-440">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="aef7a-440">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aef7a-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aef7a-441">Az.Websites</span></span>
* <span data-ttu-id="aef7a-442">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="aef7a-442">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="aef7a-443">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="aef7a-443">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aef7a-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aef7a-444">Az.Accounts</span></span>
* <span data-ttu-id="aef7a-445">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="aef7a-445">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="aef7a-446">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-446">Az.AnalysisServices</span></span>
<span data-ttu-id="aef7a-447">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="aef7a-447">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aef7a-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aef7a-448">Az.Compute</span></span>
* <span data-ttu-id="aef7a-449">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="aef7a-449">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="aef7a-450">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="aef7a-450">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="aef7a-451">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="aef7a-451">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aef7a-452">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-452">Az.RecoveryServices</span></span>
<span data-ttu-id="aef7a-453">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="aef7a-453">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="aef7a-454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aef7a-454">Az.Resources</span></span>
* <span data-ttu-id="aef7a-455">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="aef7a-455">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="aef7a-456">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="aef7a-456">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="aef7a-457">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="aef7a-457">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="aef7a-458">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="aef7a-458">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="aef7a-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aef7a-459">Az.Sql</span></span>
* <span data-ttu-id="aef7a-460">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aef7a-460">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="aef7a-461">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="aef7a-461">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="aef7a-462">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="aef7a-462">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="aef7a-463">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="aef7a-463">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aef7a-464">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aef7a-464">Az.Accounts</span></span>
* <span data-ttu-id="aef7a-465">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="aef7a-465">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="aef7a-466">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-466">Az.AnalysisServices</span></span>
* <span data-ttu-id="aef7a-467">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="aef7a-467">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aef7a-468">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-468">Az.RecoveryServices</span></span>
* <span data-ttu-id="aef7a-469">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="aef7a-469">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="aef7a-470">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="aef7a-470">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aef7a-471">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aef7a-471">Az.Accounts</span></span>
* <span data-ttu-id="aef7a-472">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="aef7a-472">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="aef7a-473">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="aef7a-473">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aef7a-474">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="aef7a-474">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="aef7a-475">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="aef7a-475">Az.Aks</span></span>
* <span data-ttu-id="aef7a-476">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="aef7a-476">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aef7a-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aef7a-477">Az.Automation</span></span>
* <span data-ttu-id="aef7a-478">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="aef7a-478">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="aef7a-479">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="aef7a-479">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="aef7a-480">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="aef7a-480">Az.Cdn</span></span>
* <span data-ttu-id="aef7a-481">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="aef7a-481">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aef7a-482">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aef7a-482">Az.Compute</span></span>
* <span data-ttu-id="aef7a-483">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="aef7a-483">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="aef7a-484">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aef7a-484">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="aef7a-485">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="aef7a-485">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="aef7a-486">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aef7a-486">Az.ContainerRegistry</span></span>
* <span data-ttu-id="aef7a-487">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="aef7a-487">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aef7a-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aef7a-488">Az.DataFactory</span></span>
* <span data-ttu-id="aef7a-489">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="aef7a-489">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aef7a-490">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aef7a-490">Az.DataLakeStore</span></span>
* <span data-ttu-id="aef7a-491">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="aef7a-491">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="aef7a-492">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="aef7a-492">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="aef7a-493">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="aef7a-493">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="aef7a-494">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="aef7a-494">Az.IotHub</span></span>
* <span data-ttu-id="aef7a-495">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="aef7a-495">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="aef7a-496">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aef7a-496">Az.KeyVault</span></span>
* <span data-ttu-id="aef7a-497">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="aef7a-497">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aef7a-498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aef7a-498">Az.Network</span></span>
* <span data-ttu-id="aef7a-499">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="aef7a-499">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="aef7a-500">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aef7a-500">Az.Resources</span></span>
* <span data-ttu-id="aef7a-501">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="aef7a-501">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="aef7a-502">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="aef7a-502">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="aef7a-503">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aef7a-503">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="aef7a-504">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="aef7a-504">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="aef7a-505">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="aef7a-505">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="aef7a-506">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="aef7a-506">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="aef7a-507">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="aef7a-507">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="aef7a-508">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aef7a-508">Az.ServiceFabric</span></span>
* <span data-ttu-id="aef7a-509">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="aef7a-509">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="aef7a-510">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="aef7a-510">Fix some error messages.</span></span>
* <span data-ttu-id="aef7a-511">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="aef7a-511">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="aef7a-512">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="aef7a-512">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="aef7a-513">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="aef7a-513">Az.SignalR</span></span>
* <span data-ttu-id="aef7a-514">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="aef7a-514">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="aef7a-515">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aef7a-515">Az.Sql</span></span>
* <span data-ttu-id="aef7a-516">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="aef7a-516">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aef7a-517">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="aef7a-517">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="aef7a-518">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="aef7a-518">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="aef7a-519">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="aef7a-519">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aef7a-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aef7a-520">Az.Storage</span></span>
* <span data-ttu-id="aef7a-521">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="aef7a-521">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aef7a-522">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="aef7a-522">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="aef7a-523">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="aef7a-523">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="aef7a-524">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="aef7a-524">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="aef7a-525">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="aef7a-525">Az.TrafficManager</span></span>
* <span data-ttu-id="aef7a-526">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="aef7a-526">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aef7a-527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aef7a-527">Az.Websites</span></span>
* <span data-ttu-id="aef7a-528">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="aef7a-528">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aef7a-529">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="aef7a-529">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="aef7a-530">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="aef7a-530">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="aef7a-531">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="aef7a-531">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aef7a-532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aef7a-532">Az.Accounts</span></span>
* <span data-ttu-id="aef7a-533">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="aef7a-533">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aef7a-534">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aef7a-534">Az.Compute</span></span>
* <span data-ttu-id="aef7a-535">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="aef7a-535">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="aef7a-536">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="aef7a-536">Updated the description of ID in help files</span></span>
* <span data-ttu-id="aef7a-537">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aef7a-537">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aef7a-538">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aef7a-538">Az.DataLakeStore</span></span>
* <span data-ttu-id="aef7a-539">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="aef7a-539">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="aef7a-540">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="aef7a-540">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="aef7a-541">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="aef7a-541">Az.EventGrid</span></span>
* <span data-ttu-id="aef7a-542">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="aef7a-542">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="aef7a-543">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="aef7a-543">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="aef7a-544">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="aef7a-544">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="aef7a-545">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="aef7a-545">Event Time-To-Live,</span></span>
        - <span data-ttu-id="aef7a-546">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="aef7a-546">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="aef7a-547">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="aef7a-547">Dead letter endpoint.</span></span>
    - <span data-ttu-id="aef7a-548">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="aef7a-548">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="aef7a-549">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="aef7a-549">Event Time-To-Live,</span></span>
        - <span data-ttu-id="aef7a-550">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="aef7a-550">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="aef7a-551">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="aef7a-551">Dead letter endpoint.</span></span>
* <span data-ttu-id="aef7a-552">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="aef7a-552">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="aef7a-553">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="aef7a-553">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="aef7a-554">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="aef7a-554">Az.IotHub</span></span>
* <span data-ttu-id="aef7a-555">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="aef7a-555">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="aef7a-556">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="aef7a-556">Az.LogicApp</span></span>
* <span data-ttu-id="aef7a-557">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="aef7a-557">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="aef7a-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aef7a-558">Az.Resources</span></span>
* <span data-ttu-id="aef7a-559">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="aef7a-559">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="aef7a-560">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="aef7a-560">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="aef7a-561">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aef7a-561">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="aef7a-562">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="aef7a-562">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="aef7a-563">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="aef7a-563">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="aef7a-564">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="aef7a-564">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="aef7a-565">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="aef7a-565">Az.SignalR</span></span>
* <span data-ttu-id="aef7a-566">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aef7a-566">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="aef7a-567">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aef7a-567">Az.Sql</span></span>
* <span data-ttu-id="aef7a-568">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="aef7a-568">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aef7a-569">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aef7a-569">Az.Storage</span></span>
* <span data-ttu-id="aef7a-570">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="aef7a-570">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="aef7a-571">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="aef7a-571">New-AzStorageContext</span></span>
* <span data-ttu-id="aef7a-572">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="aef7a-572">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="aef7a-573">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="aef7a-573">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aef7a-574">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aef7a-574">Az.Websites</span></span>
* <span data-ttu-id="aef7a-575">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="aef7a-575">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="aef7a-576">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aef7a-576">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="aef7a-577">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="aef7a-577">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="aef7a-578">Ogólne</span><span class="sxs-lookup"><span data-stu-id="aef7a-578">General</span></span>

- <span data-ttu-id="aef7a-579">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="aef7a-579">General Availability of Az Module</span></span>
- <span data-ttu-id="aef7a-580">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="aef7a-580">Online help for each module</span></span>
- <span data-ttu-id="aef7a-581">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="aef7a-581">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="aef7a-582">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="aef7a-582">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="aef7a-583">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aef7a-583">Az.Accounts</span></span>
- <span data-ttu-id="aef7a-584">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="aef7a-584">Changed from Az.Profile</span></span>
- <span data-ttu-id="aef7a-585">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="aef7a-585">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="aef7a-586">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="aef7a-586">Az.ApiManagement</span></span>
- <span data-ttu-id="aef7a-587">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="aef7a-587">Fixes for #7002</span></span>
- <span data-ttu-id="aef7a-588">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="aef7a-588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="aef7a-589">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="aef7a-589">Az.Batch</span></span>
- <span data-ttu-id="aef7a-590">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="aef7a-590">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="aef7a-591">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="aef7a-591">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="aef7a-592">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="aef7a-592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="aef7a-593">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="aef7a-593">Az.Billing</span></span>
- <span data-ttu-id="aef7a-594">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="aef7a-594">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="aef7a-595">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-595">Az.CognitivServices</span></span>
- <span data-ttu-id="aef7a-596">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="aef7a-596">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="aef7a-597">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="aef7a-597">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="aef7a-598">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="aef7a-598">Az.ContainerInstance</span></span>
- <span data-ttu-id="aef7a-599">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="aef7a-599">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="aef7a-600">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="aef7a-600">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="aef7a-601">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="aef7a-601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="aef7a-602">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aef7a-602">Az.DataLakeStore</span></span>
- <span data-ttu-id="aef7a-603">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="aef7a-603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="aef7a-604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="aef7a-604">Az.Monitor</span></span>
- <span data-ttu-id="aef7a-605">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="aef7a-605">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="aef7a-606">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aef7a-606">Az.KeyVault</span></span>
- <span data-ttu-id="aef7a-607">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="aef7a-607">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="aef7a-608">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="aef7a-608">Az.MachineLearning</span></span>
- <span data-ttu-id="aef7a-609">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="aef7a-609">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="aef7a-610">Az.Media</span><span class="sxs-lookup"><span data-stu-id="aef7a-610">Az.Media</span></span>
- <span data-ttu-id="aef7a-611">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="aef7a-611">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="aef7a-612">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aef7a-612">Az.Network</span></span>
<span data-ttu-id="aef7a-613">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="aef7a-613">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="aef7a-614">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="aef7a-614">New cmdlets added:</span></span>
        - <span data-ttu-id="aef7a-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aef7a-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aef7a-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aef7a-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aef7a-617">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aef7a-617">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aef7a-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aef7a-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aef7a-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aef7a-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aef7a-620">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="aef7a-620">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="aef7a-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="aef7a-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="aef7a-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="aef7a-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="aef7a-623">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aef7a-623">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="aef7a-624">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aef7a-624">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="aef7a-625">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="aef7a-625">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="aef7a-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="aef7a-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="aef7a-627">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aef7a-627">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="aef7a-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="aef7a-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="aef7a-629">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="aef7a-629">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="aef7a-630">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aef7a-630">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="aef7a-631">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aef7a-631">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="aef7a-632">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aef7a-632">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="aef7a-633">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aef7a-633">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="aef7a-634">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="aef7a-634">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="aef7a-635">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="aef7a-635">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="aef7a-636">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aef7a-636">Az.OperationalInsights</span></span>
- <span data-ttu-id="aef7a-637">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="aef7a-637">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="aef7a-638">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="aef7a-638">Az.Profile</span></span>
- <span data-ttu-id="aef7a-639">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aef7a-639">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="aef7a-640">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-640">Az.RecoveryServices</span></span>
- <span data-ttu-id="aef7a-641">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="aef7a-641">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="aef7a-642">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aef7a-642">Az.Resources</span></span>
- <span data-ttu-id="aef7a-643">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="aef7a-643">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="aef7a-644">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aef7a-644">Az.ServiceFabric</span></span>
- <span data-ttu-id="aef7a-645">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="aef7a-645">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="aef7a-646">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="aef7a-646">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="aef7a-647">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="aef7a-647">Az.SIgnalR</span></span>
- <span data-ttu-id="aef7a-648">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="aef7a-648">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="aef7a-649">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aef7a-649">Az.Sql</span></span>
- <span data-ttu-id="aef7a-650">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="aef7a-650">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="aef7a-651">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="aef7a-651">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="aef7a-652">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="aef7a-652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="aef7a-653">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aef7a-653">Az.Storage</span></span>
- <span data-ttu-id="aef7a-654">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="aef7a-654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="aef7a-655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aef7a-655">Az.Websites</span></span>
- <span data-ttu-id="aef7a-656">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="aef7a-656">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="aef7a-657">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="aef7a-657">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="aef7a-658">Ogólne</span><span class="sxs-lookup"><span data-stu-id="aef7a-658">General</span></span>

* <span data-ttu-id="aef7a-659">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="aef7a-659">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="aef7a-660">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aef7a-660">Az.Compute</span></span>

* <span data-ttu-id="aef7a-661">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="aef7a-661">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="aef7a-662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aef7a-662">Az.DataLakeStore</span></span>

* <span data-ttu-id="aef7a-663">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="aef7a-663">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="aef7a-664">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="aef7a-664">Az.FrontDoor</span></span>

* <span data-ttu-id="aef7a-665">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="aef7a-665">Fixed some broken links</span></span>
    - <span data-ttu-id="aef7a-666">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="aef7a-666">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="aef7a-667">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="aef7a-667">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="aef7a-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-668">Az.RecoveryServices</span></span>

* <span data-ttu-id="aef7a-669">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="aef7a-669">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="aef7a-670">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="aef7a-670">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="aef7a-671">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aef7a-671">Az.Resources</span></span>

* <span data-ttu-id="aef7a-672">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="aef7a-672">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="aef7a-673">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="aef7a-673">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="aef7a-674">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aef7a-674">Az.Sql</span></span>

* <span data-ttu-id="aef7a-675">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="aef7a-675">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="aef7a-676">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="aef7a-676">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="aef7a-677">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="aef7a-677">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="aef7a-678">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aef7a-678">Az.Storage</span></span>

* <span data-ttu-id="aef7a-679">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aef7a-679">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="aef7a-680">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="aef7a-680">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="aef7a-681">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="aef7a-681">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="aef7a-682">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="aef7a-682">Support Static Website configuration</span></span>
    - <span data-ttu-id="aef7a-683">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="aef7a-683">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="aef7a-684">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="aef7a-684">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="aef7a-685">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aef7a-685">Az.Websites</span></span>

* <span data-ttu-id="aef7a-686">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="aef7a-686">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="aef7a-687">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="aef7a-687">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="aef7a-688">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="aef7a-688">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="aef7a-689">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="aef7a-689">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="aef7a-690">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="aef7a-690">Az.ApiManagement</span></span>
* <span data-ttu-id="aef7a-691">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="aef7a-691">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="aef7a-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aef7a-692">Az.Automation</span></span>
* <span data-ttu-id="aef7a-693">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="aef7a-693">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="aef7a-694">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="aef7a-694">Added Update Management cmdlets</span></span>
* <span data-ttu-id="aef7a-695">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="aef7a-695">Added Source Control cmdlets</span></span>
* <span data-ttu-id="aef7a-696">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="aef7a-696">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="aef7a-697">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="aef7a-697">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="aef7a-698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aef7a-698">Az.Compute</span></span>
* <span data-ttu-id="aef7a-699">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="aef7a-699">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="aef7a-700">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="aef7a-700">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="aef7a-701">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="aef7a-701">Az.ContainerInstance</span></span>
* <span data-ttu-id="aef7a-702">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="aef7a-702">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="aef7a-703">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="aef7a-703">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="aef7a-704">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="aef7a-704">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="aef7a-705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aef7a-705">Az.Network</span></span>
* <span data-ttu-id="aef7a-706">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="aef7a-706">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="aef7a-707">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="aef7a-707">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="aef7a-708">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="aef7a-708">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="aef7a-709">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="aef7a-709">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="aef7a-710">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="aef7a-710">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="aef7a-711">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="aef7a-711">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="aef7a-712">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="aef7a-712">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="aef7a-713">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="aef7a-713">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="aef7a-714">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="aef7a-714">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="aef7a-715">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="aef7a-715">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="aef7a-716">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="aef7a-716">Az.Relay</span></span>
* <span data-ttu-id="aef7a-717">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="aef7a-717">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="aef7a-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aef7a-718">Az.Resources</span></span>
* <span data-ttu-id="aef7a-719">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="aef7a-719">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="aef7a-720">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="aef7a-720">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="aef7a-721">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="aef7a-721">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="aef7a-722">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aef7a-722">Az.ServiceFabric</span></span>
* <span data-ttu-id="aef7a-723">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="aef7a-723">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="aef7a-724">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aef7a-724">Az.Sql</span></span>
* <span data-ttu-id="aef7a-725">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="aef7a-725">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="aef7a-726">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aef7a-726">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aef7a-727">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aef7a-727">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aef7a-728">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aef7a-728">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aef7a-729">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aef7a-729">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aef7a-730">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aef7a-730">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="aef7a-731">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aef7a-731">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="aef7a-732">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aef7a-732">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="aef7a-733">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aef7a-733">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="aef7a-734">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="aef7a-734">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="aef7a-735">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="aef7a-735">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="aef7a-736">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="aef7a-736">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="aef7a-737">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="aef7a-737">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="aef7a-738">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="aef7a-738">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="aef7a-739">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="aef7a-739">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="aef7a-740">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="aef7a-740">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="aef7a-741">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="aef7a-741">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="aef7a-742">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="aef7a-742">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="aef7a-743">Ogólne</span><span class="sxs-lookup"><span data-stu-id="aef7a-743">General</span></span>
* <span data-ttu-id="aef7a-744">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="aef7a-744">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="aef7a-745">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="aef7a-745">Az.Profile</span></span>
* <span data-ttu-id="aef7a-746">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="aef7a-746">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="aef7a-747">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="aef7a-747">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="aef7a-748">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="aef7a-748">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="aef7a-749">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="aef7a-749">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="aef7a-750">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="aef7a-750">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="aef7a-751">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="aef7a-751">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="aef7a-752">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="aef7a-752">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="aef7a-753">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-753">Az.CognitiveServices</span></span>
* <span data-ttu-id="aef7a-754">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="aef7a-754">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aef7a-755">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aef7a-755">Az.Compute</span></span>
* <span data-ttu-id="aef7a-756">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="aef7a-756">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="aef7a-757">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="aef7a-757">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="aef7a-758">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="aef7a-758">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aef7a-759">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aef7a-759">Az.DataLakeStore</span></span>
* <span data-ttu-id="aef7a-760">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="aef7a-760">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="aef7a-761">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="aef7a-761">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="aef7a-762">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="aef7a-762">Az.Insights</span></span>
* <span data-ttu-id="aef7a-763">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="aef7a-763">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="aef7a-764">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="aef7a-764">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="aef7a-765">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="aef7a-765">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="aef7a-766">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="aef7a-766">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aef7a-767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aef7a-767">Az.Network</span></span>
* <span data-ttu-id="aef7a-768">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="aef7a-768">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="aef7a-769">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="aef7a-769">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="aef7a-770">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="aef7a-770">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="aef7a-771">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="aef7a-771">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="aef7a-772">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="aef7a-772">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="aef7a-773">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="aef7a-773">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="aef7a-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="aef7a-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="aef7a-775">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="aef7a-775">Az.PolicyInsights</span></span>
* <span data-ttu-id="aef7a-776">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="aef7a-776">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="aef7a-777">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aef7a-777">Az.Resources</span></span>
* <span data-ttu-id="aef7a-778">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="aef7a-778">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="aef7a-779">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="aef7a-779">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="aef7a-780">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aef7a-780">Az.ServiceBus</span></span>
* <span data-ttu-id="aef7a-781">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="aef7a-781">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="aef7a-782">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aef7a-782">Az.ServiceFabric</span></span>
* <span data-ttu-id="aef7a-783">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="aef7a-783">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="aef7a-784">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="aef7a-784">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="aef7a-785">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="aef7a-785">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="aef7a-786">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="aef7a-786">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="aef7a-787">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="aef7a-787">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="aef7a-788">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="aef7a-788">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="aef7a-789">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="aef7a-789">Az.Profile</span></span>
* <span data-ttu-id="aef7a-790">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="aef7a-790">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="aef7a-791">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="aef7a-791">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aef7a-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aef7a-792">Az.Compute</span></span>
* <span data-ttu-id="aef7a-793">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="aef7a-793">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="aef7a-794">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aef7a-794">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aef7a-795">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aef7a-795">Az.DataLakeStore</span></span>
* <span data-ttu-id="aef7a-796">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="aef7a-796">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="aef7a-797">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aef7a-797">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="aef7a-798">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aef7a-798">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="aef7a-799">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aef7a-799">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="aef7a-800">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aef7a-800">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aef7a-801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aef7a-801">Az.Network</span></span>
* <span data-ttu-id="aef7a-802">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="aef7a-802">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="aef7a-803">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aef7a-803">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="aef7a-804">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aef7a-804">Az.Resources</span></span>
* <span data-ttu-id="aef7a-805">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="aef7a-805">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="aef7a-806">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="aef7a-806">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="aef7a-807">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="aef7a-807">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="aef7a-808">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="aef7a-808">Azure.Storage</span></span>
* <span data-ttu-id="aef7a-809">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="aef7a-809">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="aef7a-810">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="aef7a-810">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="aef7a-811">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="aef7a-811">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="aef7a-812">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="aef7a-812">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="aef7a-813">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="aef7a-813">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="aef7a-814">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aef7a-814">Az.CognitiveServices</span></span>
* <span data-ttu-id="aef7a-815">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="aef7a-815">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aef7a-816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aef7a-816">Az.Compute</span></span>
* <span data-ttu-id="aef7a-817">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="aef7a-817">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="aef7a-818">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="aef7a-818">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="aef7a-819">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="aef7a-819">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="aef7a-820">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="aef7a-820">Az.DataFactoryV2</span></span>
* <span data-ttu-id="aef7a-821">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="aef7a-821">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aef7a-822">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aef7a-822">Az.Network</span></span>
* <span data-ttu-id="aef7a-823">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="aef7a-823">Added NetworkProfile functionality.</span></span> <span data-ttu-id="aef7a-824">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="aef7a-824">new cmdlets added</span></span>
    - <span data-ttu-id="aef7a-825">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aef7a-825">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="aef7a-826">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aef7a-826">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="aef7a-827">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aef7a-827">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="aef7a-828">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aef7a-828">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="aef7a-829">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="aef7a-829">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="aef7a-830">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="aef7a-830">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="aef7a-831">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="aef7a-831">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="aef7a-832">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="aef7a-832">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="aef7a-833">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="aef7a-833">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="aef7a-834">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="aef7a-834">Az.RedisCache</span></span>
* <span data-ttu-id="aef7a-835">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="aef7a-835">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="aef7a-836">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="aef7a-836">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="aef7a-837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aef7a-837">Az.Resources</span></span>
* <span data-ttu-id="aef7a-838">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aef7a-838">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="aef7a-839">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="aef7a-839">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="aef7a-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aef7a-840">Az.Sql</span></span>
* <span data-ttu-id="aef7a-841">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="aef7a-841">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aef7a-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aef7a-842">Az.Websites</span></span>
* <span data-ttu-id="aef7a-843">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="aef7a-843">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="aef7a-844">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="aef7a-844">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="aef7a-845">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="aef7a-845">0.2.0 - September 2018</span></span>
 <span data-ttu-id="aef7a-846">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="aef7a-846">Initial Release</span></span>