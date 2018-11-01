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
ms.openlocfilehash: eec8b5960f787fa9ca1130b4f8b49c9d896aa99e
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/01/2018
ms.locfileid: "50738108"
---
# <a name="release-notes"></a><span data-ttu-id="1bdd9-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="1bdd9-103">Release notes</span></span>

<span data-ttu-id="1bdd9-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6110---october-2018"></a><span data-ttu-id="1bdd9-105">6.11.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-105">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1bdd9-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1bdd9-106">AzureRM.Profile</span></span>
* <span data-ttu-id="1bdd9-107">Rozwiązano problem z poleceniem Get-AzureRmSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="1bdd9-107">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="1bdd9-108">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="1bdd9-108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="1bdd9-109">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="1bdd9-109">AzureRM.Backup</span></span>
* <span data-ttu-id="1bdd9-110">Przestarzałe polecenia cmdlet usługi Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-110">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1bdd9-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1bdd9-111">AzureRM.Compute</span></span>
* <span data-ttu-id="1bdd9-112">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzureRmVm”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-112">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="1bdd9-113">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-113">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="1bdd9-114">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1bdd9-114">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="1bdd9-115">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1bdd9-115">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="1bdd9-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="1bdd9-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1bdd9-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1bdd9-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1bdd9-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1bdd9-120">AzureRM.Network</span></span>
* <span data-ttu-id="1bdd9-121">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-121">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="1bdd9-122">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-122">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1bdd9-123">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1bdd9-123">AzureRM.Resources</span></span>
* <span data-ttu-id="1bdd9-124">Rozwiązano problem polegający na tym, że polecenie Get-AzureRMRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-124">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="1bdd9-125">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-125">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="1bdd9-126">6.10.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-126">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="1bdd9-127">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1bdd9-127">Azure.Storage</span></span>
* <span data-ttu-id="1bdd9-128">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="1bdd9-128">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="1bdd9-129">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1bdd9-129">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="1bdd9-130">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1bdd9-130">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="1bdd9-131">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1bdd9-131">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="1bdd9-132">Obsługa polecenia Get-AzureRmCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-132">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1bdd9-133">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1bdd9-133">AzureRM.Compute</span></span>
* <span data-ttu-id="1bdd9-134">Rozwiązano problem z poleceniem Get-AzureRmVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="1bdd9-134">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="1bdd9-135">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-135">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="1bdd9-136">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="1bdd9-136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="1bdd9-137">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1bdd9-137">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="1bdd9-138">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1bdd9-139">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1bdd9-139">AzureRM.Network</span></span>
* <span data-ttu-id="1bdd9-140">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="1bdd9-141">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="1bdd9-141">new cmdlets added</span></span>
    - <span data-ttu-id="1bdd9-142">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1bdd9-142">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="1bdd9-143">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1bdd9-143">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="1bdd9-144">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1bdd9-144">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="1bdd9-145">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1bdd9-145">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="1bdd9-146">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-146">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="1bdd9-147">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-147">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="1bdd9-148">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="1bdd9-148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="1bdd9-149">Dodano polecenia cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap i Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1bdd9-149">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="1bdd9-150">Dodano polecenia cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig i Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-150">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="1bdd9-151">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1bdd9-151">AzureRM.RedisCache</span></span>
* <span data-ttu-id="1bdd9-152">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="1bdd9-153">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="1bdd9-153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1bdd9-154">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1bdd9-154">AzureRM.Resources</span></span>
* <span data-ttu-id="1bdd9-155">Dodano brakujący parametr -Mode do polecenia Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1bdd9-155">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="1bdd9-156">Usunięto błąd polecenia Get-AzureRmProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="1bdd9-156">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1bdd9-157">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1bdd9-157">AzureRM.Sql</span></span>
* <span data-ttu-id="1bdd9-158">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1bdd9-158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="1bdd9-159">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="1bdd9-159">AzureRM.Storage</span></span>
* <span data-ttu-id="1bdd9-160">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-160">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="1bdd9-161">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="1bdd9-161">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1bdd9-162">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1bdd9-162">AzureRM.Websites</span></span>
* <span data-ttu-id="1bdd9-163">Nowe polecenie cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłe wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="1bdd9-163">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="1bdd9-164">Nowe polecenia cmdlet New-AzureRMWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="1bdd9-164">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="1bdd9-165">6.9.0 — wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-165">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1bdd9-166">Ogólne</span><span class="sxs-lookup"><span data-stu-id="1bdd9-166">General</span></span>
* <span data-ttu-id="1bdd9-167">Element AzureRM.SignalR został dodany do modułu zbiorczego AzureRM</span><span class="sxs-lookup"><span data-stu-id="1bdd9-167">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="1bdd9-168">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1bdd9-168">AzureRM.Profile</span></span>
* <span data-ttu-id="1bdd9-169">Drobne zmiany wspólnego kodu magazynu</span><span class="sxs-lookup"><span data-stu-id="1bdd9-169">Minor changes to the storage common code</span></span>
* <span data-ttu-id="1bdd9-170">Zaktualizowano pliki pomocy w celu uwzględnienia pełnych typów parametrów.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-170">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="1bdd9-171">Zmieniono opcję -ServicePrincipal na nieobowiązkową w zestawie parametrów ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1bdd9-171">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="1bdd9-172">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1bdd9-172">Azure.Storage</span></span>
* <span data-ttu-id="1bdd9-173">Obsługa tworzenia kontekstu magazynu przy użyciu protokołu OAuth.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-173">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="1bdd9-174">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1bdd9-174">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="1bdd9-175">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="1bdd9-175">AzureRM.Cdn</span></span>
* <span data-ttu-id="1bdd9-176">Dodano element Standard_Microsoft w jednostce SKU cen usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-176">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="1bdd9-177">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1bdd9-177">AzureRM.Compute</span></span>
* <span data-ttu-id="1bdd9-178">Przeniesiono zależności magazynu kluczy i magazynu do zależności wspólnych</span><span class="sxs-lookup"><span data-stu-id="1bdd9-178">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="1bdd9-179">Dodano obsługę kolejnych rozmiarów maszyn wirtualnych do poleceń cmdlet funkcji AEM</span><span class="sxs-lookup"><span data-stu-id="1bdd9-179">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="1bdd9-180">Dodano parametr PublicIPPrefix do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-180">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="1bdd9-181">Dodano parametr ResourceId do polecenia cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="1bdd9-181">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="1bdd9-182">Dodano polecenie cmdlet Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="1bdd9-182">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="1bdd9-183">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="1bdd9-183">AzureRM.Dns</span></span>
* <span data-ttu-id="1bdd9-184">Dodano obsługę rekordu aliasu podczas tworzenia rekordów DNS</span><span class="sxs-lookup"><span data-stu-id="1bdd9-184">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="1bdd9-185">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="1bdd9-185">AzureRM.Insights</span></span>
* <span data-ttu-id="1bdd9-186">Rozwiązano problemy nr 6833 i 7102 (obszar ustawień diagnostycznych)</span><span class="sxs-lookup"><span data-stu-id="1bdd9-186">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="1bdd9-187">Problemy z nazwą domyślną, np. „usługa”, podczas tworzenia i tworzenia/pobierania listy ustawień diagnostycznych</span><span class="sxs-lookup"><span data-stu-id="1bdd9-187">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="1bdd9-188">Problemy z tworzeniem ustawień diagnostycznych przy użyciu kategorii</span><span class="sxs-lookup"><span data-stu-id="1bdd9-188">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="1bdd9-189">Dodano komunikat o zakończeniu obsługi parametrów ziarn czasu metryk</span><span class="sxs-lookup"><span data-stu-id="1bdd9-189">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="1bdd9-190">Parametry typu Timegrain są nadal akceptowane (jest to zmiana niepowodująca niezgodności), ale są one ignorowane w zapleczu, ponieważ tylko wersja PT1M jest prawidłowa</span><span class="sxs-lookup"><span data-stu-id="1bdd9-190">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1bdd9-191">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1bdd9-191">AzureRM.Network</span></span>
* <span data-ttu-id="1bdd9-192">Zmiany poleceń cmdlet usługi LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1bdd9-192">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="1bdd9-193">LoadBalancerInboundNatPoolConfig: dodano parametry IdleTimeoutInMinutes, EnableFloatingIp i EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="1bdd9-193">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="1bdd9-194">LoadBalancerInboundNatRuleConfig: dodano parametr EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="1bdd9-194">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="1bdd9-195">LoadBalancerRuleConfig: dodano parametr EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="1bdd9-195">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="1bdd9-196">LoadBalancerProbeConfig: dodano obsługę wartości „Https” dla parametru Protocol</span><span class="sxs-lookup"><span data-stu-id="1bdd9-196">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="1bdd9-197">Dodano nowe polecenia dla nowego zasobu podrzędnego OutboundRule usługi LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1bdd9-197">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="1bdd9-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="1bdd9-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="1bdd9-200">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-200">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="1bdd9-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="1bdd9-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="1bdd9-203">Dodano nową właściwość HostedWorkloads dla interfejsu PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1bdd9-203">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="1bdd9-204">Dodano nowe polecenia cmdlet dla funkcji Azure Firewall za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="1bdd9-204">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="1bdd9-205">Dodano polecenie Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1bdd9-205">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="1bdd9-206">Dodano polecenie Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1bdd9-206">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="1bdd9-207">Dodano polecenie New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1bdd9-207">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="1bdd9-208">Dodano polecenie Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1bdd9-208">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="1bdd9-209">Dodano polecenie New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1bdd9-209">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="1bdd9-210">Dodano polecenie New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="1bdd9-210">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="1bdd9-211">Dodano polecenie New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1bdd9-211">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="1bdd9-212">Dodano polecenie New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="1bdd9-212">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="1bdd9-213">Dodano polecenie New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1bdd9-213">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="1bdd9-214">Dodano polecenie New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1bdd9-214">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="1bdd9-215">Dodano obsługę zaufanego certyfikatu głównego i konfiguracji skalowania automatycznego w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1bdd9-215">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="1bdd9-216">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1bdd9-216">New Cmdlets added:</span></span>
      - <span data-ttu-id="1bdd9-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1bdd9-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="1bdd9-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1bdd9-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="1bdd9-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1bdd9-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="1bdd9-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1bdd9-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="1bdd9-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1bdd9-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="1bdd9-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bdd9-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="1bdd9-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bdd9-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="1bdd9-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bdd9-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="1bdd9-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bdd9-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="1bdd9-226">Zaktualizowano polecenia cmdlet przy użyciu opcjonalnego parametru -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1bdd9-226">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="1bdd9-227">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bdd9-227">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="1bdd9-228">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bdd9-228">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="1bdd9-229">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1bdd9-229">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="1bdd9-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1bdd9-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="1bdd9-231">Zaktualizowano polecenia cmdlet przy użyciu opcjonalnego parametru -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bdd9-231">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="1bdd9-232">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bdd9-232">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="1bdd9-233">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bdd9-233">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="1bdd9-234">Dodano polecenie cmdlet dla punktu końcowego interfejsu Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1bdd9-234">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="1bdd9-235">Dodano obsługę wielu prefiksów adresów w podsieci.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-235">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="1bdd9-236">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1bdd9-236">Updated cmdlets:</span></span>
  - <span data-ttu-id="1bdd9-237">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-237">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="1bdd9-238">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-238">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="1bdd9-239">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-239">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="1bdd9-240">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-240">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="1bdd9-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1bdd9-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="1bdd9-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="1bdd9-243">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-243">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="1bdd9-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="1bdd9-245">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bdd9-245">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="1bdd9-246">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bdd9-246">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="1bdd9-247">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bdd9-247">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="1bdd9-248">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-248">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="1bdd9-249">New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="1bdd9-250">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-250">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="1bdd9-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="1bdd9-252">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-252">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="1bdd9-253">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-253">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="1bdd9-254">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-254">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="1bdd9-255">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1bdd9-255">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="1bdd9-256">Dodano polecenia cmdlet na potrzeby delegowania podsieci.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-256">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="1bdd9-257">New-AzureRmDelegation: tworzy nowe delegowanie, które można dodać do podsieci</span><span class="sxs-lookup"><span data-stu-id="1bdd9-257">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="1bdd9-258">Remove-AzureRmDelegation: pobiera podsieć i usuwa z niej podaną nazwę delegowania</span><span class="sxs-lookup"><span data-stu-id="1bdd9-258">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="1bdd9-259">Add-AzureRmDelegation: pobiera podsieć i dodaje do niej podaną nazwę usługi jako delegowanie</span><span class="sxs-lookup"><span data-stu-id="1bdd9-259">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="1bdd9-260">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="1bdd9-260">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="1bdd9-261">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="1bdd9-261">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="1bdd9-262">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="1bdd9-262">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="1bdd9-263">Obsługa dysków zarządzanych</span><span class="sxs-lookup"><span data-stu-id="1bdd9-263">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="1bdd9-264">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1bdd9-264">AzureRM.RedisCache</span></span>
* <span data-ttu-id="1bdd9-265">Zaktualizowano zależność szczegółowych informacji.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-265">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1bdd9-266">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1bdd9-266">AzureRM.Resources</span></span>
* <span data-ttu-id="1bdd9-267">Zaktualizowano polecenie New-AzureRmResourceGroupDeployment przy użyciu nowego parametru RollbackAction</span><span class="sxs-lookup"><span data-stu-id="1bdd9-267">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="1bdd9-268">Dodano obsługę elementu OnErrorDeployment przy użyciu nowego parametru.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-268">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="1bdd9-269">Obsługa tożsamości zarządzanej w przypisaniach zasad.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-269">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="1bdd9-270">Parametry z wartościami domyślnymi nie są już wymagane podczas przypisywania zasad za pomocą polecenia „New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-270">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="1bdd9-271">Dodano nowe polecenie cmdlet Get-AzureRmPolicyAlias służące do pobierania aliasów zasad</span><span class="sxs-lookup"><span data-stu-id="1bdd9-271">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1bdd9-272">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1bdd9-272">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1bdd9-273">Rozwiązano problem nr 7161</span><span class="sxs-lookup"><span data-stu-id="1bdd9-273">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="1bdd9-274">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="1bdd9-274">AzureRM.SignalR</span></span>
* <span data-ttu-id="1bdd9-275">Zaktualizowano nazwy jednostek SKU Bezpłatna_F1 i Standardowa_S1</span><span class="sxs-lookup"><span data-stu-id="1bdd9-275">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="1bdd9-276">Dodano pole wersji do obiektu PSSignalRResource i parametry połączenia do obiektu PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-276">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="1bdd9-277">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="1bdd9-277">AzureRM.Storage</span></span>
* <span data-ttu-id="1bdd9-278">Obsługa zasad niezmienności w elemencie AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="1bdd9-278">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="1bdd9-279">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1bdd9-279">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="1bdd9-280">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1bdd9-280">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="1bdd9-281">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1bdd9-281">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="1bdd9-282">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1bdd9-282">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="1bdd9-283">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1bdd9-283">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="1bdd9-284">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="1bdd9-284">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="1bdd9-285">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="1bdd9-285">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="1bdd9-286">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1bdd9-286">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="1bdd9-287">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1bdd9-287">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="1bdd9-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1bdd9-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="1bdd9-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1bdd9-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1bdd9-290">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1bdd9-290">AzureRM.Websites</span></span>
* <span data-ttu-id="1bdd9-291">Dodano dwa nowe polecenia cmdlet: Get-AzureRmDeletedWebApp i Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1bdd9-291">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="1bdd9-292">New-AzureRmAppServicePlan — dodano przełącznik funkcji Hyper-V na potrzeby tworzenia planu usługi App Service przy użyciu kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="1bdd9-292">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="1bdd9-293">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot — dodano nowe parametry (ciąg –ContainerRegistryUser -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) na potrzeby tworzenia aplikacji kontenera systemu Windows oraz zarządzania nią</span><span class="sxs-lookup"><span data-stu-id="1bdd9-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="1bdd9-294">6.8.1 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-294">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1bdd9-295">Ogólne</span><span class="sxs-lookup"><span data-stu-id="1bdd9-295">General</span></span>
* <span data-ttu-id="1bdd9-296">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-296">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="1bdd9-297">Zaktualizowano wspólne zestawy środowiska uruchomieniowego</span><span class="sxs-lookup"><span data-stu-id="1bdd9-297">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="1bdd9-298">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1bdd9-298">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="1bdd9-299">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-299">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="1bdd9-300">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="1bdd9-300">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="1bdd9-301">Polecenia cmdlet Import-AzureRmApiManagementApi i \*-AzureRmApiManagementCertificate teraz obsługują ścieżki względne</span><span class="sxs-lookup"><span data-stu-id="1bdd9-301">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="1bdd9-302">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="1bdd9-302">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="1bdd9-303">CertificateInformation to możliwa do ustawienia właściwość pozwalająca poleceniu cmdlet Set-AzureRmApiManagement poprawnie działać.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-303">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="1bdd9-304">Rozwiązano przez aktualizację do pakietu nuget 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="1bdd9-304">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="1bdd9-305">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="1bdd9-305">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="1bdd9-306">W filtrze Odata naprawiono wyszukiwanie według nazwy dla produktu</span><span class="sxs-lookup"><span data-stu-id="1bdd9-306">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="1bdd9-307">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="1bdd9-307">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="1bdd9-308">W filtrze Odata naprawiono wyszukiwanie według nazwy dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="1bdd9-308">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="1bdd9-309">Dodano obsługę rejestratora AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="1bdd9-309">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="1bdd9-310">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1bdd9-310">AzureRM.Compute</span></span>
* <span data-ttu-id="1bdd9-311">Naprawiono problem polegający na braku elementu docelowego w danych wyjściowych błędu.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-311">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="1bdd9-312">Rozwiązano problem z typem konta magazynu dla maszyny wirtualnej z dyskiem zarządzanym</span><span class="sxs-lookup"><span data-stu-id="1bdd9-312">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="1bdd9-313">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-313">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="1bdd9-314">Naprawiono polecenia cmdlet rozszerzenia AEM dla innych środowisk, na przykład Azure — Chiny</span><span class="sxs-lookup"><span data-stu-id="1bdd9-314">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1bdd9-315">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1bdd9-315">AzureRM.Network</span></span>
* <span data-ttu-id="1bdd9-316">Zmieniono domyślną prezentację danych wyjściowych polecenia cmdlet na widok tabeli</span><span class="sxs-lookup"><span data-stu-id="1bdd9-316">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="1bdd9-317">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1bdd9-317">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="1bdd9-318">Naprawiono błąd w poleceniu Update-AzureRmPowerBIEmbeddedCapacity występujący podczas próby skalowania wstrzymanej pojemności</span><span class="sxs-lookup"><span data-stu-id="1bdd9-318">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="1bdd9-319">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1bdd9-319">AzureRM.Resources</span></span>
* <span data-ttu-id="1bdd9-320">Rozwiązano problem z tworzeniem aplikacji zarządzanych z witryny MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-320">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1bdd9-321">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1bdd9-321">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1bdd9-322">Rozwiązane problemy</span><span class="sxs-lookup"><span data-stu-id="1bdd9-322">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1bdd9-323">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1bdd9-323">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1bdd9-324">Dodano obsługę metody routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="1bdd9-324">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="1bdd9-325">Nowy parametr „MaxReturn” dla routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="1bdd9-325">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="1bdd9-326">Dodano obsługę metody routingu Subnet</span><span class="sxs-lookup"><span data-stu-id="1bdd9-326">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="1bdd9-327">Obsługa zakresów adresów IP (podsieci) w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="1bdd9-327">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="1bdd9-328">Dodano obsługę nagłówków niestandardowych w profilach</span><span class="sxs-lookup"><span data-stu-id="1bdd9-328">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="1bdd9-329">Dodano obsługę zakresów kodów oczekiwanego stanu w profilach</span><span class="sxs-lookup"><span data-stu-id="1bdd9-329">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="1bdd9-330">Dodano obsługę nagłówków niestandardowych w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="1bdd9-330">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="1bdd9-331">6.8.0 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-331">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1bdd9-332">Ogólne</span><span class="sxs-lookup"><span data-stu-id="1bdd9-332">General</span></span>
* <span data-ttu-id="1bdd9-333">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-333">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="1bdd9-334">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1bdd9-334">AzureRM.Profile</span></span>
* <span data-ttu-id="1bdd9-335">Dodano właściwość wygasania do tokenów zwracanych podczas operacji Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="1bdd9-335">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1bdd9-336">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1bdd9-336">AzureRM.Compute</span></span>
* <span data-ttu-id="1bdd9-337">Naprawiono problem polegający na braku elementu docelowego w danych wyjściowych błędu.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-337">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="1bdd9-338">Rozwiązano problem z typem konta magazynu dla maszyny wirtualnej z dyskiem zarządzanym</span><span class="sxs-lookup"><span data-stu-id="1bdd9-338">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="1bdd9-339">Naprawiono polecenia cmdlet rozszerzenia AEM dla innych środowisk, na przykład Azure — Chiny</span><span class="sxs-lookup"><span data-stu-id="1bdd9-339">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="1bdd9-340">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="1bdd9-340">AzureRM.IotHub</span></span>
* <span data-ttu-id="1bdd9-341">Naprawiono przykłady dla poleceń New-AzureRmIotHubExportDevices i New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="1bdd9-341">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1bdd9-342">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1bdd9-342">AzureRM.Network</span></span>
* <span data-ttu-id="1bdd9-343">Zmieniono domyślną reprezentację modeli na widok tabeli</span><span class="sxs-lookup"><span data-stu-id="1bdd9-343">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="1bdd9-344">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1bdd9-344">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="1bdd9-345">Naprawiono błąd w poleceniu Update-AzureRmPowerBIEmbeddedCapacity występujący podczas próby skalowania wstrzymanej pojemności</span><span class="sxs-lookup"><span data-stu-id="1bdd9-345">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1bdd9-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1bdd9-346">AzureRM.Resources</span></span>
* <span data-ttu-id="1bdd9-347">Rozwiązano problem z tworzeniem aplikacji zarządzanej z witryny MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-347">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1bdd9-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1bdd9-348">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1bdd9-349">Rozwiązano problemy</span><span class="sxs-lookup"><span data-stu-id="1bdd9-349">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1bdd9-350">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1bdd9-350">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1bdd9-351">Obsługa metody routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="1bdd9-351">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="1bdd9-352">Nowy parametr „MaxReturn” dla routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="1bdd9-352">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="1bdd9-353">Obsługa metody routingu Subnet</span><span class="sxs-lookup"><span data-stu-id="1bdd9-353">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="1bdd9-354">Obsługa zakresów adresów IP (podsieci) w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="1bdd9-354">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="1bdd9-355">Obsługa nagłówków niestandardowych w profilach</span><span class="sxs-lookup"><span data-stu-id="1bdd9-355">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="1bdd9-356">Obsługa zakresów kodów oczekiwanego stanu w profilach</span><span class="sxs-lookup"><span data-stu-id="1bdd9-356">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="1bdd9-357">Obsługa nagłówków niestandardowych w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="1bdd9-357">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1bdd9-358">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1bdd9-358">AzureRM.Websites</span></span>
* <span data-ttu-id="1bdd9-359">Rozwiązano problem z niepoprawnie ustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-359">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="1bdd9-360">6.7.0 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-360">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1bdd9-361">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1bdd9-361">AzureRM.Profile</span></span>
* <span data-ttu-id="1bdd9-362">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-362">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="1bdd9-363">Dodaj identyfikator użytkownika do domyślnej nazwy kontekstu, aby uniknąć konfliktów kontekstów</span><span class="sxs-lookup"><span data-stu-id="1bdd9-363">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="1bdd9-364">Rozwiązanie problemu z poleceniem Clear-AzureRmContext, który powodował problemy w przypadku wybrania kontekstu nr 6398</span><span class="sxs-lookup"><span data-stu-id="1bdd9-364">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="1bdd9-365">Umożliwienie przekazywania domeny dzierżawy do parametru „-TenantId” polecenia „Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-365">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="1bdd9-366">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1bdd9-366">Azure.Storage</span></span>
* <span data-ttu-id="1bdd9-367">Usunięcie ograniczenia limitu przydziału udziału plików platformy Azure do 5 TB</span><span class="sxs-lookup"><span data-stu-id="1bdd9-367">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="1bdd9-368">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="1bdd9-368">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="1bdd9-369">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1bdd9-369">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="1bdd9-370">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-370">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="1bdd9-371">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1bdd9-371">Azure.AnalysisServices</span></span>
* <span data-ttu-id="1bdd9-372">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-372">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="1bdd9-373">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1bdd9-373">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="1bdd9-374">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-374">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="1bdd9-375">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="1bdd9-375">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="1bdd9-376">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-376">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="1bdd9-377">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="1bdd9-377">AzureRM.Automation</span></span>
* <span data-ttu-id="1bdd9-378">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-378">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="1bdd9-379">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="1bdd9-379">AzureRM.Backup</span></span>
* <span data-ttu-id="1bdd9-380">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-380">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="1bdd9-381">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="1bdd9-381">AzureRM.Batch</span></span>
* <span data-ttu-id="1bdd9-382">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-382">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="1bdd9-383">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="1bdd9-383">AzureRM.Billing</span></span>
* <span data-ttu-id="1bdd9-384">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-384">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="1bdd9-385">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="1bdd9-385">AzureRM.Cdn</span></span>
* <span data-ttu-id="1bdd9-386">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-386">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="1bdd9-387">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1bdd9-387">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="1bdd9-388">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1bdd9-389">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1bdd9-389">AzureRM.Compute</span></span>
* <span data-ttu-id="1bdd9-390">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-390">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="1bdd9-391">Dodanie parametru EvictionPolicy do polecenia New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-391">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="1bdd9-392">Użycie domyślnej lokalizacji w parametrze DiskFileParameterSet polecenia New-AzureRmVm, jeśli nie określono lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-392">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="1bdd9-393">Naprawienie opisu parametru w poleceniu Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1bdd9-393">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="1bdd9-394">Naprawienie działania polecenia cmdlet Get-AzureRmVMDiskEncryptionStatus w przypadku niektórych scenariuszy powiązanych z pojedynczym przebiegiem</span><span class="sxs-lookup"><span data-stu-id="1bdd9-394">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="1bdd9-395">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="1bdd9-395">AzureRM.Consumption</span></span>
* <span data-ttu-id="1bdd9-396">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="1bdd9-397">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1bdd9-397">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="1bdd9-398">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="1bdd9-399">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1bdd9-399">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="1bdd9-400">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="1bdd9-401">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="1bdd9-401">AzureRM.DataFactories</span></span>
* <span data-ttu-id="1bdd9-402">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="1bdd9-403">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1bdd9-403">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="1bdd9-404">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="1bdd9-405">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="1bdd9-405">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="1bdd9-406">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="1bdd9-407">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1bdd9-407">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="1bdd9-408">Naprawienie debugowania, gdy parametr DebugPreference jest ustawiany w wierszu polecenia programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="1bdd9-408">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="1bdd9-409">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="1bdd9-409">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="1bdd9-410">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="1bdd9-411">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1bdd9-411">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="1bdd9-412">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="1bdd9-412">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="1bdd9-413">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-413">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="1bdd9-414">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="1bdd9-414">AzureRM.Dns</span></span>
* <span data-ttu-id="1bdd9-415">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-415">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="1bdd9-416">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1bdd9-416">AzureRM.EventGrid</span></span>
* <span data-ttu-id="1bdd9-417">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-417">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="1bdd9-418">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="1bdd9-418">AzureRM.EventHub</span></span>
* <span data-ttu-id="1bdd9-419">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-419">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="1bdd9-420">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1bdd9-420">AzureRM.HDInsight</span></span>
* <span data-ttu-id="1bdd9-421">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-421">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="1bdd9-422">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="1bdd9-422">AzureRM.Insights</span></span>
* <span data-ttu-id="1bdd9-423">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="1bdd9-424">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="1bdd9-424">AzureRM.IotHub</span></span>
* <span data-ttu-id="1bdd9-425">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="1bdd9-426">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1bdd9-426">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1bdd9-427">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="1bdd9-428">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1bdd9-428">AzureRM.LogicApp</span></span>
* <span data-ttu-id="1bdd9-429">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="1bdd9-430">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1bdd9-430">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="1bdd9-431">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="1bdd9-432">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="1bdd9-432">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="1bdd9-433">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="1bdd9-434">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="1bdd9-434">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="1bdd9-435">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="1bdd9-436">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="1bdd9-436">AzureRM.Media</span></span>
* <span data-ttu-id="1bdd9-437">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1bdd9-438">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1bdd9-438">AzureRM.Network</span></span>
* <span data-ttu-id="1bdd9-439">Dodano przykład dla polecenia Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bdd9-439">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="1bdd9-440">Dodano przykłady i opisy dla poleceń Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey oraz New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1bdd9-440">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="1bdd9-441">Dodano przykłady dla poleceń Remove-AzureRmVirtualNetworkGatewayIpConfig i Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bdd9-441">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="1bdd9-442">Dodano przykład dla polecenia Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="1bdd9-442">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="1bdd9-443">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="1bdd9-443">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="1bdd9-444">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1bdd9-444">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="1bdd9-445">Ponownie wygenerowano polecenia cmdlet ApplicationSecurityGroup, RouteTable i Usage z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="1bdd9-445">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="1bdd9-446">Poprawiono czytelność komunikatu o błędzie dla polecenia Get-AzureRmVirtualNetworkSubnetConfig podczas próby pobrania podsieci, która nie istnieje</span><span class="sxs-lookup"><span data-stu-id="1bdd9-446">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="1bdd9-447">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="1bdd9-447">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="1bdd9-448">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="1bdd9-449">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1bdd9-449">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="1bdd9-450">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="1bdd9-451">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1bdd9-451">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="1bdd9-452">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="1bdd9-453">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1bdd9-453">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="1bdd9-454">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="1bdd9-455">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1bdd9-455">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="1bdd9-456">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-456">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="1bdd9-457">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1bdd9-457">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1bdd9-458">Dodano filtr zasad do polecenia cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-458">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="1bdd9-459">Polecenie zwraca listę elementów kopii zapasowej chronionych przez zasady o danym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-459">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="1bdd9-460">Zaktualizowano przestrzeń nazw Microsoft.Azure.Management.RecoveryServices.Backup do wersji 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-460">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="1bdd9-461">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-461">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="1bdd9-462">Dodano parametr TargetResourceGroupName do polecenia Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-462">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="1bdd9-463">Grupa zasobów, do której są przywracane dyski zarządzane.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-463">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="1bdd9-464">Ma zastosowanie do wykonywania kopii zapasowych maszyn wirtualnych z dyskami zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-464">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="1bdd9-465">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="1bdd9-465">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="1bdd9-466">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="1bdd9-467">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1bdd9-467">AzureRM.RedisCache</span></span>
* <span data-ttu-id="1bdd9-468">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="1bdd9-469">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="1bdd9-469">AzureRM.Relay</span></span>
* <span data-ttu-id="1bdd9-470">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1bdd9-471">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1bdd9-471">AzureRM.Resources</span></span>
* <span data-ttu-id="1bdd9-472">Obsługa wdrażania szablonów w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-472">Support template deployment at subscription scope.</span></span> <span data-ttu-id="1bdd9-473">Dodanie nowych poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1bdd9-473">Add new Cmdlets:</span></span>
    - <span data-ttu-id="1bdd9-474">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1bdd9-474">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="1bdd9-475">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1bdd9-475">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="1bdd9-476">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1bdd9-476">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="1bdd9-477">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1bdd9-477">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="1bdd9-478">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1bdd9-478">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="1bdd9-479">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="1bdd9-479">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="1bdd9-480">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1bdd9-480">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="1bdd9-481">Rozwiązanie problemu, w przypadku którego podczas przekazywania kontekstu do polecenia Set-AzureRmResource jest zgłaszany błąd</span><span class="sxs-lookup"><span data-stu-id="1bdd9-481">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="1bdd9-482">Naprawienie przykładu polecenia New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1bdd9-482">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="1bdd9-483">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="1bdd9-484">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="1bdd9-484">AzureRM.Scheduler</span></span>
* <span data-ttu-id="1bdd9-485">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1bdd9-486">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1bdd9-486">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1bdd9-487">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="1bdd9-488">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1bdd9-488">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="1bdd9-489">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1bdd9-490">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1bdd9-490">AzureRM.Sql</span></span>
* <span data-ttu-id="1bdd9-491">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="1bdd9-492">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="1bdd9-492">AzureRM.Storage</span></span>
* <span data-ttu-id="1bdd9-493">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-493">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="1bdd9-494">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="1bdd9-494">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="1bdd9-495">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-495">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="1bdd9-496">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="1bdd9-496">AzureRM.Tags</span></span>
* <span data-ttu-id="1bdd9-497">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-497">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1bdd9-498">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1bdd9-498">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1bdd9-499">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="1bdd9-500">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="1bdd9-500">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="1bdd9-501">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1bdd9-502">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1bdd9-502">AzureRM.Websites</span></span>
* <span data-ttu-id="1bdd9-503">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="1bdd9-504">6.6.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-504">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1bdd9-505">Ogólne</span><span class="sxs-lookup"><span data-stu-id="1bdd9-505">General</span></span>
* <span data-ttu-id="1bdd9-506">Zaktualizowano wszystkie pliki pomocy, aby uwzględniały pełne typy parametrów i poprawne typy wejściowe/wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-506">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="1bdd9-507">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1bdd9-507">AzureRM.Profile</span></span>
* <span data-ttu-id="1bdd9-508">Zaktualizowano bibliotekę Common.Strategy, aby mogła ona weryfikować, czy bieżąca konfiguracja zasobu jest zgodna z zasobem docelowym.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-508">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="1bdd9-509">Dodano typy ps1xml do biblioteki Common.Storage</span><span class="sxs-lookup"><span data-stu-id="1bdd9-509">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="1bdd9-510">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1bdd9-510">Azure.Storage</span></span>
* <span data-ttu-id="1bdd9-511">Dodano obsługę pobierania kontekstu magazynu z profilu DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bdd9-511">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="1bdd9-512">Dodano atrybut Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-512">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="1bdd9-513">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1bdd9-513">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="1bdd9-514">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="1bdd9-514">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="1bdd9-515">Usunięto usterkę w maperze Automapper dotyczącą translacji obiektu PsApiManagementApi na obiekt ApiContract</span><span class="sxs-lookup"><span data-stu-id="1bdd9-515">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="1bdd9-516">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="1bdd9-516">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="1bdd9-517">Usunięto usterkę w elemencie File.Save dotyczącą przeciążania typem kodowania</span><span class="sxs-lookup"><span data-stu-id="1bdd9-517">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="1bdd9-518">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="1bdd9-518">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="1bdd9-519">Uaktualniono menedżer NuGet do wersji 4.0.3, co rozwiązuje problem z występowaniem wyjątku dotyczącego wzorca w parametrze apiId</span><span class="sxs-lookup"><span data-stu-id="1bdd9-519">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1bdd9-520">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1bdd9-520">AzureRM.Compute</span></span>
* <span data-ttu-id="1bdd9-521">Rozwiązanie problemu powodującego zakończenie niepowodzeniem tworzenia maszyny wirtualnej przy użyciu zestawu DiskFileParameterSet w poleceniu New-AzureRmVm z powodu zmiany nazwy typu konta magazynu PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-521">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="1bdd9-522">Poprawienie polecenia cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="1bdd9-522">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="1bdd9-523">Zaktualizowanie polecenia Get-AzureRmAvailabilitySet, aby umożliwić zwrócenie listy wszystkich zestawów dostępności w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-523">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="1bdd9-524">(Parametr ResouceGroupName jest teraz opcjonalny).</span><span class="sxs-lookup"><span data-stu-id="1bdd9-524">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="1bdd9-525">Zaktualizowanie zestawu SimpleParameterSet polecenia „New-AzureRmVm”, aby umożliwić korzystanie z przyspieszonej łączności sieciowej na kwalifikujących się maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-525">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="1bdd9-526">Zaktualizowanie prostego zestawu parametrów polecenia New-AzureRmVmss w taki sposób, aby tworzenie zestawu skalowania maszyn wirtualnych kończyło się niepowodzeniem, gdy moduł równoważenia obciążenia określony przez użytkownika już istnieje.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-526">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="1bdd9-527">Zaktualizowanie przykładu dla polecenia New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="1bdd9-527">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="1bdd9-528">Dodanie przykładu dla polecenia „New-AzureRmVM”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-528">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="1bdd9-529">Zaktualizowanie opisu polecenia Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="1bdd9-529">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="1bdd9-530">Zaktualizowanie przykładu 1 dla polecenia Set-AzureRmVMBginfoExtension przez poprawienie pisowni i prefiksu.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-530">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="1bdd9-531">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1bdd9-531">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="1bdd9-532">Zaktualizowano zestaw ADF .Net SDK do wersji 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-532">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="1bdd9-533">Obsługa udostępniania własnego środowiska Integration Runtime dla wielu fabryk danych.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-533">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="1bdd9-534">Dodanie nowego parametru -SharedIntegrationRuntimeResourceId do polecenia cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-534">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="1bdd9-535">Dodanie nowego opcjonalnego parametru -LinkedDataFactoryName do polecenia cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-535">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="1bdd9-536">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1bdd9-536">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="1bdd9-537">Zaktualizowano zestaw SDK płaszczyzny danych (Microsoft.Azure.DataLake.Store) do wersji 1.1.9</span><span class="sxs-lookup"><span data-stu-id="1bdd9-537">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="1bdd9-538">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="1bdd9-538">AzureRM.EventHub</span></span>
* <span data-ttu-id="1bdd9-539">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="1bdd9-539">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="1bdd9-540">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="1bdd9-540">AzureRM.Insights</span></span>
* <span data-ttu-id="1bdd9-541">Naprawiono formatowanie typu OutputType w plikach pomocy</span><span class="sxs-lookup"><span data-stu-id="1bdd9-541">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="1bdd9-542">Użycie zestawu Microsoft.Azure.Management.Monitor SDK w wersji 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="1bdd9-542">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="1bdd9-543">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1bdd9-543">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1bdd9-544">Rozwiązanie problemu z potokowaniem w poleceniu Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1bdd9-544">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1bdd9-545">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1bdd9-545">AzureRM.Network</span></span>
* <span data-ttu-id="1bdd9-546">Dodano przykłady dla poleceń cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-546">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1bdd9-547">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1bdd9-547">AzureRM.Resources</span></span>
* <span data-ttu-id="1bdd9-548">Rozwiązanie problemu w przypadku podawania zarówno wartości, jak i nazwy tagu w poleceniu „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-548">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="1bdd9-549">Naprawienie scenariusza potokowania w poleceniu „Set-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-549">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1bdd9-550">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1bdd9-550">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1bdd9-551">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="1bdd9-551">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="1bdd9-552">Rozwiązano kilka problemów</span><span class="sxs-lookup"><span data-stu-id="1bdd9-552">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="1bdd9-553">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1bdd9-553">AzureRM.Sql</span></span>
* <span data-ttu-id="1bdd9-554">Dodanie obsługi zaawansowanej ochrony serwera przed zagrożeniami przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1bdd9-554">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="1bdd9-555">Enable-AzureRmSqlServerAdvancedThreatProtection, Disable-AzureRmSqlServerAdvancedThreatProtection, Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1bdd9-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="1bdd9-556">Dodanie obsługi oceny luk w zabezpieczeniach przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1bdd9-556">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="1bdd9-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="1bdd9-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="1bdd9-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="1bdd9-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="1bdd9-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan, Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord, Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="1bdd9-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="1bdd9-560">Poprawiono przykład w poleceniu Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1bdd9-560">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="1bdd9-561">Naprawienie niepoprawnej obsługi daty/godziny w przypadku podstawowej kultury innej niż Stany Zjednoczone w poleceniu Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="1bdd9-561">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="1bdd9-562">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="1bdd9-562">AzureRM.Storage</span></span>
* <span data-ttu-id="1bdd9-563">Dodanie atrybutu Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="1bdd9-563">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="1bdd9-564">Pokazywanie danych wyjściowych polecenia cmdlet StorageAccount w widoku tabeli</span><span class="sxs-lookup"><span data-stu-id="1bdd9-564">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="1bdd9-565">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1bdd9-565">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="1bdd9-566">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1bdd9-566">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="1bdd9-567">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1bdd9-567">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="1bdd9-568">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="1bdd9-568">AzureRM.Tags</span></span>
* <span data-ttu-id="1bdd9-569">Usunięcie niepoprawnej informacji z pomocy polecenia cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="1bdd9-569">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="1bdd9-570">6.5.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-570">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1bdd9-571">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1bdd9-571">AzureRM.Profile</span></span>
* <span data-ttu-id="1bdd9-572">Zaktualizowano pomoc dotyczącą polecenia „Get-AzureRmContextAutosaveSetting”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-572">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="1bdd9-573">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1bdd9-573">Azure.Storage</span></span>
* <span data-ttu-id="1bdd9-574">Dodano obsługę przekazywania obiektu blob lub pliku z tokenem sygnatury dostępu współdzielonego tylko do odczytu</span><span class="sxs-lookup"><span data-stu-id="1bdd9-574">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="1bdd9-575">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1bdd9-575">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="1bdd9-576">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1bdd9-576">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="1bdd9-577">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1bdd9-577">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="1bdd9-578">Dodano wymaganą właściwość ResourceGroupName do usługi AS.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-578">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="1bdd9-579">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="1bdd9-579">AzureRM.Automation</span></span>
* <span data-ttu-id="1bdd9-580">Zaktualizowano pomoc i dodano przykład polecenia „New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-580">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1bdd9-581">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1bdd9-581">AzureRM.Compute</span></span>
* <span data-ttu-id="1bdd9-582">Dodano parametr -Tag do polecenia Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1bdd9-582">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="1bdd9-583">Dodano przykład polecenia „Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-583">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="1bdd9-584">Dodano przykłady polecenia „Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-584">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="1bdd9-585">Zaktualizowano pomoc dotyczącą polecenia „Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-585">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="1bdd9-586">Zaktualizowano atrybut SimpleParameterSet dla polecenia New-AzureRmVmss, aby domyślnie ustawiał parametr SinglePlacementGroup na wartość false oraz dodano parametr przełącznika „SinglePlacementGroup” umożliwiający użytkownikowi tworzenie zestawów VMSS w pojedynczej grupie umieszczania.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-586">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="1bdd9-587">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="1bdd9-587">AzureRM.EventHub</span></span>
* <span data-ttu-id="1bdd9-588">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSEventHubDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="1bdd9-588">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="1bdd9-589">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1bdd9-589">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1bdd9-590">Zaktualizowano komunikat o błędzie dla polecenia Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1bdd9-590">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="1bdd9-591">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1bdd9-591">AzureRM.LogicApp</span></span>
* <span data-ttu-id="1bdd9-592">Naprawiono błąd „nie można rozpoznać zestawu parametrów” w poleceniu New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="1bdd9-592">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1bdd9-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1bdd9-593">AzureRM.Network</span></span>
* <span data-ttu-id="1bdd9-594">Włączono komunikację równorzędną między sieciami wirtualnymi w wielu dzierżawach dla polecenia Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1bdd9-594">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="1bdd9-595">Zaktualizowano poniższe polecenia cmdlet usługi Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1bdd9-595">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="1bdd9-596">New-AzureRmApplicationGateway: dodano obsługę flagi EnableFIPS i stref</span><span class="sxs-lookup"><span data-stu-id="1bdd9-596">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="1bdd9-597">New-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="1bdd9-597">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="1bdd9-598">Set-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="1bdd9-598">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="1bdd9-599">Ponownie wygenerowano polecenia cmdlet RouteTable z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="1bdd9-599">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="1bdd9-600">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="1bdd9-600">AzureRM.Relay</span></span>
* <span data-ttu-id="1bdd9-601">Zaktualizowano pliki markdown, naprawiono problem z nazwą parametru w przykładzie</span><span class="sxs-lookup"><span data-stu-id="1bdd9-601">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1bdd9-602">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1bdd9-602">AzureRM.Resources</span></span>
* <span data-ttu-id="1bdd9-603">Zaktualizowano polecenia cmdlet Roleassignment i roledefinition:</span><span class="sxs-lookup"><span data-stu-id="1bdd9-603">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="1bdd9-604">Usunięto dodatkowe wywołania polecenia roledefinition wykonywane w ramach stronicowania.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-604">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="1bdd9-605">Naprawiono polecenie cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1bdd9-605">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="1bdd9-606">Naprawiono funkcjonalność parametru polecenia -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="1bdd9-606">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="1bdd9-607">Rozwiązano problem z poleceniem „Get-AzureRmResource”, który polegał na tym, że w parametrze „-ResourceType” była uwzględniana wielkość liter</span><span class="sxs-lookup"><span data-stu-id="1bdd9-607">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1bdd9-608">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1bdd9-608">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1bdd9-609">Dodano parametry top i skip do poleceń cmdlet „list”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-609">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="1bdd9-610">Dodano polecenia cmdlet migracji przestrzeni nazw z warstwy Standardowa do warstwy Premium:</span><span class="sxs-lookup"><span data-stu-id="1bdd9-610">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="1bdd9-611">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1bdd9-611">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="1bdd9-612">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1bdd9-612">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="1bdd9-613">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1bdd9-613">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="1bdd9-614">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1bdd9-614">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="1bdd9-615">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1bdd9-615">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="1bdd9-616">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSServiceBusDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="1bdd9-616">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="1bdd9-617">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1bdd9-617">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="1bdd9-618">Zaktualizowano przykład dotyczący polecenia „New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-618">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1bdd9-619">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1bdd9-619">AzureRM.Sql</span></span>
* <span data-ttu-id="1bdd9-620">Dodano nowe polecenia cmdlet dla przestrzeni nazw Management.Sql, aby umożliwić klientom dodawanie certyfikatu TDE do wystąpienia programu SQL Server lub wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="1bdd9-620">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="1bdd9-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="1bdd9-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="1bdd9-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="1bdd9-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1bdd9-623">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1bdd9-623">AzureRM.Websites</span></span>
* <span data-ttu-id="1bdd9-624">Polecenia `Set-AzureRmWebApp -AssignIdentity` i `Set-AzureRmWebAppSlot -AssignIdentity` po ustawieniu na wartość false spowodują teraz usunięcie właściwości Identity z obiektu lokacji. Usuwany jest także tag podglądu.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-624">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="1bdd9-625">Zaktualizowano przykład dotyczący poleceń `Get-AzureRmWebAppMetrics` i `Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="1bdd9-625">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="1bdd9-626">Polecenie `Set-AzureRmWebApp -PhpVersion` obsługuje wartość off jako prawidłową wersję języka PHP</span><span class="sxs-lookup"><span data-stu-id="1bdd9-626">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="1bdd9-627">6.4.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-627">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1bdd9-628">Ogólne</span><span class="sxs-lookup"><span data-stu-id="1bdd9-628">General</span></span>
* <span data-ttu-id="1bdd9-629">Naprawiono formatowanie typu OutputType w plikach pomocy dotyczących większości modułów</span><span class="sxs-lookup"><span data-stu-id="1bdd9-629">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="1bdd9-630">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1bdd9-630">AzureRM.Profile</span></span>
* <span data-ttu-id="1bdd9-631">Dodano atrybut Ps1Xml do podstawowych typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="1bdd9-631">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1bdd9-632">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1bdd9-632">AzureRM.Compute</span></span>
* <span data-ttu-id="1bdd9-633">Funkcja tagów adresów IP dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="1bdd9-633">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="1bdd9-634">Dodano polecenie cmdlet „New-AzureRmVmssIpTagConfig”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-634">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="1bdd9-635">Dodano parametr IpTag do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-635">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="1bdd9-636">Funkcja automatycznego wycofywania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="1bdd9-636">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="1bdd9-637">Dodano parametry DisableAutoRollback do poleceń New-AzureRmVmssConfig i Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1bdd9-637">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="1bdd9-638">Funkcja historii uaktualniania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="1bdd9-638">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="1bdd9-639">Dodano parametr przełącznika OSUpgradeHistory do polecenia Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1bdd9-639">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="1bdd9-640">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="1bdd9-640">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="1bdd9-641">Dodano obsługę list ACL wykazu przy użyciu następujących poleceń:</span><span class="sxs-lookup"><span data-stu-id="1bdd9-641">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="1bdd9-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1bdd9-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="1bdd9-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1bdd9-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="1bdd9-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1bdd9-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="1bdd9-645">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1bdd9-645">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="1bdd9-646">Dodano obsługę anulowania i śledzenia postępu dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="1bdd9-646">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="1bdd9-647">Dodano obsługę anulowania dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="1bdd9-647">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="1bdd9-648">Naprawiono opróżnianie komunikatów debugowania dla poleceń cmdlet wykonujących operacje cykliczne</span><span class="sxs-lookup"><span data-stu-id="1bdd9-648">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="1bdd9-649">Naprawiono lokalizację testu poleceń cmdlet DataLake</span><span class="sxs-lookup"><span data-stu-id="1bdd9-649">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="1bdd9-650">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="1bdd9-650">AzureRM.EventHub</span></span>
* <span data-ttu-id="1bdd9-651">Dodano opcjonalny parametr MaxCount do poleceń cmdlet tworzących listę operacji: Get-AzureRmEventHub i Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1bdd9-651">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="1bdd9-652">Rozwiązano problem z poleceniem cmdlet New-AzureRmEventHub polegający na tym, że podczas tworzenia nowego centrum EventHub był wymagany co najmniej jeden parametr.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-652">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="1bdd9-653">Udostępniono zestaw parametrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-653">Provided Default Parameter set.</span></span>
* <span data-ttu-id="1bdd9-654">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmEventHubKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-654">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="1bdd9-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1bdd9-655">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1bdd9-656">Rozwiązano problem polegający na tym, że wszystkie zasoby były zwracane przez polecenie Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="1bdd9-656">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1bdd9-657">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1bdd9-657">AzureRM.Network</span></span>
* <span data-ttu-id="1bdd9-658">Uwidoczniono nowe jednostki SKU dla strefowo nadmiarowych bram VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="1bdd9-658">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="1bdd9-659">Dodano nowe polecenia dla funkcji interfejsów API partnerów usługi ExpressRoute za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="1bdd9-659">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="1bdd9-660">Dodano polecenie Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1bdd9-660">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="1bdd9-661">Dodano polecenie Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1bdd9-661">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="1bdd9-662">Dodano polecenie Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="1bdd9-662">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="1bdd9-663">Dodano polecenie Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="1bdd9-663">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="1bdd9-664">Dodano polecenie Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="1bdd9-664">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="1bdd9-665">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="1bdd9-665">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="1bdd9-666">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="1bdd9-666">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="1bdd9-667">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1bdd9-667">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="1bdd9-668">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1bdd9-668">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1bdd9-669">Dodano polecenie cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-669">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="1bdd9-670">To polecenie cmdlet pobiera identyfikator maszyny wirtualnej i sprawdza, czy maszyna wirtualna jest chroniona przez magazyn w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-670">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="1bdd9-671">Jeśli taki magazyn istnieje, polecenie cmdlet wyświetla jego szczegóły.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-671">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1bdd9-672">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1bdd9-672">AzureRM.Resources</span></span>
* <span data-ttu-id="1bdd9-673">Zaktualizowano polecenia cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="1bdd9-673">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="1bdd9-674">Dodano obsługę wyświetlania listy wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="1bdd9-674">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="1bdd9-675">Dodano obsługę pobierania poszczególnych przydziałów za pomocą wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="1bdd9-675">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="1bdd9-676">Dodano przełączniki -Effective i -All do parametru kontroli</span><span class="sxs-lookup"><span data-stu-id="1bdd9-676">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="1bdd9-677">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1bdd9-677">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="1bdd9-678">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="1bdd9-678">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="1bdd9-679">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1bdd9-679">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="1bdd9-680">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1bdd9-680">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="1bdd9-681">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="1bdd9-681">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="1bdd9-682">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1bdd9-682">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="1bdd9-683">Dodano obsługę odwołania do wpisu tajnego KeyVault w parametrach w przypadku używania elementu „TemplateParameterObject” w poleceniu „New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-683">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="1bdd9-684">Rozwiązano problem polegający na tym, że parametr „-EndDate” był ignorowany w poleceniu „New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-684">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="1bdd9-685">Rozwiązano problem polegający na tym, że w poleceniu „Add-AzureRmADGroupMember” używano nieprawidłowego adres URL podczas zgłaszania żądania</span><span class="sxs-lookup"><span data-stu-id="1bdd9-685">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="1bdd9-686">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1bdd9-686">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1bdd9-687">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmServiceBusKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-687">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1bdd9-688">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1bdd9-688">AzureRM.Sql</span></span>
* <span data-ttu-id="1bdd9-689">Objaśniono punkty przywracania zdefiniowane przez użytkownika dla usługi SQLDW w pomocy polecenia New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="1bdd9-689">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="1bdd9-690">Zaktualizowano dokumentację parametru -ComputeGeneration w kilku poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="1bdd9-690">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="1bdd9-691">6.3.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="1bdd9-691">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1bdd9-692">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1bdd9-692">AzureRM.Profile</span></span>
* <span data-ttu-id="1bdd9-693">Zaktualizowano komunikaty o błędach dotyczące polecenia Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="1bdd9-693">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="1bdd9-694">Tworzenie kontekstu dla każdej subskrypcji w przypadku uruchomienia polecenia „Connect-AzureRmAccount” bez wcześniejszego kontekstu</span><span class="sxs-lookup"><span data-stu-id="1bdd9-694">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="1bdd9-695">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1bdd9-695">Azure.Storage</span></span>
* <span data-ttu-id="1bdd9-696">Dodano informacje dotyczące parametru -Permissions w plikach pomocy.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-696">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1bdd9-697">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1bdd9-697">AzureRM.Compute</span></span>
* <span data-ttu-id="1bdd9-698">Polecenie „Get-AzureRmVmDiskEncryptionStatus” — rozwiązano problem zaobserwowany w przypadku maszyn wirtualnych bez dysków z danymi</span><span class="sxs-lookup"><span data-stu-id="1bdd9-698">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="1bdd9-699">Aktualizacja wersji biblioteki klienckiej obliczeń w celu naprawy następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1bdd9-699">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="1bdd9-700">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="1bdd9-700">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="1bdd9-701">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="1bdd9-701">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="1bdd9-702">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1bdd9-702">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="1bdd9-703">Naprawiono następujące polecenia cmdlet w celu poprawnego wyświetlania identyfikatora operacji i stanu operacji:</span><span class="sxs-lookup"><span data-stu-id="1bdd9-703">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="1bdd9-704">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1bdd9-704">Start-AzureRmVM</span></span>
    - <span data-ttu-id="1bdd9-705">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1bdd9-705">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="1bdd9-706">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1bdd9-706">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="1bdd9-707">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1bdd9-707">Set-AzureRmVM</span></span>
    - <span data-ttu-id="1bdd9-708">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="1bdd9-708">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="1bdd9-709">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1bdd9-709">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="1bdd9-710">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="1bdd9-710">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="1bdd9-711">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="1bdd9-711">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="1bdd9-712">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1bdd9-712">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="1bdd9-713">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1bdd9-713">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="1bdd9-714">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1bdd9-714">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="1bdd9-715">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1bdd9-715">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="1bdd9-716">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="1bdd9-716">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="1bdd9-717">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="1bdd9-717">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="1bdd9-718">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="1bdd9-718">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="1bdd9-719">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="1bdd9-719">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="1bdd9-720">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="1bdd9-720">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="1bdd9-721">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="1bdd9-721">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="1bdd9-722">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1bdd9-722">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="1bdd9-723">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1bdd9-723">AzureRM.EventGrid</span></span>
* <span data-ttu-id="1bdd9-724">Usunięto warunki weryfikacji ValidateNotNullOrEmpty dla elementów SubjectBeginsWith/SubjectEndsWith w poleceniu cmdlet Update-AzureRmEventGridSubscription w celu umożliwienia zmiany tych parametrów na pusty ciąg w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-724">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="1bdd9-725">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1bdd9-725">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1bdd9-726">Rozwiązano problem polegający na tym, że nie były zwracane tagi w przypadku uruchomienia polecenia Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="1bdd9-726">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="1bdd9-727">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1bdd9-727">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="1bdd9-728">Publiczne udostępnienie poleceń cmdlet usługi Policy Insights</span><span class="sxs-lookup"><span data-stu-id="1bdd9-728">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="1bdd9-729">Użycie interfejsu API w wersji z 4.04.2018</span><span class="sxs-lookup"><span data-stu-id="1bdd9-729">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="1bdd9-730">Dodano element PolicyDefinitionReferenceId do wyników polecenia Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="1bdd9-730">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="1bdd9-731">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1bdd9-731">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1bdd9-732">Dodano parametr -Vault do poleceń cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-732">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="1bdd9-733">W przypadku przekazania to polecenie przesłania polecenie cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-733">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1bdd9-734">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1bdd9-734">AzureRM.Sql</span></span>
* <span data-ttu-id="1bdd9-735">Zaktualizowano przykład w pliku pomocy polecenia Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="1bdd9-735">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1bdd9-736">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1bdd9-736">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1bdd9-737">Zaktualizowano plik pomocy polecenia Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-737">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1bdd9-738">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1bdd9-738">AzureRM.Websites</span></span>
* <span data-ttu-id="1bdd9-739">Zaktualizowano polecenie „Set-AzureRmWebApp”, aby nie zastępowało elementu AppSettings w przypadku użycia parametru -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1bdd9-739">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="1bdd9-740">Zaktualizowano polecenie „New-AzureRmWebAppSlot” w celu umożliwienia obsługi parametru AppServicePlan jako parametru opcjonalnego</span><span class="sxs-lookup"><span data-stu-id="1bdd9-740">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="1bdd9-741">6.2.1 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="1bdd9-741">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="1bdd9-742">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1bdd9-742">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="1bdd9-743">Zaktualizowano model PSWorkspace w celu umożliwienia użycia typu jako parametru w sieci</span><span class="sxs-lookup"><span data-stu-id="1bdd9-743">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="1bdd9-744">6.2.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="1bdd9-744">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1bdd9-745">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1bdd9-745">AzureRM.Profile</span></span>
* <span data-ttu-id="1bdd9-746">Naprawiono problem, który polegał na tym, że wersja 10.0.3 pliku Newtonsoft.Json nie była ładowana podczas importowania modułu</span><span class="sxs-lookup"><span data-stu-id="1bdd9-746">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1bdd9-747">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1bdd9-747">AzureRM.Compute</span></span>
* <span data-ttu-id="1bdd9-748">Funkcja aktualizacji maszyny wirtualnej usługi VMSS</span><span class="sxs-lookup"><span data-stu-id="1bdd9-748">VMSS VM Update feature</span></span>
    - <span data-ttu-id="1bdd9-749">Dodano polecenia cmdlet „Update-AzureRmVmssVM” i „New-AzureRmVMDataDisk”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-749">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="1bdd9-750">Dodano parametr VirtualMachineScaleSetVM do polecenia cmdlet „Add-AzureRmVMDataDisk” w celu obsługi dodawania dysku danych do maszyny wirtualnej usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-750">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="1bdd9-751">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1bdd9-751">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="1bdd9-752">Zaktualizowano zestaw ADF .Net SDK do wersji 0.8.0-preview zawierającej następujące zmiany:</span><span class="sxs-lookup"><span data-stu-id="1bdd9-752">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="1bdd9-753">Dodano operację repozytorium do konfigurowania fabryki</span><span class="sxs-lookup"><span data-stu-id="1bdd9-753">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="1bdd9-754">Zaktualizowano usługę QuickBooks LinkedService w celu ujawnienia właściwości consumerKey i consumerSecret</span><span class="sxs-lookup"><span data-stu-id="1bdd9-754">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="1bdd9-755">Zaktualizowano wiele typów modeli, od SecretBase do Object</span><span class="sxs-lookup"><span data-stu-id="1bdd9-755">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="1bdd9-756">Dodano wyzwalacz zdarzeń obiektów blob</span><span class="sxs-lookup"><span data-stu-id="1bdd9-756">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="1bdd9-757">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1bdd9-757">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1bdd9-758">Zaktualizowano dokumentację o przykładowe dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="1bdd9-758">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="1bdd9-759">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1bdd9-759">AzureRM.Network</span></span>
* <span data-ttu-id="1bdd9-760">Parametry włączania analizy ruchu w poleceniach cmdlet narzędzia Network Watcher</span><span class="sxs-lookup"><span data-stu-id="1bdd9-760">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1bdd9-761">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1bdd9-761">AzureRM.Resources</span></span>
* <span data-ttu-id="1bdd9-762">Rozwiązano problem z właściwością „Properties” obiektu „PSResource” zwracanego z polecenia „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="1bdd9-762">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="1bdd9-763">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="1bdd9-763">AzureRM.Scheduler</span></span>
* <span data-ttu-id="1bdd9-764">Rozwiązano problem z aktualizacją ServiceBusQueueJob, która nie ustawiała nowych wartości uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="1bdd9-764">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="1bdd9-765">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1bdd9-765">AzureRM.Sql</span></span>
* <span data-ttu-id="1bdd9-766">Zaktualizowano następujące polecenia cmdlet o opcjonalny parametr LicenseType</span><span class="sxs-lookup"><span data-stu-id="1bdd9-766">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="1bdd9-767">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1bdd9-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="1bdd9-768">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1bdd9-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="1bdd9-769">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="1bdd9-769">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="1bdd9-770">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1bdd9-770">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="1bdd9-771">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1bdd9-771">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1bdd9-772">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1bdd9-772">AzureRM.Websites</span></span>
* <span data-ttu-id="1bdd9-773">Polecenie „New-AzureRMWebApp” zostało zaktualizowane w celu używania typowych algorytmów z biblioteki strategii.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-773">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="1bdd9-774">6.1.0 — maj 2018 r.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-774">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1bdd9-775">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1bdd9-775">AzureRM.Profile</span></span>
* <span data-ttu-id="1bdd9-776">Rozwiązano problem polegający na tym, że po uruchomieniu polecenia „Clear-AzureRmContext” pozostawał pusty kontekst o nazwie takiej jak poprzedni kontekst domyślny, co uniemożliwiało użytkownikowi utworzenie nowego kontekstu ze starą nazwą</span><span class="sxs-lookup"><span data-stu-id="1bdd9-776">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="1bdd9-777">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1bdd9-777">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="1bdd9-778">Włączono operacje kojarzenia/usuwania skojarzenia bramy w usłudze AS.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-778">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="1bdd9-779">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1bdd9-779">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="1bdd9-780">Dodano obsługę elementów ApiVersion, ApiRelease oraz ApiRevision</span><span class="sxs-lookup"><span data-stu-id="1bdd9-780">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="1bdd9-781">Dodano obsługę zaplecza ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1bdd9-781">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="1bdd9-782">Dodano obsługę rejestratora usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="1bdd9-782">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="1bdd9-783">Dodano obsługę rozpoznawania jednostki SKU „Podstawowa” jako prawidłowej jednostki SKU usługi API Management</span><span class="sxs-lookup"><span data-stu-id="1bdd9-783">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="1bdd9-784">Dodano obsługę instalowania certyfikatów wystawionych przez prywatny urząd certyfikacji jako certyfikatów głównych lub certyfikatów urzędu certyfikacji</span><span class="sxs-lookup"><span data-stu-id="1bdd9-784">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="1bdd9-785">Dodano obsługę akceptowania niestandardowych certyfikatów SSL za pomocą magazynu kluczy i wielu nazw hostów serwera proxy</span><span class="sxs-lookup"><span data-stu-id="1bdd9-785">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="1bdd9-786">Dodano obsługę tożsamości MSI</span><span class="sxs-lookup"><span data-stu-id="1bdd9-786">Added support for MSI identity</span></span>
* <span data-ttu-id="1bdd9-787">Dodano obsługę akceptowania zasad za pomocą adresu URL. UWAGA: następujące polecenia cmdlet staną się przestarzałe w przyszłym wydaniu</span><span class="sxs-lookup"><span data-stu-id="1bdd9-787">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="1bdd9-788">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="1bdd9-788">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="1bdd9-789">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bdd9-789">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="1bdd9-790">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="1bdd9-790">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="1bdd9-791">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="1bdd9-791">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="1bdd9-792">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="1bdd9-792">AzureRM.Batch</span></span>
* <span data-ttu-id="1bdd9-793">Wydano nowe polecenie cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="1bdd9-793">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="1bdd9-794">Wydano nowe polecenie cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="1bdd9-794">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="1bdd9-795">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="1bdd9-795">AzureRM.Consumption</span></span>
* <span data-ttu-id="1bdd9-796">Dodano nowe parametry polecenia cmdlet Get-AzureRmConsumptionUsageDetail: Expand, ResourceGroup, InstanceName, InstanceId, Tags oraz Top</span><span class="sxs-lookup"><span data-stu-id="1bdd9-796">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="1bdd9-797">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1bdd9-797">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="1bdd9-798">Poprawiono przykład dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="1bdd9-798">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="1bdd9-799">Rozwiązano problem powodujący wyjątek parametru o wartości null dla przypadku Recurse w poleceniu Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1bdd9-799">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="1bdd9-800">Poprawiono pliki pomocy dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl oraz Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1bdd9-800">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="1bdd9-801">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1bdd9-801">AzureRM.Network</span></span>
* <span data-ttu-id="1bdd9-802">Podniesiono wersję zestawu SDK sieci z 18.0.0-preview do 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="1bdd9-802">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="1bdd9-803">Dodano polecenie cmdlet służące do tworzenia konfiguracji protokołu</span><span class="sxs-lookup"><span data-stu-id="1bdd9-803">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="1bdd9-804">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bdd9-804">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="1bdd9-805">Dodano polecenie cmdlet służące do dodawania nowego połączenia obwodu do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="1bdd9-805">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="1bdd9-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="1bdd9-807">Dodano polecenie cmdlet służące do usuwania połączenia obwodu z istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="1bdd9-807">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="1bdd9-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="1bdd9-809">Dodano polecenie cmdlet służące do pobierania połączenia obwodu</span><span class="sxs-lookup"><span data-stu-id="1bdd9-809">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="1bdd9-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1bdd9-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="1bdd9-811">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1bdd9-811">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="1bdd9-812">Naprawiono użycie uwierzytelniania serwera za pomocą wygenerowanych certyfikatów (problem nr 5998)</span><span class="sxs-lookup"><span data-stu-id="1bdd9-812">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1bdd9-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1bdd9-813">AzureRM.Sql</span></span>
* <span data-ttu-id="1bdd9-814">Zaktualizowano polecenia cmdlet inspekcji w celu umożliwienia usuwania elementów AuditAction lub AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="1bdd9-814">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="1bdd9-815">Rozwiązano problem z poleceniem Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, który powodował zakończenie polecenia niepowodzeniem podczas ustawiania nowych, elastycznych zasad przechowywania oraz zwrócenie komunikatu „Konfigurowanie zasad przechowywania długoterminowego za pomocą magazynu usługi Azure Recovery Service i zasad nie jest już obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-815">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="1bdd9-816">Prześlij żądanie z nowymi, elastycznymi zasadami przechowywania”.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-816">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="1bdd9-817">Zaktualizowano wszystkie polecenia cmdlet służące do tworzenia/aktualizowania elastycznej puli/bazy danych usługi Azure SQL Database w taki sposób, aby korzystały z nowego interfejsu API bazy danych, który obsługuje właściwość SKU na potrzeby właściwości powiązanych ze skalowaniem i warstwą.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-817">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="1bdd9-818">Zaktualizowane polecenia cmdlet to:</span><span class="sxs-lookup"><span data-stu-id="1bdd9-818">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="1bdd9-819">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1bdd9-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="1bdd9-820">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1bdd9-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="1bdd9-821">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="1bdd9-821">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="1bdd9-822">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1bdd9-822">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="1bdd9-823">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1bdd9-823">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1bdd9-824">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1bdd9-824">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1bdd9-825">Zaktualizowano parametry polecenia „Get-AzureRmTrafficManagerProfile”, aby parametr -ResourceGroupName był wymagany, gdy został podany parametr -Name.</span><span class="sxs-lookup"><span data-stu-id="1bdd9-825">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
