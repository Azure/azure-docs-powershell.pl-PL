---
ms.openlocfilehash: f89d13d6bbedaea29b62287942d8c7a509abe32b
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052638"
---
## <a name="260---august-2019"></a><span data-ttu-id="b026c-101">2.6.0 — sierpień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-101">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="b026c-102">Ogólne</span><span class="sxs-lookup"><span data-stu-id="b026c-102">General</span></span>
* <span data-ttu-id="b026c-103">Naprawiono różne literówki w wielu modułach</span><span class="sxs-lookup"><span data-stu-id="b026c-103">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b026c-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-104">Az.Accounts</span></span>
* <span data-ttu-id="b026c-105">Obsługa pliku MSI przypisanego przez użytkownika w ramach uwierzytelniania usługi Azure Functions (nr 9479)</span><span class="sxs-lookup"><span data-stu-id="b026c-105">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="b026c-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b026c-106">Az.Aks</span></span>
* <span data-ttu-id="b026c-107">Rozwiązano problem z danymi wyjściowymi polecenia „Get-AzAks”</span><span class="sxs-lookup"><span data-stu-id="b026c-107">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="b026c-108">Więcej informacji: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="b026c-108">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b026c-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b026c-109">Az.ApiManagement</span></span>
* <span data-ttu-id="b026c-110">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="b026c-110">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="b026c-111">Zaktualizowano wersję nuget .net, która nie wymusza ograniczeń dotyczących identyfikatorów productId, apiId, groupId i userId</span><span class="sxs-lookup"><span data-stu-id="b026c-111">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="b026c-112">**Get-AzApiManagementProduct** — dodano obsługę wysyłania zapytań dotyczących produktów przy użyciu interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b026c-112">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="b026c-113">**New-AzApiManagementApiRevision** — poprawka rozwiązująca problem polegający na tym, że wartość ApiRevisionDescription nie była ustawiana podczas tworzenia nowej wersji pomocniczej interfejsu API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="b026c-113">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="b026c-114">Poprawiono literówkę w modelu „PsApiManagementOAuth2AuthrozationServer” na „PsApiManagementOAuth2AuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="b026c-114">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b026c-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b026c-115">Az.Batch</span></span>
* <span data-ttu-id="b026c-116">Poprawiono literówkę w komunikacie pomocy i dokumentacji, zmieniając literę w nazwie systemu Windows na wielką</span><span class="sxs-lookup"><span data-stu-id="b026c-116">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b026c-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b026c-117">Az.Cdn</span></span>
* <span data-ttu-id="b026c-118">Poprawiono literówkę w pomocniku konwersji modułu CDN</span><span class="sxs-lookup"><span data-stu-id="b026c-118">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-119">Az.Compute</span></span>
* <span data-ttu-id="b026c-120">Dodanie polecenia VmssId to New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-120">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="b026c-121">Dodanie parametrów TerminateScheduledEvents i TerminateScheduledEventNotBeforeTimeoutInMinutes do polecenia New-AzVmssConfig and Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b026c-121">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="b026c-122">Dodanie właściwości HyperVGeneration do obiektu obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b026c-122">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="b026c-123">Dodanie funkcji Host i HostGroup</span><span class="sxs-lookup"><span data-stu-id="b026c-123">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="b026c-124">Nowe polecenia cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="b026c-124">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="b026c-125">Dodano parametr HostId do poleceń New-AzVMConfig i New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b026c-125">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="b026c-126">Aktualizacja przykładu w dokumentacji polecenia „Invoke-AzVMRunCommand” w celu użycia poprawnej nazwy parametru</span><span class="sxs-lookup"><span data-stu-id="b026c-126">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="b026c-127">Aktualizacja opisu parametru „-VolumeType” w dokumentacji referencyjnej poleceń „Set-AzVMDiskEncryptionExtension” i „Set-AzVmssDiskEncryptionExtension”</span><span class="sxs-lookup"><span data-stu-id="b026c-127">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b026c-128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b026c-128">Az.DataFactory</span></span>
* <span data-ttu-id="b026c-129">Poprawiono literówkę w poleceniu „New-AzDataFactoryEncryptValue”, zmieniając literę w nazwie systemu Windows na wielką</span><span class="sxs-lookup"><span data-stu-id="b026c-129">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="b026c-130">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.2</span><span class="sxs-lookup"><span data-stu-id="b026c-130">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="b026c-131">Dodanie parametrów „DataProxyIntegrationRuntimeName”, „DataProxyStagingLinkedServiceName” i „DataProxyStagingPath” dla polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime”, aby umożliwić konfigurowanie własnego środowiska Integration Runtime jako serwera proxy dla środowiska SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="b026c-131">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="b026c-132">Zaktualizowano PSTriggerRun na potrzeby wyświetlania wyzwalanych potoków, komunikatów i właściwości, a także PSActivityRun na potrzeby wyświetlania typu działania</span><span class="sxs-lookup"><span data-stu-id="b026c-132">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b026c-133">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b026c-133">Az.DataLakeStore</span></span>
* <span data-ttu-id="b026c-134">Poprawiono wysunięcie polecenia Get-DataLakeStoreDeletedItem pod kątem obsługi błędów lub wyjątków zdalnych.</span><span class="sxs-lookup"><span data-stu-id="b026c-134">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b026c-135">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b026c-135">Az.EventHub</span></span>
* <span data-ttu-id="b026c-136">Rozwiązano problem nr 9658: Literówka VirtualNteworkRule w poleceniu Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b026c-136">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="b026c-137">Rozwiązano problem nr 9558: Polecenie Set-AzEventHubNamespace używa elementu PATCH zamiast PUT</span><span class="sxs-lookup"><span data-stu-id="b026c-137">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="b026c-138">dodano parametr EnableKafka do polecenia cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="b026c-138">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="b026c-139">Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania</span><span class="sxs-lookup"><span data-stu-id="b026c-139">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="b026c-140">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b026c-140">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b026c-141">Poprawiono literówkę w dokumentacji: „Azure” rozpoczynające się małą literą</span><span class="sxs-lookup"><span data-stu-id="b026c-141">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b026c-142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b026c-142">Az.Monitor</span></span>
* <span data-ttu-id="b026c-143">Poprawiono niepoprawną nazwę parametru w dokumentacji pomocy</span><span class="sxs-lookup"><span data-stu-id="b026c-143">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b026c-144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-144">Az.Network</span></span>
* <span data-ttu-id="b026c-145">Zaktualizowano polecenie New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-145">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="b026c-146">Sklasyfikowano parametr „PublicIpAddress” jako przestarzały, ponieważ nie jest on nigdy używany po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="b026c-146">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="b026c-147">Dodano jeden opcjonalny parametr „Primary” wskazujący, czy bieżąca konfiguracja IP jest podstawowa, czy nie.</span><span class="sxs-lookup"><span data-stu-id="b026c-147">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="b026c-148">Ulepszono obsługę wyjątku błędu żądania z zestawu SDK — rozwiązuje to problem polegający na tym, że poprzednio wyjątki zestawu SDK nie były poprawnie obsługiwane, wskutek czego nie były wyświetlane kluczowe szczegóły błędu</span><span class="sxs-lookup"><span data-stu-id="b026c-148">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="b026c-149">Skorygowano logikę weryfikacji prefiksu IP w wersji IPv6 w celu sprawdzania, czy długość prefiksu IPv6 jest poprawna.</span><span class="sxs-lookup"><span data-stu-id="b026c-149">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="b026c-150">Zaktualizowano polecenie Get-AzVirtualNetworkSubnetConfig: Dodano parametr ustawiany w celu pobrania identyfikatora zasobu podsieci.</span><span class="sxs-lookup"><span data-stu-id="b026c-150">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="b026c-151">Zaktualizowano opis parametru Location dla AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="b026c-151">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b026c-152">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b026c-152">Az.OperationalInsights</span></span>
* <span data-ttu-id="b026c-153">Zaktualizowano dokumentację polecenia „New-AzOperationalInsightsLinuxSyslogDataSource”</span><span class="sxs-lookup"><span data-stu-id="b026c-153">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="b026c-154">Dodano przykład</span><span class="sxs-lookup"><span data-stu-id="b026c-154">Added example</span></span>
    - <span data-ttu-id="b026c-155">Zaktualizowano opis parametru „-Name”</span><span class="sxs-lookup"><span data-stu-id="b026c-155">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="b026c-156">Dodano przykład dla polecenia New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="b026c-156">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="b026c-157">Zaktualizowano opis parametru „-Name” dla polecenia New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="b026c-157">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b026c-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b026c-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="b026c-159">Aktualizacja polecenia „Get-AzRecoveryServicesBackupJobDetail.md”</span><span class="sxs-lookup"><span data-stu-id="b026c-159">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b026c-160">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-160">Az.Resources</span></span>
* <span data-ttu-id="b026c-161">Dodano obsługę nowej wersji interfejsu API (2019-05-10) dla Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="b026c-161">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="b026c-162">Dodano obsługę „copy.count = 0” dla zmiennych, zasobów i właściwości</span><span class="sxs-lookup"><span data-stu-id="b026c-162">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="b026c-163">Zasoby z ustawieniami „condition = false” lub „copy.count = 0” będą usuwane w trybie ukończenia</span><span class="sxs-lookup"><span data-stu-id="b026c-163">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="b026c-164">Dodanie do dokumentu pomocy przykładu przypisywania zasad na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b026c-164">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b026c-165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b026c-165">Az.ServiceBus</span></span>
* <span data-ttu-id="b026c-166">Rozwiązano problem nr 9658: Literówka VirtualNetworkRule w poleceniu Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b026c-166">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="b026c-167">Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania</span><span class="sxs-lookup"><span data-stu-id="b026c-167">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="b026c-168">Dodano nowe polecenie „Test-AzServiceBusNameAvailability” do sprawdzania dostępności nazwy dla kolejki i tematu</span><span class="sxs-lookup"><span data-stu-id="b026c-168">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="b026c-169">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b026c-169">Az.ServiceFabric</span></span>
* <span data-ttu-id="b026c-170">Usunięcie usterek poleceń cmdlet dodawania typu węzła:</span><span class="sxs-lookup"><span data-stu-id="b026c-170">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="b026c-171">Usterka NullReferenceException, gdy grupa zasobów ma inny zestaw VMSS niezwiązany z klastrem usługi Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="b026c-171">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="b026c-172">Rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="b026c-172">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="b026c-173">Usunięcie usterki powodującej niepowodzenie polecenia cmdlet, gdy sieć wirtualna znajdowała się w innej grupie zasobów niż klaster.</span><span class="sxs-lookup"><span data-stu-id="b026c-173">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="b026c-174">rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="b026c-174">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="b026c-175">Sklasyfikowanie polecenia cmdlet Add-AzServiceFabricApplicationCertificate jako przestarzałego</span><span class="sxs-lookup"><span data-stu-id="b026c-175">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="b026c-176">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-176">Az.Sql</span></span>
* <span data-ttu-id="b026c-177">Aktualizacja dokumentacji starych poleceń cmdlet inspekcji.</span><span class="sxs-lookup"><span data-stu-id="b026c-177">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b026c-178">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b026c-178">Az.Storage</span></span>
* <span data-ttu-id="b026c-179">Aktualizacja pomocy dotyczącej poleceń Get/Close-AzStorageFileHandle, przez dodanie kolejnych scenariuszy do przykładów dotyczących poleceń cmdlet i zaktualizowanie opisów parametrów</span><span class="sxs-lookup"><span data-stu-id="b026c-179">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="b026c-180">Obsługa StandardBlobTier w ramach przekazywania i kopiowania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="b026c-180">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="b026c-181">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b026c-181">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="b026c-182">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b026c-182">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="b026c-183">Obsługa priorytetu ponownego wypełniania w ramach kopiowania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="b026c-183">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="b026c-184">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b026c-184">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b026c-185">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b026c-185">Az.Websites</span></span>
* <span data-ttu-id="b026c-186">Dodanie wyjaśnienia do parametru -AppSettings w poleceniach Set-AzWebApp i Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b026c-186">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="b026c-187">2.5.0 — lipiec 2019</span><span class="sxs-lookup"><span data-stu-id="b026c-187">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b026c-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-188">Az.Accounts</span></span>
* <span data-ttu-id="b026c-189">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="b026c-189">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="b026c-190">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="b026c-190">Az.ApplicationInsights</span></span>
* <span data-ttu-id="b026c-191">Poprawienie pisowni w przykładzie w dokumentacji polecenia „Remove-AzApplicationInsightsApiKey”</span><span class="sxs-lookup"><span data-stu-id="b026c-191">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="b026c-192">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b026c-192">Az.Automation</span></span>
* <span data-ttu-id="b026c-193">Poprawienie pisowni w ciągu zasobu</span><span class="sxs-lookup"><span data-stu-id="b026c-193">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="b026c-194">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b026c-194">Az.CognitiveServices</span></span>
* <span data-ttu-id="b026c-195">Dodano obsługę właściwości NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="b026c-195">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-196">Az.Compute</span></span>
* <span data-ttu-id="b026c-197">Dodanie brakujących właściwości (ComputerName, OsName, OsVersion i HyperVGeneration) obiektu widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b026c-197">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b026c-198">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b026c-198">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b026c-199">Poprawienie pisowni parametru Replication w opisie polecenia Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b026c-199">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="b026c-200">Więcej informacji można znaleźć tutaj: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="b026c-200">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b026c-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b026c-201">Az.DataFactory</span></span>
* <span data-ttu-id="b026c-202">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.0</span><span class="sxs-lookup"><span data-stu-id="b026c-202">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="b026c-203">Poprawienie pisowni w dokumentacji dla polecenia „Get-AzDataFactoryV2PipelineRun”</span><span class="sxs-lookup"><span data-stu-id="b026c-203">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b026c-204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b026c-204">Az.EventHub</span></span>
* <span data-ttu-id="b026c-205">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="b026c-205">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="b026c-206">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="b026c-206">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b026c-207">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b026c-207">Az.KeyVault</span></span>
* <span data-ttu-id="b026c-208">Dodano obsługę określania rozmiaru klucza dla zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="b026c-208">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b026c-209">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b026c-209">Az.LogicApp</span></span>
* <span data-ttu-id="b026c-210">Poprawienie polecenia Get-AzIntegrationAccountMap tak, aby wyświetlało listę wszystkich typów map</span><span class="sxs-lookup"><span data-stu-id="b026c-210">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="b026c-211">Dodano nowy parametr MapType na potrzeby filtrowania</span><span class="sxs-lookup"><span data-stu-id="b026c-211">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="b026c-212">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="b026c-212">Az.ManagedServices</span></span>
* <span data-ttu-id="b026c-213">Dodano obsługę interfejsu API w wersji 2019-06-01 (ogólna dostępność)</span><span class="sxs-lookup"><span data-stu-id="b026c-213">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b026c-214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-214">Az.Network</span></span>
* <span data-ttu-id="b026c-215">Dodanie obsługi prywatnego punktu końcowego i prywatnej usługi łączenia</span><span class="sxs-lookup"><span data-stu-id="b026c-215">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="b026c-216">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b026c-216">New cmdlets</span></span>
        - <span data-ttu-id="b026c-217">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b026c-217">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b026c-218">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b026c-218">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b026c-219">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b026c-219">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b026c-220">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b026c-220">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b026c-221">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b026c-221">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b026c-222">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b026c-222">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b026c-223">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="b026c-223">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="b026c-224">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b026c-224">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="b026c-225">Zaktualizowano poniższe polecenia dla funkcji: Flaga PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies w podsieci w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b026c-225">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="b026c-226">Zaktualizowano polecenia New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-226">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="b026c-227">Dodano opcjonalny parametr -PrivateEndpointNetworkPoliciesFlag do wskazywania, czy stosowanie zasad sieciowych w prywatnym punkcie końcowym w tej podsieci ma być włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="b026c-227">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="b026c-228">Dodano opcjonalny parametr -PrivateLinkServiceNetworkPoliciesFlag do wskazywania, czy stosowanie zasad sieciowych w prywatnej usłudze łączenia w tej podsieci ma być włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="b026c-228">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="b026c-229">Nazwa parametru „ServiceName” polecenia cmdlet AzPrivateLinkService została zmieniona na „Name” z aliasem „ServiceName” w celu zachowania zgodności z poprzednimi wersjami</span><span class="sxs-lookup"><span data-stu-id="b026c-229">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="b026c-230">Włączenie protokołu ICMP dla konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="b026c-230">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="b026c-231">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b026c-231">Updated cmdlets</span></span>
        - <span data-ttu-id="b026c-232">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-232">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b026c-233">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-233">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b026c-234">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-234">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="b026c-235">Dodanie wartości ConnectionProtocolType (Ikev1/Ikev2) jako konfigurowalnego parametru dla polecenia New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b026c-235">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b026c-236">Dodanie parametru PrivateIpAddressVersion w elemencie LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b026c-236">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="b026c-237">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b026c-237">Updated cmdlet:</span></span>
        - <span data-ttu-id="b026c-238">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-238">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="b026c-239">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-239">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="b026c-240">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-240">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="b026c-241">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig usługi Application Gateway o obsługę portu niestandardowego w sondzie</span><span class="sxs-lookup"><span data-stu-id="b026c-241">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="b026c-242">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig: Dodano opcjonalny parametr Port, który służy do sondowania serwera zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b026c-242">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="b026c-243">Ten parametr ma zastosowanie w przypadku jednostek SKU Standard_V2 i WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="b026c-243">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b026c-244">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b026c-244">Az.OperationalInsights</span></span>
* <span data-ttu-id="b026c-245">Zaktualizowano domyślną wersję zapisywanych wyszukiwań na 1.</span><span class="sxs-lookup"><span data-stu-id="b026c-245">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="b026c-246">Poprawiono obsługę wyrażeń regularnych o wartości null dla dzienników niestandardowych</span><span class="sxs-lookup"><span data-stu-id="b026c-246">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b026c-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b026c-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="b026c-248">Aktualizacja pliku „Get-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="b026c-248">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="b026c-249">Aktualizacja pliku „Get-AzRecoveryServicesBackupContainer.md”</span><span class="sxs-lookup"><span data-stu-id="b026c-249">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="b026c-250">Aktualizacja pliku „Get-AzRecoveryServicesVault.md”</span><span class="sxs-lookup"><span data-stu-id="b026c-250">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="b026c-251">Aktualizacja pliku „Wait-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="b026c-251">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="b026c-252">Aktualizacja pliku „Set-AzRecoveryServicesVaultContext.md”</span><span class="sxs-lookup"><span data-stu-id="b026c-252">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="b026c-253">Aktualizacja pliku „Get-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="b026c-253">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="b026c-254">Aktualizacja pliku „Get-AzRecoveryServicesBackupRecoveryPoint.md”</span><span class="sxs-lookup"><span data-stu-id="b026c-254">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="b026c-255">Aktualizacja pliku „Restore-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="b026c-255">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="b026c-256">Zaktualizowano wywołanie usługi do wyrejestrowywania kontenera dla udziału plików platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b026c-256">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="b026c-257">Aktualizacja pliku „Set-AzRecoveryServicesAsrAlertSetting.md”</span><span class="sxs-lookup"><span data-stu-id="b026c-257">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b026c-258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-258">Az.Resources</span></span>
- <span data-ttu-id="b026c-259">Usunięcie brakującego polecenia cmdlet przywoływanego w dokumentacji polecenia „New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="b026c-259">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="b026c-260">Zaktualizowano polecenia cmdlet zasad w celu używania nowego interfejsu API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="b026c-260">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b026c-261">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b026c-261">Az.ServiceBus</span></span>
* <span data-ttu-id="b026c-262">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="b026c-262">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="b026c-263">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="b026c-263">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="b026c-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-264">Az.Sql</span></span>
* <span data-ttu-id="b026c-265">Poprawienie brakujących przykładów dla polecenia cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b026c-265">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="b026c-266">Poprawienie ustawiania cyklicznego skanowania przez rozszerzenie Ocena luk w zabezpieczeniach bez podawania żadnego adresu e-mail</span><span class="sxs-lookup"><span data-stu-id="b026c-266">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="b026c-267">Poprawienie pisowni w komunikacie ostrzegawczym.</span><span class="sxs-lookup"><span data-stu-id="b026c-267">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b026c-268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b026c-268">Az.Storage</span></span>
* <span data-ttu-id="b026c-269">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzStorageAccount” w celu użycia poprawnej nazwy parametru</span><span class="sxs-lookup"><span data-stu-id="b026c-269">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b026c-270">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b026c-270">Az.StorageSync</span></span>
* <span data-ttu-id="b026c-271">Dodanie polecenia cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="b026c-271">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="b026c-272">Rozwiązanie problemu 9551 dotyczącego respektowania wartości TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="b026c-272">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b026c-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b026c-273">Az.Websites</span></span>
* <span data-ttu-id="b026c-274">Usunięcie usterki polegającej na tym, że niektóre właściwości SiteConfig nie były zwracane przez polecenia Get-AzWebApp i Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b026c-274">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="b026c-275">Dodanie nowego parametru Location dla poleceń Get-AzDeletedWebApp i Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b026c-275">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="b026c-276">Usunięcie usterki związanej z klonowaniem miejsc aplikacji internetowych przy użyciu polecenia New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="b026c-276">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="b026c-277">2.4.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-277">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b026c-278">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-278">Az.Accounts</span></span>
* <span data-ttu-id="b026c-279">Dodano obsługę poleceń cmdlet profilu</span><span class="sxs-lookup"><span data-stu-id="b026c-279">Add support for profile cmdlets</span></span>
* <span data-ttu-id="b026c-280">Dodano obsługę środowisk i płaszczyzn danych w generowanych poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="b026c-280">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="b026c-281">Naprawiono błąd polegający na tym, że w niektórych przypadkach dla poleceń cmdlet płaszczyzny danych w programie Windows PowerShell był używany nieprawidłowy punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="b026c-281">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="b026c-282">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="b026c-282">Az.Advisor</span></span>
* <span data-ttu-id="b026c-283">Wersja ogólnodostępna modułu Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="b026c-283">GA release of Az.Advisor</span></span>
* <span data-ttu-id="b026c-284">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="b026c-284">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b026c-285">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b026c-285">Az.ApiManagement</span></span>
* <span data-ttu-id="b026c-286">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="b026c-286">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="b026c-287">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b026c-287">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="b026c-288">Dodano obsługę wykonywania zapytań dotyczących subskrypcji według użytkownika i produktu</span><span class="sxs-lookup"><span data-stu-id="b026c-288">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="b026c-289">Dodano obsługę wykonywania zapytań przy użyciu zakresu „/”, „/apis”, „/apis/echo-api”</span><span class="sxs-lookup"><span data-stu-id="b026c-289">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="b026c-290">Rozwiązano problemy https://github.com/Azure/azure-powershell/issues/9307 i https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="b026c-290">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="b026c-291">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b026c-291">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="b026c-292">Dodano obsługę określania właściwości „ApiVersion” i „ApiVersionSetId” podczas importowania interfejsów API</span><span class="sxs-lookup"><span data-stu-id="b026c-292">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b026c-293">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b026c-293">Az.Automation</span></span>
* <span data-ttu-id="b026c-294">Usunięto usterkę polecenia cmdlet Set-AzAutomationConnectionFieldValue w celu obsługi wartości ciągu.</span><span class="sxs-lookup"><span data-stu-id="b026c-294">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-295">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-295">Az.Compute</span></span>
* <span data-ttu-id="b026c-296">Dodano parametr HyperVGeneration do polecenia New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-296">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b026c-297">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b026c-297">Az.DataFactory</span></span>
* <span data-ttu-id="b026c-298">Aktualizowanie danych wyjściowych poleceń cmdlet pobierania uruchomień działań, pobierania uruchomień potoków i pobierania uruchomień wyzwalaczy usługi ADF w celu obsługi potoku Select-Object.</span><span class="sxs-lookup"><span data-stu-id="b026c-298">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b026c-299">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b026c-299">Az.EventGrid</span></span>
* <span data-ttu-id="b026c-300">Poprawiono literówkę w dokumentacji polecenia New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="b026c-300">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b026c-301">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b026c-301">Az.IotHub</span></span>
* <span data-ttu-id="b026c-302">Dodano obsługę ponownego generowania kluczy zasad autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="b026c-302">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b026c-303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-303">Az.Network</span></span>
* <span data-ttu-id="b026c-304">Dodano właściwość „RoutingPreference” do tagów publicznych adresów IP</span><span class="sxs-lookup"><span data-stu-id="b026c-304">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="b026c-305">Poprawiono przykłady dla dokumentacji referencyjnej polecenia „Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="b026c-305">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b026c-306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b026c-306">Az.PolicyInsights</span></span>
* <span data-ttu-id="b026c-307">Rozwiązano problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="b026c-307">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="b026c-308">Więcej informacji: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="b026c-308">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b026c-309">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b026c-309">Az.OperationalInsights</span></span>
* <span data-ttu-id="b026c-310">Naprawiono model źródła danych CustomLog zwracany w poleceniu Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b026c-310">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b026c-311">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b026c-311">Az.RecoveryServices</span></span>
* <span data-ttu-id="b026c-312">Poprawka dotycząca polecenia get-policy dla maszyn wirtualnych IaaS</span><span class="sxs-lookup"><span data-stu-id="b026c-312">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b026c-313">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-313">Az.Resources</span></span>
    - <span data-ttu-id="b026c-314">Poprawiono tekst pomocy dotyczącej parametru -Top polecenia Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="b026c-314">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="b026c-315">Dodano obsługę stronicowania po stronie klienta dla polecenia Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="b026c-315">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="b026c-316">Dodano nowe parametry dla polecenia Set-AzPolicyAssignment: -PolicyParameters i -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="b026c-316">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="b026c-317">Aktualizacje dokumentacji i przykładów dla poleceń cmdlet zasad</span><span class="sxs-lookup"><span data-stu-id="b026c-317">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b026c-318">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b026c-318">Az.ServiceBus</span></span>
* <span data-ttu-id="b026c-319">Poprawka rozwiązująca problem #4938 — polecenie New-AzureRmServiceBusQueue zwraca wynik BadRequest w przypadku ustawienia właściwości MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="b026c-319">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="b026c-320">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-320">Az.Sql</span></span>
* <span data-ttu-id="b026c-321">Dodano polecenia cmdlet grupy trybu failover wystąpienia z wersji zapoznawczej do wersji publicznej</span><span class="sxs-lookup"><span data-stu-id="b026c-321">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="b026c-322">Obsługa inspekcji w usłudze Azure SQL Server/Database za pomocą nowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b026c-322">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="b026c-323">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b026c-323">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b026c-324">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b026c-324">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b026c-325">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b026c-325">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b026c-326">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b026c-326">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="b026c-327">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b026c-327">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="b026c-328">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b026c-328">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="b026c-329">Usunięto ograniczenia wiadomości e-mail z ustawień oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="b026c-329">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b026c-330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b026c-330">Az.Storage</span></span>
* <span data-ttu-id="b026c-331">Zmieniono dwa parametry: „-IndexDocument” i „-ErrorDocument404Path” z wymaganych na opcjonalne w poleceniu cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b026c-331">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="b026c-332">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b026c-332">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="b026c-333">Zaktualizowano pomoc dotyczącą polecenia Get-AzStorageBlobContent przez dodanie przykładu</span><span class="sxs-lookup"><span data-stu-id="b026c-333">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="b026c-334">Wyświetlanie dodatkowych informacji o błędzie w przypadku niepowodzenia polecenia cmdlet z powodu wyjątku StorageException</span><span class="sxs-lookup"><span data-stu-id="b026c-334">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="b026c-335">Obsługa tworzenia i aktualizowania konta magazynu przy użyciu uwierzytelniania usługi AAD DS w usłudze Azure Files</span><span class="sxs-lookup"><span data-stu-id="b026c-335">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="b026c-336">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b026c-336">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="b026c-337">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b026c-337">Set-AzStorageAccount</span></span>
* <span data-ttu-id="b026c-338">Obsługa wyświetlania listy lub zamykania dojść do plików udziału plików, katalogu plików lub pliku</span><span class="sxs-lookup"><span data-stu-id="b026c-338">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="b026c-339">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b026c-339">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="b026c-340">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b026c-340">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b026c-341">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b026c-341">Az.StorageSync</span></span>
* <span data-ttu-id="b026c-342">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="b026c-342">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="b026c-343">2.3.2 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-343">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b026c-344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-344">Az.Accounts</span></span>
* <span data-ttu-id="b026c-345">Usunięto usterkę polegającą na używaniu w niektórych przypadkach niepoprawnego adresu URL w wywołaniach funkcji</span><span class="sxs-lookup"><span data-stu-id="b026c-345">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="b026c-346">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="b026c-346">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="b026c-347">Rozwiązano problem z aliasami w poleceniach cmdlet z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="b026c-347">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="b026c-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b026c-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="b026c-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="b026c-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-350">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-350">Az.Compute</span></span>
* <span data-ttu-id="b026c-351">Proste zestawy parametrów New-AzVm i New-AzVmss akceptują teraz parametr „ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="b026c-351">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="b026c-352">Poprawiono literówkę w dokumentacji referencyjnej polecenia „New-AzVM”</span><span class="sxs-lookup"><span data-stu-id="b026c-352">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="b026c-353">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="b026c-353">Az.Dns</span></span>
* <span data-ttu-id="b026c-354">Poprawiono literówkę w przykładach pomocy polecenia „Set-AzDnsZone”.</span><span class="sxs-lookup"><span data-stu-id="b026c-354">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b026c-355">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b026c-355">Az.EventGrid</span></span>
* <span data-ttu-id="b026c-356">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="b026c-356">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="b026c-357">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b026c-357">New cmdlets:</span></span>
    - <span data-ttu-id="b026c-358">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b026c-358">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b026c-359">Tworzy nową domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="b026c-359">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b026c-360">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b026c-360">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b026c-361">Pobiera szczegóły domeny usługi Event Grid lub pobiera listę wszystkich domen usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b026c-361">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="b026c-362">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b026c-362">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b026c-363">Usuwa domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="b026c-363">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b026c-364">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="b026c-364">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="b026c-365">Ponownie generuje klucz dostępu współdzielonego dla domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="b026c-365">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b026c-366">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="b026c-366">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="b026c-367">Pobiera klucze dostępu współdzielonego używane do publikowania zdarzeń w domenie usługi Event Grid.</span><span class="sxs-lookup"><span data-stu-id="b026c-367">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="b026c-368">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="b026c-368">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="b026c-369">Tworzy nowy temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="b026c-369">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="b026c-370">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="b026c-370">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="b026c-371">Pobiera szczegóły tematu domeny usługi Event Grid lub pobiera listę wszystkich tematów domeny usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b026c-371">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="b026c-372">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="b026c-372">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="b026c-373">Usuwa istniejący temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="b026c-373">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="b026c-374">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b026c-374">Updated cmdlets:</span></span>
    - <span data-ttu-id="b026c-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="b026c-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="b026c-376">Dodano nowe wymagane parametry do obsługi przesyłania potokowego nowej domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="b026c-376">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="b026c-377">Dodano nowe wymagane parametry w celu określenia nowej nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="b026c-377">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="b026c-378">Dodano nowe zestawy parametrów dla domen i tematów domen, aby umożliwić ponowne używanie istniejących parametrów (np. EndPointType, SubjectBeginsWith itp.).</span><span class="sxs-lookup"><span data-stu-id="b026c-378">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="b026c-379">Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="b026c-379">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="b026c-380">Data wygaśnięcia subskrypcji zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="b026c-380">Event subscription expiration date,</span></span>
            - <span data-ttu-id="b026c-381">Zaawansowane parametry filtrowania.</span><span class="sxs-lookup"><span data-stu-id="b026c-381">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="b026c-382">Dodano nowe wyliczenie dla elementu servicebusqueue jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="b026c-382">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="b026c-383">Uniemożliwiono użycie elementu „Wszystkie” w opcji -IncludedEventType i zamieniono go na</span><span class="sxs-lookup"><span data-stu-id="b026c-383">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="b026c-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="b026c-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="b026c-385">Dodano nowe opcjonalne parametry (Top, ODataQuery i NextLink) w celu obsługi filtrowania i stronicowania wyników.</span><span class="sxs-lookup"><span data-stu-id="b026c-385">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="b026c-386">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="b026c-386">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="b026c-387">Dodano nowe wymagane parametry do obsługi przesyłania potokowego domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="b026c-387">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="b026c-388">Dodano nowe wymagane parametry w celu określenia nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="b026c-388">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b026c-389">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b026c-389">Az.FrontDoor</span></span>
* <span data-ttu-id="b026c-390">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="b026c-390">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="b026c-391">Dodano obsługę przekształceń i nową wartość autouzupełniania operatora (wyrażenie regularne)</span><span class="sxs-lookup"><span data-stu-id="b026c-391">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="b026c-392">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="b026c-392">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="b026c-393">Dodano nowe wartości autouzupełniania</span><span class="sxs-lookup"><span data-stu-id="b026c-393">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b026c-394">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-394">Az.Network</span></span>
* <span data-ttu-id="b026c-395">Dodano obsługę zasobu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b026c-395">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="b026c-396">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b026c-396">New cmdlets</span></span>
        - <span data-ttu-id="b026c-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="b026c-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="b026c-398">Dodano element AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="b026c-398">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="b026c-399">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b026c-399">New cmdlets</span></span> 
        - <span data-ttu-id="b026c-400">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="b026c-400">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="b026c-401">Dodano element PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b026c-401">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="b026c-402">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b026c-402">New cmdlets</span></span> 
        - <span data-ttu-id="b026c-403">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b026c-403">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="b026c-404">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b026c-404">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b026c-405">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b026c-405">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b026c-406">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-406">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="b026c-407">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b026c-407">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="b026c-408">Dodano element PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b026c-408">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="b026c-409">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b026c-409">New cmdlets</span></span>
        - <span data-ttu-id="b026c-410">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b026c-410">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b026c-411">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b026c-411">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b026c-412">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b026c-412">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b026c-413">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="b026c-413">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="b026c-414">Zaktualizowano poniższe polecenia dla funkcji: Flaga UseLocalAzureIpAddress w elemencie VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b026c-414">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="b026c-415">Zaktualizowano polecenie New-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b026c-415">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="b026c-416">Zaktualizowano polecenie Set-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b026c-416">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="b026c-417">Dodano pole tylko do odczytu PeeredConnections w komunikacji równorzędnej usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b026c-417">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="b026c-418">Dodano pole tylko do odczytu GlobalReachEnabled w usłudze ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b026c-418">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="b026c-419">Dodano atrybut zmiany wywołujący zakończenie obsługi pola AllowGlobalReach w modelu ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b026c-419">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="b026c-420">Rozwiązano problem 8756 podczas używania elementu TargetListenerID z poleceniami cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b026c-420">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="b026c-421">Usunięto usterkę w poleceniu New-AzApplicationGatewayPathRuleConfig, która uniemożliwiała ustawienie zestawu reguł regenerowania.</span><span class="sxs-lookup"><span data-stu-id="b026c-421">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="b026c-422">Rozwiązano problem z wyświetlaniem elementu VirtualNetworkTaps w elemencie NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b026c-422">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="b026c-423">Naprawiono polecenia cmdlet pobierania Cortex dla listy wszystkich części</span><span class="sxs-lookup"><span data-stu-id="b026c-423">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="b026c-424">Naprawiono tworzenie odwołań elementu VirtualHub dla elementu ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="b026c-424">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="b026c-425">Dodano obsługę stref dostępności w elementach AzureFirewall i NatGateway</span><span class="sxs-lookup"><span data-stu-id="b026c-425">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="b026c-426">Dodano polecenie cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="b026c-426">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="b026c-427">Dodano obsługę wielu publicznych adresów IP usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="b026c-427">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="b026c-428">Zaktualizowano polecenie cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="b026c-428">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="b026c-429">Dodano parametr -PublicIpAddress, który akceptuje co najmniej jeden obiekt publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="b026c-429">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="b026c-430">Dodano parametr -VirtualNetwork, który akceptuje obiekt sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b026c-430">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="b026c-431">Dodano do obiektu zapory metody AddPublicIpAddress i RemovePublicIpAddress, które akceptują obiekt publicznego adresu IP jako dane wejściowe</span><span class="sxs-lookup"><span data-stu-id="b026c-431">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="b026c-432">Wycofano parametry -PublicIpName i -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b026c-432">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="b026c-433">Zaktualizowano poniższe polecenia dla funkcji: Ustawiono w opcjach uwierzytelniania usługi AAD elementu VpnClient zasób bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b026c-433">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="b026c-434">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="b026c-434">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="b026c-435">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="b026c-435">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="b026c-436">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr przełącznika RemoveAadAuthentication w celu usunięcia z bramy opcji uwierzytelniania usługi AAD elementu VpnClient.</span><span class="sxs-lookup"><span data-stu-id="b026c-436">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b026c-437">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b026c-437">Az.OperationalInsights</span></span>
* <span data-ttu-id="b026c-438">Włączono warstwę cenową **pergb2018** w poleceniu „New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="b026c-438">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="b026c-439">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-439">Az.Resources</span></span>
* <span data-ttu-id="b026c-440">Obsługa dodatkowych opcji eksportowania szablonu</span><span class="sxs-lookup"><span data-stu-id="b026c-440">Support for additional Template Export options</span></span>
    - <span data-ttu-id="b026c-441">Dodano parametr „-SkipResourceNameParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b026c-441">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="b026c-442">Dodano parametr „-SkipAllParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b026c-442">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="b026c-443">Dodano parametr „-Resource” do polecenia Export-AzResourceGroup w celu filtrowania wyeksportowanych zasobów</span><span class="sxs-lookup"><span data-stu-id="b026c-443">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b026c-444">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b026c-444">Az.ServiceFabric</span></span>
* <span data-ttu-id="b026c-445">Usunięto błąd dodawania certyfikatu polegający na pobieraniu przez element ByExistingKeyVault nieprawidłowego odcisku palca w niektórych przypadkach</span><span class="sxs-lookup"><span data-stu-id="b026c-445">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="b026c-446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-446">Az.Sql</span></span>
* <span data-ttu-id="b026c-447">Naprawiono sufiks punktu końcowego magazynu usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b026c-447">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="b026c-448">Rozwiązano problem z usługą Advanced Data Security polegający na przesłanianiu zasad usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b026c-448">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="b026c-449">Nowe polecenia cmdlet modułu Management.Sql umożliwiające klientom dodawanie kluczy funkcji TDE i ustawianie funkcji ochrony TDE dla wystąpień zarządzanych</span><span class="sxs-lookup"><span data-stu-id="b026c-449">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="b026c-450">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b026c-450">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b026c-451">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b026c-451">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b026c-452">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b026c-452">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b026c-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b026c-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="b026c-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b026c-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b026c-455">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b026c-455">Az.Storage</span></span>
* <span data-ttu-id="b026c-456">Obsługa rodzajów FileStorage i SkuName Premium_ZRS podczas tworzenia konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b026c-456">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="b026c-457">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b026c-457">New-AzStorageAccount</span></span>
* <span data-ttu-id="b026c-458">Opis z wyjaśnieniem polecenia cmdlet niezmienności obiektów blob</span><span class="sxs-lookup"><span data-stu-id="b026c-458">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="b026c-459">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b026c-459">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b026c-460">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b026c-460">Az.Websites</span></span>
* <span data-ttu-id="b026c-461">Optymalizuje polecenie Get-AzWebAppCertificate w celu filtrowania według grupy zasobów na serwerze zamiast na kliencie</span><span class="sxs-lookup"><span data-stu-id="b026c-461">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="b026c-462">Dodano parametr przełącznika -UseDisasterRecovery do polecenia Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b026c-462">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="b026c-463">2.2.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-463">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="b026c-464">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b026c-464">Az.Cdn</span></span>
* <span data-ttu-id="b026c-465">Zaktualizowano polecenia cmdlet do obsługi funkcji rulesEngine na podstawie interfejsu API w wersji 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="b026c-465">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-466">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-466">Az.Compute</span></span>
* <span data-ttu-id="b026c-467">Dodano parametr `NoWait`, który powoduje rozpoczęcie operacji i natychmiastowy powrót, bez czekania na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="b026c-467">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="b026c-468">Zaktualizowano następujące polecenia cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b026c-468">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b026c-469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b026c-469">Az.EventHub</span></span>
* <span data-ttu-id="b026c-470">Poprawka błędu #9231 — polecenie Get-AzEventHubNamespace nie zwraca tagów</span><span class="sxs-lookup"><span data-stu-id="b026c-470">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="b026c-471">Poprawka błędu #9230 — polecenie Get-AzEventHubNamespace zwraca wartość ResourceGroup zamiast wartości ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b026c-471">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b026c-472">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-472">Az.Network</span></span>
* <span data-ttu-id="b026c-473">Aktualizowanie wartości ResourceId i InputObject dla bramy translatora adresów sieciowych</span><span class="sxs-lookup"><span data-stu-id="b026c-473">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="b026c-474">Dodawanie aliasów dla wartości ResourceId i InputObject</span><span class="sxs-lookup"><span data-stu-id="b026c-474">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b026c-475">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b026c-475">Az.PolicyInsights</span></span>
* <span data-ttu-id="b026c-476">Rozwiązanie problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="b026c-476">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b026c-477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b026c-477">Az.RecoveryServices</span></span>
* <span data-ttu-id="b026c-478">Minimalny czas przechowywania zasad IaaSVM w dniach zmieniono z 7 na 1</span><span class="sxs-lookup"><span data-stu-id="b026c-478">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b026c-479">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b026c-479">Az.ServiceBus</span></span>
* <span data-ttu-id="b026c-480">Rozwiązanie problemu #9182 — Get-AzServiceBusNamespace zwraca wartość ResourceGroup zamiast ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b026c-480">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b026c-481">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b026c-481">Az.ServiceFabric</span></span>
* <span data-ttu-id="b026c-482">Poprawienie błędu pisowni w komunikacie o błędzie polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="b026c-482">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="b026c-483">Poprawienie brakującego znaku w wierszach polecenia usługi Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b026c-483">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="b026c-484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-484">Az.Sql</span></span>
* <span data-ttu-id="b026c-485">Dodanie parametru DnsZonePartner dla polecenia cmdlet New-AzureSqlInstance w celu obsługi funkcji AutoDr dla wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="b026c-485">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="b026c-486">Wycofanie polecenia cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b026c-486">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="b026c-487">Zmiana nazwy poleceń cmdlet z Wykrywanie zagrożeń na Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b026c-487">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="b026c-488">Parametry New-AzSqlInstance -StorageSizeInGB i -LicenseType są teraz opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="b026c-488">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b026c-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b026c-489">Az.Websites</span></span>
* <span data-ttu-id="b026c-490">Rozwiązanie problemu polegającego na tym, że użycie poleceń Set-AzWebApp i Set-AzWebAppSlot z właściwością -WebApp powodowało usunięcie tagów</span><span class="sxs-lookup"><span data-stu-id="b026c-490">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="b026c-491">2.1.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-491">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="b026c-492">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b026c-492">Az.ApiManagement</span></span>
* <span data-ttu-id="b026c-493">Utworzono nowe polecenia cmdlet do zarządzania diagnostyką w zakresie globalnym i interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b026c-493">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="b026c-494">**Get-AzApiManagementDiagnostic** — uzyskiwanie diagnostyki skonfigurowanej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b026c-494">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="b026c-495">**New-AzApiManagementDiagnostic** — tworzenie nowej diagnostyki w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b026c-495">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="b026c-496">**New-AzApiManagementHttpMessageDiagnostic** — tworzenie ustawienia diagnostyki określającego nagłówki do rejestrowania i rozmiar treści w bajtach</span><span class="sxs-lookup"><span data-stu-id="b026c-496">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="b026c-497">**New-AzApiManagementPipelineDiagnosticSetting** — tworzenie ustawień diagnostyki dla przychodzących/wychodzących komunikatów HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="b026c-497">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="b026c-498">**New-AzApiManagementSamplingSetting** — tworzenie ustawienia próbkowania dla żądań i odpowiedzi na potrzeby diagnostyki</span><span class="sxs-lookup"><span data-stu-id="b026c-498">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="b026c-499">**Remove-AzApiManagementDiagnostic** — usuwanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b026c-499">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="b026c-500">**Set-AzApiManagementDiagnostic** — aktualizowanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b026c-500">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="b026c-501">Utworzono nowe polecenia cmdlet do zarządzania pamięcią podręczną usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b026c-501">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="b026c-502">**Get-AzApiManagementCache** — uzyskiwanie szczegółów pamięci podręcznej określonej przez identyfikator lub wszystkich pamięci podręcznych</span><span class="sxs-lookup"><span data-stu-id="b026c-502">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="b026c-503">**New-AzApiManagementCache** — tworzenie nowej, „domyślnej” pamięci podręcznej lub pamięci podręcznej w konkretnym „regionie” platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b026c-503">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="b026c-504">**Remove-AzApiManagementCache** — usuwanie pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="b026c-504">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="b026c-505">**Update-AzApiManagementCache** — aktualizacja pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="b026c-505">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="b026c-506">Utworzono nowe polecenia cmdlet do zarządzania schematem interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b026c-506">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="b026c-507">**New-AzApiManagementSchema** — tworzenie nowego schematu dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b026c-507">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="b026c-508">**Get-AzApiManagementSchema** — pobieranie schematów skonfigurowanych w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="b026c-508">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="b026c-509">**Remove-AzApiManagementSchema** — usuwanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="b026c-509">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="b026c-510">**Set-AzApiManagementSchema** — aktualizowanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="b026c-510">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="b026c-511">Utworzono nowe polecenie cmdlet do generowania tokenu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b026c-511">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="b026c-512">**New-AzApiManagementUserToken** — generowanie nowego tokenu użytkownika ważnego domyślnie przez 8 godzin. Za pomocą tego polecenia cmdlet można wygenerować token dla użytkownika „GIT”.</span><span class="sxs-lookup"><span data-stu-id="b026c-512">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="b026c-513">Utworzono nowe polecenie cmdlet do pobierania stanu sieci.</span><span class="sxs-lookup"><span data-stu-id="b026c-513">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="b026c-514">**Get-AzApiManagementNetworkStatus** — uzyskiwanie stanu sieci dla łączności z zasobami, od których zależy usługa API Management.</span><span class="sxs-lookup"><span data-stu-id="b026c-514">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="b026c-515">Jest to przydatne w przypadku wdrażania usługi ApiManagement w sieci wirtualnej i weryfikacji, czy któreś z zależności są uszkodzone.</span><span class="sxs-lookup"><span data-stu-id="b026c-515">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="b026c-516">Zaktualizowano polecenie cmdlet **New-AzApiManagement** do zarządzania usługą ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b026c-516">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="b026c-517">Dodano obsługę nowych jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="b026c-517">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="b026c-518">Dodano obsługę włączania flagi „EnableClientCertificate” dla jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="b026c-518">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="b026c-519">Nowe polecenie cmdlet **New-AzApiManagementSslSetting** umożliwia skonfigurowanie ustawienia „TLS/SSL” na „Zaplecze” i „Fronton”.</span><span class="sxs-lookup"><span data-stu-id="b026c-519">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="b026c-520">Za jego pomocą można też skonfigurować szyfrowanie, takie jak „3DES”, i protokoły serwera, takie jak „Http2”we frontonie usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b026c-520">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="b026c-521">Dodano obsługę konfigurowania nazwy hosta „DeveloperPortal” usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b026c-521">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="b026c-522">Zaktualizowano polecenia cmdlet **Get-AzApiManagementSsoToken**, aby przyjmowały jako wejście obiekt „PsApiManagement”</span><span class="sxs-lookup"><span data-stu-id="b026c-522">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="b026c-523">Zaktualizowano polecenie cmdlet, aby wyświetlało komunikaty o błędach śródwierszowo</span><span class="sxs-lookup"><span data-stu-id="b026c-523">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="b026c-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Kod błędu: Komunikat o błędzie ValidationError: Co najmniej jedno pole zawiera nieprawidłową wartość: Szczegóły błędu:    [Code=ValidationError, Message=Błąd w elemencie „log-to-eventhub” w wierszu 3, kolumna 10: Nie znaleziono rejestratora, element docelowy=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="b026c-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="b026c-525">Zaktualizowano polecenie cmdlet **Export-AzApiManagementApi** tak, aby eksportowało interfejsy API w formacie „OpenApi 3.0”</span><span class="sxs-lookup"><span data-stu-id="b026c-525">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="b026c-526">Zaktualizowano polecenie cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b026c-526">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b026c-527">W celu importowania interfejsu Api z dokumentu ze specyfikacją interfejsu „OpenApi 3.0”.</span><span class="sxs-lookup"><span data-stu-id="b026c-527">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="b026c-528">W celu przesłonięcia właściwości „PsApiManagementSchema” określonej w dowolnym dokumencie („Swagger”, „Wadl”, „Wsdl”, „OpenApi”).</span><span class="sxs-lookup"><span data-stu-id="b026c-528">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="b026c-529">W celu przesłonięcia właściwości „ServiceUrl” określonej w dowolnym dokumencie.</span><span class="sxs-lookup"><span data-stu-id="b026c-529">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="b026c-530">Zaktualizowano polecenie cmdlet **Get-AzApiManagementPolicy** tak, aby zwracało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml”</span><span class="sxs-lookup"><span data-stu-id="b026c-530">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="b026c-531">Zaktualizowano polecenie cmdlet **Set-AzApiManagementPolicy** tak, aby akceptowało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml” i ze zmianą znaczenia Xml przy użyciu formatu „xml”</span><span class="sxs-lookup"><span data-stu-id="b026c-531">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="b026c-532">Zaktualizowano polecenie cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b026c-532">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="b026c-533">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="b026c-533">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="b026c-534">W celu utworzenia interfejsu API we właściwości ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="b026c-534">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="b026c-535">W celu sklonowania interfejsu API przy użyciu właściwości „SourceApiId” i „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="b026c-535">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="b026c-536">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b026c-536">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="b026c-537">Zaktualizowano polecenie cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b026c-537">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b026c-538">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="b026c-538">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="b026c-539">W celu zaktualizowania interfejsu API we właściwości „ApiVersionSet”.</span><span class="sxs-lookup"><span data-stu-id="b026c-539">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="b026c-540">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b026c-540">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="b026c-541">Zaktualizowano polecenie cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="b026c-541">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="b026c-542">W celu klonowania (kopiowanie tagów, produktów, operacji i zasad) istniejącej wersji przy użyciu właściwości „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="b026c-542">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="b026c-543">Dla nowej wersji przyjmowana jest wartość „ApiId” elementu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="b026c-543">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="b026c-544">W celu dostarczenia właściwości „ApiRevisionDescription”.</span><span class="sxs-lookup"><span data-stu-id="b026c-544">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="b026c-545">W celu przesłonięcia właściwości „ServiceUrl” podczas klonowania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b026c-545">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="b026c-546">Zaktualizowano polecenie cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="b026c-546">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="b026c-547">W celu skonfigurowania właściwości „AAD” lub „AADB2C” za pomocą właściwości „Authority”.</span><span class="sxs-lookup"><span data-stu-id="b026c-547">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="b026c-548">W celu skonfigurowania właściwości „SignupPolicy”, „SigninPolicy”, „ProfileEditingPolicy” i „PasswordResetPolicy”.</span><span class="sxs-lookup"><span data-stu-id="b026c-548">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="b026c-549">Zaktualizowano polecenie cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b026c-549">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="b026c-550">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="b026c-550">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="b026c-551">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="b026c-551">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="b026c-552">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b026c-552">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="b026c-553">Zaktualizowano polecenie cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b026c-553">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="b026c-554">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="b026c-554">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="b026c-555">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="b026c-555">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="b026c-556">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b026c-556">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="b026c-557">Zaktualizowano następujące polecenia cmdlet do akceptowania właściwości „ResourceId” jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="b026c-557">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="b026c-558">„New-AzApiManagementContext”</span><span class="sxs-lookup"><span data-stu-id="b026c-558">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="b026c-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="b026c-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="b026c-560">„Get-AzApiManagementApiRelease”</span><span class="sxs-lookup"><span data-stu-id="b026c-560">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="b026c-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="b026c-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="b026c-562">„Get-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="b026c-562">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="b026c-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="b026c-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="b026c-564">„Get-AzApiManagementAuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="b026c-564">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="b026c-565">„Get-AzApiManagementBackend”</span><span class="sxs-lookup"><span data-stu-id="b026c-565">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="b026c-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="b026c-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="b026c-567">„Get-AzApiManagementCertificate”</span><span class="sxs-lookup"><span data-stu-id="b026c-567">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="b026c-568">„Remove-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="b026c-568">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="b026c-569">„Remove-AzApiManagementSubscription”</span><span class="sxs-lookup"><span data-stu-id="b026c-569">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b026c-570">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b026c-570">Az.Automation</span></span>
* <span data-ttu-id="b026c-571">Zaktualizowano polecenie Get-AzAutomationJobOutputRecord tak, aby obsługiwało wartości rekordów w postaci kodu JSON i tekstowej.</span><span class="sxs-lookup"><span data-stu-id="b026c-571">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="b026c-572">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="b026c-572">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="b026c-573">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="b026c-573">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="b026c-574">Zmieniono działanie polecenia Start-AzAutomationDscCompilationJob tak, aby tylko uruchamiało zadanie zamiast czekać na jego zakończenie.</span><span class="sxs-lookup"><span data-stu-id="b026c-574">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="b026c-575">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="b026c-575">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="b026c-576">Poprawka dla polecenia Get-AzAutomationDscNode podczas używania opcji -Name zwraca wszystkie węzły.</span><span class="sxs-lookup"><span data-stu-id="b026c-576">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="b026c-577">Teraz zwraca tylko pasujące węzły.</span><span class="sxs-lookup"><span data-stu-id="b026c-577">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-578">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-578">Az.Compute</span></span>
* <span data-ttu-id="b026c-579">Dodanie parametrów ProtectFromScaleIn i ProtectFromScaleSetAction do polecenia cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="b026c-579">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="b026c-580">Nowy zestaw parametrów New-AzVM wimple teraz używa domyślnie dostępnej lokalizacji, jeśli region „Wschodnie stany USA” nie jest obsługiwany.</span><span class="sxs-lookup"><span data-stu-id="b026c-580">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b026c-581">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b026c-581">Az.DataLakeStore</span></span>
* <span data-ttu-id="b026c-582">Aktualizacja zestawu ADLS SDK do korzystania z klienta httpclient, integrowanie testowania płaszczyzny danych z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b026c-582">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b026c-583">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b026c-583">Az.Monitor</span></span>
* <span data-ttu-id="b026c-584">Naprawiono nieprawidłowe nazwy parametrów w przykładach pomocy</span><span class="sxs-lookup"><span data-stu-id="b026c-584">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b026c-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-585">Az.Network</span></span>
* <span data-ttu-id="b026c-586">Dodanie flagi DisableBgpRoutePropagation do danych wyjściowych obowiązującej tabeli routingu</span><span class="sxs-lookup"><span data-stu-id="b026c-586">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="b026c-587">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b026c-587">Updated cmdlet:</span></span>
        - <span data-ttu-id="b026c-588">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="b026c-588">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="b026c-589">Poprawienie podwójnego łącznika w dokumentacji polecenia New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b026c-589">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="b026c-590">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-590">Az.Resources</span></span>
* <span data-ttu-id="b026c-591">Dodanie nowego polecenia cmdlet Get-AzureRmDenyAssignment do pobierania przypisań odmowy</span><span class="sxs-lookup"><span data-stu-id="b026c-591">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="b026c-592">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-592">Az.Sql</span></span>
* <span data-ttu-id="b026c-593">Zmiana nazwy poleceń cmdlet usługi Advanced Threat Protection na Advanced Data Security i domyślne włączenie oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="b026c-593">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="b026c-594">2.0.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-594">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b026c-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-595">Az.Accounts</span></span>
* <span data-ttu-id="b026c-596">Aktualizacja biblioteki uwierzytelniania w celu rozwiązania problemów z usługą ADFS dotyczących uwierzytelniania nazwy użytkownika i hasła</span><span class="sxs-lookup"><span data-stu-id="b026c-596">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b026c-597">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b026c-597">Az.CognitiveServices</span></span>
* <span data-ttu-id="b026c-598">Dla usług wyszukiwania Bing wyświetlane jest tylko zrzeczenie odpowiedzialności usługi Bing.</span><span class="sxs-lookup"><span data-stu-id="b026c-598">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="b026c-599">Naprawiono błąd polegający na niepomyślnym tworzeniu konta.</span><span class="sxs-lookup"><span data-stu-id="b026c-599">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-600">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-600">Az.Compute</span></span>
* <span data-ttu-id="b026c-601">Funkcja Grupa umieszczania w pobliżu.</span><span class="sxs-lookup"><span data-stu-id="b026c-601">Proximity placement group feature.</span></span>
    - <span data-ttu-id="b026c-602">Dodano następujące nowe polecenia cmdlet:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="b026c-602">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="b026c-603">Do następujących poleceń cmdlet dodano nowy parametr ProximityPlacementGroupId:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-603">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="b026c-604">Do polecenia New-AzGalleryImageVersion dodano parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="b026c-604">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="b026c-605">Właściwość TargetRegion polecenia New-AzGalleryImageVersion może zawierać parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="b026c-605">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="b026c-606">Do poleceń Stop-AzVM i Stop-AzVmss dodano parametr przełącznika SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="b026c-606">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="b026c-607">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="b026c-607">Breaking changes</span></span>
    - <span data-ttu-id="b026c-608">Polecenie Set-AzVMBootDiagnostics zamieniono na polecenie Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="b026c-608">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="b026c-609">Polecenie Export-AzLogAnalyticThrottledRequests zamieniono na polecenie Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="b026c-609">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="b026c-610">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="b026c-610">Az.DeploymentManager</span></span>
* <span data-ttu-id="b026c-611">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="b026c-611">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="b026c-612">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="b026c-612">Az.Dns</span></span>
* <span data-ttu-id="b026c-613">Automatyczne delegowanie serwera nazw systemu DNS</span><span class="sxs-lookup"><span data-stu-id="b026c-613">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="b026c-614">Polecenie cmdlet tworzenia strefy DNS akceptuje nazwę strefy nadrzędnej jako dodatkowy parametr opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b026c-614">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="b026c-615">Dodaje rekordy serwera nazw w strefie nadrzędnej dla nowo utworzonej strefy podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="b026c-615">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b026c-616">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b026c-616">Az.FrontDoor</span></span>
* <span data-ttu-id="b026c-617">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b026c-617">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="b026c-618">Zmiana nazw poleceń cmdlet zapory aplikacji internetowej w celu dołączenia ciągu „Waf”</span><span class="sxs-lookup"><span data-stu-id="b026c-618">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="b026c-619">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b026c-619">Az.HDInsight</span></span>
* <span data-ttu-id="b026c-620">Usunięto dwa polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b026c-620">Removed two cmdlets:</span></span>
    - <span data-ttu-id="b026c-621">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b026c-621">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="b026c-622">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b026c-622">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="b026c-623">Dodano nowe polecenie cmdlet Set-AzHDInsightGatewayCredential w celu zastąpienia polecenia Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b026c-623">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="b026c-624">Zaktualizowano polecenie cmdlet Get-AzHDInsightJobOutput, aby rozróżnić rolę czytelnika i rolę operatora usługi HDInsight:</span><span class="sxs-lookup"><span data-stu-id="b026c-624">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="b026c-625">Użytkownicy z rolą czytelnika muszą jawnie określić parametr „DefaultStorageAccountKey” — w przeciwnym razie wystąpi błąd.</span><span class="sxs-lookup"><span data-stu-id="b026c-625">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="b026c-626">Nie będzie to miało wpływu na użytkowników z rolą operatora usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b026c-626">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b026c-627">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b026c-627">Az.Monitor</span></span>
* <span data-ttu-id="b026c-628">Nowe polecenia cmdlet dla interfejsu API SQR (Scheduled Query Rule, reguła zaplanowanego zapytania)</span><span class="sxs-lookup"><span data-stu-id="b026c-628">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="b026c-629">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="b026c-629">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="b026c-630">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="b026c-630">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="b026c-631">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="b026c-631">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="b026c-632">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="b026c-632">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="b026c-633">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="b026c-633">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="b026c-634">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="b026c-634">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="b026c-635">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b026c-635">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b026c-636">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b026c-636">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b026c-637">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b026c-637">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b026c-638">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b026c-638">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b026c-639">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b026c-639">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b026c-640">[Więcej](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informacji na temat interfejsu API SQR</span><span class="sxs-lookup"><span data-stu-id="b026c-640">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="b026c-641">Zaktualizowano plik Az.Monitor.md w celu uwzględnienia poleceń cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="b026c-641">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b026c-642">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-642">Az.Network</span></span>
* <span data-ttu-id="b026c-643">Dodano obsługę dla zasobu usługi NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="b026c-643">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="b026c-644">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b026c-644">New cmdlets</span></span>
        - <span data-ttu-id="b026c-645">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b026c-645">New-AzNatGateway</span></span>
        - <span data-ttu-id="b026c-646">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b026c-646">Get-AzNatGateway</span></span>
        - <span data-ttu-id="b026c-647">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b026c-647">Set-AzNatGateway</span></span>
        - <span data-ttu-id="b026c-648">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b026c-648">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="b026c-649">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b026c-649">Updated cmdlets</span></span>
        - <span data-ttu-id="b026c-650">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="b026c-650">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="b026c-651">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="b026c-651">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="b026c-652">Zaktualizowano poniższe polecenia dla funkcji: Ustawianie/usuwanie tras niestandardowych dla bramy Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="b026c-652">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="b026c-653">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="b026c-653">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="b026c-654">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="b026c-654">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b026c-655">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b026c-655">Az.PolicyInsights</span></span>
* <span data-ttu-id="b026c-656">Obsługa zapytań dotyczących szczegółów oceny zasad.</span><span class="sxs-lookup"><span data-stu-id="b026c-656">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="b026c-657">Dodano parametr „-Expand” do polecenia Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="b026c-657">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="b026c-658">Obsługa polecenia „-Expand PolicyEvaluationDetails”.</span><span class="sxs-lookup"><span data-stu-id="b026c-658">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b026c-659">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b026c-659">Az.RecoveryServices</span></span>
* <span data-ttu-id="b026c-660">Obsługa odzyskiwania lokacji między subskrypcjami z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="b026c-660">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="b026c-661">Oznaczanie nadchodzących zmian powodujących niezgodność dla usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b026c-661">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="b026c-662">Poprawka zakończenia planu akcji dla planu odzyskiwania usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b026c-662">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="b026c-663">Poprawka aktualizacji mapowania sieci usługi Azure Site Recovery z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="b026c-663">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="b026c-664">Poprawka aktualizacji kierunku ochrony usługi Azure Site Recovery z platformy Azure na platformę Azure dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="b026c-664">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="b026c-665">Inne drobne poprawki.</span><span class="sxs-lookup"><span data-stu-id="b026c-665">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="b026c-666">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b026c-666">Az.Relay</span></span>
* <span data-ttu-id="b026c-667">Poprawiono błędy pisowni w komunikatach przeznaczonych dla klientów</span><span class="sxs-lookup"><span data-stu-id="b026c-667">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b026c-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b026c-668">Az.ServiceBus</span></span>
* <span data-ttu-id="b026c-669">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="b026c-669">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b026c-670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b026c-670">Az.Storage</span></span>
* <span data-ttu-id="b026c-671">Uaktualnienie biblioteki klienta usługi Storage do wersji 10.0.1 (przestrzeń nazw wszystkich obiektów tego zestawu SDK została zmieniona z „Microsoft.WindowsAzure.Storage. *” na „Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="b026c-671">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="b026c-672">Uaktualnienie do wersji Microsoft.Azure.Management.Storage 11.0.0 w celu obsługi nowego interfejsu API w wersji 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="b026c-672">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="b026c-673">Domyślny rodzaj konta magazynu w poleceniu Utwórz konto magazynu został zmieniony ze „Storage” na „StorageV2”</span><span class="sxs-lookup"><span data-stu-id="b026c-673">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="b026c-674">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b026c-674">New-AzStorageAccount</span></span>
* <span data-ttu-id="b026c-675">Zmiana wyjściowego parametru Sku.Name polecenia cmdlet konta magazynu w celu wyrównania z wejściowym parametrem SkuName przez dodanie znaku „-”, na przykład zmiana „StandardLRS” na „Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="b026c-675">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="b026c-676">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b026c-676">New-AzStorageAccount</span></span>
    - <span data-ttu-id="b026c-677">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b026c-677">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="b026c-678">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b026c-678">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b026c-679">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b026c-679">Az.Websites</span></span>
* <span data-ttu-id="b026c-680">Właściwość „Kind” będzie teraz ustawiona dla obiektów PSSite zwracanych przez polecenie Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b026c-680">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="b026c-681">Polecenia Get-AzWebApp\*Metrics i Get-AzAppServicePlanMetrics oznaczono jako przestarzałe</span><span class="sxs-lookup"><span data-stu-id="b026c-681">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="b026c-682">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-682">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b026c-683">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="b026c-683">Highlights since the last major release</span></span>
* <span data-ttu-id="b026c-684">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="b026c-684">General availability of `Az` module</span></span>
* <span data-ttu-id="b026c-685">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b026c-685">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b026c-686">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b026c-686">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b026c-687">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-687">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b026c-688">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="b026c-688">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b026c-689">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b026c-689">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b026c-690">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="b026c-690">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b026c-691">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-691">Az.Accounts</span></span>
* <span data-ttu-id="b026c-692">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="b026c-692">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b026c-693">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b026c-693">Az.Batch</span></span>
* <span data-ttu-id="b026c-694">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b026c-695">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b026c-695">Az.Cdn</span></span>
* <span data-ttu-id="b026c-696">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-696">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b026c-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b026c-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="b026c-698">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-698">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-699">Az.Compute</span></span>
* <span data-ttu-id="b026c-700">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="b026c-700">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="b026c-701">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-701">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b026c-702">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="b026c-702">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b026c-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b026c-703">Az.DataFactory</span></span>
* <span data-ttu-id="b026c-704">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="b026c-704">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b026c-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b026c-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="b026c-706">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-706">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b026c-707">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b026c-707">Az.EventGrid</span></span>
* <span data-ttu-id="b026c-708">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="b026c-708">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b026c-709">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b026c-709">Az.EventHub</span></span>
* <span data-ttu-id="b026c-710">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="b026c-710">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="b026c-711">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b026c-711">Az.HDInsight</span></span>
* <span data-ttu-id="b026c-712">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-712">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b026c-713">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b026c-713">Az.IotHub</span></span>
* <span data-ttu-id="b026c-714">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-714">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b026c-715">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b026c-715">Az.KeyVault</span></span>
* <span data-ttu-id="b026c-716">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-716">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b026c-717">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="b026c-717">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="b026c-718">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b026c-718">Az.MachineLearning</span></span>
* <span data-ttu-id="b026c-719">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-719">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="b026c-720">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b026c-720">Az.Media</span></span>
* <span data-ttu-id="b026c-721">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-721">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b026c-722">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b026c-722">Az.Monitor</span></span>
  * <span data-ttu-id="b026c-723">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="b026c-723">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="b026c-724">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="b026c-724">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="b026c-725">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="b026c-725">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="b026c-726">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b026c-726">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b026c-727">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b026c-727">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b026c-728">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b026c-728">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="b026c-729">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="b026c-729">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b026c-730">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-730">Az.Network</span></span>
* <span data-ttu-id="b026c-731">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-731">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b026c-732">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="b026c-732">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="b026c-733">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="b026c-733">Az.NotificationHubs</span></span>
* <span data-ttu-id="b026c-734">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-734">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b026c-735">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b026c-735">Az.OperationalInsights</span></span>
* <span data-ttu-id="b026c-736">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-736">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="b026c-737">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b026c-737">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="b026c-738">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-738">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b026c-739">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b026c-739">Az.RecoveryServices</span></span>
* <span data-ttu-id="b026c-740">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-740">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b026c-741">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b026c-741">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="b026c-742">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="b026c-742">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="b026c-743">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="b026c-743">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b026c-744">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b026c-744">Az.RedisCache</span></span>
* <span data-ttu-id="b026c-745">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-745">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b026c-746">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-746">Az.Resources</span></span>
* <span data-ttu-id="b026c-747">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="b026c-747">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="b026c-748">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-748">Az.Sql</span></span>
* <span data-ttu-id="b026c-749">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="b026c-749">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="b026c-750">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-750">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b026c-751">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="b026c-751">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="b026c-752">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="b026c-752">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="b026c-753">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="b026c-753">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="b026c-754">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="b026c-754">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="b026c-755">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="b026c-755">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b026c-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b026c-756">Az.Websites</span></span>
* <span data-ttu-id="b026c-757">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="b026c-757">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="b026c-758">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="b026c-758">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b026c-759">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="b026c-759">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="b026c-760">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="b026c-760">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="b026c-761">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-761">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b026c-762">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="b026c-762">Highlights since the last major release</span></span>
* <span data-ttu-id="b026c-763">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="b026c-763">General availability of `Az` module</span></span>
* <span data-ttu-id="b026c-764">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b026c-764">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b026c-765">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b026c-765">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b026c-766">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-766">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b026c-767">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="b026c-767">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b026c-768">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b026c-768">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b026c-769">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="b026c-769">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b026c-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-770">Az.Accounts</span></span>
* <span data-ttu-id="b026c-771">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b026c-771">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b026c-772">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b026c-772">Az.AnalysisServices</span></span>
* <span data-ttu-id="b026c-773">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="b026c-773">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="b026c-774">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="b026c-774">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b026c-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b026c-775">Az.Automation</span></span>
* <span data-ttu-id="b026c-776">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="b026c-776">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="b026c-777">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="b026c-777">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="b026c-778">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="b026c-778">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-779">Az.Compute</span></span>
* <span data-ttu-id="b026c-780">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-780">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b026c-781">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="b026c-781">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="b026c-782">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b026c-782">Az.ContainerInstance</span></span>
* <span data-ttu-id="b026c-783">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="b026c-783">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b026c-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b026c-784">Az.DataFactory</span></span>
* <span data-ttu-id="b026c-785">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="b026c-785">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="b026c-786">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b026c-786">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b026c-787">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-787">Az.Resources</span></span>
* <span data-ttu-id="b026c-788">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="b026c-788">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="b026c-789">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="b026c-789">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="b026c-790">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="b026c-790">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="b026c-791">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="b026c-791">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="b026c-792">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="b026c-792">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="b026c-793">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="b026c-793">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="b026c-794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-794">Az.Sql</span></span>
* <span data-ttu-id="b026c-795">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b026c-795">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b026c-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b026c-796">Az.Storage</span></span>
* <span data-ttu-id="b026c-797">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b026c-797">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="b026c-798">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b026c-798">New-AzStorageContext</span></span>
* <span data-ttu-id="b026c-799">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="b026c-799">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="b026c-800">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b026c-800">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b026c-801">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b026c-801">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b026c-802">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b026c-802">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="b026c-803">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b026c-803">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="b026c-804">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="b026c-804">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="b026c-805">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b026c-805">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b026c-806">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b026c-806">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b026c-807">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b026c-807">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="b026c-808">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b026c-808">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="b026c-809">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="b026c-809">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b026c-810">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="b026c-810">Highlights since the last major release</span></span>
* <span data-ttu-id="b026c-811">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="b026c-811">General availability of `Az` module</span></span>
* <span data-ttu-id="b026c-812">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b026c-812">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b026c-813">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b026c-813">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b026c-814">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-814">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b026c-815">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="b026c-815">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b026c-816">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b026c-816">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b026c-817">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="b026c-817">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b026c-818">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b026c-818">Az.Automation</span></span>
* <span data-ttu-id="b026c-819">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="b026c-819">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="b026c-820">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="b026c-820">Dynamic grouping</span></span>
    * <span data-ttu-id="b026c-821">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="b026c-821">Pre-Post script</span></span>
    * <span data-ttu-id="b026c-822">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="b026c-822">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-823">Az.Compute</span></span>
* <span data-ttu-id="b026c-824">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="b026c-824">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="b026c-825">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="b026c-825">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b026c-826">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b026c-826">Az.KeyVault</span></span>
* <span data-ttu-id="b026c-827">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="b026c-827">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b026c-828">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-828">Az.Network</span></span>
* <span data-ttu-id="b026c-829">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="b026c-829">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="b026c-830">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="b026c-830">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b026c-831">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b026c-831">Az.RecoveryServices</span></span>
* <span data-ttu-id="b026c-832">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="b026c-832">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="b026c-833">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="b026c-833">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="b026c-834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-834">Az.Resources</span></span>
* <span data-ttu-id="b026c-835">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b026c-835">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="b026c-836">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="b026c-836">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="b026c-837">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-837">Az.Sql</span></span>
* <span data-ttu-id="b026c-838">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="b026c-838">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b026c-839">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b026c-839">Az.Storage</span></span>
* <span data-ttu-id="b026c-840">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="b026c-840">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="b026c-841">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b026c-841">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b026c-842">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b026c-842">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b026c-843">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b026c-843">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b026c-844">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="b026c-844">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="b026c-845">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="b026c-845">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="b026c-846">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="b026c-846">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b026c-847">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b026c-847">Az.Websites</span></span>
* <span data-ttu-id="b026c-848">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="b026c-848">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="b026c-849">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="b026c-849">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b026c-850">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-850">Az.Accounts</span></span>
* <span data-ttu-id="b026c-851">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="b026c-851">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="b026c-852">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="b026c-852">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b026c-853">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b026c-853">Az.Automation</span></span>
* <span data-ttu-id="b026c-854">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="b026c-854">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="b026c-855">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="b026c-855">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="b026c-856">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="b026c-856">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b026c-857">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b026c-857">Az.Cdn</span></span>
* <span data-ttu-id="b026c-858">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="b026c-858">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-859">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-859">Az.Compute</span></span>
* <span data-ttu-id="b026c-860">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="b026c-860">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b026c-861">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b026c-861">Az.DataFactory</span></span>
* <span data-ttu-id="b026c-862">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="b026c-862">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b026c-863">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b026c-863">Az.LogicApp</span></span>
* <span data-ttu-id="b026c-864">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="b026c-864">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b026c-865">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-865">Az.Network</span></span>
* <span data-ttu-id="b026c-866">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="b026c-866">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b026c-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b026c-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="b026c-868">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b026c-868">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="b026c-869">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="b026c-869">SDK Update</span></span>
* <span data-ttu-id="b026c-870">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b026c-870">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="b026c-871">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b026c-871">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="b026c-872">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-872">Az.Resources</span></span>
* <span data-ttu-id="b026c-873">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="b026c-873">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="b026c-874">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="b026c-874">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="b026c-875">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="b026c-875">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="b026c-876">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="b026c-876">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="b026c-877">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="b026c-877">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="b026c-878">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="b026c-878">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="b026c-879">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-879">Az.Sql</span></span>
* <span data-ttu-id="b026c-880">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="b026c-880">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="b026c-881">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="b026c-881">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b026c-882">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b026c-882">Az.Storage</span></span>
* <span data-ttu-id="b026c-883">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b026c-883">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="b026c-884">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-884">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="b026c-885">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b026c-885">Az.AnalysisServices</span></span>
* <span data-ttu-id="b026c-886">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="b026c-886">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b026c-887">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b026c-887">Az.Automation</span></span>
* <span data-ttu-id="b026c-888">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b026c-888">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="b026c-889">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b026c-889">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="b026c-890">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b026c-890">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b026c-891">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b026c-891">Az.CognitiveServices</span></span>
* <span data-ttu-id="b026c-892">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="b026c-892">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-893">Az.Compute</span></span>
* <span data-ttu-id="b026c-894">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="b026c-894">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="b026c-895">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="b026c-895">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="b026c-896">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="b026c-896">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="b026c-897">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="b026c-897">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b026c-898">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b026c-898">Az.DataLakeStore</span></span>
* <span data-ttu-id="b026c-899">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="b026c-899">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b026c-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b026c-900">Az.EventHub</span></span>
* <span data-ttu-id="b026c-901">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="b026c-901">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="b026c-902">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b026c-902">Az.KeyVault</span></span>
* <span data-ttu-id="b026c-903">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b026c-903">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b026c-904">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b026c-904">Az.LogicApp</span></span>
* <span data-ttu-id="b026c-905">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="b026c-905">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="b026c-906">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="b026c-906">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="b026c-907">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="b026c-907">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="b026c-908">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b026c-908">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b026c-909">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b026c-909">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b026c-910">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b026c-910">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b026c-911">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b026c-911">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="b026c-912">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="b026c-912">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="b026c-913">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b026c-913">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b026c-914">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b026c-914">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b026c-915">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b026c-915">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b026c-916">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b026c-916">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="b026c-917">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="b026c-917">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b026c-918">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b026c-918">Az.Monitor</span></span>
* <span data-ttu-id="b026c-919">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="b026c-919">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b026c-920">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-920">Az.Network</span></span>
* <span data-ttu-id="b026c-921">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b026c-921">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b026c-922">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b026c-922">Az.OperationalInsights</span></span>
* <span data-ttu-id="b026c-923">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="b026c-923">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="b026c-924">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b026c-924">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="b026c-925">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="b026c-925">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="b026c-926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-926">Az.Resources</span></span>
* <span data-ttu-id="b026c-927">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b026c-927">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b026c-928">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b026c-928">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="b026c-929">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="b026c-929">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="b026c-930">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="b026c-930">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="b026c-931">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-931">Az.Sql</span></span>
* <span data-ttu-id="b026c-932">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b026c-932">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="b026c-933">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="b026c-933">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b026c-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b026c-934">Az.Websites</span></span>
* <span data-ttu-id="b026c-935">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="b026c-935">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="b026c-936">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-936">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b026c-937">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-937">Az.Accounts</span></span>
* <span data-ttu-id="b026c-938">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b026c-938">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b026c-939">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b026c-939">Az.AnalysisServices</span></span>
<span data-ttu-id="b026c-940">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="b026c-940">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-941">Az.Compute</span></span>
* <span data-ttu-id="b026c-942">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="b026c-942">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="b026c-943">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b026c-943">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="b026c-944">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="b026c-944">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b026c-945">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b026c-945">Az.RecoveryServices</span></span>
<span data-ttu-id="b026c-946">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="b026c-946">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b026c-947">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-947">Az.Resources</span></span>
* <span data-ttu-id="b026c-948">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="b026c-948">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="b026c-949">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b026c-949">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b026c-950">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="b026c-950">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="b026c-951">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b026c-951">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="b026c-952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-952">Az.Sql</span></span>
* <span data-ttu-id="b026c-953">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b026c-953">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="b026c-954">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="b026c-954">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="b026c-955">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="b026c-955">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="b026c-956">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-956">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b026c-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-957">Az.Accounts</span></span>
* <span data-ttu-id="b026c-958">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="b026c-958">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b026c-959">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b026c-959">Az.AnalysisServices</span></span>
* <span data-ttu-id="b026c-960">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="b026c-960">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b026c-961">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b026c-961">Az.RecoveryServices</span></span>
* <span data-ttu-id="b026c-962">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="b026c-962">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="b026c-963">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-963">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b026c-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-964">Az.Accounts</span></span>
* <span data-ttu-id="b026c-965">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="b026c-965">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b026c-966">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b026c-966">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b026c-967">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="b026c-967">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="b026c-968">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b026c-968">Az.Aks</span></span>
* <span data-ttu-id="b026c-969">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b026c-969">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b026c-970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b026c-970">Az.Automation</span></span>
* <span data-ttu-id="b026c-971">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="b026c-971">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="b026c-972">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b026c-972">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b026c-973">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b026c-973">Az.Cdn</span></span>
* <span data-ttu-id="b026c-974">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b026c-974">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-975">Az.Compute</span></span>
* <span data-ttu-id="b026c-976">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="b026c-976">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="b026c-977">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b026c-977">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="b026c-978">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b026c-978">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b026c-979">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b026c-979">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b026c-980">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b026c-980">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b026c-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b026c-981">Az.DataFactory</span></span>
* <span data-ttu-id="b026c-982">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="b026c-982">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b026c-983">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b026c-983">Az.DataLakeStore</span></span>
* <span data-ttu-id="b026c-984">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="b026c-984">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="b026c-985">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="b026c-985">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="b026c-986">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b026c-986">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b026c-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b026c-987">Az.IotHub</span></span>
* <span data-ttu-id="b026c-988">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b026c-988">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b026c-989">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b026c-989">Az.KeyVault</span></span>
* <span data-ttu-id="b026c-990">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b026c-990">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b026c-991">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-991">Az.Network</span></span>
* <span data-ttu-id="b026c-992">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b026c-992">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b026c-993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-993">Az.Resources</span></span>
* <span data-ttu-id="b026c-994">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b026c-994">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="b026c-995">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b026c-995">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="b026c-996">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b026c-996">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="b026c-997">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="b026c-997">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="b026c-998">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="b026c-998">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="b026c-999">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b026c-999">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="b026c-1000">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="b026c-1000">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b026c-1001">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b026c-1001">Az.ServiceFabric</span></span>
* <span data-ttu-id="b026c-1002">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="b026c-1002">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="b026c-1003">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="b026c-1003">Fix some error messages.</span></span>
* <span data-ttu-id="b026c-1004">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b026c-1004">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="b026c-1005">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="b026c-1005">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b026c-1006">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b026c-1006">Az.SignalR</span></span>
* <span data-ttu-id="b026c-1007">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b026c-1007">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="b026c-1008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-1008">Az.Sql</span></span>
* <span data-ttu-id="b026c-1009">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b026c-1009">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b026c-1010">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="b026c-1010">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="b026c-1011">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="b026c-1011">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="b026c-1012">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="b026c-1012">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b026c-1013">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b026c-1013">Az.Storage</span></span>
* <span data-ttu-id="b026c-1014">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b026c-1014">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b026c-1015">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="b026c-1015">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="b026c-1016">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b026c-1016">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="b026c-1017">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="b026c-1017">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="b026c-1018">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b026c-1018">Az.TrafficManager</span></span>
* <span data-ttu-id="b026c-1019">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b026c-1019">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b026c-1020">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b026c-1020">Az.Websites</span></span>
* <span data-ttu-id="b026c-1021">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="b026c-1021">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b026c-1022">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="b026c-1022">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="b026c-1023">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="b026c-1023">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="b026c-1024">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-1024">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b026c-1025">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-1025">Az.Accounts</span></span>
* <span data-ttu-id="b026c-1026">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="b026c-1026">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-1027">Az.Compute</span></span>
* <span data-ttu-id="b026c-1028">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b026c-1028">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="b026c-1029">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="b026c-1029">Updated the description of ID in help files</span></span>
* <span data-ttu-id="b026c-1030">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-1030">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b026c-1031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b026c-1031">Az.DataLakeStore</span></span>
* <span data-ttu-id="b026c-1032">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="b026c-1032">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="b026c-1033">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="b026c-1033">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b026c-1034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b026c-1034">Az.EventGrid</span></span>
* <span data-ttu-id="b026c-1035">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="b026c-1035">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="b026c-1036">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="b026c-1036">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="b026c-1037">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="b026c-1037">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b026c-1038">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="b026c-1038">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b026c-1039">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="b026c-1039">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b026c-1040">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="b026c-1040">Dead letter endpoint.</span></span>
    - <span data-ttu-id="b026c-1041">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="b026c-1041">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b026c-1042">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="b026c-1042">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b026c-1043">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="b026c-1043">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b026c-1044">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="b026c-1044">Dead letter endpoint.</span></span>
* <span data-ttu-id="b026c-1045">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="b026c-1045">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="b026c-1046">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b026c-1046">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b026c-1047">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b026c-1047">Az.IotHub</span></span>
* <span data-ttu-id="b026c-1048">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="b026c-1048">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b026c-1049">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b026c-1049">Az.LogicApp</span></span>
* <span data-ttu-id="b026c-1050">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="b026c-1050">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="b026c-1051">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-1051">Az.Resources</span></span>
* <span data-ttu-id="b026c-1052">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="b026c-1052">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="b026c-1053">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="b026c-1053">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="b026c-1054">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b026c-1054">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b026c-1055">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="b026c-1055">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="b026c-1056">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="b026c-1056">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="b026c-1057">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="b026c-1057">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b026c-1058">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b026c-1058">Az.SignalR</span></span>
* <span data-ttu-id="b026c-1059">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-1059">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="b026c-1060">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-1060">Az.Sql</span></span>
* <span data-ttu-id="b026c-1061">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="b026c-1061">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b026c-1062">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b026c-1062">Az.Storage</span></span>
* <span data-ttu-id="b026c-1063">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="b026c-1063">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="b026c-1064">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b026c-1064">New-AzStorageContext</span></span>
* <span data-ttu-id="b026c-1065">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="b026c-1065">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="b026c-1066">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b026c-1066">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b026c-1067">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b026c-1067">Az.Websites</span></span>
* <span data-ttu-id="b026c-1068">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="b026c-1068">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="b026c-1069">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-1069">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="b026c-1070">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-1070">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="b026c-1071">Ogólne</span><span class="sxs-lookup"><span data-stu-id="b026c-1071">General</span></span>

- <span data-ttu-id="b026c-1072">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="b026c-1072">General Availability of Az Module</span></span>
- <span data-ttu-id="b026c-1073">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="b026c-1073">Online help for each module</span></span>
- <span data-ttu-id="b026c-1074">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="b026c-1074">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="b026c-1075">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="b026c-1075">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="b026c-1076">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-1076">Az.Accounts</span></span>
- <span data-ttu-id="b026c-1077">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b026c-1077">Changed from Az.Profile</span></span>
- <span data-ttu-id="b026c-1078">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="b026c-1078">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b026c-1079">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b026c-1079">Az.ApiManagement</span></span>
- <span data-ttu-id="b026c-1080">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="b026c-1080">Fixes for #7002</span></span>
- <span data-ttu-id="b026c-1081">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b026c-1081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="b026c-1082">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b026c-1082">Az.Batch</span></span>
- <span data-ttu-id="b026c-1083">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="b026c-1083">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="b026c-1084">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="b026c-1084">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="b026c-1085">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b026c-1085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="b026c-1086">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b026c-1086">Az.Billing</span></span>
- <span data-ttu-id="b026c-1087">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b026c-1087">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="b026c-1088">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="b026c-1088">Az.CognitivServices</span></span>
- <span data-ttu-id="b026c-1089">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b026c-1089">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="b026c-1090">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="b026c-1090">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b026c-1091">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b026c-1091">Az.ContainerInstance</span></span>
- <span data-ttu-id="b026c-1092">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="b026c-1092">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="b026c-1093">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b026c-1093">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="b026c-1094">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b026c-1094">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b026c-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b026c-1095">Az.DataLakeStore</span></span>
- <span data-ttu-id="b026c-1096">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b026c-1096">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="b026c-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b026c-1097">Az.Monitor</span></span>
- <span data-ttu-id="b026c-1098">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b026c-1098">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="b026c-1099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b026c-1099">Az.KeyVault</span></span>
- <span data-ttu-id="b026c-1100">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="b026c-1100">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="b026c-1101">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b026c-1101">Az.MachineLearning</span></span>
- <span data-ttu-id="b026c-1102">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="b026c-1102">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="b026c-1103">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b026c-1103">Az.Media</span></span>
- <span data-ttu-id="b026c-1104">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b026c-1104">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b026c-1105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-1105">Az.Network</span></span>
<span data-ttu-id="b026c-1106">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b026c-1106">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="b026c-1107">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b026c-1107">New cmdlets added:</span></span>
        - <span data-ttu-id="b026c-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b026c-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b026c-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b026c-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b026c-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b026c-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b026c-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b026c-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b026c-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b026c-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b026c-1113">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b026c-1113">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="b026c-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b026c-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="b026c-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b026c-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="b026c-1116">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b026c-1116">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="b026c-1117">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b026c-1117">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="b026c-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b026c-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b026c-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b026c-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b026c-1120">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-1120">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="b026c-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="b026c-1122">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="b026c-1122">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="b026c-1123">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b026c-1123">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="b026c-1124">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b026c-1124">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b026c-1125">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b026c-1125">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b026c-1126">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b026c-1126">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="b026c-1127">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b026c-1127">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="b026c-1128">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b026c-1128">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="b026c-1129">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b026c-1129">Az.OperationalInsights</span></span>
- <span data-ttu-id="b026c-1130">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b026c-1130">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="b026c-1131">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b026c-1131">Az.Profile</span></span>
- <span data-ttu-id="b026c-1132">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b026c-1132">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b026c-1133">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b026c-1133">Az.RecoveryServices</span></span>
- <span data-ttu-id="b026c-1134">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b026c-1134">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="b026c-1135">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-1135">Az.Resources</span></span>
- <span data-ttu-id="b026c-1136">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b026c-1136">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b026c-1137">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b026c-1137">Az.ServiceFabric</span></span>
- <span data-ttu-id="b026c-1138">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="b026c-1138">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="b026c-1139">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b026c-1139">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="b026c-1140">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b026c-1140">Az.SIgnalR</span></span>
- <span data-ttu-id="b026c-1141">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b026c-1141">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="b026c-1142">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-1142">Az.Sql</span></span>
- <span data-ttu-id="b026c-1143">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="b026c-1143">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="b026c-1144">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="b026c-1144">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="b026c-1145">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b026c-1145">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="b026c-1146">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b026c-1146">Az.Storage</span></span>
- <span data-ttu-id="b026c-1147">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b026c-1147">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b026c-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b026c-1148">Az.Websites</span></span>
- <span data-ttu-id="b026c-1149">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="b026c-1149">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="b026c-1150">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-1150">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="b026c-1151">Ogólne</span><span class="sxs-lookup"><span data-stu-id="b026c-1151">General</span></span>

* <span data-ttu-id="b026c-1152">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="b026c-1152">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="b026c-1153">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-1153">Az.Compute</span></span>

* <span data-ttu-id="b026c-1154">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="b026c-1154">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b026c-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b026c-1155">Az.DataLakeStore</span></span>

* <span data-ttu-id="b026c-1156">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="b026c-1156">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="b026c-1157">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b026c-1157">Az.FrontDoor</span></span>

* <span data-ttu-id="b026c-1158">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="b026c-1158">Fixed some broken links</span></span>
    - <span data-ttu-id="b026c-1159">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="b026c-1159">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="b026c-1160">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="b026c-1160">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b026c-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b026c-1161">Az.RecoveryServices</span></span>

* <span data-ttu-id="b026c-1162">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b026c-1162">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="b026c-1163">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b026c-1163">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="b026c-1164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-1164">Az.Resources</span></span>

* <span data-ttu-id="b026c-1165">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="b026c-1165">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="b026c-1166">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="b026c-1166">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="b026c-1167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-1167">Az.Sql</span></span>

* <span data-ttu-id="b026c-1168">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="b026c-1168">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="b026c-1169">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="b026c-1169">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="b026c-1170">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="b026c-1170">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="b026c-1171">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b026c-1171">Az.Storage</span></span>

* <span data-ttu-id="b026c-1172">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b026c-1172">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="b026c-1173">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="b026c-1173">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="b026c-1174">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b026c-1174">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b026c-1175">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="b026c-1175">Support Static Website configuration</span></span>
    - <span data-ttu-id="b026c-1176">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b026c-1176">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="b026c-1177">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b026c-1177">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b026c-1178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b026c-1178">Az.Websites</span></span>

* <span data-ttu-id="b026c-1179">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b026c-1179">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="b026c-1180">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="b026c-1180">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="b026c-1181">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b026c-1181">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="b026c-1182">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-1182">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b026c-1183">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b026c-1183">Az.ApiManagement</span></span>
* <span data-ttu-id="b026c-1184">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="b026c-1184">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="b026c-1185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b026c-1185">Az.Automation</span></span>
* <span data-ttu-id="b026c-1186">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="b026c-1186">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="b026c-1187">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="b026c-1187">Added Update Management cmdlets</span></span>
* <span data-ttu-id="b026c-1188">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="b026c-1188">Added Source Control cmdlets</span></span>
* <span data-ttu-id="b026c-1189">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="b026c-1189">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="b026c-1190">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="b026c-1190">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="b026c-1191">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-1191">Az.Compute</span></span>
* <span data-ttu-id="b026c-1192">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="b026c-1192">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="b026c-1193">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="b026c-1193">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b026c-1194">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b026c-1194">Az.ContainerInstance</span></span>
* <span data-ttu-id="b026c-1195">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="b026c-1195">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="b026c-1196">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b026c-1196">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b026c-1197">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="b026c-1197">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b026c-1198">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-1198">Az.Network</span></span>
* <span data-ttu-id="b026c-1199">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b026c-1199">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="b026c-1200">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b026c-1200">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="b026c-1201">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="b026c-1201">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="b026c-1202">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b026c-1202">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="b026c-1203">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b026c-1203">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b026c-1204">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="b026c-1204">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="b026c-1205">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="b026c-1205">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="b026c-1206">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b026c-1206">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b026c-1207">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b026c-1207">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="b026c-1208">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="b026c-1208">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="b026c-1209">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b026c-1209">Az.Relay</span></span>
* <span data-ttu-id="b026c-1210">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="b026c-1210">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="b026c-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-1211">Az.Resources</span></span>
* <span data-ttu-id="b026c-1212">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="b026c-1212">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="b026c-1213">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="b026c-1213">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="b026c-1214">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="b026c-1214">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b026c-1215">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b026c-1215">Az.ServiceFabric</span></span>
* <span data-ttu-id="b026c-1216">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="b026c-1216">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="b026c-1217">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-1217">Az.Sql</span></span>
* <span data-ttu-id="b026c-1218">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="b026c-1218">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="b026c-1219">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b026c-1219">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b026c-1220">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b026c-1220">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b026c-1221">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b026c-1221">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b026c-1222">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b026c-1222">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b026c-1223">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b026c-1223">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b026c-1224">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b026c-1224">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b026c-1225">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b026c-1225">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b026c-1226">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b026c-1226">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="b026c-1227">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="b026c-1227">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="b026c-1228">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="b026c-1228">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="b026c-1229">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="b026c-1229">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="b026c-1230">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b026c-1230">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b026c-1231">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b026c-1231">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b026c-1232">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b026c-1232">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="b026c-1233">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b026c-1233">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="b026c-1234">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b026c-1234">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="b026c-1235">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-1235">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b026c-1236">Ogólne</span><span class="sxs-lookup"><span data-stu-id="b026c-1236">General</span></span>
* <span data-ttu-id="b026c-1237">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="b026c-1237">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="b026c-1238">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b026c-1238">Az.Profile</span></span>
* <span data-ttu-id="b026c-1239">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="b026c-1239">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="b026c-1240">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="b026c-1240">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="b026c-1241">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="b026c-1241">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="b026c-1242">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="b026c-1242">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="b026c-1243">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="b026c-1243">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="b026c-1244">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="b026c-1244">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="b026c-1245">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="b026c-1245">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="b026c-1246">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b026c-1246">Az.CognitiveServices</span></span>
* <span data-ttu-id="b026c-1247">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="b026c-1247">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-1248">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-1248">Az.Compute</span></span>
* <span data-ttu-id="b026c-1249">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b026c-1249">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="b026c-1250">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="b026c-1250">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="b026c-1251">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="b026c-1251">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b026c-1252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b026c-1252">Az.DataLakeStore</span></span>
* <span data-ttu-id="b026c-1253">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="b026c-1253">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="b026c-1254">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="b026c-1254">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="b026c-1255">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="b026c-1255">Az.Insights</span></span>
* <span data-ttu-id="b026c-1256">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="b026c-1256">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="b026c-1257">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="b026c-1257">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="b026c-1258">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="b026c-1258">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="b026c-1259">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="b026c-1259">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b026c-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-1260">Az.Network</span></span>
* <span data-ttu-id="b026c-1261">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b026c-1261">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="b026c-1262">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b026c-1262">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="b026c-1263">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b026c-1263">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="b026c-1264">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b026c-1264">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="b026c-1265">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="b026c-1265">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b026c-1266">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b026c-1266">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b026c-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b026c-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b026c-1268">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b026c-1268">Az.PolicyInsights</span></span>
* <span data-ttu-id="b026c-1269">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="b026c-1269">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b026c-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-1270">Az.Resources</span></span>
* <span data-ttu-id="b026c-1271">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="b026c-1271">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="b026c-1272">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="b026c-1272">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b026c-1273">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b026c-1273">Az.ServiceBus</span></span>
* <span data-ttu-id="b026c-1274">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="b026c-1274">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b026c-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b026c-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="b026c-1276">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="b026c-1276">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="b026c-1277">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="b026c-1277">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="b026c-1278">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="b026c-1278">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="b026c-1279">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="b026c-1279">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="b026c-1280">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="b026c-1280">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="b026c-1281">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-1281">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="b026c-1282">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b026c-1282">Az.Profile</span></span>
* <span data-ttu-id="b026c-1283">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="b026c-1283">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="b026c-1284">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="b026c-1284">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-1285">Az.Compute</span></span>
* <span data-ttu-id="b026c-1286">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="b026c-1286">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="b026c-1287">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b026c-1287">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b026c-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b026c-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="b026c-1289">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b026c-1289">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="b026c-1290">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b026c-1290">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="b026c-1291">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b026c-1291">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b026c-1292">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b026c-1292">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b026c-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b026c-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b026c-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-1294">Az.Network</span></span>
* <span data-ttu-id="b026c-1295">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b026c-1295">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="b026c-1296">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b026c-1296">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b026c-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-1297">Az.Resources</span></span>
* <span data-ttu-id="b026c-1298">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="b026c-1298">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="b026c-1299">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="b026c-1299">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="b026c-1300">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-1300">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="b026c-1301">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b026c-1301">Azure.Storage</span></span>
* <span data-ttu-id="b026c-1302">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="b026c-1302">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="b026c-1303">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b026c-1303">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="b026c-1304">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b026c-1304">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b026c-1305">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="b026c-1305">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="b026c-1306">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b026c-1306">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="b026c-1307">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b026c-1307">Az.CognitiveServices</span></span>
* <span data-ttu-id="b026c-1308">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="b026c-1308">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b026c-1309">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b026c-1309">Az.Compute</span></span>
* <span data-ttu-id="b026c-1310">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="b026c-1310">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="b026c-1311">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="b026c-1311">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="b026c-1312">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="b026c-1312">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="b026c-1313">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b026c-1313">Az.DataFactoryV2</span></span>
* <span data-ttu-id="b026c-1314">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="b026c-1314">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b026c-1315">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b026c-1315">Az.Network</span></span>
* <span data-ttu-id="b026c-1316">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="b026c-1316">Added NetworkProfile functionality.</span></span> <span data-ttu-id="b026c-1317">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="b026c-1317">new cmdlets added</span></span>
    - <span data-ttu-id="b026c-1318">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b026c-1318">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="b026c-1319">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b026c-1319">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="b026c-1320">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b026c-1320">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="b026c-1321">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b026c-1321">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="b026c-1322">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-1322">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="b026c-1323">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-1323">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="b026c-1324">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="b026c-1324">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="b026c-1325">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b026c-1325">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="b026c-1326">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b026c-1326">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b026c-1327">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b026c-1327">Az.RedisCache</span></span>
* <span data-ttu-id="b026c-1328">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="b026c-1328">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="b026c-1329">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="b026c-1329">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="b026c-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b026c-1330">Az.Resources</span></span>
* <span data-ttu-id="b026c-1331">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b026c-1331">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b026c-1332">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="b026c-1332">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="b026c-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b026c-1333">Az.Sql</span></span>
* <span data-ttu-id="b026c-1334">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b026c-1334">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b026c-1335">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b026c-1335">Az.Websites</span></span>
* <span data-ttu-id="b026c-1336">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="b026c-1336">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="b026c-1337">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="b026c-1337">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="b026c-1338">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b026c-1338">0.2.0 - September 2018</span></span>
 <span data-ttu-id="b026c-1339">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="b026c-1339">Initial Release</span></span>