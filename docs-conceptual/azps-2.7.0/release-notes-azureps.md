---
title: Informacje o wersji programu Azure PowerShell
description: Uzyskaj informacje na temat wszystkich najnowszych aktualizacji modułów programu Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/25/2019
ms.openlocfilehash: b879d970d3237098e481dba0419ee65efa8d51cd
ms.sourcegitcommit: f0f09eee03ef9dd7fe07432252a3dc8ca93e3a7b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "71319310"
---
## <a name="270---september-2019"></a><span data-ttu-id="00f9f-103">2.7.0 — wrzesień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-103">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="00f9f-104">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="00f9f-104">Az.ApiManagement</span></span>
* <span data-ttu-id="00f9f-105">Aktualizacja opisu parametru „-Format” w dokumentacji referencyjnej polecenia „Set-AzApiManagementPolicy”</span><span class="sxs-lookup"><span data-stu-id="00f9f-105">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="00f9f-106">Usunięto z dokumentacji referencyjnej odwołania do przestarzałego polecenia cmdlet „Update-AzApiManagementDeployment”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-106">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="00f9f-107">Zamiast niego należy używać polecenia „Set-AzApiManagement”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-107">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="00f9f-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="00f9f-108">Az.Automation</span></span>
* <span data-ttu-id="00f9f-109">Poprawiono literówkę w przykładzie w dokumentacji referencyjnej polecenia „Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="00f9f-109">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="00f9f-110">Dodano wyjaśnienie dotyczące ograniczeń systemu operacyjnego dla polecenia Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="00f9f-110">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="00f9f-111">Naprawiono wyjątek odwołania o wartości null dla opcji -Wait polecenia cmdlet Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="00f9f-111">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-112">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-112">Az.Compute</span></span>
* <span data-ttu-id="00f9f-113">Dodanie parametru UploadSizeInBytes do polecenia New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-113">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="00f9f-114">Dodanie parametru Incremental do polecenia New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-114">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="00f9f-115">Dodanie funkcji maszyny wirtualnej o niskim priorytecie:</span><span class="sxs-lookup"><span data-stu-id="00f9f-115">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="00f9f-116">do polecenia New-AzVMConfig dodano parametry MaxPrice, EvictionPolicy i Priority.</span><span class="sxs-lookup"><span data-stu-id="00f9f-116">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="00f9f-117">Parametr MaxPrice został dodany do poleceń cmdlet New-AzVmssConfig, Update-AzVM i Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="00f9f-117">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="00f9f-118">Rozwiązanie problemu z odwołaniem do maszyny wirtualnej dla polecenia cmdlet Get-AzAvailabilitySet, gdy wyświetla listę wszystkich zestawów dostępności w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="00f9f-118">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="00f9f-119">Naprawienie wyjątku o wartości null dla polecenia Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="00f9f-119">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="00f9f-120">Naprawienie metody przeszukiwania wirtualnego dysku twardego dla pozycji względem końca.</span><span class="sxs-lookup"><span data-stu-id="00f9f-120">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="00f9f-121">Rozwiązanie problemu z dyskami UltraSSD dla poleceń New-AzVM i Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="00f9f-121">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="00f9f-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="00f9f-122">Az.DataFactory</span></span>
* <span data-ttu-id="00f9f-123">Dodanie 3 nowych poleceń do usługi ADF w wersji 2 — Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription i Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="00f9f-123">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="00f9f-124">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.3</span><span class="sxs-lookup"><span data-stu-id="00f9f-124">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="00f9f-125">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="00f9f-125">Az.HDInsight</span></span>
* <span data-ttu-id="00f9f-126">Wywołanie zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="00f9f-126">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="00f9f-127">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="00f9f-127">Az.IotHub</span></span>
* <span data-ttu-id="00f9f-128">Dodanie obsługi w celu wywołania trybu failover dla usługi IotHub do sparowanego geograficznie regionu odzyskiwania po awarii.</span><span class="sxs-lookup"><span data-stu-id="00f9f-128">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="00f9f-129">Dodanie obsługi do zarządzania wzbogacaniem komunikatów dla usługi IotHub.</span><span class="sxs-lookup"><span data-stu-id="00f9f-129">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="00f9f-130">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="00f9f-130">New cmdlets are:</span></span>
    - <span data-ttu-id="00f9f-131">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="00f9f-131">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="00f9f-132">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="00f9f-132">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="00f9f-133">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="00f9f-133">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="00f9f-134">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="00f9f-134">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="00f9f-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="00f9f-135">Az.Monitor</span></span>
* <span data-ttu-id="00f9f-136">Wskazanie najnowszego zestawu Monitor SDK, tj. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="00f9f-136">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="00f9f-137">Dodaje zmiany niepowodujące niezgodności do poleceń cmdlet metryk, tj. wyliczenie Unit obsługuje kilka nowych wartości.</span><span class="sxs-lookup"><span data-stu-id="00f9f-137">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="00f9f-138">Są to polecenia cmdlet tylko do odczytu, więc nie będzie żadnych zmian w danych wejściowych tych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00f9f-138">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="00f9f-139">Wartość api-version żądań **ActionGroups** to teraz **2019-06-01**, wcześniej było to **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="00f9f-139">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="00f9f-140">Testy scenariusza zostały zaktualizowane w celu dostosowania do tej zmiany.</span><span class="sxs-lookup"><span data-stu-id="00f9f-140">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="00f9f-141">Konstruktory dla klas **EmailReceiver** i **WebhookReceiver** dodały jeden nowy argument obowiązkowy, tj. wartość logiczną o nazwie **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="00f9f-141">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="00f9f-142">Obecnie wartość ta jest stała i równa **false**, aby ukryć tę zmianę powodującą niezgodność przed poleceniami cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00f9f-142">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="00f9f-143">**UWAGA**: Jest to tymczasowa zmiana, która musi być zweryfikowana przez zespół ds. alertów.</span><span class="sxs-lookup"><span data-stu-id="00f9f-143">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="00f9f-144">Kolejność argumentów konstruktora klasy **Source** (powiązanej z klasą **ScheduledQueryRuleSource**) zmieniła się od poprzedniego zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="00f9f-144">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="00f9f-145">Ta zmiana wymaga naprawienia dwóch testów jednostkowych: kompilowały się, ale nie przechodziły testów.</span><span class="sxs-lookup"><span data-stu-id="00f9f-145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="00f9f-146">Kolejność argumentów konstruktora klasy **AlertingAction** (powiązanej z klasą **ScheduledQueryRuleSource**) została zmieniona od poprzedniego zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="00f9f-146">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="00f9f-147">Ta zmiana wymaga naprawienia dwóch testów jednostkowych: kompilowały się, ale nie przechodziły testów.</span><span class="sxs-lookup"><span data-stu-id="00f9f-147">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="00f9f-148">Obsługa kryteriów progu dynamicznego dla alertu metryki w wersji 2</span><span class="sxs-lookup"><span data-stu-id="00f9f-148">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="00f9f-149">New-AzMetricAlertRuleV2Criteria: teraz tworzy kryteria progów dynamicznych</span><span class="sxs-lookup"><span data-stu-id="00f9f-149">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="00f9f-150">Add-AzMetricAlertRuleV2: teraz akceptuje kryteria progów dynamicznych</span><span class="sxs-lookup"><span data-stu-id="00f9f-150">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="00f9f-151">Ulepszenia poleceń cmdlet reguły zaplanowanego zapytania (SQR)</span><span class="sxs-lookup"><span data-stu-id="00f9f-151">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="00f9f-152">Polecenia cmdlet będą akceptować parametr „Location” w obu formatach: jako lokalizację (np. eastus) i jako nazwę wyświetlaną lokalizacji (np. East US)</span><span class="sxs-lookup"><span data-stu-id="00f9f-152">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="00f9f-153">Poprawnie zilustrowano parametr „Enabled” w plikach pomocy</span><span class="sxs-lookup"><span data-stu-id="00f9f-153">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="00f9f-154">Dodano przykłady dla opcjonalnego parametru „ActionGroup”</span><span class="sxs-lookup"><span data-stu-id="00f9f-154">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="00f9f-155">Ogólnie ulepszono pliki pomocy</span><span class="sxs-lookup"><span data-stu-id="00f9f-155">Overall improved help files</span></span>
* <span data-ttu-id="00f9f-156">Naprawienie usterki dotyczącej określania typu zakresu dla polecenia „Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="00f9f-156">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-157">Az.Network</span></span>
* <span data-ttu-id="00f9f-158">Naprawienie nieprawidłowego przykładu w dokumentacji referencyjnej polecenia „New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="00f9f-158">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="00f9f-159">Dodanie w dokumentacji referencyjnej polecenia „Get-AzNetworkWatcherPacketCapture” uwagi dotyczącej pobierania wszystkich właściwości na potrzeby przechwytywania pakietów</span><span class="sxs-lookup"><span data-stu-id="00f9f-159">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="00f9f-160">Naprawiono przykład w dokumentacji referencyjnej polecenia „Test-AzNetworkWatcherIPFlow”, aby poprawnie wyliczał karty sieciowe</span><span class="sxs-lookup"><span data-stu-id="00f9f-160">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="00f9f-161">Ulepszono analizę wyjątku w chmurze, aby wyświetlane były dodatkowe szczegóły, jeśli są obecne</span><span class="sxs-lookup"><span data-stu-id="00f9f-161">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="00f9f-162">Ulepszono analizę wyjątku w chmurze, aby był obsługiwany dodatkowy typ wyjątku zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="00f9f-162">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="00f9f-163">Naprawiono niepoprawne mapowanie modeli reguł zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="00f9f-163">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="00f9f-164">Dodano właściwości interfejsu sieciowego dla funkcji prywatnego adresu IP</span><span class="sxs-lookup"><span data-stu-id="00f9f-164">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="00f9f-165">Dodano właściwość „PrivateEndpoint” jako typ PSResourceId do elementu PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="00f9f-165">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="00f9f-166">Dodano właściwość „PrivateLinkConnectionProperties” jako typ PSIpConfigurationConnectivityInformation do elementu PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="00f9f-166">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="00f9f-167">Dodano nową klasę modelu PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="00f9f-167">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="00f9f-168">Dodano nowy typ ApplicationRuleProtocolType „mssql” dla zasobu usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="00f9f-168">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="00f9f-169">Obsługa linku wielokrotnego w wirtualnej sieci WAN</span><span class="sxs-lookup"><span data-stu-id="00f9f-169">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="00f9f-170">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="00f9f-170">New cmdlets</span></span>
        - <span data-ttu-id="00f9f-171">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="00f9f-171">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="00f9f-172">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="00f9f-172">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="00f9f-173">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="00f9f-173">Updated cmdlet:</span></span>
        - <span data-ttu-id="00f9f-174">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="00f9f-174">New-VpnSite</span></span>
        - <span data-ttu-id="00f9f-175">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="00f9f-175">Update-VpnSite</span></span>
        - <span data-ttu-id="00f9f-176">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="00f9f-176">New-VpnConnection</span></span>
        - <span data-ttu-id="00f9f-177">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="00f9f-177">Update-VpnConnection</span></span>
* <span data-ttu-id="00f9f-178">Niektóre dokumenty dla przykładów programu PowerShell naprawiono w taki sposób, aby były w nich używane polecenia cmdlet Az zamiast poleceń cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="00f9f-178">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="00f9f-179">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-179">Az.RecoveryServices</span></span>
* <span data-ttu-id="00f9f-180">Aktualizacja obiektu AzureVMpolicy o atrybut ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="00f9f-180">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="00f9f-181">Dodano testy dotyczące zasad maszyny wirtualnej i przywracania oryginalnego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="00f9f-181">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-182">Az.Resources</span></span>
* <span data-ttu-id="00f9f-183">Naprawienie usterki polegającej na tym, że nie można było wywołać polecenia New-AzRoleAssignment bez parametru Scope.</span><span class="sxs-lookup"><span data-stu-id="00f9f-183">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="00f9f-184">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="00f9f-184">Az.ServiceFabric</span></span>
* <span data-ttu-id="00f9f-185">Poprawiono literówkę w przykładzie w dokumentacji referencyjnej polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="00f9f-185">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="00f9f-186">Dodanie nowych poleceń cmdlet do zarządzania aplikacją i usługami:</span><span class="sxs-lookup"><span data-stu-id="00f9f-186">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="00f9f-187">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="00f9f-187">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="00f9f-188">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="00f9f-188">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="00f9f-189">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="00f9f-189">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="00f9f-190">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="00f9f-190">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="00f9f-191">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="00f9f-191">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="00f9f-192">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="00f9f-192">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="00f9f-193">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="00f9f-193">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="00f9f-194">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="00f9f-194">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="00f9f-195">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="00f9f-195">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="00f9f-196">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="00f9f-196">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="00f9f-197">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="00f9f-197">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="00f9f-198">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="00f9f-198">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="00f9f-199">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="00f9f-199">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="00f9f-200">Uaktualniono zestaw Service Fabric SDK do wersji 1.2.0, która korzysta z dostawcy zasobów usługi Service Fabric o wersji interfejsu API 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="00f9f-200">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="00f9f-201">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="00f9f-201">Az.SignalR</span></span>
* <span data-ttu-id="00f9f-202">Dodanie poleceń cmdlet Update, Restart, CheckNameAvailability i GetUsage</span><span class="sxs-lookup"><span data-stu-id="00f9f-202">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-203">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-203">Az.Sql</span></span>
* <span data-ttu-id="00f9f-204">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="00f9f-204">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="00f9f-205">Dodano przykład dla rdzenia wirtualnego do tworzenia elastycznej puli (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="00f9f-205">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="00f9f-206">Usunięcie weryfikacji parametru EmailAddresses i sprawdzania, czy parametr EmailAdmins nie ma wartości false w przypadku, gdy parametr EmailAddresses jest pusty w poleceniach Set-AzSqlServerAdvancedThreatProtectionPolicy i Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="00f9f-206">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="00f9f-207">Włączono usuwanie ustawień inspekcji serwera/bazy danych, gdy istnieje wiele ustawień diagnostycznych włączających kategorię inspekcji.</span><span class="sxs-lookup"><span data-stu-id="00f9f-207">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="00f9f-208">Naprawa weryfikacji adresów e-mail w wielu poleceniach cmdlet do oceny luk w zabezpieczeniach SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting i Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="00f9f-208">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="00f9f-209">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="00f9f-209">Az.Storage</span></span>
* <span data-ttu-id="00f9f-210">Zaktualizowano przykład w dokumentacji referencyjnej dla polecenia „Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="00f9f-210">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="00f9f-211">Obsługa zachowywania w pliku docelowym właściwości SMB pliku źródłowego przy przekazywaniu/pobieraniu pliku platformy Azure (atrybuty pliku, czas utworzenia pliku, czas ostatniego zapisu pliku)</span><span class="sxs-lookup"><span data-stu-id="00f9f-211">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="00f9f-212">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="00f9f-212">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="00f9f-213">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="00f9f-213">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="00f9f-214">Naprawa awarii przekazywania blokowego obiektu blob z właściwościami/metadanymi dla elementu ImmutabilityPolicy z obsługą kontenerów.</span><span class="sxs-lookup"><span data-stu-id="00f9f-214">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="00f9f-215">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="00f9f-215">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="00f9f-216">Obsługa zarządzania udziałami plików platformy Azure za pomocą interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="00f9f-216">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="00f9f-217">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="00f9f-217">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="00f9f-218">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="00f9f-218">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="00f9f-219">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="00f9f-219">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="00f9f-220">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="00f9f-220">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="00f9f-221">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="00f9f-221">Az.Websites</span></span>
* <span data-ttu-id="00f9f-222">Naprawa problemu polegającego na tym, że tagi webapp były usuwane podczas migracji aplikacji do nowej platformy ASP</span><span class="sxs-lookup"><span data-stu-id="00f9f-222">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="00f9f-223">Naprawa polecenia Publish-AzureWebapp w taki sposób, aby działało w systemach Linux i Windows</span><span class="sxs-lookup"><span data-stu-id="00f9f-223">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="00f9f-224">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzWebAppPublishingProfile”</span><span class="sxs-lookup"><span data-stu-id="00f9f-224">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="00f9f-225">2.6.0 — sierpień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-225">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="00f9f-226">Ogólne</span><span class="sxs-lookup"><span data-stu-id="00f9f-226">General</span></span>
* <span data-ttu-id="00f9f-227">Naprawiono różne literówki w wielu modułach</span><span class="sxs-lookup"><span data-stu-id="00f9f-227">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="00f9f-228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-228">Az.Accounts</span></span>
* <span data-ttu-id="00f9f-229">Obsługa pliku MSI przypisanego przez użytkownika w ramach uwierzytelniania usługi Azure Functions (nr 9479)</span><span class="sxs-lookup"><span data-stu-id="00f9f-229">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="00f9f-230">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="00f9f-230">Az.Aks</span></span>
* <span data-ttu-id="00f9f-231">Rozwiązano problem z danymi wyjściowymi polecenia „Get-AzAks”</span><span class="sxs-lookup"><span data-stu-id="00f9f-231">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="00f9f-232">Więcej informacji: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="00f9f-232">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="00f9f-233">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="00f9f-233">Az.ApiManagement</span></span>
* <span data-ttu-id="00f9f-234">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="00f9f-234">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="00f9f-235">Zaktualizowano wersję nuget .net, która nie wymusza ograniczeń dotyczących identyfikatorów productId, apiId, groupId i userId</span><span class="sxs-lookup"><span data-stu-id="00f9f-235">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="00f9f-236">**Get-AzApiManagementProduct** — dodano obsługę wysyłania zapytań dotyczących produktów przy użyciu interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="00f9f-236">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="00f9f-237">**New-AzApiManagementApiRevision** — poprawka rozwiązująca problem polegający na tym, że wartość ApiRevisionDescription nie była ustawiana podczas tworzenia nowej wersji pomocniczej interfejsu API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="00f9f-237">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="00f9f-238">Poprawiono literówkę w modelu „PsApiManagementOAuth2AuthrozationServer” na „PsApiManagementOAuth2AuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="00f9f-238">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="00f9f-239">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="00f9f-239">Az.Batch</span></span>
* <span data-ttu-id="00f9f-240">Poprawiono literówkę w komunikacie pomocy i dokumentacji, zmieniając literę w nazwie systemu Windows na wielką</span><span class="sxs-lookup"><span data-stu-id="00f9f-240">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="00f9f-241">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="00f9f-241">Az.Cdn</span></span>
* <span data-ttu-id="00f9f-242">Poprawiono literówkę w pomocniku konwersji modułu CDN</span><span class="sxs-lookup"><span data-stu-id="00f9f-242">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-243">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-243">Az.Compute</span></span>
* <span data-ttu-id="00f9f-244">Dodanie polecenia VmssId to New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-244">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="00f9f-245">Dodanie parametrów TerminateScheduledEvents i TerminateScheduledEventNotBeforeTimeoutInMinutes do polecenia New-AzVmssConfig and Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="00f9f-245">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="00f9f-246">Dodanie właściwości HyperVGeneration do obiektu obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="00f9f-246">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="00f9f-247">Dodanie funkcji Host i HostGroup</span><span class="sxs-lookup"><span data-stu-id="00f9f-247">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="00f9f-248">Nowe polecenia cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="00f9f-248">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="00f9f-249">Dodano parametr HostId do poleceń New-AzVMConfig i New-AzVM</span><span class="sxs-lookup"><span data-stu-id="00f9f-249">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="00f9f-250">Aktualizacja przykładu w dokumentacji polecenia „Invoke-AzVMRunCommand” w celu użycia poprawnej nazwy parametru</span><span class="sxs-lookup"><span data-stu-id="00f9f-250">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="00f9f-251">Aktualizacja opisu parametru „-VolumeType” w dokumentacji referencyjnej poleceń „Set-AzVMDiskEncryptionExtension” i „Set-AzVmssDiskEncryptionExtension”</span><span class="sxs-lookup"><span data-stu-id="00f9f-251">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="00f9f-252">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="00f9f-252">Az.DataFactory</span></span>
* <span data-ttu-id="00f9f-253">Poprawiono literówkę w poleceniu „New-AzDataFactoryEncryptValue”, zmieniając literę w nazwie systemu Windows na wielką</span><span class="sxs-lookup"><span data-stu-id="00f9f-253">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="00f9f-254">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.2</span><span class="sxs-lookup"><span data-stu-id="00f9f-254">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="00f9f-255">Dodanie parametrów „DataProxyIntegrationRuntimeName”, „DataProxyStagingLinkedServiceName” i „DataProxyStagingPath” dla polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime”, aby umożliwić konfigurowanie własnego środowiska Integration Runtime jako serwera proxy dla środowiska SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="00f9f-255">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="00f9f-256">Zaktualizowano PSTriggerRun na potrzeby wyświetlania wyzwalanych potoków, komunikatów i właściwości, a także PSActivityRun na potrzeby wyświetlania typu działania</span><span class="sxs-lookup"><span data-stu-id="00f9f-256">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="00f9f-257">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="00f9f-257">Az.DataLakeStore</span></span>
* <span data-ttu-id="00f9f-258">Poprawiono wysunięcie polecenia Get-DataLakeStoreDeletedItem pod kątem obsługi błędów lub wyjątków zdalnych.</span><span class="sxs-lookup"><span data-stu-id="00f9f-258">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="00f9f-259">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="00f9f-259">Az.EventHub</span></span>
* <span data-ttu-id="00f9f-260">Rozwiązano problem nr 9658: Literówka VirtualNteworkRule w poleceniu Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="00f9f-260">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="00f9f-261">Rozwiązano problem nr 9558: Polecenie Set-AzEventHubNamespace używa elementu PATCH zamiast PUT</span><span class="sxs-lookup"><span data-stu-id="00f9f-261">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="00f9f-262">dodano parametr EnableKafka do polecenia cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="00f9f-262">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="00f9f-263">Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania</span><span class="sxs-lookup"><span data-stu-id="00f9f-263">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="00f9f-264">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="00f9f-264">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="00f9f-265">Poprawiono literówkę w dokumentacji: „Azure” rozpoczynające się małą literą</span><span class="sxs-lookup"><span data-stu-id="00f9f-265">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="00f9f-266">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="00f9f-266">Az.Monitor</span></span>
* <span data-ttu-id="00f9f-267">Poprawiono niepoprawną nazwę parametru w dokumentacji pomocy</span><span class="sxs-lookup"><span data-stu-id="00f9f-267">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-268">Az.Network</span></span>
* <span data-ttu-id="00f9f-269">Zaktualizowano polecenie New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-269">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="00f9f-270">Sklasyfikowano parametr „PublicIpAddress” jako przestarzały, ponieważ nie jest on nigdy używany po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="00f9f-270">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="00f9f-271">Dodano jeden opcjonalny parametr „Primary” wskazujący, czy bieżąca konfiguracja IP jest podstawowa, czy nie.</span><span class="sxs-lookup"><span data-stu-id="00f9f-271">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="00f9f-272">Ulepszono obsługę wyjątku błędu żądania z zestawu SDK — rozwiązuje to problem polegający na tym, że poprzednio wyjątki zestawu SDK nie były poprawnie obsługiwane, wskutek czego nie były wyświetlane kluczowe szczegóły błędu</span><span class="sxs-lookup"><span data-stu-id="00f9f-272">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="00f9f-273">Skorygowano logikę weryfikacji prefiksu IP w wersji IPv6 w celu sprawdzania, czy długość prefiksu IPv6 jest poprawna.</span><span class="sxs-lookup"><span data-stu-id="00f9f-273">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="00f9f-274">Zaktualizowano polecenie Get-AzVirtualNetworkSubnetConfig: Dodano parametr ustawiany w celu pobrania identyfikatora zasobu podsieci.</span><span class="sxs-lookup"><span data-stu-id="00f9f-274">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="00f9f-275">Zaktualizowano opis parametru Location dla AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="00f9f-275">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="00f9f-276">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="00f9f-276">Az.OperationalInsights</span></span>
* <span data-ttu-id="00f9f-277">Zaktualizowano dokumentację polecenia „New-AzOperationalInsightsLinuxSyslogDataSource”</span><span class="sxs-lookup"><span data-stu-id="00f9f-277">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="00f9f-278">Dodano przykład</span><span class="sxs-lookup"><span data-stu-id="00f9f-278">Added example</span></span>
    - <span data-ttu-id="00f9f-279">Zaktualizowano opis parametru „-Name”</span><span class="sxs-lookup"><span data-stu-id="00f9f-279">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="00f9f-280">Dodano przykład dla polecenia New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="00f9f-280">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="00f9f-281">Zaktualizowano opis parametru „-Name” dla polecenia New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="00f9f-281">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="00f9f-282">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-282">Az.RecoveryServices</span></span>
* <span data-ttu-id="00f9f-283">Aktualizacja polecenia „Get-AzRecoveryServicesBackupJobDetail.md”</span><span class="sxs-lookup"><span data-stu-id="00f9f-283">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-284">Az.Resources</span></span>
* <span data-ttu-id="00f9f-285">Dodano obsługę nowej wersji interfejsu API (2019-05-10) dla Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="00f9f-285">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="00f9f-286">Dodano obsługę „copy.count = 0” dla zmiennych, zasobów i właściwości</span><span class="sxs-lookup"><span data-stu-id="00f9f-286">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="00f9f-287">Zasoby z ustawieniami „condition = false” lub „copy.count = 0” będą usuwane w trybie ukończenia</span><span class="sxs-lookup"><span data-stu-id="00f9f-287">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="00f9f-288">Dodanie do dokumentu pomocy przykładu przypisywania zasad na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="00f9f-288">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="00f9f-289">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="00f9f-289">Az.ServiceBus</span></span>
* <span data-ttu-id="00f9f-290">Rozwiązano problem nr 9658: Literówka VirtualNetworkRule w poleceniu Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="00f9f-290">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="00f9f-291">Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania</span><span class="sxs-lookup"><span data-stu-id="00f9f-291">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="00f9f-292">Dodano nowe polecenie „Test-AzServiceBusNameAvailability” do sprawdzania dostępności nazwy dla kolejki i tematu</span><span class="sxs-lookup"><span data-stu-id="00f9f-292">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="00f9f-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="00f9f-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="00f9f-294">Usunięcie usterek poleceń cmdlet dodawania typu węzła:</span><span class="sxs-lookup"><span data-stu-id="00f9f-294">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="00f9f-295">Usterka NullReferenceException, gdy grupa zasobów ma inny zestaw VMSS niezwiązany z klastrem usługi Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="00f9f-295">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="00f9f-296">Rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="00f9f-296">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="00f9f-297">Usunięcie usterki powodującej niepowodzenie polecenia cmdlet, gdy sieć wirtualna znajdowała się w innej grupie zasobów niż klaster.</span><span class="sxs-lookup"><span data-stu-id="00f9f-297">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="00f9f-298">rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="00f9f-298">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="00f9f-299">Sklasyfikowanie polecenia cmdlet Add-AzServiceFabricApplicationCertificate jako przestarzałego</span><span class="sxs-lookup"><span data-stu-id="00f9f-299">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-300">Az.Sql</span></span>
* <span data-ttu-id="00f9f-301">Aktualizacja dokumentacji starych poleceń cmdlet inspekcji.</span><span class="sxs-lookup"><span data-stu-id="00f9f-301">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="00f9f-302">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="00f9f-302">Az.Storage</span></span>
* <span data-ttu-id="00f9f-303">Aktualizacja pomocy dotyczącej poleceń Get/Close-AzStorageFileHandle, przez dodanie kolejnych scenariuszy do przykładów dotyczących poleceń cmdlet i zaktualizowanie opisów parametrów</span><span class="sxs-lookup"><span data-stu-id="00f9f-303">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="00f9f-304">Obsługa StandardBlobTier w ramach przekazywania i kopiowania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="00f9f-304">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="00f9f-305">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="00f9f-305">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="00f9f-306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="00f9f-306">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="00f9f-307">Obsługa priorytetu ponownego wypełniania w ramach kopiowania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="00f9f-307">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="00f9f-308">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="00f9f-308">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="00f9f-309">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="00f9f-309">Az.Websites</span></span>
* <span data-ttu-id="00f9f-310">Dodanie wyjaśnienia do parametru -AppSettings w poleceniach Set-AzWebApp i Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="00f9f-310">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="00f9f-311">2.5.0 — lipiec 2019</span><span class="sxs-lookup"><span data-stu-id="00f9f-311">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="00f9f-312">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-312">Az.Accounts</span></span>
* <span data-ttu-id="00f9f-313">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="00f9f-313">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="00f9f-314">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="00f9f-314">Az.ApplicationInsights</span></span>
* <span data-ttu-id="00f9f-315">Poprawienie pisowni w przykładzie w dokumentacji polecenia „Remove-AzApplicationInsightsApiKey”</span><span class="sxs-lookup"><span data-stu-id="00f9f-315">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="00f9f-316">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="00f9f-316">Az.Automation</span></span>
* <span data-ttu-id="00f9f-317">Poprawienie pisowni w ciągu zasobu</span><span class="sxs-lookup"><span data-stu-id="00f9f-317">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="00f9f-318">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-318">Az.CognitiveServices</span></span>
* <span data-ttu-id="00f9f-319">Dodano obsługę właściwości NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="00f9f-319">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-320">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-320">Az.Compute</span></span>
* <span data-ttu-id="00f9f-321">Dodanie brakujących właściwości (ComputerName, OsName, OsVersion i HyperVGeneration) obiektu widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="00f9f-321">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="00f9f-322">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="00f9f-322">Az.ContainerRegistry</span></span>
* <span data-ttu-id="00f9f-323">Poprawienie pisowni parametru Replication w opisie polecenia Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="00f9f-323">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="00f9f-324">Więcej informacji można znaleźć tutaj: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="00f9f-324">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="00f9f-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="00f9f-325">Az.DataFactory</span></span>
* <span data-ttu-id="00f9f-326">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.0</span><span class="sxs-lookup"><span data-stu-id="00f9f-326">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="00f9f-327">Poprawienie pisowni w dokumentacji dla polecenia „Get-AzDataFactoryV2PipelineRun”</span><span class="sxs-lookup"><span data-stu-id="00f9f-327">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="00f9f-328">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="00f9f-328">Az.EventHub</span></span>
* <span data-ttu-id="00f9f-329">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="00f9f-329">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="00f9f-330">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="00f9f-330">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="00f9f-331">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="00f9f-331">Az.KeyVault</span></span>
* <span data-ttu-id="00f9f-332">Dodano obsługę określania rozmiaru klucza dla zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="00f9f-332">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="00f9f-333">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="00f9f-333">Az.LogicApp</span></span>
* <span data-ttu-id="00f9f-334">Poprawienie polecenia Get-AzIntegrationAccountMap tak, aby wyświetlało listę wszystkich typów map</span><span class="sxs-lookup"><span data-stu-id="00f9f-334">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="00f9f-335">Dodano nowy parametr MapType na potrzeby filtrowania</span><span class="sxs-lookup"><span data-stu-id="00f9f-335">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="00f9f-336">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-336">Az.ManagedServices</span></span>
* <span data-ttu-id="00f9f-337">Dodano obsługę interfejsu API w wersji 2019-06-01 (ogólna dostępność)</span><span class="sxs-lookup"><span data-stu-id="00f9f-337">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-338">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-338">Az.Network</span></span>
* <span data-ttu-id="00f9f-339">Dodanie obsługi prywatnego punktu końcowego i prywatnej usługi łączenia</span><span class="sxs-lookup"><span data-stu-id="00f9f-339">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="00f9f-340">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="00f9f-340">New cmdlets</span></span>
        - <span data-ttu-id="00f9f-341">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="00f9f-341">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="00f9f-342">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="00f9f-342">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="00f9f-343">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="00f9f-343">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="00f9f-344">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="00f9f-344">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="00f9f-345">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="00f9f-345">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="00f9f-346">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="00f9f-346">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="00f9f-347">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="00f9f-347">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="00f9f-348">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="00f9f-348">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="00f9f-349">Zaktualizowano poniższe polecenia dla funkcji: Flaga PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies w podsieci w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="00f9f-349">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="00f9f-350">Zaktualizowano polecenia New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-350">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="00f9f-351">Dodano opcjonalny parametr -PrivateEndpointNetworkPoliciesFlag, który konfiguruje, czy stosować zasady sieciowe w prywatnym punkcie końcowym w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="00f9f-351">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="00f9f-352">Dodano opcjonalny parametr -PrivateLinkServiceNetworkPoliciesFlag, który konfiguruje, czy stosować zasady sieciowe w usłudze łącza prywatnego w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="00f9f-352">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="00f9f-353">Nazwa parametru „ServiceName” polecenia cmdlet AzPrivateLinkService została zmieniona na „Name” z aliasem „ServiceName” w celu zachowania zgodności z poprzednimi wersjami</span><span class="sxs-lookup"><span data-stu-id="00f9f-353">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="00f9f-354">Włączenie protokołu ICMP dla konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="00f9f-354">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="00f9f-355">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="00f9f-355">Updated cmdlets</span></span>
        - <span data-ttu-id="00f9f-356">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-356">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="00f9f-357">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-357">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="00f9f-358">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-358">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="00f9f-359">Dodanie wartości ConnectionProtocolType (Ikev1/Ikev2) jako konfigurowalnego parametru dla polecenia New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="00f9f-359">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="00f9f-360">Dodanie parametru PrivateIpAddressVersion w elemencie LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="00f9f-360">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="00f9f-361">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="00f9f-361">Updated cmdlet:</span></span>
        - <span data-ttu-id="00f9f-362">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-362">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="00f9f-363">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-363">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="00f9f-364">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-364">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="00f9f-365">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig usługi Application Gateway o obsługę portu niestandardowego w sondzie</span><span class="sxs-lookup"><span data-stu-id="00f9f-365">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="00f9f-366">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig: Dodano opcjonalny parametr Port, który służy do sondowania serwera zaplecza.</span><span class="sxs-lookup"><span data-stu-id="00f9f-366">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="00f9f-367">Ten parametr ma zastosowanie w przypadku jednostek SKU Standard_V2 i WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="00f9f-367">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="00f9f-368">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="00f9f-368">Az.OperationalInsights</span></span>
* <span data-ttu-id="00f9f-369">Zaktualizowano domyślną wersję zapisywanych wyszukiwań na 1.</span><span class="sxs-lookup"><span data-stu-id="00f9f-369">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="00f9f-370">Poprawiono obsługę wyrażeń regularnych o wartości null dla dzienników niestandardowych</span><span class="sxs-lookup"><span data-stu-id="00f9f-370">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="00f9f-371">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-371">Az.RecoveryServices</span></span>
* <span data-ttu-id="00f9f-372">Aktualizacja pliku „Get-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="00f9f-372">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="00f9f-373">Aktualizacja pliku „Get-AzRecoveryServicesBackupContainer.md”</span><span class="sxs-lookup"><span data-stu-id="00f9f-373">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="00f9f-374">Aktualizacja pliku „Get-AzRecoveryServicesVault.md”</span><span class="sxs-lookup"><span data-stu-id="00f9f-374">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="00f9f-375">Aktualizacja pliku „Wait-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="00f9f-375">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="00f9f-376">Aktualizacja pliku „Set-AzRecoveryServicesVaultContext.md”</span><span class="sxs-lookup"><span data-stu-id="00f9f-376">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="00f9f-377">Aktualizacja pliku „Get-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="00f9f-377">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="00f9f-378">Aktualizacja pliku „Get-AzRecoveryServicesBackupRecoveryPoint.md”</span><span class="sxs-lookup"><span data-stu-id="00f9f-378">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="00f9f-379">Aktualizacja pliku „Restore-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="00f9f-379">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="00f9f-380">Zaktualizowano wywołanie usługi do wyrejestrowywania kontenera dla udziału plików platformy Azure</span><span class="sxs-lookup"><span data-stu-id="00f9f-380">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="00f9f-381">Aktualizacja pliku „Set-AzRecoveryServicesAsrAlertSetting.md”</span><span class="sxs-lookup"><span data-stu-id="00f9f-381">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-382">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-382">Az.Resources</span></span>
- <span data-ttu-id="00f9f-383">Usunięcie brakującego polecenia cmdlet przywoływanego w dokumentacji polecenia „New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="00f9f-383">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="00f9f-384">Zaktualizowano polecenia cmdlet zasad w celu używania nowego interfejsu API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="00f9f-384">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="00f9f-385">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="00f9f-385">Az.ServiceBus</span></span>
* <span data-ttu-id="00f9f-386">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="00f9f-386">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="00f9f-387">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="00f9f-387">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-388">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-388">Az.Sql</span></span>
* <span data-ttu-id="00f9f-389">Poprawienie brakujących przykładów dla polecenia cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="00f9f-389">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="00f9f-390">Poprawienie ustawiania cyklicznego skanowania przez rozszerzenie Ocena luk w zabezpieczeniach bez podawania żadnego adresu e-mail</span><span class="sxs-lookup"><span data-stu-id="00f9f-390">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="00f9f-391">Poprawienie pisowni w komunikacie ostrzegawczym.</span><span class="sxs-lookup"><span data-stu-id="00f9f-391">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="00f9f-392">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="00f9f-392">Az.Storage</span></span>
* <span data-ttu-id="00f9f-393">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzStorageAccount” w celu użycia poprawnej nazwy parametru</span><span class="sxs-lookup"><span data-stu-id="00f9f-393">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="00f9f-394">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="00f9f-394">Az.StorageSync</span></span>
* <span data-ttu-id="00f9f-395">Dodanie polecenia cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="00f9f-395">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="00f9f-396">Rozwiązanie problemu 9551 dotyczącego respektowania wartości TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="00f9f-396">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="00f9f-397">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="00f9f-397">Az.Websites</span></span>
* <span data-ttu-id="00f9f-398">Usunięcie usterki polegającej na tym, że niektóre właściwości SiteConfig nie były zwracane przez polecenia Get-AzWebApp i Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="00f9f-398">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="00f9f-399">Dodanie nowego parametru Location dla poleceń Get-AzDeletedWebApp i Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="00f9f-399">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="00f9f-400">Usunięcie usterki związanej z klonowaniem miejsc aplikacji internetowych przy użyciu polecenia New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="00f9f-400">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="00f9f-401">2.4.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-401">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="00f9f-402">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-402">Az.Accounts</span></span>
* <span data-ttu-id="00f9f-403">Dodano obsługę poleceń cmdlet profilu</span><span class="sxs-lookup"><span data-stu-id="00f9f-403">Add support for profile cmdlets</span></span>
* <span data-ttu-id="00f9f-404">Dodano obsługę środowisk i płaszczyzn danych w generowanych poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="00f9f-404">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="00f9f-405">Naprawiono błąd polegający na tym, że w niektórych przypadkach dla poleceń cmdlet płaszczyzny danych w programie Windows PowerShell był używany nieprawidłowy punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="00f9f-405">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="00f9f-406">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="00f9f-406">Az.Advisor</span></span>
* <span data-ttu-id="00f9f-407">Wersja ogólnodostępna modułu Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="00f9f-407">GA release of Az.Advisor</span></span>
* <span data-ttu-id="00f9f-408">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="00f9f-408">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="00f9f-409">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="00f9f-409">Az.ApiManagement</span></span>
* <span data-ttu-id="00f9f-410">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="00f9f-410">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="00f9f-411">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="00f9f-411">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="00f9f-412">Dodano obsługę wykonywania zapytań dotyczących subskrypcji według użytkownika i produktu</span><span class="sxs-lookup"><span data-stu-id="00f9f-412">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="00f9f-413">Dodano obsługę wykonywania zapytań przy użyciu zakresu „/”, „/apis”, „/apis/echo-api”</span><span class="sxs-lookup"><span data-stu-id="00f9f-413">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="00f9f-414">Rozwiązano problemy https://github.com/Azure/azure-powershell/issues/9307 i https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="00f9f-414">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="00f9f-415">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="00f9f-415">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="00f9f-416">Dodano obsługę określania właściwości „ApiVersion” i „ApiVersionSetId” podczas importowania interfejsów API</span><span class="sxs-lookup"><span data-stu-id="00f9f-416">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="00f9f-417">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="00f9f-417">Az.Automation</span></span>
* <span data-ttu-id="00f9f-418">Usunięto usterkę polecenia cmdlet Set-AzAutomationConnectionFieldValue w celu obsługi wartości ciągu.</span><span class="sxs-lookup"><span data-stu-id="00f9f-418">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-419">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-419">Az.Compute</span></span>
* <span data-ttu-id="00f9f-420">Dodano parametr HyperVGeneration do polecenia New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-420">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="00f9f-421">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="00f9f-421">Az.DataFactory</span></span>
* <span data-ttu-id="00f9f-422">Aktualizowanie danych wyjściowych poleceń cmdlet pobierania uruchomień działań, pobierania uruchomień potoków i pobierania uruchomień wyzwalaczy usługi ADF w celu obsługi potoku Select-Object.</span><span class="sxs-lookup"><span data-stu-id="00f9f-422">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="00f9f-423">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="00f9f-423">Az.EventGrid</span></span>
* <span data-ttu-id="00f9f-424">Poprawiono literówkę w dokumentacji polecenia New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="00f9f-424">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="00f9f-425">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="00f9f-425">Az.IotHub</span></span>
* <span data-ttu-id="00f9f-426">Dodano obsługę ponownego generowania kluczy zasad autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="00f9f-426">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-427">Az.Network</span></span>
* <span data-ttu-id="00f9f-428">Dodano właściwość „RoutingPreference” do tagów publicznych adresów IP</span><span class="sxs-lookup"><span data-stu-id="00f9f-428">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="00f9f-429">Poprawiono przykłady dla dokumentacji referencyjnej polecenia „Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="00f9f-429">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="00f9f-430">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="00f9f-430">Az.PolicyInsights</span></span>
* <span data-ttu-id="00f9f-431">Rozwiązano problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="00f9f-431">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="00f9f-432">Więcej informacji: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="00f9f-432">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="00f9f-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="00f9f-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="00f9f-434">Naprawiono model źródła danych CustomLog zwracany w poleceniu Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="00f9f-434">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="00f9f-435">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-435">Az.RecoveryServices</span></span>
* <span data-ttu-id="00f9f-436">Poprawka dotycząca polecenia get-policy dla maszyn wirtualnych IaaS</span><span class="sxs-lookup"><span data-stu-id="00f9f-436">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-437">Az.Resources</span></span>
    - <span data-ttu-id="00f9f-438">Poprawiono tekst pomocy dotyczącej parametru -Top polecenia Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="00f9f-438">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="00f9f-439">Dodano obsługę stronicowania po stronie klienta dla polecenia Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="00f9f-439">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="00f9f-440">Dodano nowe parametry dla polecenia Set-AzPolicyAssignment: -PolicyParameters i -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="00f9f-440">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="00f9f-441">Aktualizacje dokumentacji i przykładów dla poleceń cmdlet zasad</span><span class="sxs-lookup"><span data-stu-id="00f9f-441">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="00f9f-442">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="00f9f-442">Az.ServiceBus</span></span>
* <span data-ttu-id="00f9f-443">Poprawka rozwiązująca problem #4938 — polecenie New-AzureRmServiceBusQueue zwraca wynik BadRequest w przypadku ustawienia właściwości MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="00f9f-443">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-444">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-444">Az.Sql</span></span>
* <span data-ttu-id="00f9f-445">Dodano polecenia cmdlet grupy trybu failover wystąpienia z wersji zapoznawczej do wersji publicznej</span><span class="sxs-lookup"><span data-stu-id="00f9f-445">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="00f9f-446">Obsługa inspekcji w usłudze Azure SQL Server/Database za pomocą nowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00f9f-446">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="00f9f-447">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="00f9f-447">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="00f9f-448">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="00f9f-448">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="00f9f-449">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="00f9f-449">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="00f9f-450">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="00f9f-450">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="00f9f-451">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="00f9f-451">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="00f9f-452">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="00f9f-452">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="00f9f-453">Usunięto ograniczenia wiadomości e-mail z ustawień oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="00f9f-453">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="00f9f-454">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="00f9f-454">Az.Storage</span></span>
* <span data-ttu-id="00f9f-455">Zmieniono dwa parametry: „-IndexDocument” i „-ErrorDocument404Path” z wymaganych na opcjonalne w poleceniu cmdlet:</span><span class="sxs-lookup"><span data-stu-id="00f9f-455">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="00f9f-456">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="00f9f-456">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="00f9f-457">Zaktualizowano pomoc dotyczącą polecenia Get-AzStorageBlobContent przez dodanie przykładu</span><span class="sxs-lookup"><span data-stu-id="00f9f-457">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="00f9f-458">Wyświetlanie dodatkowych informacji o błędzie w przypadku niepowodzenia polecenia cmdlet z powodu wyjątku StorageException</span><span class="sxs-lookup"><span data-stu-id="00f9f-458">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="00f9f-459">Obsługa tworzenia i aktualizowania konta magazynu przy użyciu uwierzytelniania usługi AAD DS w usłudze Azure Files</span><span class="sxs-lookup"><span data-stu-id="00f9f-459">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="00f9f-460">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="00f9f-460">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="00f9f-461">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="00f9f-461">Set-AzStorageAccount</span></span>
* <span data-ttu-id="00f9f-462">Obsługa wyświetlania listy lub zamykania dojść do plików udziału plików, katalogu plików lub pliku</span><span class="sxs-lookup"><span data-stu-id="00f9f-462">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="00f9f-463">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="00f9f-463">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="00f9f-464">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="00f9f-464">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="00f9f-465">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="00f9f-465">Az.StorageSync</span></span>
* <span data-ttu-id="00f9f-466">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="00f9f-466">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="00f9f-467">2.3.2 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-467">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="00f9f-468">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-468">Az.Accounts</span></span>
* <span data-ttu-id="00f9f-469">Usunięto usterkę polegającą na używaniu w niektórych przypadkach niepoprawnego adresu URL w wywołaniach funkcji</span><span class="sxs-lookup"><span data-stu-id="00f9f-469">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="00f9f-470">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="00f9f-470">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="00f9f-471">Rozwiązano problem z aliasami w poleceniach cmdlet z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="00f9f-471">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="00f9f-472">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="00f9f-472">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="00f9f-473">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="00f9f-473">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-474">Az.Compute</span></span>
* <span data-ttu-id="00f9f-475">Proste zestawy parametrów New-AzVm i New-AzVmss akceptują teraz parametr „ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-475">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="00f9f-476">Poprawiono literówkę w dokumentacji referencyjnej polecenia „New-AzVM”</span><span class="sxs-lookup"><span data-stu-id="00f9f-476">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="00f9f-477">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="00f9f-477">Az.Dns</span></span>
* <span data-ttu-id="00f9f-478">Poprawiono literówkę w przykładach pomocy polecenia „Set-AzDnsZone”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-478">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="00f9f-479">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="00f9f-479">Az.EventGrid</span></span>
* <span data-ttu-id="00f9f-480">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="00f9f-480">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="00f9f-481">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="00f9f-481">New cmdlets:</span></span>
    - <span data-ttu-id="00f9f-482">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="00f9f-482">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="00f9f-483">Tworzy nową domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="00f9f-483">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="00f9f-484">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="00f9f-484">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="00f9f-485">Pobiera szczegóły domeny usługi Event Grid lub pobiera listę wszystkich domen usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="00f9f-485">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="00f9f-486">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="00f9f-486">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="00f9f-487">Usuwa domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="00f9f-487">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="00f9f-488">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="00f9f-488">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="00f9f-489">Ponownie generuje klucz dostępu współdzielonego dla domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="00f9f-489">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="00f9f-490">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="00f9f-490">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="00f9f-491">Pobiera klucze dostępu współdzielonego używane do publikowania zdarzeń w domenie usługi Event Grid.</span><span class="sxs-lookup"><span data-stu-id="00f9f-491">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="00f9f-492">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="00f9f-492">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="00f9f-493">Tworzy nowy temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="00f9f-493">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="00f9f-494">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="00f9f-494">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="00f9f-495">Pobiera szczegóły tematu domeny usługi Event Grid lub pobiera listę wszystkich tematów domeny usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="00f9f-495">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="00f9f-496">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="00f9f-496">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="00f9f-497">Usuwa istniejący temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="00f9f-497">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="00f9f-498">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="00f9f-498">Updated cmdlets:</span></span>
    - <span data-ttu-id="00f9f-499">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="00f9f-499">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="00f9f-500">Dodano nowe wymagane parametry do obsługi przesyłania potokowego nowej domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="00f9f-500">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="00f9f-501">Dodano nowe wymagane parametry w celu określenia nowej nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="00f9f-501">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="00f9f-502">Dodano nowe zestawy parametrów dla domen i tematów domen, aby umożliwić ponowne używanie istniejących parametrów (np. EndPointType, SubjectBeginsWith itp.).</span><span class="sxs-lookup"><span data-stu-id="00f9f-502">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="00f9f-503">Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="00f9f-503">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="00f9f-504">Data wygaśnięcia subskrypcji zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="00f9f-504">Event subscription expiration date,</span></span>
            - <span data-ttu-id="00f9f-505">Zaawansowane parametry filtrowania.</span><span class="sxs-lookup"><span data-stu-id="00f9f-505">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="00f9f-506">Dodano nowe wyliczenie dla elementu servicebusqueue jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="00f9f-506">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="00f9f-507">Uniemożliwiono użycie elementu „Wszystkie” w opcji -IncludedEventType i zamieniono go na</span><span class="sxs-lookup"><span data-stu-id="00f9f-507">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="00f9f-508">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="00f9f-508">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="00f9f-509">Dodano nowe opcjonalne parametry (Top, ODataQuery i NextLink) w celu obsługi filtrowania i stronicowania wyników.</span><span class="sxs-lookup"><span data-stu-id="00f9f-509">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="00f9f-510">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="00f9f-510">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="00f9f-511">Dodano nowe wymagane parametry do obsługi przesyłania potokowego domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="00f9f-511">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="00f9f-512">Dodano nowe wymagane parametry w celu określenia nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="00f9f-512">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="00f9f-513">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="00f9f-513">Az.FrontDoor</span></span>
* <span data-ttu-id="00f9f-514">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="00f9f-514">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="00f9f-515">Dodano obsługę przekształceń i nową wartość autouzupełniania operatora (wyrażenie regularne)</span><span class="sxs-lookup"><span data-stu-id="00f9f-515">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="00f9f-516">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="00f9f-516">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="00f9f-517">Dodano nowe wartości autouzupełniania</span><span class="sxs-lookup"><span data-stu-id="00f9f-517">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-518">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-518">Az.Network</span></span>
* <span data-ttu-id="00f9f-519">Dodano obsługę zasobu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="00f9f-519">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="00f9f-520">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="00f9f-520">New cmdlets</span></span>
        - <span data-ttu-id="00f9f-521">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="00f9f-521">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="00f9f-522">Dodano element AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="00f9f-522">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="00f9f-523">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="00f9f-523">New cmdlets</span></span> 
        - <span data-ttu-id="00f9f-524">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="00f9f-524">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="00f9f-525">Dodano element PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="00f9f-525">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="00f9f-526">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="00f9f-526">New cmdlets</span></span> 
        - <span data-ttu-id="00f9f-527">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="00f9f-527">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="00f9f-528">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="00f9f-528">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="00f9f-529">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="00f9f-529">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="00f9f-530">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-530">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="00f9f-531">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="00f9f-531">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="00f9f-532">Dodano element PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="00f9f-532">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="00f9f-533">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="00f9f-533">New cmdlets</span></span>
        - <span data-ttu-id="00f9f-534">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="00f9f-534">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="00f9f-535">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="00f9f-535">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="00f9f-536">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="00f9f-536">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="00f9f-537">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="00f9f-537">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="00f9f-538">Zaktualizowano poniższe polecenia dla funkcji: Flaga UseLocalAzureIpAddress w elemencie VpnConnection</span><span class="sxs-lookup"><span data-stu-id="00f9f-538">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="00f9f-539">Zaktualizowano polecenie New-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="00f9f-539">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="00f9f-540">Zaktualizowano polecenie Set-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="00f9f-540">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="00f9f-541">Dodano pole tylko do odczytu PeeredConnections w komunikacji równorzędnej usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="00f9f-541">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="00f9f-542">Dodano pole tylko do odczytu GlobalReachEnabled w usłudze ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="00f9f-542">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="00f9f-543">Dodano atrybut zmiany wywołujący zakończenie obsługi pola AllowGlobalReach w modelu ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="00f9f-543">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="00f9f-544">Rozwiązano problem 8756 podczas używania elementu TargetListenerID z poleceniami cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="00f9f-544">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="00f9f-545">Usunięto usterkę w poleceniu New-AzApplicationGatewayPathRuleConfig, która uniemożliwiała ustawienie zestawu reguł regenerowania.</span><span class="sxs-lookup"><span data-stu-id="00f9f-545">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="00f9f-546">Rozwiązano problem z wyświetlaniem elementu VirtualNetworkTaps w elemencie NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="00f9f-546">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="00f9f-547">Naprawiono polecenia cmdlet pobierania Cortex dla listy wszystkich części</span><span class="sxs-lookup"><span data-stu-id="00f9f-547">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="00f9f-548">Naprawiono tworzenie odwołań elementu VirtualHub dla elementu ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="00f9f-548">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="00f9f-549">Dodano obsługę stref dostępności w elementach AzureFirewall i NatGateway</span><span class="sxs-lookup"><span data-stu-id="00f9f-549">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="00f9f-550">Dodano polecenie cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="00f9f-550">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="00f9f-551">Dodano obsługę wielu publicznych adresów IP usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="00f9f-551">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="00f9f-552">Zaktualizowano polecenie cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="00f9f-552">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="00f9f-553">Dodano parametr -PublicIpAddress, który akceptuje co najmniej jeden obiekt publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="00f9f-553">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="00f9f-554">Dodano parametr -VirtualNetwork, który akceptuje obiekt sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="00f9f-554">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="00f9f-555">Dodano do obiektu zapory metody AddPublicIpAddress i RemovePublicIpAddress, które akceptują obiekt publicznego adresu IP jako dane wejściowe</span><span class="sxs-lookup"><span data-stu-id="00f9f-555">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="00f9f-556">Wycofano parametry -PublicIpName i -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="00f9f-556">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="00f9f-557">Zaktualizowano poniższe polecenia dla funkcji: Ustawiono w opcjach uwierzytelniania usługi AAD elementu VpnClient zasób bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="00f9f-557">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="00f9f-558">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="00f9f-558">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="00f9f-559">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="00f9f-559">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="00f9f-560">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr przełącznika RemoveAadAuthentication w celu usunięcia z bramy opcji uwierzytelniania usługi AAD elementu VpnClient.</span><span class="sxs-lookup"><span data-stu-id="00f9f-560">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="00f9f-561">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="00f9f-561">Az.OperationalInsights</span></span>
* <span data-ttu-id="00f9f-562">Włączono warstwę cenową **pergb2018** w poleceniu „New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="00f9f-562">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-563">Az.Resources</span></span>
* <span data-ttu-id="00f9f-564">Obsługa dodatkowych opcji eksportowania szablonu</span><span class="sxs-lookup"><span data-stu-id="00f9f-564">Support for additional Template Export options</span></span>
    - <span data-ttu-id="00f9f-565">Dodano parametr „-SkipResourceNameParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="00f9f-565">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="00f9f-566">Dodano parametr „-SkipAllParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="00f9f-566">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="00f9f-567">Dodano parametr „-Resource” do polecenia Export-AzResourceGroup w celu filtrowania wyeksportowanych zasobów</span><span class="sxs-lookup"><span data-stu-id="00f9f-567">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="00f9f-568">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="00f9f-568">Az.ServiceFabric</span></span>
* <span data-ttu-id="00f9f-569">Usunięto błąd dodawania certyfikatu polegający na pobieraniu przez element ByExistingKeyVault nieprawidłowego odcisku palca w niektórych przypadkach</span><span class="sxs-lookup"><span data-stu-id="00f9f-569">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-570">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-570">Az.Sql</span></span>
* <span data-ttu-id="00f9f-571">Naprawiono sufiks punktu końcowego magazynu usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="00f9f-571">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="00f9f-572">Rozwiązano problem z usługą Advanced Data Security polegający na przesłanianiu zasad usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="00f9f-572">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="00f9f-573">Nowe polecenia cmdlet modułu Management.Sql umożliwiające klientom dodawanie kluczy funkcji TDE i ustawianie funkcji ochrony TDE dla wystąpień zarządzanych</span><span class="sxs-lookup"><span data-stu-id="00f9f-573">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="00f9f-574">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="00f9f-574">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="00f9f-575">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="00f9f-575">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="00f9f-576">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="00f9f-576">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="00f9f-577">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="00f9f-577">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="00f9f-578">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="00f9f-578">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="00f9f-579">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="00f9f-579">Az.Storage</span></span>
* <span data-ttu-id="00f9f-580">Obsługa rodzajów FileStorage i SkuName Premium_ZRS podczas tworzenia konta magazynu</span><span class="sxs-lookup"><span data-stu-id="00f9f-580">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="00f9f-581">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="00f9f-581">New-AzStorageAccount</span></span>
* <span data-ttu-id="00f9f-582">Opis z wyjaśnieniem polecenia cmdlet niezmienności obiektów blob</span><span class="sxs-lookup"><span data-stu-id="00f9f-582">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="00f9f-583">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="00f9f-583">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="00f9f-584">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="00f9f-584">Az.Websites</span></span>
* <span data-ttu-id="00f9f-585">Optymalizuje polecenie Get-AzWebAppCertificate w celu filtrowania według grupy zasobów na serwerze zamiast na kliencie</span><span class="sxs-lookup"><span data-stu-id="00f9f-585">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="00f9f-586">Dodano parametr przełącznika -UseDisasterRecovery do polecenia Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="00f9f-586">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="00f9f-587">2.2.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-587">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="00f9f-588">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="00f9f-588">Az.Cdn</span></span>
* <span data-ttu-id="00f9f-589">Zaktualizowano polecenia cmdlet do obsługi funkcji rulesEngine na podstawie interfejsu API w wersji 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="00f9f-589">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-590">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-590">Az.Compute</span></span>
* <span data-ttu-id="00f9f-591">Dodano parametr `NoWait`, który powoduje rozpoczęcie operacji i natychmiastowy powrót, bez czekania na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="00f9f-591">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="00f9f-592">Zaktualizowano następujące polecenia cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="00f9f-592">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="00f9f-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="00f9f-593">Az.EventHub</span></span>
* <span data-ttu-id="00f9f-594">Poprawka błędu #9231 — polecenie Get-AzEventHubNamespace nie zwraca tagów</span><span class="sxs-lookup"><span data-stu-id="00f9f-594">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="00f9f-595">Poprawka błędu #9230 — polecenie Get-AzEventHubNamespace zwraca wartość ResourceGroup zamiast wartości ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f9f-595">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-596">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-596">Az.Network</span></span>
* <span data-ttu-id="00f9f-597">Aktualizowanie wartości ResourceId i InputObject dla bramy translatora adresów sieciowych</span><span class="sxs-lookup"><span data-stu-id="00f9f-597">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="00f9f-598">Dodawanie aliasów dla wartości ResourceId i InputObject</span><span class="sxs-lookup"><span data-stu-id="00f9f-598">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="00f9f-599">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="00f9f-599">Az.PolicyInsights</span></span>
* <span data-ttu-id="00f9f-600">Rozwiązanie problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="00f9f-600">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="00f9f-601">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-601">Az.RecoveryServices</span></span>
* <span data-ttu-id="00f9f-602">Minimalny czas przechowywania zasad IaaSVM w dniach zmieniono z 7 na 1</span><span class="sxs-lookup"><span data-stu-id="00f9f-602">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="00f9f-603">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="00f9f-603">Az.ServiceBus</span></span>
* <span data-ttu-id="00f9f-604">Rozwiązanie problemu #9182 — Get-AzServiceBusNamespace zwraca wartość ResourceGroup zamiast ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f9f-604">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="00f9f-605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="00f9f-605">Az.ServiceFabric</span></span>
* <span data-ttu-id="00f9f-606">Poprawienie błędu pisowni w komunikacie o błędzie polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="00f9f-606">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="00f9f-607">Poprawienie brakującego znaku w wierszach polecenia usługi Service Fabric</span><span class="sxs-lookup"><span data-stu-id="00f9f-607">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-608">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-608">Az.Sql</span></span>
* <span data-ttu-id="00f9f-609">Dodanie parametru DnsZonePartner dla polecenia cmdlet New-AzureSqlInstance w celu obsługi funkcji AutoDr dla wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="00f9f-609">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="00f9f-610">Wycofanie polecenia cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="00f9f-610">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="00f9f-611">Zmiana nazwy poleceń cmdlet z Wykrywanie zagrożeń na Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="00f9f-611">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="00f9f-612">Parametry New-AzSqlInstance -StorageSizeInGB i -LicenseType są teraz opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="00f9f-612">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="00f9f-613">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="00f9f-613">Az.Websites</span></span>
* <span data-ttu-id="00f9f-614">Rozwiązanie problemu polegającego na tym, że użycie poleceń Set-AzWebApp i Set-AzWebAppSlot z właściwością -WebApp powodowało usunięcie tagów</span><span class="sxs-lookup"><span data-stu-id="00f9f-614">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="00f9f-615">2.1.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-615">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="00f9f-616">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="00f9f-616">Az.ApiManagement</span></span>
* <span data-ttu-id="00f9f-617">Utworzono nowe polecenia cmdlet do zarządzania diagnostyką w zakresie globalnym i interfejsu API</span><span class="sxs-lookup"><span data-stu-id="00f9f-617">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="00f9f-618">**Get-AzApiManagementDiagnostic** — uzyskiwanie diagnostyki skonfigurowanej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="00f9f-618">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="00f9f-619">**New-AzApiManagementDiagnostic** — tworzenie nowej diagnostyki w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="00f9f-619">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="00f9f-620">**New-AzApiManagementHttpMessageDiagnostic** — tworzenie ustawienia diagnostyki określającego nagłówki do rejestrowania i rozmiar treści w bajtach</span><span class="sxs-lookup"><span data-stu-id="00f9f-620">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="00f9f-621">**New-AzApiManagementPipelineDiagnosticSetting** — tworzenie ustawień diagnostyki dla przychodzących/wychodzących komunikatów HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="00f9f-621">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="00f9f-622">**New-AzApiManagementSamplingSetting** — tworzenie ustawienia próbkowania dla żądań i odpowiedzi na potrzeby diagnostyki</span><span class="sxs-lookup"><span data-stu-id="00f9f-622">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="00f9f-623">**Remove-AzApiManagementDiagnostic** — usuwanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="00f9f-623">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="00f9f-624">**Set-AzApiManagementDiagnostic** — aktualizowanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="00f9f-624">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="00f9f-625">Utworzono nowe polecenia cmdlet do zarządzania pamięcią podręczną usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="00f9f-625">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="00f9f-626">**Get-AzApiManagementCache** — uzyskiwanie szczegółów pamięci podręcznej określonej przez identyfikator lub wszystkich pamięci podręcznych</span><span class="sxs-lookup"><span data-stu-id="00f9f-626">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="00f9f-627">**New-AzApiManagementCache** — tworzenie nowej, „domyślnej” pamięci podręcznej lub pamięci podręcznej w konkretnym „regionie” platformy Azure</span><span class="sxs-lookup"><span data-stu-id="00f9f-627">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="00f9f-628">**Remove-AzApiManagementCache** — usuwanie pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="00f9f-628">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="00f9f-629">**Update-AzApiManagementCache** — aktualizacja pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="00f9f-629">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="00f9f-630">Utworzono nowe polecenia cmdlet do zarządzania schematem interfejsu API</span><span class="sxs-lookup"><span data-stu-id="00f9f-630">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="00f9f-631">**New-AzApiManagementSchema** — tworzenie nowego schematu dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="00f9f-631">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="00f9f-632">**Get-AzApiManagementSchema** — pobieranie schematów skonfigurowanych w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="00f9f-632">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="00f9f-633">**Remove-AzApiManagementSchema** — usuwanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="00f9f-633">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="00f9f-634">**Set-AzApiManagementSchema** — aktualizowanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="00f9f-634">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="00f9f-635">Utworzono nowe polecenie cmdlet do generowania tokenu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00f9f-635">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="00f9f-636">**New-AzApiManagementUserToken** — generowanie nowego tokenu użytkownika ważnego domyślnie przez 8 godzin. Za pomocą tego polecenia cmdlet można wygenerować token dla użytkownika „GIT”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-636">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="00f9f-637">Utworzono nowe polecenie cmdlet do pobierania stanu sieci.</span><span class="sxs-lookup"><span data-stu-id="00f9f-637">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="00f9f-638">**Get-AzApiManagementNetworkStatus** — uzyskiwanie stanu sieci dla łączności z zasobami, od których zależy usługa API Management.</span><span class="sxs-lookup"><span data-stu-id="00f9f-638">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="00f9f-639">Jest to przydatne w przypadku wdrażania usługi ApiManagement w sieci wirtualnej i weryfikacji, czy któreś z zależności są uszkodzone.</span><span class="sxs-lookup"><span data-stu-id="00f9f-639">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="00f9f-640">Zaktualizowano polecenie cmdlet **New-AzApiManagement** do zarządzania usługą ApiManagement</span><span class="sxs-lookup"><span data-stu-id="00f9f-640">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="00f9f-641">Dodano obsługę nowych jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="00f9f-641">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="00f9f-642">Dodano obsługę włączania flagi „EnableClientCertificate” dla jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="00f9f-642">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="00f9f-643">Nowe polecenie cmdlet **New-AzApiManagementSslSetting** umożliwia skonfigurowanie ustawienia „TLS/SSL” na „Zaplecze” i „Fronton”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-643">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="00f9f-644">Za jego pomocą można też skonfigurować szyfrowanie, takie jak „3DES”, i protokoły serwera, takie jak „Http2”we frontonie usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="00f9f-644">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="00f9f-645">Dodano obsługę konfigurowania nazwy hosta „DeveloperPortal” usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="00f9f-645">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="00f9f-646">Zaktualizowano polecenia cmdlet **Get-AzApiManagementSsoToken**, aby przyjmowały jako wejście obiekt „PsApiManagement”</span><span class="sxs-lookup"><span data-stu-id="00f9f-646">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="00f9f-647">Zaktualizowano polecenie cmdlet, aby wyświetlało komunikaty o błędach śródwierszowo</span><span class="sxs-lookup"><span data-stu-id="00f9f-647">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="00f9f-648">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Kod błędu: Komunikat o błędzie ValidationError: Co najmniej jedno pole zawiera nieprawidłową wartość: Szczegóły błędu:    [Code=ValidationError, Message=Błąd w elemencie „log-to-eventhub” w wierszu 3, kolumna 10: Nie znaleziono rejestratora, element docelowy=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="00f9f-648">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="00f9f-649">Zaktualizowano polecenie cmdlet **Export-AzApiManagementApi** tak, aby eksportowało interfejsy API w formacie „OpenApi 3.0”</span><span class="sxs-lookup"><span data-stu-id="00f9f-649">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="00f9f-650">Zaktualizowano polecenie cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="00f9f-650">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="00f9f-651">W celu importowania interfejsu Api z dokumentu ze specyfikacją interfejsu „OpenApi 3.0”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-651">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="00f9f-652">W celu przesłonięcia właściwości „PsApiManagementSchema” określonej w dowolnym dokumencie („Swagger”, „Wadl”, „Wsdl”, „OpenApi”).</span><span class="sxs-lookup"><span data-stu-id="00f9f-652">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="00f9f-653">W celu przesłonięcia właściwości „ServiceUrl” określonej w dowolnym dokumencie.</span><span class="sxs-lookup"><span data-stu-id="00f9f-653">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="00f9f-654">Zaktualizowano polecenie cmdlet **Get-AzApiManagementPolicy** tak, aby zwracało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml”</span><span class="sxs-lookup"><span data-stu-id="00f9f-654">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="00f9f-655">Zaktualizowano polecenie cmdlet **Set-AzApiManagementPolicy** tak, aby akceptowało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml” i ze zmianą znaczenia Xml przy użyciu formatu „xml”</span><span class="sxs-lookup"><span data-stu-id="00f9f-655">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="00f9f-656">Zaktualizowano polecenie cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="00f9f-656">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="00f9f-657">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-657">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="00f9f-658">W celu utworzenia interfejsu API we właściwości ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="00f9f-658">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="00f9f-659">W celu sklonowania interfejsu API przy użyciu właściwości „SourceApiId” i „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-659">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="00f9f-660">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="00f9f-660">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="00f9f-661">Zaktualizowano polecenie cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="00f9f-661">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="00f9f-662">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-662">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="00f9f-663">W celu zaktualizowania interfejsu API we właściwości „ApiVersionSet”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-663">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="00f9f-664">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="00f9f-664">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="00f9f-665">Zaktualizowano polecenie cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="00f9f-665">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="00f9f-666">W celu klonowania (kopiowanie tagów, produktów, operacji i zasad) istniejącej wersji przy użyciu właściwości „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-666">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="00f9f-667">Dla nowej wersji przyjmowana jest wartość „ApiId” elementu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="00f9f-667">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="00f9f-668">W celu dostarczenia właściwości „ApiRevisionDescription”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-668">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="00f9f-669">W celu przesłonięcia właściwości „ServiceUrl” podczas klonowania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="00f9f-669">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="00f9f-670">Zaktualizowano polecenie cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="00f9f-670">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="00f9f-671">W celu skonfigurowania właściwości „AAD” lub „AADB2C” za pomocą właściwości „Authority”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-671">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="00f9f-672">W celu skonfigurowania właściwości „SignupPolicy”, „SigninPolicy”, „ProfileEditingPolicy” i „PasswordResetPolicy”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-672">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="00f9f-673">Zaktualizowano polecenie cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="00f9f-673">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="00f9f-674">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-674">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="00f9f-675">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-675">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="00f9f-676">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="00f9f-676">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="00f9f-677">Zaktualizowano polecenie cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="00f9f-677">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="00f9f-678">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-678">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="00f9f-679">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-679">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="00f9f-680">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="00f9f-680">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="00f9f-681">Zaktualizowano następujące polecenia cmdlet do akceptowania właściwości „ResourceId” jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="00f9f-681">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="00f9f-682">„New-AzApiManagementContext”</span><span class="sxs-lookup"><span data-stu-id="00f9f-682">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="00f9f-683">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="00f9f-683">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="00f9f-684">„Get-AzApiManagementApiRelease”</span><span class="sxs-lookup"><span data-stu-id="00f9f-684">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="00f9f-685">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="00f9f-685">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="00f9f-686">„Get-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="00f9f-686">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="00f9f-687">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="00f9f-687">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="00f9f-688">„Get-AzApiManagementAuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="00f9f-688">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="00f9f-689">„Get-AzApiManagementBackend”</span><span class="sxs-lookup"><span data-stu-id="00f9f-689">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="00f9f-690">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="00f9f-690">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="00f9f-691">„Get-AzApiManagementCertificate”</span><span class="sxs-lookup"><span data-stu-id="00f9f-691">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="00f9f-692">„Remove-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="00f9f-692">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="00f9f-693">„Remove-AzApiManagementSubscription”</span><span class="sxs-lookup"><span data-stu-id="00f9f-693">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="00f9f-694">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="00f9f-694">Az.Automation</span></span>
* <span data-ttu-id="00f9f-695">Zaktualizowano polecenie Get-AzAutomationJobOutputRecord tak, aby obsługiwało wartości rekordów w postaci kodu JSON i tekstowej.</span><span class="sxs-lookup"><span data-stu-id="00f9f-695">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="00f9f-696">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="00f9f-696">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="00f9f-697">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="00f9f-697">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="00f9f-698">Zmieniono działanie polecenia Start-AzAutomationDscCompilationJob tak, aby tylko uruchamiało zadanie zamiast czekać na jego zakończenie.</span><span class="sxs-lookup"><span data-stu-id="00f9f-698">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="00f9f-699">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="00f9f-699">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="00f9f-700">Poprawka dla polecenia Get-AzAutomationDscNode podczas używania opcji -Name zwraca wszystkie węzły.</span><span class="sxs-lookup"><span data-stu-id="00f9f-700">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="00f9f-701">Teraz zwraca tylko pasujące węzły.</span><span class="sxs-lookup"><span data-stu-id="00f9f-701">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-702">Az.Compute</span></span>
* <span data-ttu-id="00f9f-703">Dodanie parametrów ProtectFromScaleIn i ProtectFromScaleSetAction do polecenia cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="00f9f-703">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="00f9f-704">Nowy zestaw parametrów New-AzVM wimple teraz używa domyślnie dostępnej lokalizacji, jeśli region „Wschodnie stany USA” nie jest obsługiwany.</span><span class="sxs-lookup"><span data-stu-id="00f9f-704">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="00f9f-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="00f9f-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="00f9f-706">Aktualizacja zestawu ADLS SDK do korzystania z klienta httpclient, integrowanie testowania płaszczyzny danych z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="00f9f-706">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="00f9f-707">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="00f9f-707">Az.Monitor</span></span>
* <span data-ttu-id="00f9f-708">Naprawiono nieprawidłowe nazwy parametrów w przykładach pomocy</span><span class="sxs-lookup"><span data-stu-id="00f9f-708">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-709">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-709">Az.Network</span></span>
* <span data-ttu-id="00f9f-710">Dodanie flagi DisableBgpRoutePropagation do danych wyjściowych obowiązującej tabeli routingu</span><span class="sxs-lookup"><span data-stu-id="00f9f-710">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="00f9f-711">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="00f9f-711">Updated cmdlet:</span></span>
        - <span data-ttu-id="00f9f-712">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="00f9f-712">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="00f9f-713">Poprawienie podwójnego łącznika w dokumentacji polecenia New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="00f9f-713">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-714">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-714">Az.Resources</span></span>
* <span data-ttu-id="00f9f-715">Dodanie nowego polecenia cmdlet Get-AzureRmDenyAssignment do pobierania przypisań odmowy</span><span class="sxs-lookup"><span data-stu-id="00f9f-715">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-716">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-716">Az.Sql</span></span>
* <span data-ttu-id="00f9f-717">Zmiana nazwy poleceń cmdlet usługi Advanced Threat Protection na Advanced Data Security i domyślne włączenie oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="00f9f-717">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="00f9f-718">2.0.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-718">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="00f9f-719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-719">Az.Accounts</span></span>
* <span data-ttu-id="00f9f-720">Aktualizacja biblioteki uwierzytelniania w celu rozwiązania problemów z usługą ADFS dotyczących uwierzytelniania nazwy użytkownika i hasła</span><span class="sxs-lookup"><span data-stu-id="00f9f-720">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="00f9f-721">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-721">Az.CognitiveServices</span></span>
* <span data-ttu-id="00f9f-722">Dla usług wyszukiwania Bing wyświetlane jest tylko zrzeczenie odpowiedzialności usługi Bing.</span><span class="sxs-lookup"><span data-stu-id="00f9f-722">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="00f9f-723">Naprawiono błąd polegający na niepomyślnym tworzeniu konta.</span><span class="sxs-lookup"><span data-stu-id="00f9f-723">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-724">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-724">Az.Compute</span></span>
* <span data-ttu-id="00f9f-725">Funkcja Grupa umieszczania w pobliżu.</span><span class="sxs-lookup"><span data-stu-id="00f9f-725">Proximity placement group feature.</span></span>
    - <span data-ttu-id="00f9f-726">Dodano następujące nowe polecenia cmdlet:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="00f9f-726">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="00f9f-727">Do następujących poleceń cmdlet dodano nowy parametr ProximityPlacementGroupId:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-727">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="00f9f-728">Do polecenia New-AzGalleryImageVersion dodano parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="00f9f-728">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="00f9f-729">Właściwość TargetRegion polecenia New-AzGalleryImageVersion może zawierać parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="00f9f-729">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="00f9f-730">Do poleceń Stop-AzVM i Stop-AzVmss dodano parametr przełącznika SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="00f9f-730">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="00f9f-731">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="00f9f-731">Breaking changes</span></span>
    - <span data-ttu-id="00f9f-732">Polecenie Set-AzVMBootDiagnostics zamieniono na polecenie Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="00f9f-732">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="00f9f-733">Polecenie Export-AzLogAnalyticThrottledRequests zamieniono na polecenie Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="00f9f-733">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="00f9f-734">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="00f9f-734">Az.DeploymentManager</span></span>
* <span data-ttu-id="00f9f-735">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="00f9f-735">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="00f9f-736">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="00f9f-736">Az.Dns</span></span>
* <span data-ttu-id="00f9f-737">Automatyczne delegowanie serwera nazw systemu DNS</span><span class="sxs-lookup"><span data-stu-id="00f9f-737">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="00f9f-738">Polecenie cmdlet tworzenia strefy DNS akceptuje nazwę strefy nadrzędnej jako dodatkowy parametr opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="00f9f-738">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="00f9f-739">Dodaje rekordy serwera nazw w strefie nadrzędnej dla nowo utworzonej strefy podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="00f9f-739">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="00f9f-740">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="00f9f-740">Az.FrontDoor</span></span>
* <span data-ttu-id="00f9f-741">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="00f9f-741">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="00f9f-742">Zmiana nazw poleceń cmdlet zapory aplikacji internetowej w celu dołączenia ciągu „Waf”</span><span class="sxs-lookup"><span data-stu-id="00f9f-742">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="00f9f-743">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="00f9f-743">Az.HDInsight</span></span>
* <span data-ttu-id="00f9f-744">Usunięto dwa polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="00f9f-744">Removed two cmdlets:</span></span>
    - <span data-ttu-id="00f9f-745">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="00f9f-745">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="00f9f-746">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="00f9f-746">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="00f9f-747">Dodano nowe polecenie cmdlet Set-AzHDInsightGatewayCredential w celu zastąpienia polecenia Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="00f9f-747">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="00f9f-748">Zaktualizowano polecenie cmdlet Get-AzHDInsightJobOutput, aby rozróżnić rolę czytelnika i rolę operatora usługi HDInsight:</span><span class="sxs-lookup"><span data-stu-id="00f9f-748">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="00f9f-749">Użytkownicy z rolą czytelnika muszą jawnie określić parametr „DefaultStorageAccountKey” — w przeciwnym razie wystąpi błąd.</span><span class="sxs-lookup"><span data-stu-id="00f9f-749">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="00f9f-750">Nie będzie to miało wpływu na użytkowników z rolą operatora usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="00f9f-750">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="00f9f-751">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="00f9f-751">Az.Monitor</span></span>
* <span data-ttu-id="00f9f-752">Nowe polecenia cmdlet dla interfejsu API SQR (Scheduled Query Rule, reguła zaplanowanego zapytania)</span><span class="sxs-lookup"><span data-stu-id="00f9f-752">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="00f9f-753">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="00f9f-753">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="00f9f-754">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="00f9f-754">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="00f9f-755">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="00f9f-755">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="00f9f-756">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="00f9f-756">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="00f9f-757">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="00f9f-757">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="00f9f-758">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="00f9f-758">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="00f9f-759">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="00f9f-759">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="00f9f-760">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="00f9f-760">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="00f9f-761">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="00f9f-761">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="00f9f-762">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="00f9f-762">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="00f9f-763">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="00f9f-763">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="00f9f-764">[Więcej](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informacji na temat interfejsu API SQR</span><span class="sxs-lookup"><span data-stu-id="00f9f-764">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="00f9f-765">Zaktualizowano plik Az.Monitor.md w celu uwzględnienia poleceń cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="00f9f-765">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-766">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-766">Az.Network</span></span>
* <span data-ttu-id="00f9f-767">Dodano obsługę dla zasobu usługi NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="00f9f-767">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="00f9f-768">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="00f9f-768">New cmdlets</span></span>
        - <span data-ttu-id="00f9f-769">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="00f9f-769">New-AzNatGateway</span></span>
        - <span data-ttu-id="00f9f-770">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="00f9f-770">Get-AzNatGateway</span></span>
        - <span data-ttu-id="00f9f-771">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="00f9f-771">Set-AzNatGateway</span></span>
        - <span data-ttu-id="00f9f-772">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="00f9f-772">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="00f9f-773">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="00f9f-773">Updated cmdlets</span></span>
        - <span data-ttu-id="00f9f-774">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="00f9f-774">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="00f9f-775">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="00f9f-775">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="00f9f-776">Zaktualizowano poniższe polecenia dla funkcji: Ustawianie/usuwanie tras niestandardowych dla bramy Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="00f9f-776">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="00f9f-777">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="00f9f-777">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="00f9f-778">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="00f9f-778">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="00f9f-779">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="00f9f-779">Az.PolicyInsights</span></span>
* <span data-ttu-id="00f9f-780">Obsługa zapytań dotyczących szczegółów oceny zasad.</span><span class="sxs-lookup"><span data-stu-id="00f9f-780">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="00f9f-781">Dodano parametr „-Expand” do polecenia Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="00f9f-781">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="00f9f-782">Obsługa polecenia „-Expand PolicyEvaluationDetails”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-782">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="00f9f-783">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-783">Az.RecoveryServices</span></span>
* <span data-ttu-id="00f9f-784">Obsługa odzyskiwania lokacji między subskrypcjami z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="00f9f-784">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="00f9f-785">Oznaczanie nadchodzących zmian powodujących niezgodność dla usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="00f9f-785">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="00f9f-786">Poprawka zakończenia planu akcji dla planu odzyskiwania usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="00f9f-786">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="00f9f-787">Poprawka aktualizacji mapowania sieci usługi Azure Site Recovery z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="00f9f-787">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="00f9f-788">Poprawka aktualizacji kierunku ochrony usługi Azure Site Recovery z platformy Azure na platformę Azure dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="00f9f-788">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="00f9f-789">Inne drobne poprawki.</span><span class="sxs-lookup"><span data-stu-id="00f9f-789">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="00f9f-790">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="00f9f-790">Az.Relay</span></span>
* <span data-ttu-id="00f9f-791">Poprawiono błędy pisowni w komunikatach przeznaczonych dla klientów</span><span class="sxs-lookup"><span data-stu-id="00f9f-791">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="00f9f-792">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="00f9f-792">Az.ServiceBus</span></span>
* <span data-ttu-id="00f9f-793">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="00f9f-793">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="00f9f-794">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="00f9f-794">Az.Storage</span></span>
* <span data-ttu-id="00f9f-795">Uaktualnienie biblioteki klienta usługi Storage do wersji 10.0.1 (przestrzeń nazw wszystkich obiektów tego zestawu SDK została zmieniona z „Microsoft.WindowsAzure.Storage. *” na „Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="00f9f-795">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="00f9f-796">Uaktualnienie do wersji Microsoft.Azure.Management.Storage 11.0.0 w celu obsługi nowego interfejsu API w wersji 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="00f9f-796">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="00f9f-797">Domyślny rodzaj konta magazynu w poleceniu Utwórz konto magazynu został zmieniony ze „Storage” na „StorageV2”</span><span class="sxs-lookup"><span data-stu-id="00f9f-797">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="00f9f-798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="00f9f-798">New-AzStorageAccount</span></span>
* <span data-ttu-id="00f9f-799">Zmiana wyjściowego parametru Sku.Name polecenia cmdlet konta magazynu w celu wyrównania z wejściowym parametrem SkuName przez dodanie znaku „-”, na przykład zmiana „StandardLRS” na „Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="00f9f-799">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="00f9f-800">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="00f9f-800">New-AzStorageAccount</span></span>
    - <span data-ttu-id="00f9f-801">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="00f9f-801">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="00f9f-802">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="00f9f-802">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="00f9f-803">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="00f9f-803">Az.Websites</span></span>
* <span data-ttu-id="00f9f-804">Właściwość „Kind” będzie teraz ustawiona dla obiektów PSSite zwracanych przez polecenie Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="00f9f-804">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="00f9f-805">Polecenia Get-AzWebApp\*Metrics i Get-AzAppServicePlanMetrics oznaczono jako przestarzałe</span><span class="sxs-lookup"><span data-stu-id="00f9f-805">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="00f9f-806">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-806">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="00f9f-807">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="00f9f-807">Highlights since the last major release</span></span>
* <span data-ttu-id="00f9f-808">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="00f9f-808">General availability of `Az` module</span></span>
* <span data-ttu-id="00f9f-809">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="00f9f-809">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="00f9f-810">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="00f9f-810">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="00f9f-811">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-811">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="00f9f-812">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="00f9f-812">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="00f9f-813">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="00f9f-813">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="00f9f-814">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="00f9f-814">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="00f9f-815">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-815">Az.Accounts</span></span>
* <span data-ttu-id="00f9f-816">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="00f9f-816">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="00f9f-817">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="00f9f-817">Az.Batch</span></span>
* <span data-ttu-id="00f9f-818">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="00f9f-819">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="00f9f-819">Az.Cdn</span></span>
* <span data-ttu-id="00f9f-820">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="00f9f-821">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-821">Az.CognitiveServices</span></span>
* <span data-ttu-id="00f9f-822">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-822">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-823">Az.Compute</span></span>
* <span data-ttu-id="00f9f-824">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="00f9f-824">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="00f9f-825">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-825">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="00f9f-826">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="00f9f-826">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="00f9f-827">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="00f9f-827">Az.DataFactory</span></span>
* <span data-ttu-id="00f9f-828">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="00f9f-828">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="00f9f-829">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="00f9f-829">Az.DataLakeStore</span></span>
* <span data-ttu-id="00f9f-830">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-830">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="00f9f-831">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="00f9f-831">Az.EventGrid</span></span>
* <span data-ttu-id="00f9f-832">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="00f9f-832">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="00f9f-833">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="00f9f-833">Az.EventHub</span></span>
* <span data-ttu-id="00f9f-834">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="00f9f-834">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="00f9f-835">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="00f9f-835">Az.HDInsight</span></span>
* <span data-ttu-id="00f9f-836">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="00f9f-837">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="00f9f-837">Az.IotHub</span></span>
* <span data-ttu-id="00f9f-838">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="00f9f-839">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="00f9f-839">Az.KeyVault</span></span>
* <span data-ttu-id="00f9f-840">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-840">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="00f9f-841">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="00f9f-841">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="00f9f-842">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="00f9f-842">Az.MachineLearning</span></span>
* <span data-ttu-id="00f9f-843">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="00f9f-844">Az.Media</span><span class="sxs-lookup"><span data-stu-id="00f9f-844">Az.Media</span></span>
* <span data-ttu-id="00f9f-845">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-845">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="00f9f-846">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="00f9f-846">Az.Monitor</span></span>
  * <span data-ttu-id="00f9f-847">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="00f9f-847">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="00f9f-848">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="00f9f-848">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="00f9f-849">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="00f9f-849">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="00f9f-850">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="00f9f-850">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="00f9f-851">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="00f9f-851">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="00f9f-852">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="00f9f-852">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="00f9f-853">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="00f9f-853">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-854">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-854">Az.Network</span></span>
* <span data-ttu-id="00f9f-855">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-855">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="00f9f-856">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="00f9f-856">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="00f9f-857">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="00f9f-857">Az.NotificationHubs</span></span>
* <span data-ttu-id="00f9f-858">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="00f9f-859">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="00f9f-859">Az.OperationalInsights</span></span>
* <span data-ttu-id="00f9f-860">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="00f9f-861">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="00f9f-861">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="00f9f-862">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="00f9f-863">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-863">Az.RecoveryServices</span></span>
* <span data-ttu-id="00f9f-864">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-864">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="00f9f-865">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="00f9f-865">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="00f9f-866">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="00f9f-866">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="00f9f-867">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="00f9f-867">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="00f9f-868">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="00f9f-868">Az.RedisCache</span></span>
* <span data-ttu-id="00f9f-869">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-869">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-870">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-870">Az.Resources</span></span>
* <span data-ttu-id="00f9f-871">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="00f9f-871">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-872">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-872">Az.Sql</span></span>
* <span data-ttu-id="00f9f-873">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="00f9f-873">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="00f9f-874">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-874">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="00f9f-875">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="00f9f-875">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="00f9f-876">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="00f9f-876">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="00f9f-877">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="00f9f-877">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="00f9f-878">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="00f9f-878">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="00f9f-879">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="00f9f-879">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="00f9f-880">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="00f9f-880">Az.Websites</span></span>
* <span data-ttu-id="00f9f-881">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="00f9f-881">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="00f9f-882">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="00f9f-882">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="00f9f-883">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="00f9f-883">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="00f9f-884">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="00f9f-884">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="00f9f-885">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-885">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="00f9f-886">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="00f9f-886">Highlights since the last major release</span></span>
* <span data-ttu-id="00f9f-887">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="00f9f-887">General availability of `Az` module</span></span>
* <span data-ttu-id="00f9f-888">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="00f9f-888">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="00f9f-889">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="00f9f-889">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="00f9f-890">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-890">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="00f9f-891">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="00f9f-891">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="00f9f-892">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="00f9f-892">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="00f9f-893">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="00f9f-893">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="00f9f-894">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-894">Az.Accounts</span></span>
* <span data-ttu-id="00f9f-895">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="00f9f-895">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="00f9f-896">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-896">Az.AnalysisServices</span></span>
* <span data-ttu-id="00f9f-897">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="00f9f-897">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="00f9f-898">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="00f9f-898">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="00f9f-899">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="00f9f-899">Az.Automation</span></span>
* <span data-ttu-id="00f9f-900">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="00f9f-900">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="00f9f-901">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="00f9f-901">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="00f9f-902">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="00f9f-902">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-903">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-903">Az.Compute</span></span>
* <span data-ttu-id="00f9f-904">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-904">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="00f9f-905">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="00f9f-905">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="00f9f-906">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="00f9f-906">Az.ContainerInstance</span></span>
* <span data-ttu-id="00f9f-907">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="00f9f-907">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="00f9f-908">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="00f9f-908">Az.DataFactory</span></span>
* <span data-ttu-id="00f9f-909">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="00f9f-909">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="00f9f-910">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="00f9f-910">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-911">Az.Resources</span></span>
* <span data-ttu-id="00f9f-912">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="00f9f-912">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="00f9f-913">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="00f9f-913">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="00f9f-914">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="00f9f-914">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="00f9f-915">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="00f9f-915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="00f9f-916">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="00f9f-916">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="00f9f-917">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="00f9f-917">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-918">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-918">Az.Sql</span></span>
* <span data-ttu-id="00f9f-919">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="00f9f-919">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="00f9f-920">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="00f9f-920">Az.Storage</span></span>
* <span data-ttu-id="00f9f-921">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="00f9f-921">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="00f9f-922">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="00f9f-922">New-AzStorageContext</span></span>
* <span data-ttu-id="00f9f-923">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="00f9f-923">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="00f9f-924">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="00f9f-924">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="00f9f-925">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="00f9f-925">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="00f9f-926">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="00f9f-926">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="00f9f-927">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="00f9f-927">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="00f9f-928">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="00f9f-928">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="00f9f-929">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="00f9f-929">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="00f9f-930">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="00f9f-930">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="00f9f-931">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="00f9f-931">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="00f9f-932">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="00f9f-932">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="00f9f-933">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="00f9f-933">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="00f9f-934">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="00f9f-934">Highlights since the last major release</span></span>
* <span data-ttu-id="00f9f-935">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="00f9f-935">General availability of `Az` module</span></span>
* <span data-ttu-id="00f9f-936">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="00f9f-936">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="00f9f-937">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="00f9f-937">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="00f9f-938">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-938">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="00f9f-939">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="00f9f-939">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="00f9f-940">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="00f9f-940">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="00f9f-941">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="00f9f-941">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="00f9f-942">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="00f9f-942">Az.Automation</span></span>
* <span data-ttu-id="00f9f-943">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="00f9f-943">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="00f9f-944">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="00f9f-944">Dynamic grouping</span></span>
    * <span data-ttu-id="00f9f-945">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="00f9f-945">Pre-Post script</span></span>
    * <span data-ttu-id="00f9f-946">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="00f9f-946">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-947">Az.Compute</span></span>
* <span data-ttu-id="00f9f-948">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="00f9f-948">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="00f9f-949">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="00f9f-949">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="00f9f-950">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="00f9f-950">Az.KeyVault</span></span>
* <span data-ttu-id="00f9f-951">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="00f9f-951">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-952">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-952">Az.Network</span></span>
* <span data-ttu-id="00f9f-953">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="00f9f-953">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="00f9f-954">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="00f9f-954">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="00f9f-955">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-955">Az.RecoveryServices</span></span>
* <span data-ttu-id="00f9f-956">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="00f9f-956">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="00f9f-957">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="00f9f-957">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-958">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-958">Az.Resources</span></span>
* <span data-ttu-id="00f9f-959">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="00f9f-959">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="00f9f-960">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="00f9f-960">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-961">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-961">Az.Sql</span></span>
* <span data-ttu-id="00f9f-962">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="00f9f-962">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="00f9f-963">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="00f9f-963">Az.Storage</span></span>
* <span data-ttu-id="00f9f-964">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="00f9f-964">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="00f9f-965">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="00f9f-965">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="00f9f-966">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="00f9f-966">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="00f9f-967">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="00f9f-967">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="00f9f-968">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="00f9f-968">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="00f9f-969">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="00f9f-969">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="00f9f-970">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="00f9f-970">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="00f9f-971">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="00f9f-971">Az.Websites</span></span>
* <span data-ttu-id="00f9f-972">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="00f9f-972">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="00f9f-973">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="00f9f-973">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="00f9f-974">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-974">Az.Accounts</span></span>
* <span data-ttu-id="00f9f-975">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="00f9f-975">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="00f9f-976">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="00f9f-976">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="00f9f-977">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="00f9f-977">Az.Automation</span></span>
* <span data-ttu-id="00f9f-978">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="00f9f-978">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="00f9f-979">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="00f9f-979">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="00f9f-980">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="00f9f-980">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="00f9f-981">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="00f9f-981">Az.Cdn</span></span>
* <span data-ttu-id="00f9f-982">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="00f9f-982">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-983">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-983">Az.Compute</span></span>
* <span data-ttu-id="00f9f-984">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="00f9f-984">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="00f9f-985">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="00f9f-985">Az.DataFactory</span></span>
* <span data-ttu-id="00f9f-986">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="00f9f-986">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="00f9f-987">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="00f9f-987">Az.LogicApp</span></span>
* <span data-ttu-id="00f9f-988">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="00f9f-988">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-989">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-989">Az.Network</span></span>
* <span data-ttu-id="00f9f-990">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="00f9f-990">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="00f9f-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="00f9f-992">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="00f9f-992">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="00f9f-993">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="00f9f-993">SDK Update</span></span>
* <span data-ttu-id="00f9f-994">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="00f9f-994">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="00f9f-995">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="00f9f-995">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-996">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-996">Az.Resources</span></span>
* <span data-ttu-id="00f9f-997">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="00f9f-997">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="00f9f-998">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="00f9f-998">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="00f9f-999">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="00f9f-999">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="00f9f-1000">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="00f9f-1000">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="00f9f-1001">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="00f9f-1001">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="00f9f-1002">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="00f9f-1002">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-1003">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-1003">Az.Sql</span></span>
* <span data-ttu-id="00f9f-1004">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1004">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="00f9f-1005">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1005">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="00f9f-1006">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="00f9f-1006">Az.Storage</span></span>
* <span data-ttu-id="00f9f-1007">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="00f9f-1007">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="00f9f-1008">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1008">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="00f9f-1009">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-1009">Az.AnalysisServices</span></span>
* <span data-ttu-id="00f9f-1010">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="00f9f-1010">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="00f9f-1011">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="00f9f-1011">Az.Automation</span></span>
* <span data-ttu-id="00f9f-1012">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="00f9f-1012">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="00f9f-1013">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="00f9f-1013">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="00f9f-1014">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="00f9f-1014">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="00f9f-1015">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-1015">Az.CognitiveServices</span></span>
* <span data-ttu-id="00f9f-1016">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1016">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-1017">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-1017">Az.Compute</span></span>
* <span data-ttu-id="00f9f-1018">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="00f9f-1018">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="00f9f-1019">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="00f9f-1019">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="00f9f-1020">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="00f9f-1020">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="00f9f-1021">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1021">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="00f9f-1022">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="00f9f-1022">Az.DataLakeStore</span></span>
* <span data-ttu-id="00f9f-1023">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="00f9f-1023">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="00f9f-1024">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="00f9f-1024">Az.EventHub</span></span>
* <span data-ttu-id="00f9f-1025">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="00f9f-1025">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="00f9f-1026">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="00f9f-1026">Az.KeyVault</span></span>
* <span data-ttu-id="00f9f-1027">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="00f9f-1027">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="00f9f-1028">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="00f9f-1028">Az.LogicApp</span></span>
* <span data-ttu-id="00f9f-1029">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="00f9f-1029">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="00f9f-1030">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="00f9f-1030">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="00f9f-1031">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="00f9f-1031">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="00f9f-1032">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="00f9f-1032">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="00f9f-1033">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="00f9f-1033">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="00f9f-1034">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="00f9f-1034">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="00f9f-1035">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="00f9f-1035">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="00f9f-1036">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="00f9f-1036">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="00f9f-1037">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="00f9f-1037">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="00f9f-1038">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="00f9f-1038">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="00f9f-1039">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="00f9f-1039">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="00f9f-1040">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="00f9f-1040">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="00f9f-1041">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="00f9f-1041">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="00f9f-1042">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="00f9f-1042">Az.Monitor</span></span>
* <span data-ttu-id="00f9f-1043">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="00f9f-1043">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-1044">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-1044">Az.Network</span></span>
* <span data-ttu-id="00f9f-1045">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="00f9f-1045">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="00f9f-1046">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="00f9f-1046">Az.OperationalInsights</span></span>
* <span data-ttu-id="00f9f-1047">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1047">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="00f9f-1048">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1048">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="00f9f-1049">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1049">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="00f9f-1050">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-1050">Az.Resources</span></span>
* <span data-ttu-id="00f9f-1051">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="00f9f-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="00f9f-1052">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="00f9f-1052">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="00f9f-1053">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="00f9f-1053">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="00f9f-1054">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="00f9f-1054">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-1055">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-1055">Az.Sql</span></span>
* <span data-ttu-id="00f9f-1056">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="00f9f-1056">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="00f9f-1057">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="00f9f-1057">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="00f9f-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="00f9f-1058">Az.Websites</span></span>
* <span data-ttu-id="00f9f-1059">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="00f9f-1059">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="00f9f-1060">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1060">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="00f9f-1061">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-1061">Az.Accounts</span></span>
* <span data-ttu-id="00f9f-1062">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="00f9f-1062">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="00f9f-1063">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-1063">Az.AnalysisServices</span></span>
<span data-ttu-id="00f9f-1064">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1064">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-1065">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-1065">Az.Compute</span></span>
* <span data-ttu-id="00f9f-1066">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="00f9f-1066">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="00f9f-1067">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="00f9f-1067">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="00f9f-1068">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="00f9f-1068">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="00f9f-1069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-1069">Az.RecoveryServices</span></span>
<span data-ttu-id="00f9f-1070">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1070">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-1071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-1071">Az.Resources</span></span>
* <span data-ttu-id="00f9f-1072">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="00f9f-1072">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="00f9f-1073">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="00f9f-1073">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="00f9f-1074">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="00f9f-1074">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="00f9f-1075">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="00f9f-1075">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-1076">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-1076">Az.Sql</span></span>
* <span data-ttu-id="00f9f-1077">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="00f9f-1077">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="00f9f-1078">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="00f9f-1078">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="00f9f-1079">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="00f9f-1079">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="00f9f-1080">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1080">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="00f9f-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-1081">Az.Accounts</span></span>
* <span data-ttu-id="00f9f-1082">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="00f9f-1082">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="00f9f-1083">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-1083">Az.AnalysisServices</span></span>
* <span data-ttu-id="00f9f-1084">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="00f9f-1084">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="00f9f-1085">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-1085">Az.RecoveryServices</span></span>
* <span data-ttu-id="00f9f-1086">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="00f9f-1086">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="00f9f-1087">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1087">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="00f9f-1088">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-1088">Az.Accounts</span></span>
* <span data-ttu-id="00f9f-1089">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="00f9f-1089">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="00f9f-1090">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="00f9f-1090">Update incorrect online help URLs</span></span>
* <span data-ttu-id="00f9f-1091">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="00f9f-1091">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="00f9f-1092">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="00f9f-1092">Az.Aks</span></span>
* <span data-ttu-id="00f9f-1093">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="00f9f-1093">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="00f9f-1094">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="00f9f-1094">Az.Automation</span></span>
* <span data-ttu-id="00f9f-1095">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="00f9f-1095">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="00f9f-1096">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="00f9f-1096">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="00f9f-1097">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="00f9f-1097">Az.Cdn</span></span>
* <span data-ttu-id="00f9f-1098">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="00f9f-1098">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-1099">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-1099">Az.Compute</span></span>
* <span data-ttu-id="00f9f-1100">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="00f9f-1100">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="00f9f-1101">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="00f9f-1101">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="00f9f-1102">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="00f9f-1102">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="00f9f-1103">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="00f9f-1103">Az.ContainerRegistry</span></span>
* <span data-ttu-id="00f9f-1104">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="00f9f-1104">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="00f9f-1105">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="00f9f-1105">Az.DataFactory</span></span>
* <span data-ttu-id="00f9f-1106">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="00f9f-1106">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="00f9f-1107">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="00f9f-1107">Az.DataLakeStore</span></span>
* <span data-ttu-id="00f9f-1108">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="00f9f-1108">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="00f9f-1109">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="00f9f-1109">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="00f9f-1110">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="00f9f-1110">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="00f9f-1111">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="00f9f-1111">Az.IotHub</span></span>
* <span data-ttu-id="00f9f-1112">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1112">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="00f9f-1113">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="00f9f-1113">Az.KeyVault</span></span>
* <span data-ttu-id="00f9f-1114">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="00f9f-1114">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-1115">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-1115">Az.Network</span></span>
* <span data-ttu-id="00f9f-1116">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="00f9f-1116">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-1117">Az.Resources</span></span>
* <span data-ttu-id="00f9f-1118">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="00f9f-1118">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="00f9f-1119">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="00f9f-1119">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="00f9f-1120">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="00f9f-1120">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="00f9f-1121">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="00f9f-1121">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="00f9f-1122">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="00f9f-1122">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="00f9f-1123">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="00f9f-1123">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="00f9f-1124">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="00f9f-1124">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="00f9f-1125">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="00f9f-1125">Az.ServiceFabric</span></span>
* <span data-ttu-id="00f9f-1126">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="00f9f-1126">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="00f9f-1127">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1127">Fix some error messages.</span></span>
* <span data-ttu-id="00f9f-1128">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1128">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="00f9f-1129">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1129">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="00f9f-1130">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="00f9f-1130">Az.SignalR</span></span>
* <span data-ttu-id="00f9f-1131">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="00f9f-1131">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-1132">Az.Sql</span></span>
* <span data-ttu-id="00f9f-1133">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="00f9f-1133">Update incorrect online help URLs</span></span>
* <span data-ttu-id="00f9f-1134">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="00f9f-1134">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="00f9f-1135">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="00f9f-1135">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="00f9f-1136">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="00f9f-1136">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="00f9f-1137">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="00f9f-1137">Az.Storage</span></span>
* <span data-ttu-id="00f9f-1138">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="00f9f-1138">Update incorrect online help URLs</span></span>
* <span data-ttu-id="00f9f-1139">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1139">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="00f9f-1140">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="00f9f-1140">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="00f9f-1141">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="00f9f-1141">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="00f9f-1142">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="00f9f-1142">Az.TrafficManager</span></span>
* <span data-ttu-id="00f9f-1143">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="00f9f-1143">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="00f9f-1144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="00f9f-1144">Az.Websites</span></span>
* <span data-ttu-id="00f9f-1145">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="00f9f-1145">Update incorrect online help URLs</span></span>
* <span data-ttu-id="00f9f-1146">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1146">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="00f9f-1147">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="00f9f-1147">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="00f9f-1148">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1148">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="00f9f-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-1149">Az.Accounts</span></span>
* <span data-ttu-id="00f9f-1150">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="00f9f-1150">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-1151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-1151">Az.Compute</span></span>
* <span data-ttu-id="00f9f-1152">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="00f9f-1152">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="00f9f-1153">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="00f9f-1153">Updated the description of ID in help files</span></span>
* <span data-ttu-id="00f9f-1154">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-1154">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="00f9f-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="00f9f-1155">Az.DataLakeStore</span></span>
* <span data-ttu-id="00f9f-1156">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1156">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="00f9f-1157">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="00f9f-1157">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="00f9f-1158">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="00f9f-1158">Az.EventGrid</span></span>
* <span data-ttu-id="00f9f-1159">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1159">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="00f9f-1160">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="00f9f-1160">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="00f9f-1161">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="00f9f-1161">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="00f9f-1162">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="00f9f-1162">Event Time-To-Live,</span></span>
        - <span data-ttu-id="00f9f-1163">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="00f9f-1163">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="00f9f-1164">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1164">Dead letter endpoint.</span></span>
    - <span data-ttu-id="00f9f-1165">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="00f9f-1165">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="00f9f-1166">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="00f9f-1166">Event Time-To-Live,</span></span>
        - <span data-ttu-id="00f9f-1167">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="00f9f-1167">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="00f9f-1168">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1168">Dead letter endpoint.</span></span>
* <span data-ttu-id="00f9f-1169">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1169">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="00f9f-1170">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1170">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="00f9f-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="00f9f-1171">Az.IotHub</span></span>
* <span data-ttu-id="00f9f-1172">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="00f9f-1172">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="00f9f-1173">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="00f9f-1173">Az.LogicApp</span></span>
* <span data-ttu-id="00f9f-1174">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="00f9f-1174">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-1175">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-1175">Az.Resources</span></span>
* <span data-ttu-id="00f9f-1176">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="00f9f-1176">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="00f9f-1177">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="00f9f-1177">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="00f9f-1178">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="00f9f-1178">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="00f9f-1179">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="00f9f-1179">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="00f9f-1180">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="00f9f-1180">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="00f9f-1181">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="00f9f-1181">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="00f9f-1182">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="00f9f-1182">Az.SignalR</span></span>
* <span data-ttu-id="00f9f-1183">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-1183">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-1184">Az.Sql</span></span>
* <span data-ttu-id="00f9f-1185">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1185">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="00f9f-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="00f9f-1186">Az.Storage</span></span>
* <span data-ttu-id="00f9f-1187">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="00f9f-1187">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="00f9f-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="00f9f-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="00f9f-1189">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="00f9f-1189">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="00f9f-1190">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="00f9f-1190">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="00f9f-1191">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="00f9f-1191">Az.Websites</span></span>
* <span data-ttu-id="00f9f-1192">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="00f9f-1192">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="00f9f-1193">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-1193">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="00f9f-1194">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1194">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="00f9f-1195">Ogólne</span><span class="sxs-lookup"><span data-stu-id="00f9f-1195">General</span></span>

- <span data-ttu-id="00f9f-1196">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="00f9f-1196">General Availability of Az Module</span></span>
- <span data-ttu-id="00f9f-1197">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="00f9f-1197">Online help for each module</span></span>
- <span data-ttu-id="00f9f-1198">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="00f9f-1198">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="00f9f-1199">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="00f9f-1199">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="00f9f-1200">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-1200">Az.Accounts</span></span>
- <span data-ttu-id="00f9f-1201">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="00f9f-1201">Changed from Az.Profile</span></span>
- <span data-ttu-id="00f9f-1202">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="00f9f-1202">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="00f9f-1203">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="00f9f-1203">Az.ApiManagement</span></span>
- <span data-ttu-id="00f9f-1204">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="00f9f-1204">Fixes for #7002</span></span>
- <span data-ttu-id="00f9f-1205">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="00f9f-1205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="00f9f-1206">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="00f9f-1206">Az.Batch</span></span>
- <span data-ttu-id="00f9f-1207">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1207">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="00f9f-1208">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1208">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="00f9f-1209">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="00f9f-1209">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="00f9f-1210">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="00f9f-1210">Az.Billing</span></span>
- <span data-ttu-id="00f9f-1211">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="00f9f-1211">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="00f9f-1212">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-1212">Az.CognitivServices</span></span>
- <span data-ttu-id="00f9f-1213">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="00f9f-1213">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="00f9f-1214">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="00f9f-1214">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="00f9f-1215">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="00f9f-1215">Az.ContainerInstance</span></span>
- <span data-ttu-id="00f9f-1216">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="00f9f-1216">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="00f9f-1217">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="00f9f-1217">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="00f9f-1218">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="00f9f-1218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="00f9f-1219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="00f9f-1219">Az.DataLakeStore</span></span>
- <span data-ttu-id="00f9f-1220">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="00f9f-1220">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="00f9f-1221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="00f9f-1221">Az.Monitor</span></span>
- <span data-ttu-id="00f9f-1222">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="00f9f-1222">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="00f9f-1223">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="00f9f-1223">Az.KeyVault</span></span>
- <span data-ttu-id="00f9f-1224">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="00f9f-1224">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="00f9f-1225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="00f9f-1225">Az.MachineLearning</span></span>
- <span data-ttu-id="00f9f-1226">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="00f9f-1226">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="00f9f-1227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="00f9f-1227">Az.Media</span></span>
- <span data-ttu-id="00f9f-1228">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="00f9f-1228">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="00f9f-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-1229">Az.Network</span></span>
<span data-ttu-id="00f9f-1230">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="00f9f-1230">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="00f9f-1231">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="00f9f-1231">New cmdlets added:</span></span>
        - <span data-ttu-id="00f9f-1232">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="00f9f-1232">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="00f9f-1233">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="00f9f-1233">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="00f9f-1234">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="00f9f-1234">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="00f9f-1235">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="00f9f-1235">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="00f9f-1236">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="00f9f-1236">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="00f9f-1237">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="00f9f-1237">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="00f9f-1238">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="00f9f-1238">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="00f9f-1239">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="00f9f-1239">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="00f9f-1240">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="00f9f-1240">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="00f9f-1241">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00f9f-1241">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="00f9f-1242">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="00f9f-1242">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="00f9f-1243">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="00f9f-1243">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="00f9f-1244">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-1244">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="00f9f-1245">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-1245">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="00f9f-1246">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1246">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="00f9f-1247">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="00f9f-1247">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="00f9f-1248">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="00f9f-1248">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="00f9f-1249">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="00f9f-1249">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="00f9f-1250">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="00f9f-1250">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="00f9f-1251">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="00f9f-1251">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="00f9f-1252">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="00f9f-1252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="00f9f-1253">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="00f9f-1253">Az.OperationalInsights</span></span>
- <span data-ttu-id="00f9f-1254">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="00f9f-1254">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="00f9f-1255">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="00f9f-1255">Az.Profile</span></span>
- <span data-ttu-id="00f9f-1256">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="00f9f-1256">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="00f9f-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-1257">Az.RecoveryServices</span></span>
- <span data-ttu-id="00f9f-1258">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="00f9f-1258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="00f9f-1259">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-1259">Az.Resources</span></span>
- <span data-ttu-id="00f9f-1260">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="00f9f-1260">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="00f9f-1261">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="00f9f-1261">Az.ServiceFabric</span></span>
- <span data-ttu-id="00f9f-1262">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="00f9f-1262">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="00f9f-1263">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="00f9f-1263">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="00f9f-1264">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="00f9f-1264">Az.SIgnalR</span></span>
- <span data-ttu-id="00f9f-1265">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="00f9f-1265">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="00f9f-1266">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-1266">Az.Sql</span></span>
- <span data-ttu-id="00f9f-1267">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="00f9f-1267">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="00f9f-1268">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="00f9f-1268">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="00f9f-1269">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="00f9f-1269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="00f9f-1270">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="00f9f-1270">Az.Storage</span></span>
- <span data-ttu-id="00f9f-1271">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="00f9f-1271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="00f9f-1272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="00f9f-1272">Az.Websites</span></span>
- <span data-ttu-id="00f9f-1273">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="00f9f-1273">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="00f9f-1274">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1274">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="00f9f-1275">Ogólne</span><span class="sxs-lookup"><span data-stu-id="00f9f-1275">General</span></span>

* <span data-ttu-id="00f9f-1276">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="00f9f-1276">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="00f9f-1277">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-1277">Az.Compute</span></span>

* <span data-ttu-id="00f9f-1278">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1278">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="00f9f-1279">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="00f9f-1279">Az.DataLakeStore</span></span>

* <span data-ttu-id="00f9f-1280">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="00f9f-1280">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="00f9f-1281">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="00f9f-1281">Az.FrontDoor</span></span>

* <span data-ttu-id="00f9f-1282">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="00f9f-1282">Fixed some broken links</span></span>
    - <span data-ttu-id="00f9f-1283">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1283">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="00f9f-1284">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1284">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="00f9f-1285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-1285">Az.RecoveryServices</span></span>

* <span data-ttu-id="00f9f-1286">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1286">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="00f9f-1287">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1287">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="00f9f-1288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-1288">Az.Resources</span></span>

* <span data-ttu-id="00f9f-1289">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="00f9f-1289">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="00f9f-1290">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1290">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="00f9f-1291">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-1291">Az.Sql</span></span>

* <span data-ttu-id="00f9f-1292">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="00f9f-1292">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="00f9f-1293">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="00f9f-1293">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="00f9f-1294">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1294">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="00f9f-1295">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="00f9f-1295">Az.Storage</span></span>

* <span data-ttu-id="00f9f-1296">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="00f9f-1296">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="00f9f-1297">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="00f9f-1297">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="00f9f-1298">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="00f9f-1298">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="00f9f-1299">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="00f9f-1299">Support Static Website configuration</span></span>
    - <span data-ttu-id="00f9f-1300">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="00f9f-1300">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="00f9f-1301">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="00f9f-1301">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="00f9f-1302">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="00f9f-1302">Az.Websites</span></span>

* <span data-ttu-id="00f9f-1303">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="00f9f-1303">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="00f9f-1304">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1304">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="00f9f-1305">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1305">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="00f9f-1306">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1306">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="00f9f-1307">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="00f9f-1307">Az.ApiManagement</span></span>
* <span data-ttu-id="00f9f-1308">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="00f9f-1308">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="00f9f-1309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="00f9f-1309">Az.Automation</span></span>
* <span data-ttu-id="00f9f-1310">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="00f9f-1310">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="00f9f-1311">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="00f9f-1311">Added Update Management cmdlets</span></span>
* <span data-ttu-id="00f9f-1312">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="00f9f-1312">Added Source Control cmdlets</span></span>
* <span data-ttu-id="00f9f-1313">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="00f9f-1313">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="00f9f-1314">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="00f9f-1314">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="00f9f-1315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-1315">Az.Compute</span></span>
* <span data-ttu-id="00f9f-1316">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="00f9f-1316">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="00f9f-1317">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="00f9f-1317">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="00f9f-1318">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="00f9f-1318">Az.ContainerInstance</span></span>
* <span data-ttu-id="00f9f-1319">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="00f9f-1319">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="00f9f-1320">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="00f9f-1320">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="00f9f-1321">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="00f9f-1321">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="00f9f-1322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-1322">Az.Network</span></span>
* <span data-ttu-id="00f9f-1323">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="00f9f-1323">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="00f9f-1324">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="00f9f-1324">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="00f9f-1325">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1325">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="00f9f-1326">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="00f9f-1326">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="00f9f-1327">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="00f9f-1327">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="00f9f-1328">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1328">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="00f9f-1329">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1329">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="00f9f-1330">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="00f9f-1330">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="00f9f-1331">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="00f9f-1331">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="00f9f-1332">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="00f9f-1332">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="00f9f-1333">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="00f9f-1333">Az.Relay</span></span>
* <span data-ttu-id="00f9f-1334">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1334">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="00f9f-1335">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-1335">Az.Resources</span></span>
* <span data-ttu-id="00f9f-1336">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="00f9f-1336">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="00f9f-1337">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="00f9f-1337">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="00f9f-1338">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="00f9f-1338">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="00f9f-1339">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="00f9f-1339">Az.ServiceFabric</span></span>
* <span data-ttu-id="00f9f-1340">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="00f9f-1340">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="00f9f-1341">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-1341">Az.Sql</span></span>
* <span data-ttu-id="00f9f-1342">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="00f9f-1342">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="00f9f-1343">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="00f9f-1343">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="00f9f-1344">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="00f9f-1344">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="00f9f-1345">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="00f9f-1345">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="00f9f-1346">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="00f9f-1346">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="00f9f-1347">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="00f9f-1347">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="00f9f-1348">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="00f9f-1348">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="00f9f-1349">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="00f9f-1349">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="00f9f-1350">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="00f9f-1350">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="00f9f-1351">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1351">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="00f9f-1352">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1352">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="00f9f-1353">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1353">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="00f9f-1354">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1354">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="00f9f-1355">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1355">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="00f9f-1356">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1356">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="00f9f-1357">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1357">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="00f9f-1358">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="00f9f-1358">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="00f9f-1359">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1359">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="00f9f-1360">Ogólne</span><span class="sxs-lookup"><span data-stu-id="00f9f-1360">General</span></span>
* <span data-ttu-id="00f9f-1361">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="00f9f-1361">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="00f9f-1362">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="00f9f-1362">Az.Profile</span></span>
* <span data-ttu-id="00f9f-1363">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="00f9f-1363">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="00f9f-1364">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="00f9f-1364">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="00f9f-1365">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="00f9f-1365">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="00f9f-1366">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="00f9f-1366">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="00f9f-1367">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="00f9f-1367">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="00f9f-1368">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="00f9f-1368">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="00f9f-1369">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="00f9f-1369">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="00f9f-1370">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-1370">Az.CognitiveServices</span></span>
* <span data-ttu-id="00f9f-1371">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1371">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-1372">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-1372">Az.Compute</span></span>
* <span data-ttu-id="00f9f-1373">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="00f9f-1373">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="00f9f-1374">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="00f9f-1374">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="00f9f-1375">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1375">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="00f9f-1376">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="00f9f-1376">Az.DataLakeStore</span></span>
* <span data-ttu-id="00f9f-1377">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1377">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="00f9f-1378">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1378">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="00f9f-1379">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="00f9f-1379">Az.Insights</span></span>
* <span data-ttu-id="00f9f-1380">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="00f9f-1380">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="00f9f-1381">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="00f9f-1381">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="00f9f-1382">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="00f9f-1382">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="00f9f-1383">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="00f9f-1383">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-1384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-1384">Az.Network</span></span>
* <span data-ttu-id="00f9f-1385">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="00f9f-1385">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="00f9f-1386">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="00f9f-1386">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="00f9f-1387">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="00f9f-1387">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="00f9f-1388">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="00f9f-1388">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="00f9f-1389">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="00f9f-1389">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="00f9f-1390">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="00f9f-1390">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="00f9f-1391">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="00f9f-1391">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="00f9f-1392">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="00f9f-1392">Az.PolicyInsights</span></span>
* <span data-ttu-id="00f9f-1393">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="00f9f-1393">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-1394">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-1394">Az.Resources</span></span>
* <span data-ttu-id="00f9f-1395">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="00f9f-1395">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="00f9f-1396">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="00f9f-1396">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="00f9f-1397">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="00f9f-1397">Az.ServiceBus</span></span>
* <span data-ttu-id="00f9f-1398">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1398">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="00f9f-1399">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="00f9f-1399">Az.ServiceFabric</span></span>
* <span data-ttu-id="00f9f-1400">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1400">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="00f9f-1401">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="00f9f-1401">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="00f9f-1402">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="00f9f-1402">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="00f9f-1403">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="00f9f-1403">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="00f9f-1404">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1404">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="00f9f-1405">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1405">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="00f9f-1406">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="00f9f-1406">Az.Profile</span></span>
* <span data-ttu-id="00f9f-1407">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="00f9f-1407">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="00f9f-1408">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="00f9f-1408">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-1409">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-1409">Az.Compute</span></span>
* <span data-ttu-id="00f9f-1410">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="00f9f-1410">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="00f9f-1411">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1411">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="00f9f-1412">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="00f9f-1412">Az.DataLakeStore</span></span>
* <span data-ttu-id="00f9f-1413">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="00f9f-1413">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="00f9f-1414">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1414">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="00f9f-1415">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1415">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="00f9f-1416">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1416">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="00f9f-1417">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1417">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-1418">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-1418">Az.Network</span></span>
* <span data-ttu-id="00f9f-1419">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1419">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="00f9f-1420">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1420">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-1421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-1421">Az.Resources</span></span>
* <span data-ttu-id="00f9f-1422">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1422">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="00f9f-1423">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1423">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="00f9f-1424">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1424">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="00f9f-1425">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="00f9f-1425">Azure.Storage</span></span>
* <span data-ttu-id="00f9f-1426">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="00f9f-1426">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="00f9f-1427">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="00f9f-1427">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="00f9f-1428">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="00f9f-1428">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="00f9f-1429">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1429">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="00f9f-1430">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="00f9f-1430">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="00f9f-1431">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="00f9f-1431">Az.CognitiveServices</span></span>
* <span data-ttu-id="00f9f-1432">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1432">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="00f9f-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="00f9f-1433">Az.Compute</span></span>
* <span data-ttu-id="00f9f-1434">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="00f9f-1434">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="00f9f-1435">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1435">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="00f9f-1436">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="00f9f-1436">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="00f9f-1437">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="00f9f-1437">Az.DataFactoryV2</span></span>
* <span data-ttu-id="00f9f-1438">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1438">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="00f9f-1439">Az.Network</span><span class="sxs-lookup"><span data-stu-id="00f9f-1439">Az.Network</span></span>
* <span data-ttu-id="00f9f-1440">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1440">Added NetworkProfile functionality.</span></span> <span data-ttu-id="00f9f-1441">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="00f9f-1441">new cmdlets added</span></span>
    - <span data-ttu-id="00f9f-1442">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="00f9f-1442">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="00f9f-1443">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="00f9f-1443">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="00f9f-1444">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="00f9f-1444">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="00f9f-1445">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="00f9f-1445">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="00f9f-1446">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-1446">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="00f9f-1447">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-1447">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="00f9f-1448">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="00f9f-1448">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="00f9f-1449">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="00f9f-1449">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="00f9f-1450">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="00f9f-1450">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="00f9f-1451">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="00f9f-1451">Az.RedisCache</span></span>
* <span data-ttu-id="00f9f-1452">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1452">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="00f9f-1453">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="00f9f-1453">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="00f9f-1454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="00f9f-1454">Az.Resources</span></span>
* <span data-ttu-id="00f9f-1455">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="00f9f-1455">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="00f9f-1456">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="00f9f-1456">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="00f9f-1457">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="00f9f-1457">Az.Sql</span></span>
* <span data-ttu-id="00f9f-1458">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="00f9f-1458">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="00f9f-1459">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="00f9f-1459">Az.Websites</span></span>
* <span data-ttu-id="00f9f-1460">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="00f9f-1460">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="00f9f-1461">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="00f9f-1461">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="00f9f-1462">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="00f9f-1462">0.2.0 - September 2018</span></span>
 <span data-ttu-id="00f9f-1463">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="00f9f-1463">Initial Release</span></span>