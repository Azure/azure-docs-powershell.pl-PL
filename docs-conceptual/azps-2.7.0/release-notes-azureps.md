---
ms.openlocfilehash: 96e6d7bc0cc29adc1c0e49ba344d27349454c214
ms.sourcegitcommit: 92722d603b60dc769660e7517da60110133d9959
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/24/2019
ms.locfileid: "71226443"
---
## <a name="270---september-2019"></a><span data-ttu-id="b3a6e-101">2.7.0 — wrzesień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-101">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="b3a6e-102">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3a6e-102">Az.ApiManagement</span></span>
* <span data-ttu-id="b3a6e-103">Aktualizacja opisu parametru „-Format” w dokumentacji referencyjnej polecenia „Set-AzApiManagementPolicy”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-103">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="b3a6e-104">Usunięto z dokumentacji referencyjnej odwołania do przestarzałego polecenia cmdlet „Update-AzApiManagementDeployment”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-104">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="b3a6e-105">Zamiast niego należy używać polecenia „Set-AzApiManagement”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-105">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b3a6e-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-106">Az.Automation</span></span>
* <span data-ttu-id="b3a6e-107">Poprawiono literówkę w przykładzie w dokumentacji referencyjnej polecenia „Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-107">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="b3a6e-108">Dodano wyjaśnienie dotyczące ograniczeń systemu operacyjnego dla polecenia Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="b3a6e-108">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="b3a6e-109">Naprawiono wyjątek odwołania o wartości null dla opcji -Wait polecenia cmdlet Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-109">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-110">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-111">Dodanie parametru UploadSizeInBytes do polecenia New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-111">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="b3a6e-112">Dodanie parametru Incremental do polecenia New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-112">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b3a6e-113">Dodanie funkcji maszyny wirtualnej o niskim priorytecie:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-113">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="b3a6e-114">do polecenia New-AzVMConfig dodano parametry MaxPrice, EvictionPolicy i Priority.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-114">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="b3a6e-115">Parametr MaxPrice został dodany do poleceń cmdlet New-AzVmssConfig, Update-AzVM i Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-115">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="b3a6e-116">Rozwiązanie problemu z odwołaniem do maszyny wirtualnej dla polecenia cmdlet Get-AzAvailabilitySet, gdy wyświetla listę wszystkich zestawów dostępności w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-116">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="b3a6e-117">Naprawienie wyjątku o wartości null dla polecenia Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-117">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="b3a6e-118">Naprawienie metody przeszukiwania wirtualnego dysku twardego dla pozycji względem końca.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-118">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="b3a6e-119">Rozwiązanie problemu z dyskami UltraSSD dla poleceń New-AzVM i Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-119">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b3a6e-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b3a6e-120">Az.DataFactory</span></span>
* <span data-ttu-id="b3a6e-121">Dodanie 3 nowych poleceń do usługi ADF w wersji 2 — Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription i Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="b3a6e-121">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="b3a6e-122">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.3</span><span class="sxs-lookup"><span data-stu-id="b3a6e-122">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b3a6e-123">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b3a6e-123">Az.HDInsight</span></span>
* <span data-ttu-id="b3a6e-124">Wywołanie zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="b3a6e-124">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b3a6e-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b3a6e-125">Az.IotHub</span></span>
* <span data-ttu-id="b3a6e-126">Dodanie obsługi w celu wywołania trybu failover dla usługi IotHub do sparowanego geograficznie regionu odzyskiwania po awarii.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-126">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="b3a6e-127">Dodanie obsługi do zarządzania wzbogacaniem komunikatów dla usługi IotHub.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-127">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="b3a6e-128">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-128">New cmdlets are:</span></span>
    - <span data-ttu-id="b3a6e-129">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b3a6e-129">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="b3a6e-130">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b3a6e-130">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="b3a6e-131">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b3a6e-131">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="b3a6e-132">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b3a6e-132">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b3a6e-133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b3a6e-133">Az.Monitor</span></span>
* <span data-ttu-id="b3a6e-134">Wskazanie najnowszego zestawu Monitor SDK, tj. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="b3a6e-134">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="b3a6e-135">Dodaje zmiany niepowodujące niezgodności do poleceń cmdlet metryk, tj. wyliczenie Unit obsługuje kilka nowych wartości.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-135">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="b3a6e-136">Są to polecenia cmdlet tylko do odczytu, więc nie będzie żadnych zmian w danych wejściowych tych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-136">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="b3a6e-137">Wartość api-version żądań **ActionGroups** to teraz **2019-06-01**, wcześniej było to **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-137">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="b3a6e-138">Testy scenariusza zostały zaktualizowane w celu dostosowania do tej zmiany.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-138">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="b3a6e-139">Konstruktory dla klas **EmailReceiver** i **WebhookReceiver** dodały jeden nowy argument obowiązkowy, tj. wartość logiczną o nazwie **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-139">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="b3a6e-140">Obecnie wartość ta jest stała i równa **false**, aby ukryć tę zmianę powodującą niezgodność przed poleceniami cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-140">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="b3a6e-141">**UWAGA**: Jest to tymczasowa zmiana, która musi być zweryfikowana przez zespół ds. alertów.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-141">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="b3a6e-142">Kolejność argumentów konstruktora klasy **Source** (powiązanej z klasą **ScheduledQueryRuleSource**) zmieniła się od poprzedniego zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-142">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="b3a6e-143">Ta zmiana wymaga naprawienia dwóch testów jednostkowych: kompilowały się, ale nie przechodziły testów.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-143">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="b3a6e-144">Kolejność argumentów konstruktora klasy **AlertingAction** (powiązanej z klasą **ScheduledQueryRuleSource**) została zmieniona od poprzedniego zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-144">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="b3a6e-145">Ta zmiana wymaga naprawienia dwóch testów jednostkowych: kompilowały się, ale nie przechodziły testów.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="b3a6e-146">Obsługa kryteriów progu dynamicznego dla alertu metryki w wersji 2</span><span class="sxs-lookup"><span data-stu-id="b3a6e-146">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="b3a6e-147">New-AzMetricAlertRuleV2Criteria: teraz tworzy kryteria progów dynamicznych</span><span class="sxs-lookup"><span data-stu-id="b3a6e-147">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="b3a6e-148">Add-AzMetricAlertRuleV2: teraz akceptuje kryteria progów dynamicznych</span><span class="sxs-lookup"><span data-stu-id="b3a6e-148">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="b3a6e-149">Ulepszenia poleceń cmdlet reguły zaplanowanego zapytania (SQR)</span><span class="sxs-lookup"><span data-stu-id="b3a6e-149">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="b3a6e-150">Polecenia cmdlet będą akceptować parametr „Location” w obu formatach: jako lokalizację (np. eastus) i jako nazwę wyświetlaną lokalizacji (np. East US)</span><span class="sxs-lookup"><span data-stu-id="b3a6e-150">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="b3a6e-151">Poprawnie zilustrowano parametr „Enabled” w plikach pomocy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-151">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="b3a6e-152">Dodano przykłady dla opcjonalnego parametru „ActionGroup”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-152">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="b3a6e-153">Ogólnie ulepszono pliki pomocy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-153">Overall improved help files</span></span>
* <span data-ttu-id="b3a6e-154">Naprawienie usterki dotyczącej określania typu zakresu dla polecenia „Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-154">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-155">Az.Network</span></span>
* <span data-ttu-id="b3a6e-156">Naprawienie nieprawidłowego przykładu w dokumentacji referencyjnej polecenia „New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-156">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="b3a6e-157">Dodanie w dokumentacji referencyjnej polecenia „Get-AzNetworkWatcherPacketCapture” uwagi dotyczącej pobierania wszystkich właściwości na potrzeby przechwytywania pakietów</span><span class="sxs-lookup"><span data-stu-id="b3a6e-157">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="b3a6e-158">Naprawiono przykład w dokumentacji referencyjnej polecenia „Test-AzNetworkWatcherIPFlow”, aby poprawnie wyliczał karty sieciowe</span><span class="sxs-lookup"><span data-stu-id="b3a6e-158">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="b3a6e-159">Ulepszono analizę wyjątku w chmurze, aby wyświetlane były dodatkowe szczegóły, jeśli są obecne</span><span class="sxs-lookup"><span data-stu-id="b3a6e-159">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="b3a6e-160">Ulepszono analizę wyjątku w chmurze, aby był obsługiwany dodatkowy typ wyjątku zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="b3a6e-160">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="b3a6e-161">Naprawiono niepoprawne mapowanie modeli reguł zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="b3a6e-161">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="b3a6e-162">Dodano właściwości interfejsu sieciowego dla funkcji prywatnego adresu IP</span><span class="sxs-lookup"><span data-stu-id="b3a6e-162">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="b3a6e-163">Dodano właściwość „PrivateEndpoint” jako typ PSResourceId do elementu PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b3a6e-163">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="b3a6e-164">Dodano właściwość „PrivateLinkConnectionProperties” jako typ PSIpConfigurationConnectivityInformation do elementu PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6e-164">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="b3a6e-165">Dodano nową klasę modelu PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-165">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="b3a6e-166">Dodano nowy typ ApplicationRuleProtocolType „mssql” dla zasobu usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="b3a6e-166">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="b3a6e-167">Obsługa linku wielokrotnego w wirtualnej sieci WAN</span><span class="sxs-lookup"><span data-stu-id="b3a6e-167">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="b3a6e-168">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-168">New cmdlets</span></span>
        - <span data-ttu-id="b3a6e-169">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="b3a6e-169">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="b3a6e-170">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="b3a6e-170">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="b3a6e-171">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-171">Updated cmdlet:</span></span>
        - <span data-ttu-id="b3a6e-172">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="b3a6e-172">New-VpnSite</span></span>
        - <span data-ttu-id="b3a6e-173">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="b3a6e-173">Update-VpnSite</span></span>
        - <span data-ttu-id="b3a6e-174">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b3a6e-174">New-VpnConnection</span></span>
        - <span data-ttu-id="b3a6e-175">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b3a6e-175">Update-VpnConnection</span></span>
* <span data-ttu-id="b3a6e-176">Niektóre dokumenty dla przykładów programu PowerShell naprawiono w taki sposób, aby były w nich używane polecenia cmdlet Az zamiast poleceń cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="b3a6e-176">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b3a6e-177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-177">Az.RecoveryServices</span></span>
* <span data-ttu-id="b3a6e-178">Aktualizacja obiektu AzureVMpolicy o atrybut ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="b3a6e-178">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="b3a6e-179">Dodano testy dotyczące zasad maszyny wirtualnej i przywracania oryginalnego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-179">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-180">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-180">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-181">Naprawienie usterki polegającej na tym, że nie można było wywołać polecenia New-AzRoleAssignment bez parametru Scope.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-181">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b3a6e-182">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b3a6e-182">Az.ServiceFabric</span></span>
* <span data-ttu-id="b3a6e-183">Poprawiono literówkę w przykładzie w dokumentacji referencyjnej polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-183">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="b3a6e-184">Dodanie nowych poleceń cmdlet do zarządzania aplikacją i usługami:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-184">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="b3a6e-185">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b3a6e-185">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b3a6e-186">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b3a6e-186">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="b3a6e-187">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b3a6e-187">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="b3a6e-188">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="b3a6e-188">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="b3a6e-189">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b3a6e-189">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b3a6e-190">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b3a6e-190">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b3a6e-191">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b3a6e-191">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="b3a6e-192">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b3a6e-192">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="b3a6e-193">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="b3a6e-193">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="b3a6e-194">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b3a6e-194">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b3a6e-195">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b3a6e-195">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="b3a6e-196">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b3a6e-196">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="b3a6e-197">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="b3a6e-197">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="b3a6e-198">Uaktualniono zestaw Service Fabric SDK do wersji 1.2.0, która korzysta z dostawcy zasobów usługi Service Fabric o wersji interfejsu API 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-198">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b3a6e-199">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b3a6e-199">Az.SignalR</span></span>
* <span data-ttu-id="b3a6e-200">Dodanie poleceń cmdlet Update, Restart, CheckNameAvailability i GetUsage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-200">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-201">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-202">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-202">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="b3a6e-203">Dodano przykład dla rdzenia wirtualnego do tworzenia elastycznej puli (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="b3a6e-203">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="b3a6e-204">Usunięcie weryfikacji parametru EmailAddresses i sprawdzania, czy parametr EmailAdmins nie ma wartości false w przypadku, gdy parametr EmailAddresses jest pusty w poleceniach Set-AzSqlServerAdvancedThreatProtectionPolicy i Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-204">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="b3a6e-205">Włączono usuwanie ustawień inspekcji serwera/bazy danych, gdy istnieje wiele ustawień diagnostycznych włączających kategorię inspekcji.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-205">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="b3a6e-206">Naprawa weryfikacji adresów e-mail w wielu poleceniach cmdlet do oceny luk w zabezpieczeniach SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting i Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="b3a6e-206">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b3a6e-207">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-207">Az.Storage</span></span>
* <span data-ttu-id="b3a6e-208">Zaktualizowano przykład w dokumentacji referencyjnej dla polecenia „Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-208">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="b3a6e-209">Obsługa zachowywania w pliku docelowym właściwości SMB pliku źródłowego przy przekazywaniu/pobieraniu pliku platformy Azure (atrybuty pliku, czas utworzenia pliku, czas ostatniego zapisu pliku)</span><span class="sxs-lookup"><span data-stu-id="b3a6e-209">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="b3a6e-210">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b3a6e-210">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="b3a6e-211">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b3a6e-211">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="b3a6e-212">Naprawa awarii przekazywania blokowego obiektu blob z właściwościami/metadanymi dla elementu ImmutabilityPolicy z obsługą kontenerów.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-212">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="b3a6e-213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b3a6e-213">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="b3a6e-214">Obsługa zarządzania udziałami plików platformy Azure za pomocą interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="b3a6e-214">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="b3a6e-215">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b3a6e-215">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="b3a6e-216">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b3a6e-216">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="b3a6e-217">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b3a6e-217">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="b3a6e-218">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b3a6e-218">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b3a6e-219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b3a6e-219">Az.Websites</span></span>
* <span data-ttu-id="b3a6e-220">Naprawa problemu polegającego na tym, że tagi webapp były usuwane podczas migracji aplikacji do nowej platformy ASP</span><span class="sxs-lookup"><span data-stu-id="b3a6e-220">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="b3a6e-221">Naprawa polecenia Publish-AzureWebapp w taki sposób, aby działało w systemach Linux i Windows</span><span class="sxs-lookup"><span data-stu-id="b3a6e-221">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="b3a6e-222">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzWebAppPublishingProfile”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-222">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="b3a6e-223">2.6.0 — sierpień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-223">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="b3a6e-224">Ogólne</span><span class="sxs-lookup"><span data-stu-id="b3a6e-224">General</span></span>
* <span data-ttu-id="b3a6e-225">Naprawiono różne literówki w wielu modułach</span><span class="sxs-lookup"><span data-stu-id="b3a6e-225">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b3a6e-226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-226">Az.Accounts</span></span>
* <span data-ttu-id="b3a6e-227">Obsługa pliku MSI przypisanego przez użytkownika w ramach uwierzytelniania usługi Azure Functions (nr 9479)</span><span class="sxs-lookup"><span data-stu-id="b3a6e-227">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="b3a6e-228">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b3a6e-228">Az.Aks</span></span>
* <span data-ttu-id="b3a6e-229">Rozwiązano problem z danymi wyjściowymi polecenia „Get-AzAks”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-229">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="b3a6e-230">Więcej informacji: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="b3a6e-230">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b3a6e-231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3a6e-231">Az.ApiManagement</span></span>
* <span data-ttu-id="b3a6e-232">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="b3a6e-232">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="b3a6e-233">Zaktualizowano wersję nuget .net, która nie wymusza ograniczeń dotyczących identyfikatorów productId, apiId, groupId i userId</span><span class="sxs-lookup"><span data-stu-id="b3a6e-233">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="b3a6e-234">**Get-AzApiManagementProduct** — dodano obsługę wysyłania zapytań dotyczących produktów przy użyciu interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-234">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="b3a6e-235">**New-AzApiManagementApiRevision** — poprawka rozwiązująca problem polegający na tym, że wartość ApiRevisionDescription nie była ustawiana podczas tworzenia nowej wersji pomocniczej interfejsu API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="b3a6e-235">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="b3a6e-236">Poprawiono literówkę w modelu „PsApiManagementOAuth2AuthrozationServer” na „PsApiManagementOAuth2AuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-236">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b3a6e-237">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b3a6e-237">Az.Batch</span></span>
* <span data-ttu-id="b3a6e-238">Poprawiono literówkę w komunikacie pomocy i dokumentacji, zmieniając literę w nazwie systemu Windows na wielką</span><span class="sxs-lookup"><span data-stu-id="b3a6e-238">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b3a6e-239">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b3a6e-239">Az.Cdn</span></span>
* <span data-ttu-id="b3a6e-240">Poprawiono literówkę w pomocniku konwersji modułu CDN</span><span class="sxs-lookup"><span data-stu-id="b3a6e-240">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-241">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-241">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-242">Dodanie polecenia VmssId to New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-242">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="b3a6e-243">Dodanie parametrów TerminateScheduledEvents i TerminateScheduledEventNotBeforeTimeoutInMinutes do polecenia New-AzVmssConfig and Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b3a6e-243">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="b3a6e-244">Dodanie właściwości HyperVGeneration do obiektu obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b3a6e-244">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="b3a6e-245">Dodanie funkcji Host i HostGroup</span><span class="sxs-lookup"><span data-stu-id="b3a6e-245">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="b3a6e-246">Nowe polecenia cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="b3a6e-246">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="b3a6e-247">Dodano parametr HostId do poleceń New-AzVMConfig i New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3a6e-247">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="b3a6e-248">Aktualizacja przykładu w dokumentacji polecenia „Invoke-AzVMRunCommand” w celu użycia poprawnej nazwy parametru</span><span class="sxs-lookup"><span data-stu-id="b3a6e-248">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="b3a6e-249">Aktualizacja opisu parametru „-VolumeType” w dokumentacji referencyjnej poleceń „Set-AzVMDiskEncryptionExtension” i „Set-AzVmssDiskEncryptionExtension”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-249">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b3a6e-250">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b3a6e-250">Az.DataFactory</span></span>
* <span data-ttu-id="b3a6e-251">Poprawiono literówkę w poleceniu „New-AzDataFactoryEncryptValue”, zmieniając literę w nazwie systemu Windows na wielką</span><span class="sxs-lookup"><span data-stu-id="b3a6e-251">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="b3a6e-252">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.2</span><span class="sxs-lookup"><span data-stu-id="b3a6e-252">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="b3a6e-253">Dodanie parametrów „DataProxyIntegrationRuntimeName”, „DataProxyStagingLinkedServiceName” i „DataProxyStagingPath” dla polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime”, aby umożliwić konfigurowanie własnego środowiska Integration Runtime jako serwera proxy dla środowiska SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="b3a6e-253">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="b3a6e-254">Zaktualizowano PSTriggerRun na potrzeby wyświetlania wyzwalanych potoków, komunikatów i właściwości, a także PSActivityRun na potrzeby wyświetlania typu działania</span><span class="sxs-lookup"><span data-stu-id="b3a6e-254">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b3a6e-255">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b3a6e-255">Az.DataLakeStore</span></span>
* <span data-ttu-id="b3a6e-256">Poprawiono wysunięcie polecenia Get-DataLakeStoreDeletedItem pod kątem obsługi błędów lub wyjątków zdalnych.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-256">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b3a6e-257">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b3a6e-257">Az.EventHub</span></span>
* <span data-ttu-id="b3a6e-258">Rozwiązano problem nr 9658: Literówka VirtualNteworkRule w poleceniu Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-258">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="b3a6e-259">Rozwiązano problem nr 9558: Polecenie Set-AzEventHubNamespace używa elementu PATCH zamiast PUT</span><span class="sxs-lookup"><span data-stu-id="b3a6e-259">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="b3a6e-260">dodano parametr EnableKafka do polecenia cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="b3a6e-260">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="b3a6e-261">Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania</span><span class="sxs-lookup"><span data-stu-id="b3a6e-261">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="b3a6e-262">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b3a6e-262">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b3a6e-263">Poprawiono literówkę w dokumentacji: „Azure” rozpoczynające się małą literą</span><span class="sxs-lookup"><span data-stu-id="b3a6e-263">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b3a6e-264">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b3a6e-264">Az.Monitor</span></span>
* <span data-ttu-id="b3a6e-265">Poprawiono niepoprawną nazwę parametru w dokumentacji pomocy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-265">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-266">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-266">Az.Network</span></span>
* <span data-ttu-id="b3a6e-267">Zaktualizowano polecenie New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-267">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="b3a6e-268">Sklasyfikowano parametr „PublicIpAddress” jako przestarzały, ponieważ nie jest on nigdy używany po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-268">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="b3a6e-269">Dodano jeden opcjonalny parametr „Primary” wskazujący, czy bieżąca konfiguracja IP jest podstawowa, czy nie.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-269">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="b3a6e-270">Ulepszono obsługę wyjątku błędu żądania z zestawu SDK — rozwiązuje to problem polegający na tym, że poprzednio wyjątki zestawu SDK nie były poprawnie obsługiwane, wskutek czego nie były wyświetlane kluczowe szczegóły błędu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-270">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="b3a6e-271">Skorygowano logikę weryfikacji prefiksu IP w wersji IPv6 w celu sprawdzania, czy długość prefiksu IPv6 jest poprawna.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-271">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="b3a6e-272">Zaktualizowano polecenie Get-AzVirtualNetworkSubnetConfig: Dodano parametr ustawiany w celu pobrania identyfikatora zasobu podsieci.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-272">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="b3a6e-273">Zaktualizowano opis parametru Location dla AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="b3a6e-273">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b3a6e-274">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b3a6e-274">Az.OperationalInsights</span></span>
* <span data-ttu-id="b3a6e-275">Zaktualizowano dokumentację polecenia „New-AzOperationalInsightsLinuxSyslogDataSource”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-275">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="b3a6e-276">Dodano przykład</span><span class="sxs-lookup"><span data-stu-id="b3a6e-276">Added example</span></span>
    - <span data-ttu-id="b3a6e-277">Zaktualizowano opis parametru „-Name”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-277">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="b3a6e-278">Dodano przykład dla polecenia New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="b3a6e-278">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="b3a6e-279">Zaktualizowano opis parametru „-Name” dla polecenia New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="b3a6e-279">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b3a6e-280">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-280">Az.RecoveryServices</span></span>
* <span data-ttu-id="b3a6e-281">Aktualizacja polecenia „Get-AzRecoveryServicesBackupJobDetail.md”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-281">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-282">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-282">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-283">Dodano obsługę nowej wersji interfejsu API (2019-05-10) dla Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="b3a6e-283">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="b3a6e-284">Dodano obsługę „copy.count = 0” dla zmiennych, zasobów i właściwości</span><span class="sxs-lookup"><span data-stu-id="b3a6e-284">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="b3a6e-285">Zasoby z ustawieniami „condition = false” lub „copy.count = 0” będą usuwane w trybie ukończenia</span><span class="sxs-lookup"><span data-stu-id="b3a6e-285">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="b3a6e-286">Dodanie do dokumentu pomocy przykładu przypisywania zasad na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b3a6e-286">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b3a6e-287">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b3a6e-287">Az.ServiceBus</span></span>
* <span data-ttu-id="b3a6e-288">Rozwiązano problem nr 9658: Literówka VirtualNetworkRule w poleceniu Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-288">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="b3a6e-289">Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania</span><span class="sxs-lookup"><span data-stu-id="b3a6e-289">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="b3a6e-290">Dodano nowe polecenie „Test-AzServiceBusNameAvailability” do sprawdzania dostępności nazwy dla kolejki i tematu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-290">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="b3a6e-291">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b3a6e-291">Az.ServiceFabric</span></span>
* <span data-ttu-id="b3a6e-292">Usunięcie usterek poleceń cmdlet dodawania typu węzła:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-292">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="b3a6e-293">Usterka NullReferenceException, gdy grupa zasobów ma inny zestaw VMSS niezwiązany z klastrem usługi Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-293">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="b3a6e-294">Rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="b3a6e-294">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="b3a6e-295">Usunięcie usterki powodującej niepowodzenie polecenia cmdlet, gdy sieć wirtualna znajdowała się w innej grupie zasobów niż klaster.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-295">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="b3a6e-296">rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="b3a6e-296">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="b3a6e-297">Sklasyfikowanie polecenia cmdlet Add-AzServiceFabricApplicationCertificate jako przestarzałego</span><span class="sxs-lookup"><span data-stu-id="b3a6e-297">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-298">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-299">Aktualizacja dokumentacji starych poleceń cmdlet inspekcji.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-299">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b3a6e-300">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-300">Az.Storage</span></span>
* <span data-ttu-id="b3a6e-301">Aktualizacja pomocy dotyczącej poleceń Get/Close-AzStorageFileHandle, przez dodanie kolejnych scenariuszy do przykładów dotyczących poleceń cmdlet i zaktualizowanie opisów parametrów</span><span class="sxs-lookup"><span data-stu-id="b3a6e-301">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="b3a6e-302">Obsługa StandardBlobTier w ramach przekazywania i kopiowania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="b3a6e-302">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="b3a6e-303">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b3a6e-303">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="b3a6e-304">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-304">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="b3a6e-305">Obsługa priorytetu ponownego wypełniania w ramach kopiowania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="b3a6e-305">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="b3a6e-306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-306">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b3a6e-307">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b3a6e-307">Az.Websites</span></span>
* <span data-ttu-id="b3a6e-308">Dodanie wyjaśnienia do parametru -AppSettings w poleceniach Set-AzWebApp i Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b3a6e-308">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="b3a6e-309">2.5.0 — lipiec 2019</span><span class="sxs-lookup"><span data-stu-id="b3a6e-309">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b3a6e-310">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-310">Az.Accounts</span></span>
* <span data-ttu-id="b3a6e-311">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="b3a6e-311">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="b3a6e-312">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="b3a6e-312">Az.ApplicationInsights</span></span>
* <span data-ttu-id="b3a6e-313">Poprawienie pisowni w przykładzie w dokumentacji polecenia „Remove-AzApplicationInsightsApiKey”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-313">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="b3a6e-314">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-314">Az.Automation</span></span>
* <span data-ttu-id="b3a6e-315">Poprawienie pisowni w ciągu zasobu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-315">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="b3a6e-316">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-316">Az.CognitiveServices</span></span>
* <span data-ttu-id="b3a6e-317">Dodano obsługę właściwości NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-317">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-318">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-318">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-319">Dodanie brakujących właściwości (ComputerName, OsName, OsVersion i HyperVGeneration) obiektu widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-319">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b3a6e-320">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b3a6e-320">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b3a6e-321">Poprawienie pisowni parametru Replication w opisie polecenia Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b3a6e-321">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="b3a6e-322">Więcej informacji można znaleźć tutaj: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="b3a6e-322">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b3a6e-323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b3a6e-323">Az.DataFactory</span></span>
* <span data-ttu-id="b3a6e-324">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.0</span><span class="sxs-lookup"><span data-stu-id="b3a6e-324">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="b3a6e-325">Poprawienie pisowni w dokumentacji dla polecenia „Get-AzDataFactoryV2PipelineRun”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-325">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b3a6e-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b3a6e-326">Az.EventHub</span></span>
* <span data-ttu-id="b3a6e-327">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="b3a6e-327">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="b3a6e-328">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-328">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b3a6e-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b3a6e-329">Az.KeyVault</span></span>
* <span data-ttu-id="b3a6e-330">Dodano obsługę określania rozmiaru klucza dla zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="b3a6e-330">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b3a6e-331">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b3a6e-331">Az.LogicApp</span></span>
* <span data-ttu-id="b3a6e-332">Poprawienie polecenia Get-AzIntegrationAccountMap tak, aby wyświetlało listę wszystkich typów map</span><span class="sxs-lookup"><span data-stu-id="b3a6e-332">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="b3a6e-333">Dodano nowy parametr MapType na potrzeby filtrowania</span><span class="sxs-lookup"><span data-stu-id="b3a6e-333">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="b3a6e-334">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-334">Az.ManagedServices</span></span>
* <span data-ttu-id="b3a6e-335">Dodano obsługę interfejsu API w wersji 2019-06-01 (ogólna dostępność)</span><span class="sxs-lookup"><span data-stu-id="b3a6e-335">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-336">Az.Network</span></span>
* <span data-ttu-id="b3a6e-337">Dodanie obsługi prywatnego punktu końcowego i prywatnej usługi łączenia</span><span class="sxs-lookup"><span data-stu-id="b3a6e-337">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="b3a6e-338">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-338">New cmdlets</span></span>
        - <span data-ttu-id="b3a6e-339">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3a6e-339">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b3a6e-340">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b3a6e-340">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b3a6e-341">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b3a6e-341">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b3a6e-342">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b3a6e-342">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b3a6e-343">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b3a6e-343">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b3a6e-344">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b3a6e-344">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b3a6e-345">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="b3a6e-345">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="b3a6e-346">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b3a6e-346">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="b3a6e-347">Zaktualizowano poniższe polecenia dla funkcji: Flaga PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies w podsieci w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b3a6e-347">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="b3a6e-348">Zaktualizowano polecenia New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-348">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="b3a6e-349">Dodano opcjonalny parametr -PrivateEndpointNetworkPoliciesFlag, który konfiguruje, czy stosować zasady sieciowe w prywatnym punkcie końcowym w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-349">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="b3a6e-350">Dodano opcjonalny parametr -PrivateLinkServiceNetworkPoliciesFlag, który konfiguruje, czy stosować zasady sieciowe w usłudze łącza prywatnego w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-350">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="b3a6e-351">Nazwa parametru „ServiceName” polecenia cmdlet AzPrivateLinkService została zmieniona na „Name” z aliasem „ServiceName” w celu zachowania zgodności z poprzednimi wersjami</span><span class="sxs-lookup"><span data-stu-id="b3a6e-351">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="b3a6e-352">Włączenie protokołu ICMP dla konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="b3a6e-352">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="b3a6e-353">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-353">Updated cmdlets</span></span>
        - <span data-ttu-id="b3a6e-354">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-354">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b3a6e-355">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-355">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b3a6e-356">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-356">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="b3a6e-357">Dodanie wartości ConnectionProtocolType (Ikev1/Ikev2) jako konfigurowalnego parametru dla polecenia New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b3a6e-357">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b3a6e-358">Dodanie parametru PrivateIpAddressVersion w elemencie LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6e-358">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="b3a6e-359">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-359">Updated cmdlet:</span></span>
        - <span data-ttu-id="b3a6e-360">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-360">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="b3a6e-361">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-361">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="b3a6e-362">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-362">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="b3a6e-363">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig usługi Application Gateway o obsługę portu niestandardowego w sondzie</span><span class="sxs-lookup"><span data-stu-id="b3a6e-363">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="b3a6e-364">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig: Dodano opcjonalny parametr Port, który służy do sondowania serwera zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-364">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="b3a6e-365">Ten parametr ma zastosowanie w przypadku jednostek SKU Standard_V2 i WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-365">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b3a6e-366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b3a6e-366">Az.OperationalInsights</span></span>
* <span data-ttu-id="b3a6e-367">Zaktualizowano domyślną wersję zapisywanych wyszukiwań na 1.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-367">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="b3a6e-368">Poprawiono obsługę wyrażeń regularnych o wartości null dla dzienników niestandardowych</span><span class="sxs-lookup"><span data-stu-id="b3a6e-368">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b3a6e-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="b3a6e-370">Aktualizacja pliku „Get-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-370">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="b3a6e-371">Aktualizacja pliku „Get-AzRecoveryServicesBackupContainer.md”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-371">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="b3a6e-372">Aktualizacja pliku „Get-AzRecoveryServicesVault.md”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-372">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="b3a6e-373">Aktualizacja pliku „Wait-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-373">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="b3a6e-374">Aktualizacja pliku „Set-AzRecoveryServicesVaultContext.md”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-374">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="b3a6e-375">Aktualizacja pliku „Get-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-375">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="b3a6e-376">Aktualizacja pliku „Get-AzRecoveryServicesBackupRecoveryPoint.md”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-376">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="b3a6e-377">Aktualizacja pliku „Restore-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-377">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="b3a6e-378">Zaktualizowano wywołanie usługi do wyrejestrowywania kontenera dla udziału plików platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b3a6e-378">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="b3a6e-379">Aktualizacja pliku „Set-AzRecoveryServicesAsrAlertSetting.md”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-379">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-380">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-380">Az.Resources</span></span>
- <span data-ttu-id="b3a6e-381">Usunięcie brakującego polecenia cmdlet przywoływanego w dokumentacji polecenia „New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-381">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="b3a6e-382">Zaktualizowano polecenia cmdlet zasad w celu używania nowego interfejsu API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="b3a6e-382">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b3a6e-383">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b3a6e-383">Az.ServiceBus</span></span>
* <span data-ttu-id="b3a6e-384">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="b3a6e-384">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="b3a6e-385">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-385">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-386">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-387">Poprawienie brakujących przykładów dla polecenia cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b3a6e-387">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="b3a6e-388">Poprawienie ustawiania cyklicznego skanowania przez rozszerzenie Ocena luk w zabezpieczeniach bez podawania żadnego adresu e-mail</span><span class="sxs-lookup"><span data-stu-id="b3a6e-388">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="b3a6e-389">Poprawienie pisowni w komunikacie ostrzegawczym.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-389">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b3a6e-390">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-390">Az.Storage</span></span>
* <span data-ttu-id="b3a6e-391">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzStorageAccount” w celu użycia poprawnej nazwy parametru</span><span class="sxs-lookup"><span data-stu-id="b3a6e-391">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b3a6e-392">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b3a6e-392">Az.StorageSync</span></span>
* <span data-ttu-id="b3a6e-393">Dodanie polecenia cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-393">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="b3a6e-394">Rozwiązanie problemu 9551 dotyczącego respektowania wartości TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="b3a6e-394">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b3a6e-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b3a6e-395">Az.Websites</span></span>
* <span data-ttu-id="b3a6e-396">Usunięcie usterki polegającej na tym, że niektóre właściwości SiteConfig nie były zwracane przez polecenia Get-AzWebApp i Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b3a6e-396">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="b3a6e-397">Dodanie nowego parametru Location dla poleceń Get-AzDeletedWebApp i Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b3a6e-397">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="b3a6e-398">Usunięcie usterki związanej z klonowaniem miejsc aplikacji internetowych przy użyciu polecenia New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="b3a6e-398">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="b3a6e-399">2.4.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-399">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b3a6e-400">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-400">Az.Accounts</span></span>
* <span data-ttu-id="b3a6e-401">Dodano obsługę poleceń cmdlet profilu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-401">Add support for profile cmdlets</span></span>
* <span data-ttu-id="b3a6e-402">Dodano obsługę środowisk i płaszczyzn danych w generowanych poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-402">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="b3a6e-403">Naprawiono błąd polegający na tym, że w niektórych przypadkach dla poleceń cmdlet płaszczyzny danych w programie Windows PowerShell był używany nieprawidłowy punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-403">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="b3a6e-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="b3a6e-404">Az.Advisor</span></span>
* <span data-ttu-id="b3a6e-405">Wersja ogólnodostępna modułu Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="b3a6e-405">GA release of Az.Advisor</span></span>
* <span data-ttu-id="b3a6e-406">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="b3a6e-406">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b3a6e-407">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3a6e-407">Az.ApiManagement</span></span>
* <span data-ttu-id="b3a6e-408">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="b3a6e-408">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="b3a6e-409">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b3a6e-409">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="b3a6e-410">Dodano obsługę wykonywania zapytań dotyczących subskrypcji według użytkownika i produktu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-410">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="b3a6e-411">Dodano obsługę wykonywania zapytań przy użyciu zakresu „/”, „/apis”, „/apis/echo-api”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-411">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="b3a6e-412">Rozwiązano problemy https://github.com/Azure/azure-powershell/issues/9307 i https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="b3a6e-412">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="b3a6e-413">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b3a6e-413">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="b3a6e-414">Dodano obsługę określania właściwości „ApiVersion” i „ApiVersionSetId” podczas importowania interfejsów API</span><span class="sxs-lookup"><span data-stu-id="b3a6e-414">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b3a6e-415">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-415">Az.Automation</span></span>
* <span data-ttu-id="b3a6e-416">Usunięto usterkę polecenia cmdlet Set-AzAutomationConnectionFieldValue w celu obsługi wartości ciągu.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-416">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-417">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-418">Dodano parametr HyperVGeneration do polecenia New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-418">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b3a6e-419">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b3a6e-419">Az.DataFactory</span></span>
* <span data-ttu-id="b3a6e-420">Aktualizowanie danych wyjściowych poleceń cmdlet pobierania uruchomień działań, pobierania uruchomień potoków i pobierania uruchomień wyzwalaczy usługi ADF w celu obsługi potoku Select-Object.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-420">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b3a6e-421">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b3a6e-421">Az.EventGrid</span></span>
* <span data-ttu-id="b3a6e-422">Poprawiono literówkę w dokumentacji polecenia New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="b3a6e-422">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b3a6e-423">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b3a6e-423">Az.IotHub</span></span>
* <span data-ttu-id="b3a6e-424">Dodano obsługę ponownego generowania kluczy zasad autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-424">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-425">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-425">Az.Network</span></span>
* <span data-ttu-id="b3a6e-426">Dodano właściwość „RoutingPreference” do tagów publicznych adresów IP</span><span class="sxs-lookup"><span data-stu-id="b3a6e-426">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="b3a6e-427">Poprawiono przykłady dla dokumentacji referencyjnej polecenia „Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-427">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b3a6e-428">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b3a6e-428">Az.PolicyInsights</span></span>
* <span data-ttu-id="b3a6e-429">Rozwiązano problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="b3a6e-429">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="b3a6e-430">Więcej informacji: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="b3a6e-430">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b3a6e-431">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b3a6e-431">Az.OperationalInsights</span></span>
* <span data-ttu-id="b3a6e-432">Naprawiono model źródła danych CustomLog zwracany w poleceniu Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b3a6e-432">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b3a6e-433">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-433">Az.RecoveryServices</span></span>
* <span data-ttu-id="b3a6e-434">Poprawka dotycząca polecenia get-policy dla maszyn wirtualnych IaaS</span><span class="sxs-lookup"><span data-stu-id="b3a6e-434">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-435">Az.Resources</span></span>
    - <span data-ttu-id="b3a6e-436">Poprawiono tekst pomocy dotyczącej parametru -Top polecenia Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="b3a6e-436">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="b3a6e-437">Dodano obsługę stronicowania po stronie klienta dla polecenia Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="b3a6e-437">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="b3a6e-438">Dodano nowe parametry dla polecenia Set-AzPolicyAssignment: -PolicyParameters i -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="b3a6e-438">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="b3a6e-439">Aktualizacje dokumentacji i przykładów dla poleceń cmdlet zasad</span><span class="sxs-lookup"><span data-stu-id="b3a6e-439">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b3a6e-440">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b3a6e-440">Az.ServiceBus</span></span>
* <span data-ttu-id="b3a6e-441">Poprawka rozwiązująca problem #4938 — polecenie New-AzureRmServiceBusQueue zwraca wynik BadRequest w przypadku ustawienia właściwości MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="b3a6e-441">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-442">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-442">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-443">Dodano polecenia cmdlet grupy trybu failover wystąpienia z wersji zapoznawczej do wersji publicznej</span><span class="sxs-lookup"><span data-stu-id="b3a6e-443">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="b3a6e-444">Obsługa inspekcji w usłudze Azure SQL Server/Database za pomocą nowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-444">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="b3a6e-445">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b3a6e-445">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b3a6e-446">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b3a6e-446">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b3a6e-447">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b3a6e-447">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b3a6e-448">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b3a6e-448">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="b3a6e-449">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b3a6e-449">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="b3a6e-450">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b3a6e-450">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="b3a6e-451">Usunięto ograniczenia wiadomości e-mail z ustawień oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="b3a6e-451">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b3a6e-452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-452">Az.Storage</span></span>
* <span data-ttu-id="b3a6e-453">Zmieniono dwa parametry: „-IndexDocument” i „-ErrorDocument404Path” z wymaganych na opcjonalne w poleceniu cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-453">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="b3a6e-454">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b3a6e-454">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="b3a6e-455">Zaktualizowano pomoc dotyczącą polecenia Get-AzStorageBlobContent przez dodanie przykładu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-455">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="b3a6e-456">Wyświetlanie dodatkowych informacji o błędzie w przypadku niepowodzenia polecenia cmdlet z powodu wyjątku StorageException</span><span class="sxs-lookup"><span data-stu-id="b3a6e-456">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="b3a6e-457">Obsługa tworzenia i aktualizowania konta magazynu przy użyciu uwierzytelniania usługi AAD DS w usłudze Azure Files</span><span class="sxs-lookup"><span data-stu-id="b3a6e-457">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="b3a6e-458">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3a6e-458">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="b3a6e-459">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3a6e-459">Set-AzStorageAccount</span></span>
* <span data-ttu-id="b3a6e-460">Obsługa wyświetlania listy lub zamykania dojść do plików udziału plików, katalogu plików lub pliku</span><span class="sxs-lookup"><span data-stu-id="b3a6e-460">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="b3a6e-461">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b3a6e-461">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="b3a6e-462">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b3a6e-462">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b3a6e-463">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b3a6e-463">Az.StorageSync</span></span>
* <span data-ttu-id="b3a6e-464">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="b3a6e-464">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="b3a6e-465">2.3.2 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-465">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b3a6e-466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-466">Az.Accounts</span></span>
* <span data-ttu-id="b3a6e-467">Usunięto usterkę polegającą na używaniu w niektórych przypadkach niepoprawnego adresu URL w wywołaniach funkcji</span><span class="sxs-lookup"><span data-stu-id="b3a6e-467">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="b3a6e-468">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="b3a6e-468">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="b3a6e-469">Rozwiązano problem z aliasami w poleceniach cmdlet z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="b3a6e-469">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="b3a6e-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b3a6e-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="b3a6e-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="b3a6e-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-472">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-472">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-473">Proste zestawy parametrów New-AzVm i New-AzVmss akceptują teraz parametr „ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-473">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="b3a6e-474">Poprawiono literówkę w dokumentacji referencyjnej polecenia „New-AzVM”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-474">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="b3a6e-475">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="b3a6e-475">Az.Dns</span></span>
* <span data-ttu-id="b3a6e-476">Poprawiono literówkę w przykładach pomocy polecenia „Set-AzDnsZone”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-476">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b3a6e-477">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b3a6e-477">Az.EventGrid</span></span>
* <span data-ttu-id="b3a6e-478">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-478">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="b3a6e-479">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-479">New cmdlets:</span></span>
    - <span data-ttu-id="b3a6e-480">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b3a6e-480">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b3a6e-481">Tworzy nową domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-481">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b3a6e-482">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b3a6e-482">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b3a6e-483">Pobiera szczegóły domeny usługi Event Grid lub pobiera listę wszystkich domen usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-483">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="b3a6e-484">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b3a6e-484">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b3a6e-485">Usuwa domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-485">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b3a6e-486">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="b3a6e-486">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="b3a6e-487">Ponownie generuje klucz dostępu współdzielonego dla domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-487">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b3a6e-488">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="b3a6e-488">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="b3a6e-489">Pobiera klucze dostępu współdzielonego używane do publikowania zdarzeń w domenie usługi Event Grid.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-489">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="b3a6e-490">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-490">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="b3a6e-491">Tworzy nowy temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-491">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="b3a6e-492">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="b3a6e-492">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="b3a6e-493">Pobiera szczegóły tematu domeny usługi Event Grid lub pobiera listę wszystkich tematów domeny usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-493">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="b3a6e-494">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-494">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="b3a6e-495">Usuwa istniejący temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-495">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="b3a6e-496">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-496">Updated cmdlets:</span></span>
    - <span data-ttu-id="b3a6e-497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="b3a6e-498">Dodano nowe wymagane parametry do obsługi przesyłania potokowego nowej domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-498">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="b3a6e-499">Dodano nowe wymagane parametry w celu określenia nowej nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-499">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="b3a6e-500">Dodano nowe zestawy parametrów dla domen i tematów domen, aby umożliwić ponowne używanie istniejących parametrów (np. EndPointType, SubjectBeginsWith itp.).</span><span class="sxs-lookup"><span data-stu-id="b3a6e-500">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="b3a6e-501">Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-501">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="b3a6e-502">Data wygaśnięcia subskrypcji zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="b3a6e-502">Event subscription expiration date,</span></span>
            - <span data-ttu-id="b3a6e-503">Zaawansowane parametry filtrowania.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-503">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="b3a6e-504">Dodano nowe wyliczenie dla elementu servicebusqueue jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-504">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="b3a6e-505">Uniemożliwiono użycie elementu „Wszystkie” w opcji -IncludedEventType i zamieniono go na</span><span class="sxs-lookup"><span data-stu-id="b3a6e-505">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="b3a6e-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="b3a6e-507">Dodano nowe opcjonalne parametry (Top, ODataQuery i NextLink) w celu obsługi filtrowania i stronicowania wyników.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-507">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="b3a6e-508">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="b3a6e-508">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="b3a6e-509">Dodano nowe wymagane parametry do obsługi przesyłania potokowego domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-509">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="b3a6e-510">Dodano nowe wymagane parametry w celu określenia nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-510">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b3a6e-511">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b3a6e-511">Az.FrontDoor</span></span>
* <span data-ttu-id="b3a6e-512">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="b3a6e-512">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="b3a6e-513">Dodano obsługę przekształceń i nową wartość autouzupełniania operatora (wyrażenie regularne)</span><span class="sxs-lookup"><span data-stu-id="b3a6e-513">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="b3a6e-514">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="b3a6e-514">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="b3a6e-515">Dodano nowe wartości autouzupełniania</span><span class="sxs-lookup"><span data-stu-id="b3a6e-515">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-516">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-516">Az.Network</span></span>
* <span data-ttu-id="b3a6e-517">Dodano obsługę zasobu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b3a6e-517">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="b3a6e-518">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-518">New cmdlets</span></span>
        - <span data-ttu-id="b3a6e-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="b3a6e-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="b3a6e-520">Dodano element AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="b3a6e-520">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="b3a6e-521">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-521">New cmdlets</span></span> 
        - <span data-ttu-id="b3a6e-522">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="b3a6e-522">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="b3a6e-523">Dodano element PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b3a6e-523">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="b3a6e-524">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-524">New cmdlets</span></span> 
        - <span data-ttu-id="b3a6e-525">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b3a6e-525">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="b3a6e-526">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b3a6e-526">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b3a6e-527">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b3a6e-527">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b3a6e-528">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-528">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="b3a6e-529">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b3a6e-529">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="b3a6e-530">Dodano element PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3a6e-530">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="b3a6e-531">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-531">New cmdlets</span></span>
        - <span data-ttu-id="b3a6e-532">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3a6e-532">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b3a6e-533">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3a6e-533">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b3a6e-534">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3a6e-534">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b3a6e-535">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="b3a6e-535">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="b3a6e-536">Zaktualizowano poniższe polecenia dla funkcji: Flaga UseLocalAzureIpAddress w elemencie VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b3a6e-536">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="b3a6e-537">Zaktualizowano polecenie New-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-537">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="b3a6e-538">Zaktualizowano polecenie Set-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-538">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="b3a6e-539">Dodano pole tylko do odczytu PeeredConnections w komunikacji równorzędnej usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-539">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="b3a6e-540">Dodano pole tylko do odczytu GlobalReachEnabled w usłudze ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-540">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="b3a6e-541">Dodano atrybut zmiany wywołujący zakończenie obsługi pola AllowGlobalReach w modelu ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b3a6e-541">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="b3a6e-542">Rozwiązano problem 8756 podczas używania elementu TargetListenerID z poleceniami cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6e-542">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="b3a6e-543">Usunięto usterkę w poleceniu New-AzApplicationGatewayPathRuleConfig, która uniemożliwiała ustawienie zestawu reguł regenerowania.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-543">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="b3a6e-544">Rozwiązano problem z wyświetlaniem elementu VirtualNetworkTaps w elemencie NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6e-544">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="b3a6e-545">Naprawiono polecenia cmdlet pobierania Cortex dla listy wszystkich części</span><span class="sxs-lookup"><span data-stu-id="b3a6e-545">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="b3a6e-546">Naprawiono tworzenie odwołań elementu VirtualHub dla elementu ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="b3a6e-546">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="b3a6e-547">Dodano obsługę stref dostępności w elementach AzureFirewall i NatGateway</span><span class="sxs-lookup"><span data-stu-id="b3a6e-547">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="b3a6e-548">Dodano polecenie cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="b3a6e-548">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="b3a6e-549">Dodano obsługę wielu publicznych adresów IP usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="b3a6e-549">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="b3a6e-550">Zaktualizowano polecenie cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-550">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="b3a6e-551">Dodano parametr -PublicIpAddress, który akceptuje co najmniej jeden obiekt publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="b3a6e-551">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="b3a6e-552">Dodano parametr -VirtualNetwork, który akceptuje obiekt sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b3a6e-552">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="b3a6e-553">Dodano do obiektu zapory metody AddPublicIpAddress i RemovePublicIpAddress, które akceptują obiekt publicznego adresu IP jako dane wejściowe</span><span class="sxs-lookup"><span data-stu-id="b3a6e-553">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="b3a6e-554">Wycofano parametry -PublicIpName i -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b3a6e-554">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="b3a6e-555">Zaktualizowano poniższe polecenia dla funkcji: Ustawiono w opcjach uwierzytelniania usługi AAD elementu VpnClient zasób bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-555">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="b3a6e-556">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-556">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="b3a6e-557">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-557">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="b3a6e-558">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr przełącznika RemoveAadAuthentication w celu usunięcia z bramy opcji uwierzytelniania usługi AAD elementu VpnClient.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-558">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b3a6e-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b3a6e-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="b3a6e-560">Włączono warstwę cenową **pergb2018** w poleceniu „New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-560">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-561">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-561">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-562">Obsługa dodatkowych opcji eksportowania szablonu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-562">Support for additional Template Export options</span></span>
    - <span data-ttu-id="b3a6e-563">Dodano parametr „-SkipResourceNameParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b3a6e-563">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="b3a6e-564">Dodano parametr „-SkipAllParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b3a6e-564">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="b3a6e-565">Dodano parametr „-Resource” do polecenia Export-AzResourceGroup w celu filtrowania wyeksportowanych zasobów</span><span class="sxs-lookup"><span data-stu-id="b3a6e-565">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b3a6e-566">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b3a6e-566">Az.ServiceFabric</span></span>
* <span data-ttu-id="b3a6e-567">Usunięto błąd dodawania certyfikatu polegający na pobieraniu przez element ByExistingKeyVault nieprawidłowego odcisku palca w niektórych przypadkach</span><span class="sxs-lookup"><span data-stu-id="b3a6e-567">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-568">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-568">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-569">Naprawiono sufiks punktu końcowego magazynu usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b3a6e-569">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="b3a6e-570">Rozwiązano problem z usługą Advanced Data Security polegający na przesłanianiu zasad usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b3a6e-570">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="b3a6e-571">Nowe polecenia cmdlet modułu Management.Sql umożliwiające klientom dodawanie kluczy funkcji TDE i ustawianie funkcji ochrony TDE dla wystąpień zarządzanych</span><span class="sxs-lookup"><span data-stu-id="b3a6e-571">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="b3a6e-572">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b3a6e-572">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b3a6e-573">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b3a6e-573">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b3a6e-574">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b3a6e-574">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b3a6e-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b3a6e-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="b3a6e-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b3a6e-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b3a6e-577">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-577">Az.Storage</span></span>
* <span data-ttu-id="b3a6e-578">Obsługa rodzajów FileStorage i SkuName Premium_ZRS podczas tworzenia konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-578">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="b3a6e-579">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3a6e-579">New-AzStorageAccount</span></span>
* <span data-ttu-id="b3a6e-580">Opis z wyjaśnieniem polecenia cmdlet niezmienności obiektów blob</span><span class="sxs-lookup"><span data-stu-id="b3a6e-580">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="b3a6e-581">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-581">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b3a6e-582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b3a6e-582">Az.Websites</span></span>
* <span data-ttu-id="b3a6e-583">Optymalizuje polecenie Get-AzWebAppCertificate w celu filtrowania według grupy zasobów na serwerze zamiast na kliencie</span><span class="sxs-lookup"><span data-stu-id="b3a6e-583">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="b3a6e-584">Dodano parametr przełącznika -UseDisasterRecovery do polecenia Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b3a6e-584">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="b3a6e-585">2.2.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-585">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="b3a6e-586">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b3a6e-586">Az.Cdn</span></span>
* <span data-ttu-id="b3a6e-587">Zaktualizowano polecenia cmdlet do obsługi funkcji rulesEngine na podstawie interfejsu API w wersji 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-587">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-588">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-589">Dodano parametr `NoWait`, który powoduje rozpoczęcie operacji i natychmiastowy powrót, bez czekania na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-589">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="b3a6e-590">Zaktualizowano następujące polecenia cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3a6e-590">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b3a6e-591">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b3a6e-591">Az.EventHub</span></span>
* <span data-ttu-id="b3a6e-592">Poprawka błędu #9231 — polecenie Get-AzEventHubNamespace nie zwraca tagów</span><span class="sxs-lookup"><span data-stu-id="b3a6e-592">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="b3a6e-593">Poprawka błędu #9230 — polecenie Get-AzEventHubNamespace zwraca wartość ResourceGroup zamiast wartości ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a6e-593">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-594">Az.Network</span></span>
* <span data-ttu-id="b3a6e-595">Aktualizowanie wartości ResourceId i InputObject dla bramy translatora adresów sieciowych</span><span class="sxs-lookup"><span data-stu-id="b3a6e-595">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="b3a6e-596">Dodawanie aliasów dla wartości ResourceId i InputObject</span><span class="sxs-lookup"><span data-stu-id="b3a6e-596">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b3a6e-597">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b3a6e-597">Az.PolicyInsights</span></span>
* <span data-ttu-id="b3a6e-598">Rozwiązanie problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="b3a6e-598">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b3a6e-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="b3a6e-600">Minimalny czas przechowywania zasad IaaSVM w dniach zmieniono z 7 na 1</span><span class="sxs-lookup"><span data-stu-id="b3a6e-600">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b3a6e-601">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b3a6e-601">Az.ServiceBus</span></span>
* <span data-ttu-id="b3a6e-602">Rozwiązanie problemu #9182 — Get-AzServiceBusNamespace zwraca wartość ResourceGroup zamiast ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a6e-602">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b3a6e-603">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b3a6e-603">Az.ServiceFabric</span></span>
* <span data-ttu-id="b3a6e-604">Poprawienie błędu pisowni w komunikacie o błędzie polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-604">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="b3a6e-605">Poprawienie brakującego znaku w wierszach polecenia usługi Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b3a6e-605">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-606">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-606">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-607">Dodanie parametru DnsZonePartner dla polecenia cmdlet New-AzureSqlInstance w celu obsługi funkcji AutoDr dla wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-607">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="b3a6e-608">Wycofanie polecenia cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-608">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="b3a6e-609">Zmiana nazwy poleceń cmdlet z Wykrywanie zagrożeń na Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b3a6e-609">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="b3a6e-610">Parametry New-AzSqlInstance -StorageSizeInGB i -LicenseType są teraz opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-610">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b3a6e-611">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b3a6e-611">Az.Websites</span></span>
* <span data-ttu-id="b3a6e-612">Rozwiązanie problemu polegającego na tym, że użycie poleceń Set-AzWebApp i Set-AzWebAppSlot z właściwością -WebApp powodowało usunięcie tagów</span><span class="sxs-lookup"><span data-stu-id="b3a6e-612">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="b3a6e-613">2.1.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-613">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="b3a6e-614">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3a6e-614">Az.ApiManagement</span></span>
* <span data-ttu-id="b3a6e-615">Utworzono nowe polecenia cmdlet do zarządzania diagnostyką w zakresie globalnym i interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b3a6e-615">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="b3a6e-616">**Get-AzApiManagementDiagnostic** — uzyskiwanie diagnostyki skonfigurowanej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b3a6e-616">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="b3a6e-617">**New-AzApiManagementDiagnostic** — tworzenie nowej diagnostyki w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b3a6e-617">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="b3a6e-618">**New-AzApiManagementHttpMessageDiagnostic** — tworzenie ustawienia diagnostyki określającego nagłówki do rejestrowania i rozmiar treści w bajtach</span><span class="sxs-lookup"><span data-stu-id="b3a6e-618">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="b3a6e-619">**New-AzApiManagementPipelineDiagnosticSetting** — tworzenie ustawień diagnostyki dla przychodzących/wychodzących komunikatów HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-619">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="b3a6e-620">**New-AzApiManagementSamplingSetting** — tworzenie ustawienia próbkowania dla żądań i odpowiedzi na potrzeby diagnostyki</span><span class="sxs-lookup"><span data-stu-id="b3a6e-620">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="b3a6e-621">**Remove-AzApiManagementDiagnostic** — usuwanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b3a6e-621">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="b3a6e-622">**Set-AzApiManagementDiagnostic** — aktualizowanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b3a6e-622">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="b3a6e-623">Utworzono nowe polecenia cmdlet do zarządzania pamięcią podręczną usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3a6e-623">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="b3a6e-624">**Get-AzApiManagementCache** — uzyskiwanie szczegółów pamięci podręcznej określonej przez identyfikator lub wszystkich pamięci podręcznych</span><span class="sxs-lookup"><span data-stu-id="b3a6e-624">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="b3a6e-625">**New-AzApiManagementCache** — tworzenie nowej, „domyślnej” pamięci podręcznej lub pamięci podręcznej w konkretnym „regionie” platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b3a6e-625">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="b3a6e-626">**Remove-AzApiManagementCache** — usuwanie pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="b3a6e-626">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="b3a6e-627">**Update-AzApiManagementCache** — aktualizacja pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="b3a6e-627">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="b3a6e-628">Utworzono nowe polecenia cmdlet do zarządzania schematem interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b3a6e-628">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="b3a6e-629">**New-AzApiManagementSchema** — tworzenie nowego schematu dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b3a6e-629">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="b3a6e-630">**Get-AzApiManagementSchema** — pobieranie schematów skonfigurowanych w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="b3a6e-630">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="b3a6e-631">**Remove-AzApiManagementSchema** — usuwanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="b3a6e-631">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="b3a6e-632">**Set-AzApiManagementSchema** — aktualizowanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="b3a6e-632">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="b3a6e-633">Utworzono nowe polecenie cmdlet do generowania tokenu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-633">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="b3a6e-634">**New-AzApiManagementUserToken** — generowanie nowego tokenu użytkownika ważnego domyślnie przez 8 godzin. Za pomocą tego polecenia cmdlet można wygenerować token dla użytkownika „GIT”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-634">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="b3a6e-635">Utworzono nowe polecenie cmdlet do pobierania stanu sieci.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-635">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="b3a6e-636">**Get-AzApiManagementNetworkStatus** — uzyskiwanie stanu sieci dla łączności z zasobami, od których zależy usługa API Management.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-636">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="b3a6e-637">Jest to przydatne w przypadku wdrażania usługi ApiManagement w sieci wirtualnej i weryfikacji, czy któreś z zależności są uszkodzone.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-637">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="b3a6e-638">Zaktualizowano polecenie cmdlet **New-AzApiManagement** do zarządzania usługą ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3a6e-638">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="b3a6e-639">Dodano obsługę nowych jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-639">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="b3a6e-640">Dodano obsługę włączania flagi „EnableClientCertificate” dla jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-640">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="b3a6e-641">Nowe polecenie cmdlet **New-AzApiManagementSslSetting** umożliwia skonfigurowanie ustawienia „TLS/SSL” na „Zaplecze” i „Fronton”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-641">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="b3a6e-642">Za jego pomocą można też skonfigurować szyfrowanie, takie jak „3DES”, i protokoły serwera, takie jak „Http2”we frontonie usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-642">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="b3a6e-643">Dodano obsługę konfigurowania nazwy hosta „DeveloperPortal” usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-643">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="b3a6e-644">Zaktualizowano polecenia cmdlet **Get-AzApiManagementSsoToken**, aby przyjmowały jako wejście obiekt „PsApiManagement”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-644">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="b3a6e-645">Zaktualizowano polecenie cmdlet, aby wyświetlało komunikaty o błędach śródwierszowo</span><span class="sxs-lookup"><span data-stu-id="b3a6e-645">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="b3a6e-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Kod błędu: Komunikat o błędzie ValidationError: Co najmniej jedno pole zawiera nieprawidłową wartość: Szczegóły błędu:    [Code=ValidationError, Message=Błąd w elemencie „log-to-eventhub” w wierszu 3, kolumna 10: Nie znaleziono rejestratora, element docelowy=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="b3a6e-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="b3a6e-647">Zaktualizowano polecenie cmdlet **Export-AzApiManagementApi** tak, aby eksportowało interfejsy API w formacie „OpenApi 3.0”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-647">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="b3a6e-648">Zaktualizowano polecenie cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b3a6e-648">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b3a6e-649">W celu importowania interfejsu Api z dokumentu ze specyfikacją interfejsu „OpenApi 3.0”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-649">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="b3a6e-650">W celu przesłonięcia właściwości „PsApiManagementSchema” określonej w dowolnym dokumencie („Swagger”, „Wadl”, „Wsdl”, „OpenApi”).</span><span class="sxs-lookup"><span data-stu-id="b3a6e-650">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="b3a6e-651">W celu przesłonięcia właściwości „ServiceUrl” określonej w dowolnym dokumencie.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-651">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="b3a6e-652">Zaktualizowano polecenie cmdlet **Get-AzApiManagementPolicy** tak, aby zwracało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-652">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="b3a6e-653">Zaktualizowano polecenie cmdlet **Set-AzApiManagementPolicy** tak, aby akceptowało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml” i ze zmianą znaczenia Xml przy użyciu formatu „xml”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-653">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="b3a6e-654">Zaktualizowano polecenie cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b3a6e-654">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="b3a6e-655">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-655">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="b3a6e-656">W celu utworzenia interfejsu API we właściwości ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-656">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="b3a6e-657">W celu sklonowania interfejsu API przy użyciu właściwości „SourceApiId” i „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-657">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="b3a6e-658">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-658">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="b3a6e-659">Zaktualizowano polecenie cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b3a6e-659">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b3a6e-660">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-660">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="b3a6e-661">W celu zaktualizowania interfejsu API we właściwości „ApiVersionSet”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-661">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="b3a6e-662">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-662">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="b3a6e-663">Zaktualizowano polecenie cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="b3a6e-663">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="b3a6e-664">W celu klonowania (kopiowanie tagów, produktów, operacji i zasad) istniejącej wersji przy użyciu właściwości „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-664">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="b3a6e-665">Dla nowej wersji przyjmowana jest wartość „ApiId” elementu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-665">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="b3a6e-666">W celu dostarczenia właściwości „ApiRevisionDescription”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-666">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="b3a6e-667">W celu przesłonięcia właściwości „ServiceUrl” podczas klonowania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-667">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="b3a6e-668">Zaktualizowano polecenie cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="b3a6e-668">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="b3a6e-669">W celu skonfigurowania właściwości „AAD” lub „AADB2C” za pomocą właściwości „Authority”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-669">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="b3a6e-670">W celu skonfigurowania właściwości „SignupPolicy”, „SigninPolicy”, „ProfileEditingPolicy” i „PasswordResetPolicy”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-670">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="b3a6e-671">Zaktualizowano polecenie cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b3a6e-671">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="b3a6e-672">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-672">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="b3a6e-673">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-673">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="b3a6e-674">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-674">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="b3a6e-675">Zaktualizowano polecenie cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b3a6e-675">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="b3a6e-676">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-676">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="b3a6e-677">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-677">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="b3a6e-678">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-678">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="b3a6e-679">Zaktualizowano następujące polecenia cmdlet do akceptowania właściwości „ResourceId” jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="b3a6e-679">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="b3a6e-680">„New-AzApiManagementContext”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-680">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="b3a6e-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="b3a6e-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="b3a6e-682">„Get-AzApiManagementApiRelease”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-682">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="b3a6e-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="b3a6e-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="b3a6e-684">„Get-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-684">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="b3a6e-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="b3a6e-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="b3a6e-686">„Get-AzApiManagementAuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-686">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="b3a6e-687">„Get-AzApiManagementBackend”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-687">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="b3a6e-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="b3a6e-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="b3a6e-689">„Get-AzApiManagementCertificate”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-689">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="b3a6e-690">„Remove-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-690">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="b3a6e-691">„Remove-AzApiManagementSubscription”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-691">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b3a6e-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-692">Az.Automation</span></span>
* <span data-ttu-id="b3a6e-693">Zaktualizowano polecenie Get-AzAutomationJobOutputRecord tak, aby obsługiwało wartości rekordów w postaci kodu JSON i tekstowej.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-693">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="b3a6e-694">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="b3a6e-694">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="b3a6e-695">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="b3a6e-695">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="b3a6e-696">Zmieniono działanie polecenia Start-AzAutomationDscCompilationJob tak, aby tylko uruchamiało zadanie zamiast czekać na jego zakończenie.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-696">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="b3a6e-697">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="b3a6e-697">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="b3a6e-698">Poprawka dla polecenia Get-AzAutomationDscNode podczas używania opcji -Name zwraca wszystkie węzły.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-698">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="b3a6e-699">Teraz zwraca tylko pasujące węzły.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-699">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-700">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-701">Dodanie parametrów ProtectFromScaleIn i ProtectFromScaleSetAction do polecenia cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-701">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="b3a6e-702">Nowy zestaw parametrów New-AzVM wimple teraz używa domyślnie dostępnej lokalizacji, jeśli region „Wschodnie stany USA” nie jest obsługiwany.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-702">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b3a6e-703">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b3a6e-703">Az.DataLakeStore</span></span>
* <span data-ttu-id="b3a6e-704">Aktualizacja zestawu ADLS SDK do korzystania z klienta httpclient, integrowanie testowania płaszczyzny danych z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b3a6e-704">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b3a6e-705">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b3a6e-705">Az.Monitor</span></span>
* <span data-ttu-id="b3a6e-706">Naprawiono nieprawidłowe nazwy parametrów w przykładach pomocy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-706">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-707">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-707">Az.Network</span></span>
* <span data-ttu-id="b3a6e-708">Dodanie flagi DisableBgpRoutePropagation do danych wyjściowych obowiązującej tabeli routingu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-708">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="b3a6e-709">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-709">Updated cmdlet:</span></span>
        - <span data-ttu-id="b3a6e-710">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3a6e-710">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="b3a6e-711">Poprawienie podwójnego łącznika w dokumentacji polecenia New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b3a6e-711">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-712">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-712">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-713">Dodanie nowego polecenia cmdlet Get-AzureRmDenyAssignment do pobierania przypisań odmowy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-713">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-714">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-715">Zmiana nazwy poleceń cmdlet usługi Advanced Threat Protection na Advanced Data Security i domyślne włączenie oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="b3a6e-715">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="b3a6e-716">2.0.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-716">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b3a6e-717">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-717">Az.Accounts</span></span>
* <span data-ttu-id="b3a6e-718">Aktualizacja biblioteki uwierzytelniania w celu rozwiązania problemów z usługą ADFS dotyczących uwierzytelniania nazwy użytkownika i hasła</span><span class="sxs-lookup"><span data-stu-id="b3a6e-718">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b3a6e-719">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-719">Az.CognitiveServices</span></span>
* <span data-ttu-id="b3a6e-720">Dla usług wyszukiwania Bing wyświetlane jest tylko zrzeczenie odpowiedzialności usługi Bing.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-720">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="b3a6e-721">Naprawiono błąd polegający na niepomyślnym tworzeniu konta.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-721">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-722">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-723">Funkcja Grupa umieszczania w pobliżu.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-723">Proximity placement group feature.</span></span>
    - <span data-ttu-id="b3a6e-724">Dodano następujące nowe polecenia cmdlet:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="b3a6e-724">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="b3a6e-725">Do następujących poleceń cmdlet dodano nowy parametr ProximityPlacementGroupId:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-725">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="b3a6e-726">Do polecenia New-AzGalleryImageVersion dodano parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-726">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="b3a6e-727">Właściwość TargetRegion polecenia New-AzGalleryImageVersion może zawierać parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-727">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="b3a6e-728">Do poleceń Stop-AzVM i Stop-AzVmss dodano parametr przełącznika SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="b3a6e-728">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="b3a6e-729">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="b3a6e-729">Breaking changes</span></span>
    - <span data-ttu-id="b3a6e-730">Polecenie Set-AzVMBootDiagnostics zamieniono na polecenie Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-730">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="b3a6e-731">Polecenie Export-AzLogAnalyticThrottledRequests zamieniono na polecenie Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-731">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="b3a6e-732">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="b3a6e-732">Az.DeploymentManager</span></span>
* <span data-ttu-id="b3a6e-733">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="b3a6e-733">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="b3a6e-734">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="b3a6e-734">Az.Dns</span></span>
* <span data-ttu-id="b3a6e-735">Automatyczne delegowanie serwera nazw systemu DNS</span><span class="sxs-lookup"><span data-stu-id="b3a6e-735">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="b3a6e-736">Polecenie cmdlet tworzenia strefy DNS akceptuje nazwę strefy nadrzędnej jako dodatkowy parametr opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-736">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="b3a6e-737">Dodaje rekordy serwera nazw w strefie nadrzędnej dla nowo utworzonej strefy podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-737">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b3a6e-738">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b3a6e-738">Az.FrontDoor</span></span>
* <span data-ttu-id="b3a6e-739">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b3a6e-739">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="b3a6e-740">Zmiana nazw poleceń cmdlet zapory aplikacji internetowej w celu dołączenia ciągu „Waf”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-740">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="b3a6e-741">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b3a6e-741">Az.HDInsight</span></span>
* <span data-ttu-id="b3a6e-742">Usunięto dwa polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-742">Removed two cmdlets:</span></span>
    - <span data-ttu-id="b3a6e-743">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b3a6e-743">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="b3a6e-744">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b3a6e-744">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="b3a6e-745">Dodano nowe polecenie cmdlet Set-AzHDInsightGatewayCredential w celu zastąpienia polecenia Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b3a6e-745">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="b3a6e-746">Zaktualizowano polecenie cmdlet Get-AzHDInsightJobOutput, aby rozróżnić rolę czytelnika i rolę operatora usługi HDInsight:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-746">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="b3a6e-747">Użytkownicy z rolą czytelnika muszą jawnie określić parametr „DefaultStorageAccountKey” — w przeciwnym razie wystąpi błąd.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-747">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="b3a6e-748">Nie będzie to miało wpływu na użytkowników z rolą operatora usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-748">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b3a6e-749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b3a6e-749">Az.Monitor</span></span>
* <span data-ttu-id="b3a6e-750">Nowe polecenia cmdlet dla interfejsu API SQR (Scheduled Query Rule, reguła zaplanowanego zapytania)</span><span class="sxs-lookup"><span data-stu-id="b3a6e-750">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="b3a6e-751">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="b3a6e-751">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="b3a6e-752">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="b3a6e-752">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="b3a6e-753">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="b3a6e-753">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="b3a6e-754">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="b3a6e-754">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="b3a6e-755">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="b3a6e-755">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="b3a6e-756">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="b3a6e-756">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="b3a6e-757">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b3a6e-757">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b3a6e-758">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b3a6e-758">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b3a6e-759">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b3a6e-759">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b3a6e-760">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b3a6e-760">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b3a6e-761">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b3a6e-761">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b3a6e-762">[Więcej](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informacji na temat interfejsu API SQR</span><span class="sxs-lookup"><span data-stu-id="b3a6e-762">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="b3a6e-763">Zaktualizowano plik Az.Monitor.md w celu uwzględnienia poleceń cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="b3a6e-763">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-764">Az.Network</span></span>
* <span data-ttu-id="b3a6e-765">Dodano obsługę dla zasobu usługi NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="b3a6e-765">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="b3a6e-766">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-766">New cmdlets</span></span>
        - <span data-ttu-id="b3a6e-767">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b3a6e-767">New-AzNatGateway</span></span>
        - <span data-ttu-id="b3a6e-768">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b3a6e-768">Get-AzNatGateway</span></span>
        - <span data-ttu-id="b3a6e-769">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b3a6e-769">Set-AzNatGateway</span></span>
        - <span data-ttu-id="b3a6e-770">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b3a6e-770">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="b3a6e-771">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-771">Updated cmdlets</span></span>
        - <span data-ttu-id="b3a6e-772">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="b3a6e-772">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="b3a6e-773">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="b3a6e-773">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="b3a6e-774">Zaktualizowano poniższe polecenia dla funkcji: Ustawianie/usuwanie tras niestandardowych dla bramy Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-774">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="b3a6e-775">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-775">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="b3a6e-776">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-776">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b3a6e-777">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b3a6e-777">Az.PolicyInsights</span></span>
* <span data-ttu-id="b3a6e-778">Obsługa zapytań dotyczących szczegółów oceny zasad.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-778">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="b3a6e-779">Dodano parametr „-Expand” do polecenia Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-779">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="b3a6e-780">Obsługa polecenia „-Expand PolicyEvaluationDetails”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-780">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b3a6e-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="b3a6e-782">Obsługa odzyskiwania lokacji między subskrypcjami z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-782">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="b3a6e-783">Oznaczanie nadchodzących zmian powodujących niezgodność dla usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-783">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="b3a6e-784">Poprawka zakończenia planu akcji dla planu odzyskiwania usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-784">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="b3a6e-785">Poprawka aktualizacji mapowania sieci usługi Azure Site Recovery z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-785">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="b3a6e-786">Poprawka aktualizacji kierunku ochrony usługi Azure Site Recovery z platformy Azure na platformę Azure dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-786">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="b3a6e-787">Inne drobne poprawki.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-787">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="b3a6e-788">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b3a6e-788">Az.Relay</span></span>
* <span data-ttu-id="b3a6e-789">Poprawiono błędy pisowni w komunikatach przeznaczonych dla klientów</span><span class="sxs-lookup"><span data-stu-id="b3a6e-789">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b3a6e-790">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b3a6e-790">Az.ServiceBus</span></span>
* <span data-ttu-id="b3a6e-791">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="b3a6e-791">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b3a6e-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-792">Az.Storage</span></span>
* <span data-ttu-id="b3a6e-793">Uaktualnienie biblioteki klienta usługi Storage do wersji 10.0.1 (przestrzeń nazw wszystkich obiektów tego zestawu SDK została zmieniona z „Microsoft.WindowsAzure.Storage. *” na „Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="b3a6e-793">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="b3a6e-794">Uaktualnienie do wersji Microsoft.Azure.Management.Storage 11.0.0 w celu obsługi nowego interfejsu API w wersji 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-794">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="b3a6e-795">Domyślny rodzaj konta magazynu w poleceniu Utwórz konto magazynu został zmieniony ze „Storage” na „StorageV2”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-795">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="b3a6e-796">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3a6e-796">New-AzStorageAccount</span></span>
* <span data-ttu-id="b3a6e-797">Zmiana wyjściowego parametru Sku.Name polecenia cmdlet konta magazynu w celu wyrównania z wejściowym parametrem SkuName przez dodanie znaku „-”, na przykład zmiana „StandardLRS” na „Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-797">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="b3a6e-798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3a6e-798">New-AzStorageAccount</span></span>
    - <span data-ttu-id="b3a6e-799">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3a6e-799">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="b3a6e-800">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3a6e-800">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b3a6e-801">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b3a6e-801">Az.Websites</span></span>
* <span data-ttu-id="b3a6e-802">Właściwość „Kind” będzie teraz ustawiona dla obiektów PSSite zwracanych przez polecenie Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b3a6e-802">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="b3a6e-803">Polecenia Get-AzWebApp\*Metrics i Get-AzAppServicePlanMetrics oznaczono jako przestarzałe</span><span class="sxs-lookup"><span data-stu-id="b3a6e-803">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="b3a6e-804">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-804">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b3a6e-805">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="b3a6e-805">Highlights since the last major release</span></span>
* <span data-ttu-id="b3a6e-806">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="b3a6e-806">General availability of `Az` module</span></span>
* <span data-ttu-id="b3a6e-807">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b3a6e-807">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b3a6e-808">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b3a6e-808">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b3a6e-809">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-809">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b3a6e-810">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="b3a6e-810">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b3a6e-811">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-811">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b3a6e-812">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="b3a6e-812">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b3a6e-813">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-813">Az.Accounts</span></span>
* <span data-ttu-id="b3a6e-814">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="b3a6e-814">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b3a6e-815">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b3a6e-815">Az.Batch</span></span>
* <span data-ttu-id="b3a6e-816">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-816">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b3a6e-817">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b3a6e-817">Az.Cdn</span></span>
* <span data-ttu-id="b3a6e-818">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b3a6e-819">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-819">Az.CognitiveServices</span></span>
* <span data-ttu-id="b3a6e-820">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-821">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-821">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-822">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-822">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="b3a6e-823">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-823">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b3a6e-824">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="b3a6e-824">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b3a6e-825">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b3a6e-825">Az.DataFactory</span></span>
* <span data-ttu-id="b3a6e-826">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-826">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b3a6e-827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b3a6e-827">Az.DataLakeStore</span></span>
* <span data-ttu-id="b3a6e-828">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-828">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b3a6e-829">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b3a6e-829">Az.EventGrid</span></span>
* <span data-ttu-id="b3a6e-830">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-830">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b3a6e-831">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b3a6e-831">Az.EventHub</span></span>
* <span data-ttu-id="b3a6e-832">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="b3a6e-832">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="b3a6e-833">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b3a6e-833">Az.HDInsight</span></span>
* <span data-ttu-id="b3a6e-834">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-834">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b3a6e-835">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b3a6e-835">Az.IotHub</span></span>
* <span data-ttu-id="b3a6e-836">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b3a6e-837">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b3a6e-837">Az.KeyVault</span></span>
* <span data-ttu-id="b3a6e-838">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b3a6e-839">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="b3a6e-839">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="b3a6e-840">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b3a6e-840">Az.MachineLearning</span></span>
* <span data-ttu-id="b3a6e-841">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-841">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="b3a6e-842">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b3a6e-842">Az.Media</span></span>
* <span data-ttu-id="b3a6e-843">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b3a6e-844">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b3a6e-844">Az.Monitor</span></span>
  * <span data-ttu-id="b3a6e-845">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="b3a6e-845">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="b3a6e-846">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="b3a6e-846">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="b3a6e-847">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="b3a6e-847">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="b3a6e-848">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b3a6e-848">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b3a6e-849">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b3a6e-849">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b3a6e-850">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b3a6e-850">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="b3a6e-851">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="b3a6e-851">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-852">Az.Network</span></span>
* <span data-ttu-id="b3a6e-853">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b3a6e-854">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="b3a6e-854">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="b3a6e-855">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="b3a6e-855">Az.NotificationHubs</span></span>
* <span data-ttu-id="b3a6e-856">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-856">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b3a6e-857">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b3a6e-857">Az.OperationalInsights</span></span>
* <span data-ttu-id="b3a6e-858">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="b3a6e-859">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b3a6e-859">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="b3a6e-860">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b3a6e-861">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-861">Az.RecoveryServices</span></span>
* <span data-ttu-id="b3a6e-862">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b3a6e-863">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b3a6e-863">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="b3a6e-864">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="b3a6e-864">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="b3a6e-865">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="b3a6e-865">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b3a6e-866">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b3a6e-866">Az.RedisCache</span></span>
* <span data-ttu-id="b3a6e-867">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-867">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-868">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-868">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-869">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="b3a6e-869">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-870">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-870">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-871">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="b3a6e-871">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="b3a6e-872">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-872">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b3a6e-873">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-873">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="b3a6e-874">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-874">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="b3a6e-875">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-875">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="b3a6e-876">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-876">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="b3a6e-877">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="b3a6e-877">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b3a6e-878">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b3a6e-878">Az.Websites</span></span>
* <span data-ttu-id="b3a6e-879">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-879">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="b3a6e-880">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-880">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b3a6e-881">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-881">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="b3a6e-882">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-882">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="b3a6e-883">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-883">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b3a6e-884">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="b3a6e-884">Highlights since the last major release</span></span>
* <span data-ttu-id="b3a6e-885">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="b3a6e-885">General availability of `Az` module</span></span>
* <span data-ttu-id="b3a6e-886">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b3a6e-886">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b3a6e-887">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b3a6e-887">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b3a6e-888">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-888">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b3a6e-889">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="b3a6e-889">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b3a6e-890">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-890">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b3a6e-891">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="b3a6e-891">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b3a6e-892">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-892">Az.Accounts</span></span>
* <span data-ttu-id="b3a6e-893">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a6e-893">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b3a6e-894">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-894">Az.AnalysisServices</span></span>
* <span data-ttu-id="b3a6e-895">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="b3a6e-895">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="b3a6e-896">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="b3a6e-896">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b3a6e-897">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-897">Az.Automation</span></span>
* <span data-ttu-id="b3a6e-898">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-898">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="b3a6e-899">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-899">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="b3a6e-900">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-900">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-901">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-901">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-902">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-902">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b3a6e-903">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-903">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="b3a6e-904">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b3a6e-904">Az.ContainerInstance</span></span>
* <span data-ttu-id="b3a6e-905">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="b3a6e-905">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b3a6e-906">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b3a6e-906">Az.DataFactory</span></span>
* <span data-ttu-id="b3a6e-907">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="b3a6e-907">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="b3a6e-908">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-908">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-909">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-909">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-910">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-910">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="b3a6e-911">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-911">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="b3a6e-912">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="b3a6e-912">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="b3a6e-913">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="b3a6e-913">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="b3a6e-914">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="b3a6e-914">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="b3a6e-915">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="b3a6e-915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-916">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-916">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-917">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-917">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b3a6e-918">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-918">Az.Storage</span></span>
* <span data-ttu-id="b3a6e-919">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b3a6e-919">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="b3a6e-920">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b3a6e-920">New-AzStorageContext</span></span>
* <span data-ttu-id="b3a6e-921">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="b3a6e-921">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="b3a6e-922">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b3a6e-922">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b3a6e-923">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b3a6e-923">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b3a6e-924">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-924">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="b3a6e-925">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-925">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="b3a6e-926">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="b3a6e-926">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="b3a6e-927">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b3a6e-927">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b3a6e-928">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b3a6e-928">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b3a6e-929">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b3a6e-929">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="b3a6e-930">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b3a6e-930">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="b3a6e-931">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="b3a6e-931">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b3a6e-932">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="b3a6e-932">Highlights since the last major release</span></span>
* <span data-ttu-id="b3a6e-933">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="b3a6e-933">General availability of `Az` module</span></span>
* <span data-ttu-id="b3a6e-934">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b3a6e-934">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b3a6e-935">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b3a6e-935">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b3a6e-936">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-936">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b3a6e-937">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="b3a6e-937">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b3a6e-938">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-938">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b3a6e-939">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="b3a6e-939">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b3a6e-940">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-940">Az.Automation</span></span>
* <span data-ttu-id="b3a6e-941">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-941">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="b3a6e-942">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="b3a6e-942">Dynamic grouping</span></span>
    * <span data-ttu-id="b3a6e-943">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-943">Pre-Post script</span></span>
    * <span data-ttu-id="b3a6e-944">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="b3a6e-944">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-945">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-945">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-946">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="b3a6e-946">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="b3a6e-947">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-947">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b3a6e-948">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b3a6e-948">Az.KeyVault</span></span>
* <span data-ttu-id="b3a6e-949">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="b3a6e-949">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-950">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-950">Az.Network</span></span>
* <span data-ttu-id="b3a6e-951">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="b3a6e-951">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="b3a6e-952">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="b3a6e-952">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b3a6e-953">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-953">Az.RecoveryServices</span></span>
* <span data-ttu-id="b3a6e-954">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="b3a6e-954">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="b3a6e-955">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="b3a6e-955">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-956">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-957">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b3a6e-957">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="b3a6e-958">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="b3a6e-958">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-959">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-959">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-960">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-960">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b3a6e-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-961">Az.Storage</span></span>
* <span data-ttu-id="b3a6e-962">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-962">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="b3a6e-963">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-963">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b3a6e-964">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-964">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b3a6e-965">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-965">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b3a6e-966">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="b3a6e-966">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="b3a6e-967">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="b3a6e-967">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="b3a6e-968">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="b3a6e-968">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b3a6e-969">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b3a6e-969">Az.Websites</span></span>
* <span data-ttu-id="b3a6e-970">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-970">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="b3a6e-971">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="b3a6e-971">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b3a6e-972">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-972">Az.Accounts</span></span>
* <span data-ttu-id="b3a6e-973">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="b3a6e-973">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="b3a6e-974">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="b3a6e-974">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b3a6e-975">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-975">Az.Automation</span></span>
* <span data-ttu-id="b3a6e-976">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-976">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="b3a6e-977">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-977">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="b3a6e-978">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="b3a6e-978">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b3a6e-979">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b3a6e-979">Az.Cdn</span></span>
* <span data-ttu-id="b3a6e-980">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="b3a6e-980">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-981">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-982">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="b3a6e-982">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b3a6e-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b3a6e-983">Az.DataFactory</span></span>
* <span data-ttu-id="b3a6e-984">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="b3a6e-984">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b3a6e-985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b3a6e-985">Az.LogicApp</span></span>
* <span data-ttu-id="b3a6e-986">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="b3a6e-986">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-987">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-987">Az.Network</span></span>
* <span data-ttu-id="b3a6e-988">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="b3a6e-988">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b3a6e-989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-989">Az.RecoveryServices</span></span>
* <span data-ttu-id="b3a6e-990">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b3a6e-990">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="b3a6e-991">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="b3a6e-991">SDK Update</span></span>
* <span data-ttu-id="b3a6e-992">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b3a6e-992">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="b3a6e-993">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b3a6e-993">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-994">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-995">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="b3a6e-995">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="b3a6e-996">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="b3a6e-996">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="b3a6e-997">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="b3a6e-997">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="b3a6e-998">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="b3a6e-998">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="b3a6e-999">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="b3a6e-999">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="b3a6e-1000">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1000">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-1001">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1001">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-1002">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1002">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="b3a6e-1003">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1003">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b3a6e-1004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1004">Az.Storage</span></span>
* <span data-ttu-id="b3a6e-1005">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1005">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="b3a6e-1006">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1006">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="b3a6e-1007">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1007">Az.AnalysisServices</span></span>
* <span data-ttu-id="b3a6e-1008">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1008">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b3a6e-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1009">Az.Automation</span></span>
* <span data-ttu-id="b3a6e-1010">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1010">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="b3a6e-1011">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1011">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="b3a6e-1012">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1012">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b3a6e-1013">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1013">Az.CognitiveServices</span></span>
* <span data-ttu-id="b3a6e-1014">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1014">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1015">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-1016">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1016">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="b3a6e-1017">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1017">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="b3a6e-1018">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1018">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="b3a6e-1019">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1019">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b3a6e-1020">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1020">Az.DataLakeStore</span></span>
* <span data-ttu-id="b3a6e-1021">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1021">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b3a6e-1022">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1022">Az.EventHub</span></span>
* <span data-ttu-id="b3a6e-1023">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1023">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="b3a6e-1024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1024">Az.KeyVault</span></span>
* <span data-ttu-id="b3a6e-1025">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1025">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b3a6e-1026">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1026">Az.LogicApp</span></span>
* <span data-ttu-id="b3a6e-1027">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1027">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="b3a6e-1028">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1028">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="b3a6e-1029">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1029">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="b3a6e-1030">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1030">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b3a6e-1031">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1031">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b3a6e-1032">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1032">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b3a6e-1033">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1033">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="b3a6e-1034">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1034">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="b3a6e-1035">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1035">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b3a6e-1036">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1036">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b3a6e-1037">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1037">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b3a6e-1038">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1038">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="b3a6e-1039">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1039">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b3a6e-1040">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1040">Az.Monitor</span></span>
* <span data-ttu-id="b3a6e-1041">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1041">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-1042">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1042">Az.Network</span></span>
* <span data-ttu-id="b3a6e-1043">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1043">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b3a6e-1044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1044">Az.OperationalInsights</span></span>
* <span data-ttu-id="b3a6e-1045">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1045">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="b3a6e-1046">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1046">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="b3a6e-1047">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1047">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="b3a6e-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1048">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-1049">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1049">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b3a6e-1050">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1050">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="b3a6e-1051">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="b3a6e-1052">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1052">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1053">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-1054">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1054">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="b3a6e-1055">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1055">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b3a6e-1056">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1056">Az.Websites</span></span>
* <span data-ttu-id="b3a6e-1057">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1057">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="b3a6e-1058">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1058">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b3a6e-1059">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1059">Az.Accounts</span></span>
* <span data-ttu-id="b3a6e-1060">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1060">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b3a6e-1061">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1061">Az.AnalysisServices</span></span>
<span data-ttu-id="b3a6e-1062">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1062">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-1063">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1063">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-1064">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1064">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="b3a6e-1065">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1065">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="b3a6e-1066">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1066">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b3a6e-1067">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1067">Az.RecoveryServices</span></span>
<span data-ttu-id="b3a6e-1068">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1068">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-1069">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1069">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-1070">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1070">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="b3a6e-1071">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1071">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b3a6e-1072">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1072">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="b3a6e-1073">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1073">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-1074">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1074">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-1075">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1075">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="b3a6e-1076">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1076">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="b3a6e-1077">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1077">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="b3a6e-1078">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1078">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b3a6e-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1079">Az.Accounts</span></span>
* <span data-ttu-id="b3a6e-1080">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1080">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b3a6e-1081">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1081">Az.AnalysisServices</span></span>
* <span data-ttu-id="b3a6e-1082">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1082">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b3a6e-1083">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1083">Az.RecoveryServices</span></span>
* <span data-ttu-id="b3a6e-1084">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1084">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="b3a6e-1085">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1085">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b3a6e-1086">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1086">Az.Accounts</span></span>
* <span data-ttu-id="b3a6e-1087">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1087">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b3a6e-1088">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1088">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b3a6e-1089">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1089">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="b3a6e-1090">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1090">Az.Aks</span></span>
* <span data-ttu-id="b3a6e-1091">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1091">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b3a6e-1092">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1092">Az.Automation</span></span>
* <span data-ttu-id="b3a6e-1093">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1093">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="b3a6e-1094">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1094">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b3a6e-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1095">Az.Cdn</span></span>
* <span data-ttu-id="b3a6e-1096">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1096">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1097">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-1098">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1098">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="b3a6e-1099">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1099">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="b3a6e-1100">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1100">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b3a6e-1101">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1101">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b3a6e-1102">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1102">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b3a6e-1103">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1103">Az.DataFactory</span></span>
* <span data-ttu-id="b3a6e-1104">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1104">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b3a6e-1105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1105">Az.DataLakeStore</span></span>
* <span data-ttu-id="b3a6e-1106">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1106">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="b3a6e-1107">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1107">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="b3a6e-1108">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1108">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b3a6e-1109">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1109">Az.IotHub</span></span>
* <span data-ttu-id="b3a6e-1110">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1110">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b3a6e-1111">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1111">Az.KeyVault</span></span>
* <span data-ttu-id="b3a6e-1112">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1112">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-1113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1113">Az.Network</span></span>
* <span data-ttu-id="b3a6e-1114">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1114">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1115">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-1116">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1116">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="b3a6e-1117">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1117">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="b3a6e-1118">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1118">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="b3a6e-1119">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1119">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="b3a6e-1120">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1120">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="b3a6e-1121">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1121">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="b3a6e-1122">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1122">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b3a6e-1123">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1123">Az.ServiceFabric</span></span>
* <span data-ttu-id="b3a6e-1124">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1124">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="b3a6e-1125">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1125">Fix some error messages.</span></span>
* <span data-ttu-id="b3a6e-1126">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1126">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="b3a6e-1127">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1127">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b3a6e-1128">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1128">Az.SignalR</span></span>
* <span data-ttu-id="b3a6e-1129">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1129">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-1130">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1130">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-1131">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1131">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b3a6e-1132">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1132">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="b3a6e-1133">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1133">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="b3a6e-1134">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1134">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b3a6e-1135">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1135">Az.Storage</span></span>
* <span data-ttu-id="b3a6e-1136">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1136">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b3a6e-1137">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1137">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="b3a6e-1138">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1138">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="b3a6e-1139">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1139">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="b3a6e-1140">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1140">Az.TrafficManager</span></span>
* <span data-ttu-id="b3a6e-1141">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1141">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b3a6e-1142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1142">Az.Websites</span></span>
* <span data-ttu-id="b3a6e-1143">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1143">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b3a6e-1144">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1144">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="b3a6e-1145">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1145">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="b3a6e-1146">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1146">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b3a6e-1147">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1147">Az.Accounts</span></span>
* <span data-ttu-id="b3a6e-1148">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1148">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-1149">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1149">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-1150">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1150">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="b3a6e-1151">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1151">Updated the description of ID in help files</span></span>
* <span data-ttu-id="b3a6e-1152">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1152">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b3a6e-1153">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1153">Az.DataLakeStore</span></span>
* <span data-ttu-id="b3a6e-1154">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1154">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="b3a6e-1155">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1155">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b3a6e-1156">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1156">Az.EventGrid</span></span>
* <span data-ttu-id="b3a6e-1157">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1157">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="b3a6e-1158">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1158">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="b3a6e-1159">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1159">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b3a6e-1160">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1160">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b3a6e-1161">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1161">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b3a6e-1162">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1162">Dead letter endpoint.</span></span>
    - <span data-ttu-id="b3a6e-1163">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1163">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b3a6e-1164">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1164">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b3a6e-1165">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1165">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b3a6e-1166">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1166">Dead letter endpoint.</span></span>
* <span data-ttu-id="b3a6e-1167">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1167">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="b3a6e-1168">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1168">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b3a6e-1169">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1169">Az.IotHub</span></span>
* <span data-ttu-id="b3a6e-1170">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1170">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b3a6e-1171">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1171">Az.LogicApp</span></span>
* <span data-ttu-id="b3a6e-1172">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1172">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-1173">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1173">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-1174">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1174">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="b3a6e-1175">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1175">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="b3a6e-1176">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1176">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b3a6e-1177">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1177">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="b3a6e-1178">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1178">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="b3a6e-1179">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1179">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b3a6e-1180">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1180">Az.SignalR</span></span>
* <span data-ttu-id="b3a6e-1181">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1181">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-1182">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1182">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-1183">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1183">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b3a6e-1184">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1184">Az.Storage</span></span>
* <span data-ttu-id="b3a6e-1185">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1185">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="b3a6e-1186">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1186">New-AzStorageContext</span></span>
* <span data-ttu-id="b3a6e-1187">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1187">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="b3a6e-1188">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1188">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b3a6e-1189">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1189">Az.Websites</span></span>
* <span data-ttu-id="b3a6e-1190">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1190">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="b3a6e-1191">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1191">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="b3a6e-1192">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1192">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="b3a6e-1193">Ogólne</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1193">General</span></span>

- <span data-ttu-id="b3a6e-1194">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1194">General Availability of Az Module</span></span>
- <span data-ttu-id="b3a6e-1195">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1195">Online help for each module</span></span>
- <span data-ttu-id="b3a6e-1196">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1196">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="b3a6e-1197">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1197">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="b3a6e-1198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1198">Az.Accounts</span></span>
- <span data-ttu-id="b3a6e-1199">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1199">Changed from Az.Profile</span></span>
- <span data-ttu-id="b3a6e-1200">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1200">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b3a6e-1201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1201">Az.ApiManagement</span></span>
- <span data-ttu-id="b3a6e-1202">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1202">Fixes for #7002</span></span>
- <span data-ttu-id="b3a6e-1203">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1203">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="b3a6e-1204">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1204">Az.Batch</span></span>
- <span data-ttu-id="b3a6e-1205">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1205">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="b3a6e-1206">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1206">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="b3a6e-1207">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="b3a6e-1208">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1208">Az.Billing</span></span>
- <span data-ttu-id="b3a6e-1209">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1209">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="b3a6e-1210">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1210">Az.CognitivServices</span></span>
- <span data-ttu-id="b3a6e-1211">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1211">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="b3a6e-1212">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1212">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b3a6e-1213">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1213">Az.ContainerInstance</span></span>
- <span data-ttu-id="b3a6e-1214">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1214">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="b3a6e-1215">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1215">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="b3a6e-1216">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1216">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b3a6e-1217">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1217">Az.DataLakeStore</span></span>
- <span data-ttu-id="b3a6e-1218">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="b3a6e-1219">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1219">Az.Monitor</span></span>
- <span data-ttu-id="b3a6e-1220">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1220">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="b3a6e-1221">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1221">Az.KeyVault</span></span>
- <span data-ttu-id="b3a6e-1222">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1222">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="b3a6e-1223">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1223">Az.MachineLearning</span></span>
- <span data-ttu-id="b3a6e-1224">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1224">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="b3a6e-1225">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1225">Az.Media</span></span>
- <span data-ttu-id="b3a6e-1226">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1226">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b3a6e-1227">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1227">Az.Network</span></span>
<span data-ttu-id="b3a6e-1228">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1228">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="b3a6e-1229">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1229">New cmdlets added:</span></span>
        - <span data-ttu-id="b3a6e-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b3a6e-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b3a6e-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b3a6e-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b3a6e-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b3a6e-1235">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1235">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="b3a6e-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="b3a6e-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="b3a6e-1238">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1238">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="b3a6e-1239">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1239">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="b3a6e-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b3a6e-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b3a6e-1242">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1242">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="b3a6e-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="b3a6e-1244">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1244">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="b3a6e-1245">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1245">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="b3a6e-1246">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1246">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b3a6e-1247">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1247">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b3a6e-1248">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1248">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="b3a6e-1249">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1249">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="b3a6e-1250">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1250">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="b3a6e-1251">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1251">Az.OperationalInsights</span></span>
- <span data-ttu-id="b3a6e-1252">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="b3a6e-1253">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1253">Az.Profile</span></span>
- <span data-ttu-id="b3a6e-1254">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1254">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b3a6e-1255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1255">Az.RecoveryServices</span></span>
- <span data-ttu-id="b3a6e-1256">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1256">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="b3a6e-1257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1257">Az.Resources</span></span>
- <span data-ttu-id="b3a6e-1258">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b3a6e-1259">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1259">Az.ServiceFabric</span></span>
- <span data-ttu-id="b3a6e-1260">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1260">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="b3a6e-1261">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1261">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="b3a6e-1262">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1262">Az.SIgnalR</span></span>
- <span data-ttu-id="b3a6e-1263">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1263">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="b3a6e-1264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1264">Az.Sql</span></span>
- <span data-ttu-id="b3a6e-1265">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1265">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="b3a6e-1266">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1266">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="b3a6e-1267">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1267">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="b3a6e-1268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1268">Az.Storage</span></span>
- <span data-ttu-id="b3a6e-1269">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b3a6e-1270">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1270">Az.Websites</span></span>
- <span data-ttu-id="b3a6e-1271">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="b3a6e-1272">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1272">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="b3a6e-1273">Ogólne</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1273">General</span></span>

* <span data-ttu-id="b3a6e-1274">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1274">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="b3a6e-1275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1275">Az.Compute</span></span>

* <span data-ttu-id="b3a6e-1276">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1276">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b3a6e-1277">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1277">Az.DataLakeStore</span></span>

* <span data-ttu-id="b3a6e-1278">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1278">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="b3a6e-1279">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1279">Az.FrontDoor</span></span>

* <span data-ttu-id="b3a6e-1280">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1280">Fixed some broken links</span></span>
    - <span data-ttu-id="b3a6e-1281">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1281">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="b3a6e-1282">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1282">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b3a6e-1283">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1283">Az.RecoveryServices</span></span>

* <span data-ttu-id="b3a6e-1284">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1284">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="b3a6e-1285">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1285">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="b3a6e-1286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1286">Az.Resources</span></span>

* <span data-ttu-id="b3a6e-1287">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1287">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="b3a6e-1288">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1288">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="b3a6e-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1289">Az.Sql</span></span>

* <span data-ttu-id="b3a6e-1290">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1290">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="b3a6e-1291">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1291">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="b3a6e-1292">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1292">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="b3a6e-1293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1293">Az.Storage</span></span>

* <span data-ttu-id="b3a6e-1294">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1294">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="b3a6e-1295">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1295">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="b3a6e-1296">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1296">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b3a6e-1297">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1297">Support Static Website configuration</span></span>
    - <span data-ttu-id="b3a6e-1298">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1298">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="b3a6e-1299">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1299">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b3a6e-1300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1300">Az.Websites</span></span>

* <span data-ttu-id="b3a6e-1301">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1301">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="b3a6e-1302">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1302">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="b3a6e-1303">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1303">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="b3a6e-1304">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1304">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b3a6e-1305">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1305">Az.ApiManagement</span></span>
* <span data-ttu-id="b3a6e-1306">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1306">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="b3a6e-1307">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1307">Az.Automation</span></span>
* <span data-ttu-id="b3a6e-1308">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1308">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="b3a6e-1309">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1309">Added Update Management cmdlets</span></span>
* <span data-ttu-id="b3a6e-1310">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1310">Added Source Control cmdlets</span></span>
* <span data-ttu-id="b3a6e-1311">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1311">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="b3a6e-1312">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1312">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="b3a6e-1313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1313">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-1314">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1314">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="b3a6e-1315">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1315">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b3a6e-1316">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1316">Az.ContainerInstance</span></span>
* <span data-ttu-id="b3a6e-1317">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1317">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="b3a6e-1318">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1318">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b3a6e-1319">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1319">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b3a6e-1320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1320">Az.Network</span></span>
* <span data-ttu-id="b3a6e-1321">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1321">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="b3a6e-1322">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1322">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="b3a6e-1323">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1323">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="b3a6e-1324">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1324">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="b3a6e-1325">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1325">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b3a6e-1326">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1326">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="b3a6e-1327">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1327">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="b3a6e-1328">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1328">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b3a6e-1329">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1329">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="b3a6e-1330">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1330">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="b3a6e-1331">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1331">Az.Relay</span></span>
* <span data-ttu-id="b3a6e-1332">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1332">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="b3a6e-1333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1333">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-1334">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1334">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="b3a6e-1335">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1335">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="b3a6e-1336">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1336">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b3a6e-1337">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1337">Az.ServiceFabric</span></span>
* <span data-ttu-id="b3a6e-1338">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1338">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="b3a6e-1339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1339">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-1340">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1340">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="b3a6e-1341">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1341">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b3a6e-1342">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1342">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b3a6e-1343">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1343">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b3a6e-1344">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1344">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b3a6e-1345">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1345">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b3a6e-1346">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1346">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b3a6e-1347">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1347">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b3a6e-1348">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1348">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="b3a6e-1349">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1349">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="b3a6e-1350">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1350">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="b3a6e-1351">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1351">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="b3a6e-1352">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1352">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b3a6e-1353">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1353">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b3a6e-1354">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1354">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="b3a6e-1355">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1355">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="b3a6e-1356">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1356">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="b3a6e-1357">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1357">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b3a6e-1358">Ogólne</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1358">General</span></span>
* <span data-ttu-id="b3a6e-1359">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1359">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="b3a6e-1360">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1360">Az.Profile</span></span>
* <span data-ttu-id="b3a6e-1361">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1361">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="b3a6e-1362">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1362">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="b3a6e-1363">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1363">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="b3a6e-1364">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1364">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="b3a6e-1365">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1365">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="b3a6e-1366">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1366">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="b3a6e-1367">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1367">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="b3a6e-1368">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1368">Az.CognitiveServices</span></span>
* <span data-ttu-id="b3a6e-1369">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1369">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-1370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1370">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-1371">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1371">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="b3a6e-1372">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1372">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="b3a6e-1373">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1373">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b3a6e-1374">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1374">Az.DataLakeStore</span></span>
* <span data-ttu-id="b3a6e-1375">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1375">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="b3a6e-1376">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1376">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="b3a6e-1377">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1377">Az.Insights</span></span>
* <span data-ttu-id="b3a6e-1378">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1378">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="b3a6e-1379">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1379">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="b3a6e-1380">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1380">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="b3a6e-1381">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1381">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-1382">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1382">Az.Network</span></span>
* <span data-ttu-id="b3a6e-1383">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1383">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="b3a6e-1384">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1384">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="b3a6e-1385">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1385">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="b3a6e-1386">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1386">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="b3a6e-1387">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1387">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b3a6e-1388">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1388">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b3a6e-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b3a6e-1390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1390">Az.PolicyInsights</span></span>
* <span data-ttu-id="b3a6e-1391">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1391">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-1392">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1392">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-1393">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1393">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="b3a6e-1394">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1394">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b3a6e-1395">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1395">Az.ServiceBus</span></span>
* <span data-ttu-id="b3a6e-1396">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1396">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b3a6e-1397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1397">Az.ServiceFabric</span></span>
* <span data-ttu-id="b3a6e-1398">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1398">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="b3a6e-1399">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1399">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="b3a6e-1400">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1400">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="b3a6e-1401">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1401">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="b3a6e-1402">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1402">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="b3a6e-1403">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1403">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="b3a6e-1404">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1404">Az.Profile</span></span>
* <span data-ttu-id="b3a6e-1405">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1405">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="b3a6e-1406">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1406">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-1407">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1407">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-1408">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1408">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="b3a6e-1409">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1409">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b3a6e-1410">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1410">Az.DataLakeStore</span></span>
* <span data-ttu-id="b3a6e-1411">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1411">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="b3a6e-1412">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1412">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="b3a6e-1413">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1413">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b3a6e-1414">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1414">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b3a6e-1415">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1415">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1416">Az.Network</span></span>
* <span data-ttu-id="b3a6e-1417">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1417">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="b3a6e-1418">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1418">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-1419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1419">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-1420">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1420">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="b3a6e-1421">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1421">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="b3a6e-1422">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1422">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="b3a6e-1423">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1423">Azure.Storage</span></span>
* <span data-ttu-id="b3a6e-1424">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1424">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="b3a6e-1425">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1425">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="b3a6e-1426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b3a6e-1427">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1427">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="b3a6e-1428">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1428">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="b3a6e-1429">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1429">Az.CognitiveServices</span></span>
* <span data-ttu-id="b3a6e-1430">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1430">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b3a6e-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1431">Az.Compute</span></span>
* <span data-ttu-id="b3a6e-1432">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1432">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="b3a6e-1433">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1433">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="b3a6e-1434">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1434">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="b3a6e-1435">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1435">Az.DataFactoryV2</span></span>
* <span data-ttu-id="b3a6e-1436">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1436">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b3a6e-1437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1437">Az.Network</span></span>
* <span data-ttu-id="b3a6e-1438">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1438">Added NetworkProfile functionality.</span></span> <span data-ttu-id="b3a6e-1439">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1439">new cmdlets added</span></span>
    - <span data-ttu-id="b3a6e-1440">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1440">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="b3a6e-1441">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1441">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="b3a6e-1442">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1442">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="b3a6e-1443">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1443">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="b3a6e-1444">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1444">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="b3a6e-1445">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1445">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="b3a6e-1446">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1446">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="b3a6e-1447">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1447">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="b3a6e-1448">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1448">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b3a6e-1449">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1449">Az.RedisCache</span></span>
* <span data-ttu-id="b3a6e-1450">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1450">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="b3a6e-1451">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1451">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="b3a6e-1452">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1452">Az.Resources</span></span>
* <span data-ttu-id="b3a6e-1453">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1453">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b3a6e-1454">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1454">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="b3a6e-1455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1455">Az.Sql</span></span>
* <span data-ttu-id="b3a6e-1456">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1456">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b3a6e-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1457">Az.Websites</span></span>
* <span data-ttu-id="b3a6e-1458">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1458">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="b3a6e-1459">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1459">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="b3a6e-1460">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1460">0.2.0 - September 2018</span></span>
 <span data-ttu-id="b3a6e-1461">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="b3a6e-1461">Initial Release</span></span>