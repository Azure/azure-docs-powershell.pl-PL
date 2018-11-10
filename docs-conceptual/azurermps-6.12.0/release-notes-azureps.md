---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: c60bc9197266cc1da37cc9af7baf03e7ba8fb7ac
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/07/2018
ms.locfileid: "51212881"
---
# <a name="release-notes"></a><span data-ttu-id="69846-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="69846-103">Release notes</span></span>

<span data-ttu-id="69846-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="69846-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6120---november-2018"></a><span data-ttu-id="69846-105">6.12.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="69846-105">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="69846-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="69846-106">AzureRM.Profile</span></span>
* <span data-ttu-id="69846-107">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="69846-107">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="69846-108">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzureRmAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="69846-108">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="69846-109">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="69846-109">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="69846-110">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="69846-110">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="69846-111">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="69846-111">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="69846-112">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="69846-112">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="69846-113">Rozwiązano problem polegający na zgłaszaniu elementu „Disconnect-AzureRmAccount” w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="69846-113">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="69846-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="69846-114">AzureRM.Automation</span></span>
* <span data-ttu-id="69846-115">Zmieniono nazwę biblioteki DLL polecenia cmdlet na Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="69846-115">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="69846-116">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="69846-116">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="69846-117">Dodano operację Get-AzureRmCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="69846-117">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="69846-118">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="69846-118">AzureRM.Compute</span></span>
* <span data-ttu-id="69846-119">Dodano polecenia cmdlet Add-AzureRmVmssVMDataDisk i Remove-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="69846-119">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="69846-120">Polecenie Get-AzureRmVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="69846-120">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="69846-121">Rozwiązano problem polegający na tym, że wartości opcji SetAzureRmVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="69846-121">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="69846-122">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="69846-122">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="69846-123">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="69846-123">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="69846-124">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="69846-124">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="69846-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="69846-125">AzureRM.Insights</span></span>
* <span data-ttu-id="69846-126">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="69846-126">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="69846-127">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="69846-127">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="69846-128">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzureRMDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="69846-128">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="69846-129">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="69846-129">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="69846-130">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="69846-130">AzureRM.Network</span></span>
* <span data-ttu-id="69846-131">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="69846-131">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="69846-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="69846-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="69846-133">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="69846-133">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="69846-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="69846-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="69846-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="69846-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="69846-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="69846-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="69846-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="69846-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="69846-138">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="69846-138">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="69846-139">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="69846-139">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="69846-140">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="69846-140">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="69846-141">Dodano obsługę udziałów plików platformy Azure do usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="69846-141">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="69846-142">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="69846-142">AzureRM.Resources</span></span>
* <span data-ttu-id="69846-143">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="69846-143">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="69846-144">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="69846-144">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="69846-145">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="69846-145">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="69846-146">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="69846-146">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="69846-147">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="69846-147">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="69846-148">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="69846-148">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="69846-149">Rozwiązano problem z poleceniem „Add-AzureRmServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="69846-149">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="69846-150">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="69846-150">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="69846-151">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="69846-151">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="69846-152">Rozwiązano problem z poleceniem „Update-AzureRmServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="69846-152">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="69846-153">6.11.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="69846-153">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="69846-154">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="69846-154">AzureRM.Profile</span></span>
* <span data-ttu-id="69846-155">Rozwiązano problem z poleceniem Get-AzureRmSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="69846-155">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="69846-156">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="69846-156">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="69846-157">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="69846-157">AzureRM.Backup</span></span>
* <span data-ttu-id="69846-158">Przestarzałe polecenia cmdlet usługi Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="69846-158">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="69846-159">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="69846-159">AzureRM.Compute</span></span>
* <span data-ttu-id="69846-160">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzureRmVm”</span><span class="sxs-lookup"><span data-stu-id="69846-160">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="69846-161">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69846-161">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="69846-162">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="69846-162">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="69846-163">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="69846-163">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="69846-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="69846-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="69846-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="69846-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="69846-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="69846-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="69846-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="69846-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="69846-168">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="69846-168">AzureRM.Network</span></span>
* <span data-ttu-id="69846-169">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="69846-169">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="69846-170">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69846-170">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="69846-171">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="69846-171">AzureRM.Resources</span></span>
* <span data-ttu-id="69846-172">Rozwiązano problem polegający na tym, że polecenie Get-AzureRMRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="69846-172">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="69846-173">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="69846-173">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="69846-174">6.10.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="69846-174">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="69846-175">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="69846-175">Azure.Storage</span></span>
* <span data-ttu-id="69846-176">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="69846-176">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="69846-177">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="69846-177">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="69846-178">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="69846-178">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="69846-179">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="69846-179">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="69846-180">Obsługa polecenia Get-AzureRmCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="69846-180">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="69846-181">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="69846-181">AzureRM.Compute</span></span>
* <span data-ttu-id="69846-182">Rozwiązano problem z poleceniem Get-AzureRmVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="69846-182">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="69846-183">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="69846-183">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="69846-184">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="69846-184">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="69846-185">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="69846-185">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="69846-186">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="69846-186">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="69846-187">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="69846-187">AzureRM.Network</span></span>
* <span data-ttu-id="69846-188">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="69846-188">Added NetworkProfile functionality.</span></span> <span data-ttu-id="69846-189">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="69846-189">new cmdlets added</span></span>
    - <span data-ttu-id="69846-190">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="69846-190">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="69846-191">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="69846-191">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="69846-192">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="69846-192">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="69846-193">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="69846-193">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="69846-194">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="69846-194">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="69846-195">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="69846-195">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="69846-196">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="69846-196">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="69846-197">Dodano polecenia cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap i Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="69846-197">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="69846-198">Dodano polecenia cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig i Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="69846-198">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="69846-199">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="69846-199">AzureRM.RedisCache</span></span>
* <span data-ttu-id="69846-200">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="69846-200">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="69846-201">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="69846-201">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="69846-202">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="69846-202">AzureRM.Resources</span></span>
* <span data-ttu-id="69846-203">Dodano brakujący parametr -Mode do polecenia Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="69846-203">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="69846-204">Usunięto błąd polecenia Get-AzureRmProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="69846-204">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="69846-205">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="69846-205">AzureRM.Sql</span></span>
* <span data-ttu-id="69846-206">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="69846-206">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="69846-207">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="69846-207">AzureRM.Storage</span></span>
* <span data-ttu-id="69846-208">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="69846-208">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="69846-209">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="69846-209">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="69846-210">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="69846-210">AzureRM.Websites</span></span>
* <span data-ttu-id="69846-211">Nowe polecenie cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłe wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="69846-211">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="69846-212">Nowe polecenia cmdlet New-AzureRMWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="69846-212">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="69846-213">6.9.0 — wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="69846-213">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="69846-214">Ogólne</span><span class="sxs-lookup"><span data-stu-id="69846-214">General</span></span>
* <span data-ttu-id="69846-215">Element AzureRM.SignalR został dodany do modułu zbiorczego AzureRM</span><span class="sxs-lookup"><span data-stu-id="69846-215">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="69846-216">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="69846-216">AzureRM.Profile</span></span>
* <span data-ttu-id="69846-217">Drobne zmiany wspólnego kodu magazynu</span><span class="sxs-lookup"><span data-stu-id="69846-217">Minor changes to the storage common code</span></span>
* <span data-ttu-id="69846-218">Zaktualizowano pliki pomocy w celu uwzględnienia pełnych typów parametrów.</span><span class="sxs-lookup"><span data-stu-id="69846-218">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="69846-219">Zmieniono opcję -ServicePrincipal na nieobowiązkową w zestawie parametrów ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69846-219">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="69846-220">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="69846-220">Azure.Storage</span></span>
* <span data-ttu-id="69846-221">Obsługa tworzenia kontekstu magazynu przy użyciu protokołu OAuth.</span><span class="sxs-lookup"><span data-stu-id="69846-221">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="69846-222">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="69846-222">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="69846-223">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="69846-223">AzureRM.Cdn</span></span>
* <span data-ttu-id="69846-224">Dodano element Standard_Microsoft w jednostce SKU cen usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="69846-224">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="69846-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="69846-225">AzureRM.Compute</span></span>
* <span data-ttu-id="69846-226">Przeniesiono zależności magazynu kluczy i magazynu do zależności wspólnych</span><span class="sxs-lookup"><span data-stu-id="69846-226">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="69846-227">Dodano obsługę kolejnych rozmiarów maszyn wirtualnych do poleceń cmdlet funkcji AEM</span><span class="sxs-lookup"><span data-stu-id="69846-227">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="69846-228">Dodano parametr PublicIPPrefix do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="69846-228">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="69846-229">Dodano parametr ResourceId do polecenia cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="69846-229">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="69846-230">Dodano polecenie cmdlet Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="69846-230">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="69846-231">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="69846-231">AzureRM.Dns</span></span>
* <span data-ttu-id="69846-232">Dodano obsługę rekordu aliasu podczas tworzenia rekordów DNS</span><span class="sxs-lookup"><span data-stu-id="69846-232">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="69846-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="69846-233">AzureRM.Insights</span></span>
* <span data-ttu-id="69846-234">Rozwiązano problemy nr 6833 i 7102 (obszar ustawień diagnostycznych)</span><span class="sxs-lookup"><span data-stu-id="69846-234">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="69846-235">Problemy z nazwą domyślną, np. „usługa”, podczas tworzenia i tworzenia/pobierania listy ustawień diagnostycznych</span><span class="sxs-lookup"><span data-stu-id="69846-235">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="69846-236">Problemy z tworzeniem ustawień diagnostycznych przy użyciu kategorii</span><span class="sxs-lookup"><span data-stu-id="69846-236">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="69846-237">Dodano komunikat o zakończeniu obsługi parametrów ziarn czasu metryk</span><span class="sxs-lookup"><span data-stu-id="69846-237">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="69846-238">Parametry typu Timegrain są nadal akceptowane (jest to zmiana niepowodująca niezgodności), ale są one ignorowane w zapleczu, ponieważ tylko wersja PT1M jest prawidłowa</span><span class="sxs-lookup"><span data-stu-id="69846-238">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="69846-239">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="69846-239">AzureRM.Network</span></span>
* <span data-ttu-id="69846-240">Zmiany poleceń cmdlet usługi LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69846-240">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="69846-241">LoadBalancerInboundNatPoolConfig: dodano parametry IdleTimeoutInMinutes, EnableFloatingIp i EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="69846-241">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="69846-242">LoadBalancerInboundNatRuleConfig: dodano parametr EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="69846-242">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="69846-243">LoadBalancerRuleConfig: dodano parametr EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="69846-243">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="69846-244">LoadBalancerProbeConfig: dodano obsługę wartości „Https” dla parametru Protocol</span><span class="sxs-lookup"><span data-stu-id="69846-244">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="69846-245">Dodano nowe polecenia dla nowego zasobu podrzędnego OutboundRule usługi LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69846-245">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="69846-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69846-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="69846-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69846-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="69846-248">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69846-248">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="69846-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69846-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="69846-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="69846-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="69846-251">Dodano nową właściwość HostedWorkloads dla interfejsu PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="69846-251">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="69846-252">Dodano nowe polecenia cmdlet dla funkcji Azure Firewall za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="69846-252">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="69846-253">Dodano polecenie Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="69846-253">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="69846-254">Dodano polecenie Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="69846-254">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="69846-255">Dodano polecenie New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="69846-255">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="69846-256">Dodano polecenie Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="69846-256">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="69846-257">Dodano polecenie New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="69846-257">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="69846-258">Dodano polecenie New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="69846-258">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="69846-259">Dodano polecenie New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="69846-259">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="69846-260">Dodano polecenie New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="69846-260">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="69846-261">Dodano polecenie New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="69846-261">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="69846-262">Dodano polecenie New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="69846-262">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="69846-263">Dodano obsługę zaufanego certyfikatu głównego i konfiguracji skalowania automatycznego w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="69846-263">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="69846-264">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="69846-264">New Cmdlets added:</span></span>
      - <span data-ttu-id="69846-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="69846-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="69846-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="69846-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="69846-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="69846-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="69846-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="69846-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="69846-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="69846-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="69846-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="69846-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="69846-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="69846-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="69846-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="69846-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="69846-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="69846-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="69846-274">Zaktualizowano polecenia cmdlet przy użyciu opcjonalnego parametru -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="69846-274">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="69846-275">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69846-275">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="69846-276">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69846-276">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="69846-277">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="69846-277">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="69846-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="69846-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="69846-279">Zaktualizowano polecenia cmdlet przy użyciu opcjonalnego parametru -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="69846-279">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="69846-280">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69846-280">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="69846-281">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69846-281">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="69846-282">Dodano polecenie cmdlet dla punktu końcowego interfejsu Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="69846-282">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="69846-283">Dodano obsługę wielu prefiksów adresów w podsieci.</span><span class="sxs-lookup"><span data-stu-id="69846-283">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="69846-284">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="69846-284">Updated cmdlets:</span></span>
  - <span data-ttu-id="69846-285">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="69846-285">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="69846-286">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="69846-286">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="69846-287">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="69846-287">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="69846-288">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="69846-288">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="69846-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="69846-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="69846-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="69846-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="69846-291">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="69846-291">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="69846-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="69846-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="69846-293">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="69846-293">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="69846-294">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="69846-294">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="69846-295">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="69846-295">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="69846-296">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="69846-296">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="69846-297">New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="69846-297">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="69846-298">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="69846-298">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="69846-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="69846-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="69846-300">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="69846-300">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="69846-301">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="69846-301">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="69846-302">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="69846-302">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="69846-303">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="69846-303">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="69846-304">Dodano polecenia cmdlet na potrzeby delegowania podsieci.</span><span class="sxs-lookup"><span data-stu-id="69846-304">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="69846-305">New-AzureRmDelegation: tworzy nowe delegowanie, które można dodać do podsieci</span><span class="sxs-lookup"><span data-stu-id="69846-305">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="69846-306">Remove-AzureRmDelegation: pobiera podsieć i usuwa z niej podaną nazwę delegowania</span><span class="sxs-lookup"><span data-stu-id="69846-306">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="69846-307">Add-AzureRmDelegation: pobiera podsieć i dodaje do niej podaną nazwę usługi jako delegowanie</span><span class="sxs-lookup"><span data-stu-id="69846-307">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="69846-308">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="69846-308">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="69846-309">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="69846-309">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="69846-310">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="69846-310">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="69846-311">Obsługa dysków zarządzanych</span><span class="sxs-lookup"><span data-stu-id="69846-311">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="69846-312">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="69846-312">AzureRM.RedisCache</span></span>
* <span data-ttu-id="69846-313">Zaktualizowano zależność szczegółowych informacji.</span><span class="sxs-lookup"><span data-stu-id="69846-313">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="69846-314">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="69846-314">AzureRM.Resources</span></span>
* <span data-ttu-id="69846-315">Zaktualizowano polecenie New-AzureRmResourceGroupDeployment przy użyciu nowego parametru RollbackAction</span><span class="sxs-lookup"><span data-stu-id="69846-315">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="69846-316">Dodano obsługę elementu OnErrorDeployment przy użyciu nowego parametru.</span><span class="sxs-lookup"><span data-stu-id="69846-316">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="69846-317">Obsługa tożsamości zarządzanej w przypisaniach zasad.</span><span class="sxs-lookup"><span data-stu-id="69846-317">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="69846-318">Parametry z wartościami domyślnymi nie są już wymagane podczas przypisywania zasad za pomocą polecenia „New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="69846-318">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="69846-319">Dodano nowe polecenie cmdlet Get-AzureRmPolicyAlias służące do pobierania aliasów zasad</span><span class="sxs-lookup"><span data-stu-id="69846-319">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="69846-320">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="69846-320">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="69846-321">Rozwiązano problem nr 7161</span><span class="sxs-lookup"><span data-stu-id="69846-321">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="69846-322">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="69846-322">AzureRM.SignalR</span></span>
* <span data-ttu-id="69846-323">Zaktualizowano nazwy jednostek SKU Bezpłatna_F1 i Standardowa_S1</span><span class="sxs-lookup"><span data-stu-id="69846-323">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="69846-324">Dodano pole wersji do obiektu PSSignalRResource i parametry połączenia do obiektu PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="69846-324">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="69846-325">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="69846-325">AzureRM.Storage</span></span>
* <span data-ttu-id="69846-326">Obsługa zasad niezmienności w elemencie AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="69846-326">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="69846-327">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="69846-327">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="69846-328">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="69846-328">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="69846-329">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="69846-329">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="69846-330">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="69846-330">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="69846-331">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="69846-331">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="69846-332">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="69846-332">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="69846-333">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="69846-333">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="69846-334">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="69846-334">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="69846-335">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="69846-335">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="69846-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="69846-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="69846-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="69846-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="69846-338">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="69846-338">AzureRM.Websites</span></span>
* <span data-ttu-id="69846-339">Dodano dwa nowe polecenia cmdlet: Get-AzureRmDeletedWebApp i Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="69846-339">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="69846-340">New-AzureRmAppServicePlan — dodano przełącznik funkcji Hyper-V na potrzeby tworzenia planu usługi App Service przy użyciu kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="69846-340">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="69846-341">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot — dodano nowe parametry (ciąg –ContainerRegistryUser -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) na potrzeby tworzenia aplikacji kontenera systemu Windows oraz zarządzania nią</span><span class="sxs-lookup"><span data-stu-id="69846-341">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="69846-342">6.8.1 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="69846-342">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="69846-343">Ogólne</span><span class="sxs-lookup"><span data-stu-id="69846-343">General</span></span>
* <span data-ttu-id="69846-344">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="69846-344">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="69846-345">Zaktualizowano wspólne zestawy środowiska uruchomieniowego</span><span class="sxs-lookup"><span data-stu-id="69846-345">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="69846-346">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="69846-346">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="69846-347">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="69846-347">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="69846-348">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="69846-348">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="69846-349">Polecenia cmdlet Import-AzureRmApiManagementApi i \*-AzureRmApiManagementCertificate teraz obsługują ścieżki względne</span><span class="sxs-lookup"><span data-stu-id="69846-349">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="69846-350">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="69846-350">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="69846-351">CertificateInformation to możliwa do ustawienia właściwość pozwalająca poleceniu cmdlet Set-AzureRmApiManagement poprawnie działać.</span><span class="sxs-lookup"><span data-stu-id="69846-351">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="69846-352">Rozwiązano przez aktualizację do pakietu nuget 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="69846-352">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="69846-353">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="69846-353">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="69846-354">W filtrze Odata naprawiono wyszukiwanie według nazwy dla produktu</span><span class="sxs-lookup"><span data-stu-id="69846-354">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="69846-355">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="69846-355">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="69846-356">W filtrze Odata naprawiono wyszukiwanie według nazwy dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="69846-356">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="69846-357">Dodano obsługę rejestratora AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="69846-357">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="69846-358">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="69846-358">AzureRM.Compute</span></span>
* <span data-ttu-id="69846-359">Naprawiono problem polegający na braku elementu docelowego w danych wyjściowych błędu.</span><span class="sxs-lookup"><span data-stu-id="69846-359">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="69846-360">Rozwiązano problem z typem konta magazynu dla maszyny wirtualnej z dyskiem zarządzanym</span><span class="sxs-lookup"><span data-stu-id="69846-360">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="69846-361">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="69846-361">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="69846-362">Naprawiono polecenia cmdlet rozszerzenia AEM dla innych środowisk, na przykład Azure — Chiny</span><span class="sxs-lookup"><span data-stu-id="69846-362">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="69846-363">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="69846-363">AzureRM.Network</span></span>
* <span data-ttu-id="69846-364">Zmieniono domyślną prezentację danych wyjściowych polecenia cmdlet na widok tabeli</span><span class="sxs-lookup"><span data-stu-id="69846-364">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="69846-365">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="69846-365">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="69846-366">Naprawiono błąd w poleceniu Update-AzureRmPowerBIEmbeddedCapacity występujący podczas próby skalowania wstrzymanej pojemności</span><span class="sxs-lookup"><span data-stu-id="69846-366">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="69846-367">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="69846-367">AzureRM.Resources</span></span>
* <span data-ttu-id="69846-368">Rozwiązano problem z tworzeniem aplikacji zarządzanych z witryny MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="69846-368">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="69846-369">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="69846-369">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="69846-370">Rozwiązane problemy</span><span class="sxs-lookup"><span data-stu-id="69846-370">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="69846-371">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="69846-371">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="69846-372">Dodano obsługę metody routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="69846-372">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="69846-373">Nowy parametr „MaxReturn” dla routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="69846-373">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="69846-374">Dodano obsługę metody routingu Subnet</span><span class="sxs-lookup"><span data-stu-id="69846-374">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="69846-375">Obsługa zakresów adresów IP (podsieci) w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="69846-375">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="69846-376">Dodano obsługę nagłówków niestandardowych w profilach</span><span class="sxs-lookup"><span data-stu-id="69846-376">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="69846-377">Dodano obsługę zakresów kodów oczekiwanego stanu w profilach</span><span class="sxs-lookup"><span data-stu-id="69846-377">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="69846-378">Dodano obsługę nagłówków niestandardowych w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="69846-378">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="69846-379">6.8.0 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="69846-379">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="69846-380">Ogólne</span><span class="sxs-lookup"><span data-stu-id="69846-380">General</span></span>
* <span data-ttu-id="69846-381">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="69846-381">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="69846-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="69846-382">AzureRM.Profile</span></span>
* <span data-ttu-id="69846-383">Dodano właściwość wygasania do tokenów zwracanych podczas operacji Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="69846-383">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="69846-384">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="69846-384">AzureRM.Compute</span></span>
* <span data-ttu-id="69846-385">Naprawiono problem polegający na braku elementu docelowego w danych wyjściowych błędu.</span><span class="sxs-lookup"><span data-stu-id="69846-385">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="69846-386">Rozwiązano problem z typem konta magazynu dla maszyny wirtualnej z dyskiem zarządzanym</span><span class="sxs-lookup"><span data-stu-id="69846-386">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="69846-387">Naprawiono polecenia cmdlet rozszerzenia AEM dla innych środowisk, na przykład Azure — Chiny</span><span class="sxs-lookup"><span data-stu-id="69846-387">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="69846-388">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="69846-388">AzureRM.IotHub</span></span>
* <span data-ttu-id="69846-389">Naprawiono przykłady dla poleceń New-AzureRmIotHubExportDevices i New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="69846-389">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="69846-390">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="69846-390">AzureRM.Network</span></span>
* <span data-ttu-id="69846-391">Zmieniono domyślną reprezentację modeli na widok tabeli</span><span class="sxs-lookup"><span data-stu-id="69846-391">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="69846-392">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="69846-392">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="69846-393">Naprawiono błąd w poleceniu Update-AzureRmPowerBIEmbeddedCapacity występujący podczas próby skalowania wstrzymanej pojemności</span><span class="sxs-lookup"><span data-stu-id="69846-393">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="69846-394">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="69846-394">AzureRM.Resources</span></span>
* <span data-ttu-id="69846-395">Rozwiązano problem z tworzeniem aplikacji zarządzanej z witryny MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="69846-395">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="69846-396">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="69846-396">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="69846-397">Rozwiązano problemy</span><span class="sxs-lookup"><span data-stu-id="69846-397">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="69846-398">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="69846-398">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="69846-399">Obsługa metody routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="69846-399">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="69846-400">Nowy parametr „MaxReturn” dla routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="69846-400">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="69846-401">Obsługa metody routingu Subnet</span><span class="sxs-lookup"><span data-stu-id="69846-401">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="69846-402">Obsługa zakresów adresów IP (podsieci) w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="69846-402">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="69846-403">Obsługa nagłówków niestandardowych w profilach</span><span class="sxs-lookup"><span data-stu-id="69846-403">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="69846-404">Obsługa zakresów kodów oczekiwanego stanu w profilach</span><span class="sxs-lookup"><span data-stu-id="69846-404">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="69846-405">Obsługa nagłówków niestandardowych w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="69846-405">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="69846-406">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="69846-406">AzureRM.Websites</span></span>
* <span data-ttu-id="69846-407">Rozwiązano problem z niepoprawnie ustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="69846-407">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="69846-408">6.7.0 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="69846-408">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="69846-409">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="69846-409">AzureRM.Profile</span></span>
* <span data-ttu-id="69846-410">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="69846-411">Dodaj identyfikator użytkownika do domyślnej nazwy kontekstu, aby uniknąć konfliktów kontekstów</span><span class="sxs-lookup"><span data-stu-id="69846-411">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="69846-412">Rozwiązanie problemu z poleceniem Clear-AzureRmContext, który powodował problemy w przypadku wybrania kontekstu nr 6398</span><span class="sxs-lookup"><span data-stu-id="69846-412">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="69846-413">Umożliwienie przekazywania domeny dzierżawy do parametru „-TenantId” polecenia „Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="69846-413">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="69846-414">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="69846-414">Azure.Storage</span></span>
* <span data-ttu-id="69846-415">Usunięcie ograniczenia limitu przydziału udziału plików platformy Azure do 5 TB</span><span class="sxs-lookup"><span data-stu-id="69846-415">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="69846-416">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="69846-416">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="69846-417">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="69846-417">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="69846-418">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-418">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="69846-419">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="69846-419">Azure.AnalysisServices</span></span>
* <span data-ttu-id="69846-420">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-420">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="69846-421">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="69846-421">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="69846-422">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-422">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="69846-423">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="69846-423">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="69846-424">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-424">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="69846-425">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="69846-425">AzureRM.Automation</span></span>
* <span data-ttu-id="69846-426">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-426">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="69846-427">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="69846-427">AzureRM.Backup</span></span>
* <span data-ttu-id="69846-428">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-428">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="69846-429">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="69846-429">AzureRM.Batch</span></span>
* <span data-ttu-id="69846-430">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-430">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="69846-431">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="69846-431">AzureRM.Billing</span></span>
* <span data-ttu-id="69846-432">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-432">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="69846-433">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="69846-433">AzureRM.Cdn</span></span>
* <span data-ttu-id="69846-434">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-434">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="69846-435">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="69846-435">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="69846-436">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-436">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="69846-437">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="69846-437">AzureRM.Compute</span></span>
* <span data-ttu-id="69846-438">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-438">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="69846-439">Dodanie parametru EvictionPolicy do polecenia New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="69846-439">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="69846-440">Użycie domyślnej lokalizacji w parametrze DiskFileParameterSet polecenia New-AzureRmVm, jeśli nie określono lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="69846-440">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="69846-441">Naprawienie opisu parametru w poleceniu Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="69846-441">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="69846-442">Naprawienie działania polecenia cmdlet Get-AzureRmVMDiskEncryptionStatus w przypadku niektórych scenariuszy powiązanych z pojedynczym przebiegiem</span><span class="sxs-lookup"><span data-stu-id="69846-442">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="69846-443">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="69846-443">AzureRM.Consumption</span></span>
* <span data-ttu-id="69846-444">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-444">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="69846-445">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="69846-445">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="69846-446">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-446">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="69846-447">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="69846-447">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="69846-448">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="69846-449">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="69846-449">AzureRM.DataFactories</span></span>
* <span data-ttu-id="69846-450">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="69846-451">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="69846-451">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="69846-452">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="69846-453">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="69846-453">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="69846-454">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="69846-455">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="69846-455">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="69846-456">Naprawienie debugowania, gdy parametr DebugPreference jest ustawiany w wierszu polecenia programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="69846-456">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="69846-457">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="69846-457">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="69846-458">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-458">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="69846-459">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="69846-459">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="69846-460">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="69846-460">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="69846-461">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-461">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="69846-462">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="69846-462">AzureRM.Dns</span></span>
* <span data-ttu-id="69846-463">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-463">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="69846-464">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="69846-464">AzureRM.EventGrid</span></span>
* <span data-ttu-id="69846-465">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-465">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="69846-466">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="69846-466">AzureRM.EventHub</span></span>
* <span data-ttu-id="69846-467">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-467">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="69846-468">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="69846-468">AzureRM.HDInsight</span></span>
* <span data-ttu-id="69846-469">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-469">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="69846-470">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="69846-470">AzureRM.Insights</span></span>
* <span data-ttu-id="69846-471">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-471">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="69846-472">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="69846-472">AzureRM.IotHub</span></span>
* <span data-ttu-id="69846-473">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="69846-474">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="69846-474">AzureRM.KeyVault</span></span>
* <span data-ttu-id="69846-475">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="69846-476">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="69846-476">AzureRM.LogicApp</span></span>
* <span data-ttu-id="69846-477">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="69846-478">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="69846-478">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="69846-479">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="69846-480">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="69846-480">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="69846-481">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="69846-482">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="69846-482">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="69846-483">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="69846-484">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="69846-484">AzureRM.Media</span></span>
* <span data-ttu-id="69846-485">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="69846-486">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="69846-486">AzureRM.Network</span></span>
* <span data-ttu-id="69846-487">Dodano przykład dla polecenia Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="69846-487">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="69846-488">Dodano przykłady i opisy dla poleceń Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey oraz New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="69846-488">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="69846-489">Dodano przykłady dla poleceń Remove-AzureRmVirtualNetworkGatewayIpConfig i Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="69846-489">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="69846-490">Dodano przykład dla polecenia Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="69846-490">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="69846-491">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="69846-491">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="69846-492">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="69846-492">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="69846-493">Ponownie wygenerowano polecenia cmdlet ApplicationSecurityGroup, RouteTable i Usage z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="69846-493">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="69846-494">Poprawiono czytelność komunikatu o błędzie dla polecenia Get-AzureRmVirtualNetworkSubnetConfig podczas próby pobrania podsieci, która nie istnieje</span><span class="sxs-lookup"><span data-stu-id="69846-494">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="69846-495">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="69846-495">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="69846-496">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-496">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="69846-497">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="69846-497">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="69846-498">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-498">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="69846-499">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="69846-499">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="69846-500">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-500">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="69846-501">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="69846-501">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="69846-502">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-502">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="69846-503">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="69846-503">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="69846-504">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-504">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="69846-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="69846-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="69846-506">Dodano filtr zasad do polecenia cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="69846-506">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="69846-507">Polecenie zwraca listę elementów kopii zapasowej chronionych przez zasady o danym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="69846-507">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="69846-508">Zaktualizowano przestrzeń nazw Microsoft.Azure.Management.RecoveryServices.Backup do wersji 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="69846-508">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="69846-509">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-509">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="69846-510">Dodano parametr TargetResourceGroupName do polecenia Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="69846-510">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="69846-511">Grupa zasobów, do której są przywracane dyski zarządzane.</span><span class="sxs-lookup"><span data-stu-id="69846-511">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="69846-512">Ma zastosowanie do wykonywania kopii zapasowych maszyn wirtualnych z dyskami zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="69846-512">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="69846-513">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="69846-513">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="69846-514">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-514">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="69846-515">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="69846-515">AzureRM.RedisCache</span></span>
* <span data-ttu-id="69846-516">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="69846-517">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="69846-517">AzureRM.Relay</span></span>
* <span data-ttu-id="69846-518">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="69846-519">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="69846-519">AzureRM.Resources</span></span>
* <span data-ttu-id="69846-520">Obsługa wdrażania szablonów w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="69846-520">Support template deployment at subscription scope.</span></span> <span data-ttu-id="69846-521">Dodanie nowych poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="69846-521">Add new Cmdlets:</span></span>
    - <span data-ttu-id="69846-522">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="69846-522">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="69846-523">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="69846-523">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="69846-524">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="69846-524">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="69846-525">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="69846-525">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="69846-526">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="69846-526">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="69846-527">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="69846-527">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="69846-528">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="69846-528">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="69846-529">Rozwiązanie problemu, w przypadku którego podczas przekazywania kontekstu do polecenia Set-AzureRmResource jest zgłaszany błąd</span><span class="sxs-lookup"><span data-stu-id="69846-529">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="69846-530">Naprawienie przykładu polecenia New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="69846-530">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="69846-531">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-531">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="69846-532">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="69846-532">AzureRM.Scheduler</span></span>
* <span data-ttu-id="69846-533">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-533">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="69846-534">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="69846-534">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="69846-535">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-535">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="69846-536">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="69846-536">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="69846-537">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-537">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="69846-538">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="69846-538">AzureRM.Sql</span></span>
* <span data-ttu-id="69846-539">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-539">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="69846-540">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="69846-540">AzureRM.Storage</span></span>
* <span data-ttu-id="69846-541">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-541">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="69846-542">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="69846-542">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="69846-543">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-543">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="69846-544">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="69846-544">AzureRM.Tags</span></span>
* <span data-ttu-id="69846-545">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-545">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="69846-546">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="69846-546">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="69846-547">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-547">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="69846-548">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="69846-548">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="69846-549">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-549">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="69846-550">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="69846-550">AzureRM.Websites</span></span>
* <span data-ttu-id="69846-551">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="69846-552">6.6.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="69846-552">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="69846-553">Ogólne</span><span class="sxs-lookup"><span data-stu-id="69846-553">General</span></span>
* <span data-ttu-id="69846-554">Zaktualizowano wszystkie pliki pomocy, aby uwzględniały pełne typy parametrów i poprawne typy wejściowe/wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="69846-554">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="69846-555">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="69846-555">AzureRM.Profile</span></span>
* <span data-ttu-id="69846-556">Zaktualizowano bibliotekę Common.Strategy, aby mogła ona weryfikować, czy bieżąca konfiguracja zasobu jest zgodna z zasobem docelowym.</span><span class="sxs-lookup"><span data-stu-id="69846-556">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="69846-557">Dodano typy ps1xml do biblioteki Common.Storage</span><span class="sxs-lookup"><span data-stu-id="69846-557">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="69846-558">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="69846-558">Azure.Storage</span></span>
* <span data-ttu-id="69846-559">Dodano obsługę pobierania kontekstu magazynu z profilu DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69846-559">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="69846-560">Dodano atrybut Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69846-560">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="69846-561">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="69846-561">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="69846-562">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="69846-562">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="69846-563">Usunięto usterkę w maperze Automapper dotyczącą translacji obiektu PsApiManagementApi na obiekt ApiContract</span><span class="sxs-lookup"><span data-stu-id="69846-563">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="69846-564">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="69846-564">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="69846-565">Usunięto usterkę w elemencie File.Save dotyczącą przeciążania typem kodowania</span><span class="sxs-lookup"><span data-stu-id="69846-565">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="69846-566">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="69846-566">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="69846-567">Uaktualniono menedżer NuGet do wersji 4.0.3, co rozwiązuje problem z występowaniem wyjątku dotyczącego wzorca w parametrze apiId</span><span class="sxs-lookup"><span data-stu-id="69846-567">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="69846-568">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="69846-568">AzureRM.Compute</span></span>
* <span data-ttu-id="69846-569">Rozwiązanie problemu powodującego zakończenie niepowodzeniem tworzenia maszyny wirtualnej przy użyciu zestawu DiskFileParameterSet w poleceniu New-AzureRmVm z powodu zmiany nazwy typu konta magazynu PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="69846-569">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="69846-570">Poprawienie polecenia cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="69846-570">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="69846-571">Zaktualizowanie polecenia Get-AzureRmAvailabilitySet, aby umożliwić zwrócenie listy wszystkich zestawów dostępności w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="69846-571">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="69846-572">(Parametr ResouceGroupName jest teraz opcjonalny).</span><span class="sxs-lookup"><span data-stu-id="69846-572">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="69846-573">Zaktualizowanie zestawu SimpleParameterSet polecenia „New-AzureRmVm”, aby umożliwić korzystanie z przyspieszonej łączności sieciowej na kwalifikujących się maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="69846-573">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="69846-574">Zaktualizowanie prostego zestawu parametrów polecenia New-AzureRmVmss w taki sposób, aby tworzenie zestawu skalowania maszyn wirtualnych kończyło się niepowodzeniem, gdy moduł równoważenia obciążenia określony przez użytkownika już istnieje.</span><span class="sxs-lookup"><span data-stu-id="69846-574">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="69846-575">Zaktualizowanie przykładu dla polecenia New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="69846-575">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="69846-576">Dodanie przykładu dla polecenia „New-AzureRmVM”</span><span class="sxs-lookup"><span data-stu-id="69846-576">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="69846-577">Zaktualizowanie opisu polecenia Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="69846-577">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="69846-578">Zaktualizowanie przykładu 1 dla polecenia Set-AzureRmVMBginfoExtension przez poprawienie pisowni i prefiksu.</span><span class="sxs-lookup"><span data-stu-id="69846-578">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="69846-579">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="69846-579">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="69846-580">Zaktualizowano zestaw ADF .Net SDK do wersji 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="69846-580">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="69846-581">Obsługa udostępniania własnego środowiska Integration Runtime dla wielu fabryk danych.</span><span class="sxs-lookup"><span data-stu-id="69846-581">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="69846-582">Dodanie nowego parametru -SharedIntegrationRuntimeResourceId do polecenia cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-582">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="69846-583">Dodanie nowego opcjonalnego parametru -LinkedDataFactoryName do polecenia cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="69846-583">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="69846-584">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="69846-584">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="69846-585">Zaktualizowano zestaw SDK płaszczyzny danych (Microsoft.Azure.DataLake.Store) do wersji 1.1.9</span><span class="sxs-lookup"><span data-stu-id="69846-585">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="69846-586">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="69846-586">AzureRM.EventHub</span></span>
* <span data-ttu-id="69846-587">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="69846-587">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="69846-588">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="69846-588">AzureRM.Insights</span></span>
* <span data-ttu-id="69846-589">Naprawiono formatowanie typu OutputType w plikach pomocy</span><span class="sxs-lookup"><span data-stu-id="69846-589">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="69846-590">Użycie zestawu Microsoft.Azure.Management.Monitor SDK w wersji 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="69846-590">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="69846-591">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="69846-591">AzureRM.KeyVault</span></span>
* <span data-ttu-id="69846-592">Rozwiązanie problemu z potokowaniem w poleceniu Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="69846-592">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="69846-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="69846-593">AzureRM.Network</span></span>
* <span data-ttu-id="69846-594">Dodano przykłady dla poleceń cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="69846-594">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="69846-595">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="69846-595">AzureRM.Resources</span></span>
* <span data-ttu-id="69846-596">Rozwiązanie problemu w przypadku podawania zarówno wartości, jak i nazwy tagu w poleceniu „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="69846-596">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="69846-597">Naprawienie scenariusza potokowania w poleceniu „Set-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="69846-597">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="69846-598">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="69846-598">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="69846-599">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="69846-599">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="69846-600">Rozwiązano kilka problemów</span><span class="sxs-lookup"><span data-stu-id="69846-600">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="69846-601">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="69846-601">AzureRM.Sql</span></span>
* <span data-ttu-id="69846-602">Dodanie obsługi zaawansowanej ochrony serwera przed zagrożeniami przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="69846-602">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="69846-603">Enable-AzureRmSqlServerAdvancedThreatProtection, Disable-AzureRmSqlServerAdvancedThreatProtection, Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="69846-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="69846-604">Dodanie obsługi oceny luk w zabezpieczeniach przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="69846-604">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="69846-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="69846-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="69846-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="69846-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="69846-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan, Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord, Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="69846-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="69846-608">Poprawiono przykład w poleceniu Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="69846-608">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="69846-609">Naprawienie niepoprawnej obsługi daty/godziny w przypadku podstawowej kultury innej niż Stany Zjednoczone w poleceniu Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="69846-609">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="69846-610">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="69846-610">AzureRM.Storage</span></span>
* <span data-ttu-id="69846-611">Dodanie atrybutu Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="69846-611">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="69846-612">Pokazywanie danych wyjściowych polecenia cmdlet StorageAccount w widoku tabeli</span><span class="sxs-lookup"><span data-stu-id="69846-612">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="69846-613">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="69846-613">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="69846-614">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="69846-614">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="69846-615">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="69846-615">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="69846-616">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="69846-616">AzureRM.Tags</span></span>
* <span data-ttu-id="69846-617">Usunięcie niepoprawnej informacji z pomocy polecenia cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="69846-617">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="69846-618">6.5.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="69846-618">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="69846-619">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="69846-619">AzureRM.Profile</span></span>
* <span data-ttu-id="69846-620">Zaktualizowano pomoc dotyczącą polecenia „Get-AzureRmContextAutosaveSetting”</span><span class="sxs-lookup"><span data-stu-id="69846-620">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="69846-621">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="69846-621">Azure.Storage</span></span>
* <span data-ttu-id="69846-622">Dodano obsługę przekazywania obiektu blob lub pliku z tokenem sygnatury dostępu współdzielonego tylko do odczytu</span><span class="sxs-lookup"><span data-stu-id="69846-622">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="69846-623">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="69846-623">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="69846-624">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="69846-624">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="69846-625">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="69846-625">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="69846-626">Dodano wymaganą właściwość ResourceGroupName do usługi AS.</span><span class="sxs-lookup"><span data-stu-id="69846-626">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="69846-627">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="69846-627">AzureRM.Automation</span></span>
* <span data-ttu-id="69846-628">Zaktualizowano pomoc i dodano przykład polecenia „New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="69846-628">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="69846-629">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="69846-629">AzureRM.Compute</span></span>
* <span data-ttu-id="69846-630">Dodano parametr -Tag do polecenia Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="69846-630">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="69846-631">Dodano przykład polecenia „Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="69846-631">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="69846-632">Dodano przykłady polecenia „Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="69846-632">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="69846-633">Zaktualizowano pomoc dotyczącą polecenia „Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="69846-633">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="69846-634">Zaktualizowano atrybut SimpleParameterSet dla polecenia New-AzureRmVmss, aby domyślnie ustawiał parametr SinglePlacementGroup na wartość false oraz dodano parametr przełącznika „SinglePlacementGroup” umożliwiający użytkownikowi tworzenie zestawów VMSS w pojedynczej grupie umieszczania.</span><span class="sxs-lookup"><span data-stu-id="69846-634">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="69846-635">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="69846-635">AzureRM.EventHub</span></span>
* <span data-ttu-id="69846-636">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSEventHubDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="69846-636">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="69846-637">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="69846-637">AzureRM.KeyVault</span></span>
* <span data-ttu-id="69846-638">Zaktualizowano komunikat o błędzie dla polecenia Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="69846-638">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="69846-639">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="69846-639">AzureRM.LogicApp</span></span>
* <span data-ttu-id="69846-640">Naprawiono błąd „nie można rozpoznać zestawu parametrów” w poleceniu New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="69846-640">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="69846-641">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="69846-641">AzureRM.Network</span></span>
* <span data-ttu-id="69846-642">Włączono komunikację równorzędną między sieciami wirtualnymi w wielu dzierżawach dla polecenia Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="69846-642">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="69846-643">Zaktualizowano poniższe polecenia cmdlet usługi Application Gateway</span><span class="sxs-lookup"><span data-stu-id="69846-643">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="69846-644">New-AzureRmApplicationGateway: dodano obsługę flagi EnableFIPS i stref</span><span class="sxs-lookup"><span data-stu-id="69846-644">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="69846-645">New-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="69846-645">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="69846-646">Set-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="69846-646">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="69846-647">Ponownie wygenerowano polecenia cmdlet RouteTable z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="69846-647">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="69846-648">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="69846-648">AzureRM.Relay</span></span>
* <span data-ttu-id="69846-649">Zaktualizowano pliki markdown, naprawiono problem z nazwą parametru w przykładzie</span><span class="sxs-lookup"><span data-stu-id="69846-649">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="69846-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="69846-650">AzureRM.Resources</span></span>
* <span data-ttu-id="69846-651">Zaktualizowano polecenia cmdlet Roleassignment i roledefinition:</span><span class="sxs-lookup"><span data-stu-id="69846-651">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="69846-652">Usunięto dodatkowe wywołania polecenia roledefinition wykonywane w ramach stronicowania.</span><span class="sxs-lookup"><span data-stu-id="69846-652">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="69846-653">Naprawiono polecenie cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="69846-653">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="69846-654">Naprawiono funkcjonalność parametru polecenia -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="69846-654">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="69846-655">Rozwiązano problem z poleceniem „Get-AzureRmResource”, który polegał na tym, że w parametrze „-ResourceType” była uwzględniana wielkość liter</span><span class="sxs-lookup"><span data-stu-id="69846-655">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="69846-656">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="69846-656">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="69846-657">Dodano parametry top i skip do poleceń cmdlet „list”</span><span class="sxs-lookup"><span data-stu-id="69846-657">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="69846-658">Dodano polecenia cmdlet migracji przestrzeni nazw z warstwy Standardowa do warstwy Premium:</span><span class="sxs-lookup"><span data-stu-id="69846-658">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="69846-659">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="69846-659">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="69846-660">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="69846-660">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="69846-661">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="69846-661">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="69846-662">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="69846-662">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="69846-663">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="69846-663">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="69846-664">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSServiceBusDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="69846-664">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="69846-665">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="69846-665">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="69846-666">Zaktualizowano przykład dotyczący polecenia „New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="69846-666">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="69846-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="69846-667">AzureRM.Sql</span></span>
* <span data-ttu-id="69846-668">Dodano nowe polecenia cmdlet dla przestrzeni nazw Management.Sql, aby umożliwić klientom dodawanie certyfikatu TDE do wystąpienia programu SQL Server lub wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="69846-668">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="69846-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="69846-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="69846-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="69846-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="69846-671">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="69846-671">AzureRM.Websites</span></span>
* <span data-ttu-id="69846-672">Polecenia `Set-AzureRmWebApp -AssignIdentity` i `Set-AzureRmWebAppSlot -AssignIdentity` po ustawieniu na wartość false spowodują teraz usunięcie właściwości Identity z obiektu lokacji. Usuwany jest także tag podglądu.</span><span class="sxs-lookup"><span data-stu-id="69846-672">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="69846-673">Zaktualizowano przykład dotyczący poleceń `Get-AzureRmWebAppMetrics` i `Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="69846-673">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="69846-674">Polecenie `Set-AzureRmWebApp -PhpVersion` obsługuje wartość off jako prawidłową wersję języka PHP</span><span class="sxs-lookup"><span data-stu-id="69846-674">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="69846-675">6.4.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="69846-675">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="69846-676">Ogólne</span><span class="sxs-lookup"><span data-stu-id="69846-676">General</span></span>
* <span data-ttu-id="69846-677">Naprawiono formatowanie typu OutputType w plikach pomocy dotyczących większości modułów</span><span class="sxs-lookup"><span data-stu-id="69846-677">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="69846-678">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="69846-678">AzureRM.Profile</span></span>
* <span data-ttu-id="69846-679">Dodano atrybut Ps1Xml do podstawowych typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="69846-679">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="69846-680">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="69846-680">AzureRM.Compute</span></span>
* <span data-ttu-id="69846-681">Funkcja tagów adresów IP dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="69846-681">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="69846-682">Dodano polecenie cmdlet „New-AzureRmVmssIpTagConfig”</span><span class="sxs-lookup"><span data-stu-id="69846-682">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="69846-683">Dodano parametr IpTag do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="69846-683">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="69846-684">Funkcja automatycznego wycofywania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="69846-684">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="69846-685">Dodano parametry DisableAutoRollback do poleceń New-AzureRmVmssConfig i Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="69846-685">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="69846-686">Funkcja historii uaktualniania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="69846-686">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="69846-687">Dodano parametr przełącznika OSUpgradeHistory do polecenia Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="69846-687">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="69846-688">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="69846-688">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="69846-689">Dodano obsługę list ACL wykazu przy użyciu następujących poleceń:</span><span class="sxs-lookup"><span data-stu-id="69846-689">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="69846-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="69846-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="69846-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="69846-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="69846-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="69846-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="69846-693">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="69846-693">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="69846-694">Dodano obsługę anulowania i śledzenia postępu dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="69846-694">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="69846-695">Dodano obsługę anulowania dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="69846-695">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="69846-696">Naprawiono opróżnianie komunikatów debugowania dla poleceń cmdlet wykonujących operacje cykliczne</span><span class="sxs-lookup"><span data-stu-id="69846-696">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="69846-697">Naprawiono lokalizację testu poleceń cmdlet DataLake</span><span class="sxs-lookup"><span data-stu-id="69846-697">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="69846-698">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="69846-698">AzureRM.EventHub</span></span>
* <span data-ttu-id="69846-699">Dodano opcjonalny parametr MaxCount do poleceń cmdlet tworzących listę operacji: Get-AzureRmEventHub i Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="69846-699">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="69846-700">Rozwiązano problem z poleceniem cmdlet New-AzureRmEventHub polegający na tym, że podczas tworzenia nowego centrum EventHub był wymagany co najmniej jeden parametr.</span><span class="sxs-lookup"><span data-stu-id="69846-700">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="69846-701">Udostępniono zestaw parametrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="69846-701">Provided Default Parameter set.</span></span>
* <span data-ttu-id="69846-702">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmEventHubKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="69846-702">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="69846-703">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="69846-703">AzureRM.KeyVault</span></span>
* <span data-ttu-id="69846-704">Rozwiązano problem polegający na tym, że wszystkie zasoby były zwracane przez polecenie Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="69846-704">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="69846-705">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="69846-705">AzureRM.Network</span></span>
* <span data-ttu-id="69846-706">Uwidoczniono nowe jednostki SKU dla strefowo nadmiarowych bram VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="69846-706">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="69846-707">Dodano nowe polecenia dla funkcji interfejsów API partnerów usługi ExpressRoute za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="69846-707">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="69846-708">Dodano polecenie Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="69846-708">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="69846-709">Dodano polecenie Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="69846-709">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="69846-710">Dodano polecenie Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="69846-710">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="69846-711">Dodano polecenie Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="69846-711">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="69846-712">Dodano polecenie Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="69846-712">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="69846-713">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="69846-713">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="69846-714">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="69846-714">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="69846-715">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="69846-715">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="69846-716">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="69846-716">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="69846-717">Dodano polecenie cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="69846-717">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="69846-718">To polecenie cmdlet pobiera identyfikator maszyny wirtualnej i sprawdza, czy maszyna wirtualna jest chroniona przez magazyn w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="69846-718">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="69846-719">Jeśli taki magazyn istnieje, polecenie cmdlet wyświetla jego szczegóły.</span><span class="sxs-lookup"><span data-stu-id="69846-719">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="69846-720">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="69846-720">AzureRM.Resources</span></span>
* <span data-ttu-id="69846-721">Zaktualizowano polecenia cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="69846-721">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="69846-722">Dodano obsługę wyświetlania listy wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="69846-722">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="69846-723">Dodano obsługę pobierania poszczególnych przydziałów za pomocą wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="69846-723">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="69846-724">Dodano przełączniki -Effective i -All do parametru kontroli</span><span class="sxs-lookup"><span data-stu-id="69846-724">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="69846-725">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="69846-725">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="69846-726">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="69846-726">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="69846-727">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="69846-727">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="69846-728">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="69846-728">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="69846-729">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="69846-729">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="69846-730">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="69846-730">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="69846-731">Dodano obsługę odwołania do wpisu tajnego KeyVault w parametrach w przypadku używania elementu „TemplateParameterObject” w poleceniu „New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="69846-731">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="69846-732">Rozwiązano problem polegający na tym, że parametr „-EndDate” był ignorowany w poleceniu „New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="69846-732">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="69846-733">Rozwiązano problem polegający na tym, że w poleceniu „Add-AzureRmADGroupMember” używano nieprawidłowego adres URL podczas zgłaszania żądania</span><span class="sxs-lookup"><span data-stu-id="69846-733">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="69846-734">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="69846-734">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="69846-735">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmServiceBusKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="69846-735">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="69846-736">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="69846-736">AzureRM.Sql</span></span>
* <span data-ttu-id="69846-737">Objaśniono punkty przywracania zdefiniowane przez użytkownika dla usługi SQLDW w pomocy polecenia New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="69846-737">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="69846-738">Zaktualizowano dokumentację parametru -ComputeGeneration w kilku poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="69846-738">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="69846-739">6.3.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="69846-739">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="69846-740">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="69846-740">AzureRM.Profile</span></span>
* <span data-ttu-id="69846-741">Zaktualizowano komunikaty o błędach dotyczące polecenia Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="69846-741">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="69846-742">Tworzenie kontekstu dla każdej subskrypcji w przypadku uruchomienia polecenia „Connect-AzureRmAccount” bez wcześniejszego kontekstu</span><span class="sxs-lookup"><span data-stu-id="69846-742">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="69846-743">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="69846-743">Azure.Storage</span></span>
* <span data-ttu-id="69846-744">Dodano informacje dotyczące parametru -Permissions w plikach pomocy.</span><span class="sxs-lookup"><span data-stu-id="69846-744">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="69846-745">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="69846-745">AzureRM.Compute</span></span>
* <span data-ttu-id="69846-746">Polecenie „Get-AzureRmVmDiskEncryptionStatus” — rozwiązano problem zaobserwowany w przypadku maszyn wirtualnych bez dysków z danymi</span><span class="sxs-lookup"><span data-stu-id="69846-746">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="69846-747">Aktualizacja wersji biblioteki klienckiej obliczeń w celu naprawy następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="69846-747">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="69846-748">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="69846-748">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="69846-749">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="69846-749">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="69846-750">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="69846-750">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="69846-751">Naprawiono następujące polecenia cmdlet w celu poprawnego wyświetlania identyfikatora operacji i stanu operacji:</span><span class="sxs-lookup"><span data-stu-id="69846-751">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="69846-752">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="69846-752">Start-AzureRmVM</span></span>
    - <span data-ttu-id="69846-753">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="69846-753">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="69846-754">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="69846-754">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="69846-755">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="69846-755">Set-AzureRmVM</span></span>
    - <span data-ttu-id="69846-756">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="69846-756">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="69846-757">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="69846-757">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="69846-758">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="69846-758">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="69846-759">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="69846-759">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="69846-760">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="69846-760">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="69846-761">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="69846-761">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="69846-762">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="69846-762">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="69846-763">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="69846-763">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="69846-764">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="69846-764">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="69846-765">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="69846-765">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="69846-766">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="69846-766">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="69846-767">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="69846-767">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="69846-768">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="69846-768">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="69846-769">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="69846-769">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="69846-770">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="69846-770">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="69846-771">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="69846-771">AzureRM.EventGrid</span></span>
* <span data-ttu-id="69846-772">Usunięto warunki weryfikacji ValidateNotNullOrEmpty dla elementów SubjectBeginsWith/SubjectEndsWith w poleceniu cmdlet Update-AzureRmEventGridSubscription w celu umożliwienia zmiany tych parametrów na pusty ciąg w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="69846-772">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="69846-773">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="69846-773">AzureRM.KeyVault</span></span>
* <span data-ttu-id="69846-774">Rozwiązano problem polegający na tym, że nie były zwracane tagi w przypadku uruchomienia polecenia Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="69846-774">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="69846-775">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="69846-775">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="69846-776">Publiczne udostępnienie poleceń cmdlet usługi Policy Insights</span><span class="sxs-lookup"><span data-stu-id="69846-776">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="69846-777">Użycie interfejsu API w wersji z 4.04.2018</span><span class="sxs-lookup"><span data-stu-id="69846-777">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="69846-778">Dodano element PolicyDefinitionReferenceId do wyników polecenia Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="69846-778">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="69846-779">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="69846-779">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="69846-780">Dodano parametr -Vault do poleceń cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="69846-780">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="69846-781">W przypadku przekazania to polecenie przesłania polecenie cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="69846-781">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="69846-782">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="69846-782">AzureRM.Sql</span></span>
* <span data-ttu-id="69846-783">Zaktualizowano przykład w pliku pomocy polecenia Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="69846-783">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="69846-784">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="69846-784">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="69846-785">Zaktualizowano plik pomocy polecenia Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="69846-785">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="69846-786">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="69846-786">AzureRM.Websites</span></span>
* <span data-ttu-id="69846-787">Zaktualizowano polecenie „Set-AzureRmWebApp”, aby nie zastępowało elementu AppSettings w przypadku użycia parametru -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="69846-787">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="69846-788">Zaktualizowano polecenie „New-AzureRmWebAppSlot” w celu umożliwienia obsługi parametru AppServicePlan jako parametru opcjonalnego</span><span class="sxs-lookup"><span data-stu-id="69846-788">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="69846-789">6.2.1 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="69846-789">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="69846-790">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="69846-790">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="69846-791">Zaktualizowano model PSWorkspace w celu umożliwienia użycia typu jako parametru w sieci</span><span class="sxs-lookup"><span data-stu-id="69846-791">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="69846-792">6.2.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="69846-792">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="69846-793">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="69846-793">AzureRM.Profile</span></span>
* <span data-ttu-id="69846-794">Naprawiono problem, który polegał na tym, że wersja 10.0.3 pliku Newtonsoft.Json nie była ładowana podczas importowania modułu</span><span class="sxs-lookup"><span data-stu-id="69846-794">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="69846-795">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="69846-795">AzureRM.Compute</span></span>
* <span data-ttu-id="69846-796">Funkcja aktualizacji maszyny wirtualnej usługi VMSS</span><span class="sxs-lookup"><span data-stu-id="69846-796">VMSS VM Update feature</span></span>
    - <span data-ttu-id="69846-797">Dodano polecenia cmdlet „Update-AzureRmVmssVM” i „New-AzureRmVMDataDisk”</span><span class="sxs-lookup"><span data-stu-id="69846-797">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="69846-798">Dodano parametr VirtualMachineScaleSetVM do polecenia cmdlet „Add-AzureRmVMDataDisk” w celu obsługi dodawania dysku danych do maszyny wirtualnej usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="69846-798">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="69846-799">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="69846-799">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="69846-800">Zaktualizowano zestaw ADF .Net SDK do wersji 0.8.0-preview zawierającej następujące zmiany:</span><span class="sxs-lookup"><span data-stu-id="69846-800">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="69846-801">Dodano operację repozytorium do konfigurowania fabryki</span><span class="sxs-lookup"><span data-stu-id="69846-801">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="69846-802">Zaktualizowano usługę QuickBooks LinkedService w celu ujawnienia właściwości consumerKey i consumerSecret</span><span class="sxs-lookup"><span data-stu-id="69846-802">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="69846-803">Zaktualizowano wiele typów modeli, od SecretBase do Object</span><span class="sxs-lookup"><span data-stu-id="69846-803">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="69846-804">Dodano wyzwalacz zdarzeń obiektów blob</span><span class="sxs-lookup"><span data-stu-id="69846-804">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="69846-805">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="69846-805">AzureRM.KeyVault</span></span>
* <span data-ttu-id="69846-806">Zaktualizowano dokumentację o przykładowe dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="69846-806">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="69846-807">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="69846-807">AzureRM.Network</span></span>
* <span data-ttu-id="69846-808">Parametry włączania analizy ruchu w poleceniach cmdlet narzędzia Network Watcher</span><span class="sxs-lookup"><span data-stu-id="69846-808">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="69846-809">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="69846-809">AzureRM.Resources</span></span>
* <span data-ttu-id="69846-810">Rozwiązano problem z właściwością „Properties” obiektu „PSResource” zwracanego z polecenia „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="69846-810">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="69846-811">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="69846-811">AzureRM.Scheduler</span></span>
* <span data-ttu-id="69846-812">Rozwiązano problem z aktualizacją ServiceBusQueueJob, która nie ustawiała nowych wartości uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="69846-812">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="69846-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="69846-813">AzureRM.Sql</span></span>
* <span data-ttu-id="69846-814">Zaktualizowano następujące polecenia cmdlet o opcjonalny parametr LicenseType</span><span class="sxs-lookup"><span data-stu-id="69846-814">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="69846-815">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="69846-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="69846-816">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="69846-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="69846-817">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="69846-817">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="69846-818">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="69846-818">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="69846-819">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="69846-819">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="69846-820">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="69846-820">AzureRM.Websites</span></span>
* <span data-ttu-id="69846-821">Polecenie „New-AzureRMWebApp” zostało zaktualizowane w celu używania typowych algorytmów z biblioteki strategii.</span><span class="sxs-lookup"><span data-stu-id="69846-821">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="69846-822">6.1.0 — maj 2018 r.</span><span class="sxs-lookup"><span data-stu-id="69846-822">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="69846-823">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="69846-823">AzureRM.Profile</span></span>
* <span data-ttu-id="69846-824">Rozwiązano problem polegający na tym, że po uruchomieniu polecenia „Clear-AzureRmContext” pozostawał pusty kontekst o nazwie takiej jak poprzedni kontekst domyślny, co uniemożliwiało użytkownikowi utworzenie nowego kontekstu ze starą nazwą</span><span class="sxs-lookup"><span data-stu-id="69846-824">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="69846-825">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="69846-825">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="69846-826">Włączono operacje kojarzenia/usuwania skojarzenia bramy w usłudze AS.</span><span class="sxs-lookup"><span data-stu-id="69846-826">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="69846-827">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="69846-827">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="69846-828">Dodano obsługę elementów ApiVersion, ApiRelease oraz ApiRevision</span><span class="sxs-lookup"><span data-stu-id="69846-828">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="69846-829">Dodano obsługę zaplecza ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="69846-829">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="69846-830">Dodano obsługę rejestratora usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="69846-830">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="69846-831">Dodano obsługę rozpoznawania jednostki SKU „Podstawowa” jako prawidłowej jednostki SKU usługi API Management</span><span class="sxs-lookup"><span data-stu-id="69846-831">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="69846-832">Dodano obsługę instalowania certyfikatów wystawionych przez prywatny urząd certyfikacji jako certyfikatów głównych lub certyfikatów urzędu certyfikacji</span><span class="sxs-lookup"><span data-stu-id="69846-832">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="69846-833">Dodano obsługę akceptowania niestandardowych certyfikatów SSL za pomocą magazynu kluczy i wielu nazw hostów serwera proxy</span><span class="sxs-lookup"><span data-stu-id="69846-833">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="69846-834">Dodano obsługę tożsamości MSI</span><span class="sxs-lookup"><span data-stu-id="69846-834">Added support for MSI identity</span></span>
* <span data-ttu-id="69846-835">Dodano obsługę akceptowania zasad za pomocą adresu URL. UWAGA: następujące polecenia cmdlet staną się przestarzałe w przyszłym wydaniu</span><span class="sxs-lookup"><span data-stu-id="69846-835">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="69846-836">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="69846-836">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="69846-837">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="69846-837">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="69846-838">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="69846-838">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="69846-839">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="69846-839">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="69846-840">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="69846-840">AzureRM.Batch</span></span>
* <span data-ttu-id="69846-841">Wydano nowe polecenie cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="69846-841">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="69846-842">Wydano nowe polecenie cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="69846-842">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="69846-843">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="69846-843">AzureRM.Consumption</span></span>
* <span data-ttu-id="69846-844">Dodano nowe parametry polecenia cmdlet Get-AzureRmConsumptionUsageDetail: Expand, ResourceGroup, InstanceName, InstanceId, Tags oraz Top</span><span class="sxs-lookup"><span data-stu-id="69846-844">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="69846-845">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="69846-845">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="69846-846">Poprawiono przykład dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="69846-846">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="69846-847">Rozwiązano problem powodujący wyjątek parametru o wartości null dla przypadku Recurse w poleceniu Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="69846-847">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="69846-848">Poprawiono pliki pomocy dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl oraz Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="69846-848">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="69846-849">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="69846-849">AzureRM.Network</span></span>
* <span data-ttu-id="69846-850">Podniesiono wersję zestawu SDK sieci z 18.0.0-preview do 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="69846-850">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="69846-851">Dodano polecenie cmdlet służące do tworzenia konfiguracji protokołu</span><span class="sxs-lookup"><span data-stu-id="69846-851">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="69846-852">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="69846-852">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="69846-853">Dodano polecenie cmdlet służące do dodawania nowego połączenia obwodu do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="69846-853">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="69846-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="69846-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="69846-855">Dodano polecenie cmdlet służące do usuwania połączenia obwodu z istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="69846-855">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="69846-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="69846-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="69846-857">Dodano polecenie cmdlet służące do pobierania połączenia obwodu</span><span class="sxs-lookup"><span data-stu-id="69846-857">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="69846-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="69846-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="69846-859">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="69846-859">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="69846-860">Naprawiono użycie uwierzytelniania serwera za pomocą wygenerowanych certyfikatów (problem nr 5998)</span><span class="sxs-lookup"><span data-stu-id="69846-860">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="69846-861">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="69846-861">AzureRM.Sql</span></span>
* <span data-ttu-id="69846-862">Zaktualizowano polecenia cmdlet inspekcji w celu umożliwienia usuwania elementów AuditAction lub AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="69846-862">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="69846-863">Rozwiązano problem z poleceniem Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, który powodował zakończenie polecenia niepowodzeniem podczas ustawiania nowych, elastycznych zasad przechowywania oraz zwrócenie komunikatu „Konfigurowanie zasad przechowywania długoterminowego za pomocą magazynu usługi Azure Recovery Service i zasad nie jest już obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="69846-863">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="69846-864">Prześlij żądanie z nowymi, elastycznymi zasadami przechowywania”.</span><span class="sxs-lookup"><span data-stu-id="69846-864">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="69846-865">Zaktualizowano wszystkie polecenia cmdlet służące do tworzenia/aktualizowania elastycznej puli/bazy danych usługi Azure SQL Database w taki sposób, aby korzystały z nowego interfejsu API bazy danych, który obsługuje właściwość SKU na potrzeby właściwości powiązanych ze skalowaniem i warstwą.</span><span class="sxs-lookup"><span data-stu-id="69846-865">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="69846-866">Zaktualizowane polecenia cmdlet to:</span><span class="sxs-lookup"><span data-stu-id="69846-866">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="69846-867">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="69846-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="69846-868">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="69846-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="69846-869">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="69846-869">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="69846-870">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="69846-870">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="69846-871">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="69846-871">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="69846-872">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="69846-872">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="69846-873">Zaktualizowano parametry polecenia „Get-AzureRmTrafficManagerProfile”, aby parametr -ResourceGroupName był wymagany, gdy został podany parametr -Name.</span><span class="sxs-lookup"><span data-stu-id="69846-873">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>