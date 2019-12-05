---
title: Informacje o wersji programu Azure PowerShell
description: Uzyskaj informacje na temat wszystkich najnowszych aktualizacji modułów programu Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 8c1369cdedf8848f3c62ca6b6bc4eb3d2d78be95
ms.sourcegitcommit: f9445d1525eac8c165637e1a80fbc92b1ab005c2
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/28/2019
ms.locfileid: "74656823"
---
## <a name="280---october-2019"></a><span data-ttu-id="c8c8b-103">2.8.0 — październik 2019 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="c8c8b-104">Ogólne</span><span class="sxs-lookup"><span data-stu-id="c8c8b-104">General</span></span>
* <span data-ttu-id="c8c8b-105">Wydanie Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="c8c8b-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c8c8b-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-106">Az.Accounts</span></span>
* <span data-ttu-id="c8c8b-107">Aktualizacja telemetrii i ponowne zapisywanie adresów URL dla wygenerowanych modułów oraz naprawa testów jednostkowych systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c8c8b-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c8c8b-108">Az.ApiManagement</span></span>
* <span data-ttu-id="c8c8b-109">**Set-AzApiManagementApi** — Dodano obsługę aktualizowania interfejsu API do właściwości ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="c8c8b-110">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="c8c8b-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c8c8b-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-111">Az.Automation</span></span>
* <span data-ttu-id="c8c8b-112">Naprawiono parametr ponownego uruchamiania polecenia cmdlet New-AzureAutomationSoftwareUpdateConfiguration dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="c8c8b-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c8c8b-113">Az.Batch</span></span>
* <span data-ttu-id="c8c8b-114">Polecenie **Get-AzBatchNodeAgentSku** jest przestarzałe i zostanie zastąpione poleceniem **Get-AzBatchSupportImage** w wersji 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-115">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-116">Dodano parametry Priority, EvictionPolicy i MaxPrice do poleceń cmdlet New-AzVM i New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c8c8b-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="c8c8b-117">Naprawiono komunikat ostrzegawczy i dokumentację pomocy dla poleceń Add-AzVMAdditionalUnattendContent i Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="c8c8b-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="c8c8b-118">Naprawiono wyjątek -skipVmBackup dla maszyn wirtualnych z systemem Linux z dyskami zarządzanymi dla polecenia Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="c8c8b-119">Naprawiono usterkę w ustawieniach szyfrowania aktualizacji w scenariuszu dwuprzebiegowym polecenia Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c8c8b-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c8c8b-120">Az.DataFactory</span></span>
* <span data-ttu-id="c8c8b-121">Dodano polecenia CRUD dla przepływu danych usługi ADF w wersji 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow i Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="c8c8b-122">Dodano polecenia akcji dla sesji debugowania przepływu danych usługi ADF w wersji 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand i Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="c8c8b-123">Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.2.0</span><span class="sxs-lookup"><span data-stu-id="c8c8b-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c8c8b-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c8c8b-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="c8c8b-125">Naprawiono weryfikację kont, aby umożliwić przekazywanie kont ze znakiem „-” bez domeny</span><span class="sxs-lookup"><span data-stu-id="c8c8b-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="c8c8b-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="c8c8b-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="c8c8b-127">Zaktualizowano program PowerShell do wersji 1.0.0</span><span class="sxs-lookup"><span data-stu-id="c8c8b-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="c8c8b-128">Zaktualizowano zestaw SDK do wersji 1.0.2</span><span class="sxs-lookup"><span data-stu-id="c8c8b-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="c8c8b-129">Zaktualizowano testy, aby odwoływały się do nowej wersji zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="c8c8b-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="c8c8b-130">Zaktualizowano strukturę wyjściową z zagnieżdżonej do spłaszczonej.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c8c8b-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c8c8b-131">Az.IotHub</span></span>
* <span data-ttu-id="c8c8b-132">Dodano nowe źródło routingu: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="c8c8b-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="c8c8b-133">Drobna poprawka usterki: Polecenie Get-AzIothub nie zwraca wartości subscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8c8b-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="c8c8b-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c8c8b-134">Az.Monitor</span></span>
* <span data-ttu-id="c8c8b-135">Dodano nowe odbiorniki grupy akcji dla polecenia cmdlet New-AzActionGroupReceiver: -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="c8c8b-135">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="c8c8b-136">Włączono korzystanie z typowych schematów alertów dla odbiorników.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="c8c8b-137">Nie dotyczy to odbiorników wiadomości SMS, powiadomień push usługi Azure App , narzędzia ITSM i połączeń głosowych</span><span class="sxs-lookup"><span data-stu-id="c8c8b-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="c8c8b-138">Elementy webhook obsługują teraz uwierzytelnianie za pomocą usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-138">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-139">Az.Network</span></span>
* <span data-ttu-id="c8c8b-140">Dodano nowe polecenie cmdlet Get-AzAvailableServiceAlias, które można wywołać, aby pobrać aliasy do użytku z zasadami punktu końcowego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="c8c8b-141">Dodano obsługę dodawania selektorów ruchu do połączeń bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c8c8b-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="c8c8b-142">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-142">New cmdlets added:</span></span>
        - <span data-ttu-id="c8c8b-143">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-143">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="c8c8b-144">Polecenia cmdlet zostały zaktualizowane o opcjonalny parametr -TrafficSelectorPolicies -New-AzVirtualNetworkGatewayConnection -Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzVirtualNetworkGatewayConnection   -Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c8c8b-145">Dodano obsługę protokołów ESP i AH do konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="c8c8b-145">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="c8c8b-146">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-146">Updated cmdlets:</span></span>
        - <span data-ttu-id="c8c8b-147">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-147">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c8c8b-148">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-148">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c8c8b-149">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-149">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="c8c8b-150">Poprawiono obsługę wyjątków w poleceniach cmdlet usługi Cortex</span><span class="sxs-lookup"><span data-stu-id="c8c8b-150">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="c8c8b-151">Dodano nowe generacje i jednostki SKU dla elementów VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c8c8b-151">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="c8c8b-152">Wprowadzono nowe generacje dla elementów VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-152">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="c8c8b-153">Wprowadzono nowe jednostki SKU o wysokiej przepływności dla elementów VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-153">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c8c8b-154">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c8c8b-154">Az.RedisCache</span></span>
* <span data-ttu-id="c8c8b-155">Zaktualizowano dokumentację referencyjną polecenia „Set-AzRedisCache” w celu uwzględnienia brakujących wartości parametru „-Size”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-155">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-156">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-157">Dodano obsługę ustawiania administratora usługi Active Directory w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="c8c8b-157">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c8c8b-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-158">Az.Storage</span></span>
* <span data-ttu-id="c8c8b-159">Uaktualniono bibliotekę klienta usługi Azure Storage do wersji 11.1.0</span><span class="sxs-lookup"><span data-stu-id="c8c8b-159">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="c8c8b-160">Utworzenie listy kontenerów przy użyciu interfejsu API płaszczyzny zarządzania spowoduje wyświetlenie listy przy użyciu właściwości NextPageLink</span><span class="sxs-lookup"><span data-stu-id="c8c8b-160">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="c8c8b-161">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c8c8b-161">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="c8c8b-162">Utworzenie listy kont magazynu z subskrypcji spowoduje wyświetlenie listy przy użyciu właściwości NextPageLink</span><span class="sxs-lookup"><span data-stu-id="c8c8b-162">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="c8c8b-163">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8c8b-163">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c8c8b-164">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c8c8b-164">Az.StorageSync</span></span>
* <span data-ttu-id="c8c8b-165">Naprawiono problem 9810 w poleceniu Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-165">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c8c8b-166">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c8c8b-166">Az.Websites</span></span>
* <span data-ttu-id="c8c8b-167">Aktualizowanie elementu ASP aplikacji przy użyciu polecenia Set-AzWebApp kończyło się niepowodzeniem</span><span class="sxs-lookup"><span data-stu-id="c8c8b-167">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="c8c8b-168">2.7.0 — wrzesień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-168">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="c8c8b-169">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c8c8b-169">Az.ApiManagement</span></span>
* <span data-ttu-id="c8c8b-170">Aktualizacja opisu parametru „-Format” w dokumentacji referencyjnej polecenia „Set-AzApiManagementPolicy”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-170">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="c8c8b-171">Usunięto z dokumentacji referencyjnej odwołania do przestarzałego polecenia cmdlet „Update-AzApiManagementDeployment”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-171">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="c8c8b-172">Zamiast niego należy używać polecenia „Set-AzApiManagement”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-172">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c8c8b-173">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-173">Az.Automation</span></span>
* <span data-ttu-id="c8c8b-174">Poprawiono literówkę w przykładzie w dokumentacji referencyjnej polecenia „Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-174">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="c8c8b-175">Dodano wyjaśnienie dotyczące ograniczeń systemu operacyjnego dla polecenia Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="c8c8b-175">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="c8c8b-176">Naprawiono wyjątek odwołania o wartości null dla opcji -Wait polecenia cmdlet Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-176">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-177">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-177">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-178">Dodanie parametru UploadSizeInBytes do polecenia New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-178">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="c8c8b-179">Dodanie parametru Incremental do polecenia New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-179">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="c8c8b-180">Dodanie funkcji maszyny wirtualnej o niskim priorytecie:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-180">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="c8c8b-181">do polecenia New-AzVMConfig dodano parametry MaxPrice, EvictionPolicy i Priority.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-181">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="c8c8b-182">Parametr MaxPrice został dodany do poleceń cmdlet New-AzVmssConfig, Update-AzVM i Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-182">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="c8c8b-183">Rozwiązanie problemu z odwołaniem do maszyny wirtualnej dla polecenia cmdlet Get-AzAvailabilitySet, gdy wyświetla listę wszystkich zestawów dostępności w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-183">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="c8c8b-184">Naprawienie wyjątku o wartości null dla polecenia Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-184">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="c8c8b-185">Naprawienie metody przeszukiwania wirtualnego dysku twardego dla pozycji względem końca.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-185">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="c8c8b-186">Rozwiązanie problemu z dyskami UltraSSD dla poleceń New-AzVM i Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-186">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c8c8b-187">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c8c8b-187">Az.DataFactory</span></span>
* <span data-ttu-id="c8c8b-188">Dodanie 3 nowych poleceń do usługi ADF w wersji 2 — Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription i Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="c8c8b-188">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="c8c8b-189">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.3</span><span class="sxs-lookup"><span data-stu-id="c8c8b-189">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c8c8b-190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c8c8b-190">Az.HDInsight</span></span>
* <span data-ttu-id="c8c8b-191">Wywołanie zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="c8c8b-191">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c8c8b-192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c8c8b-192">Az.IotHub</span></span>
* <span data-ttu-id="c8c8b-193">Dodanie obsługi w celu wywołania trybu failover dla usługi IotHub do sparowanego geograficznie regionu odzyskiwania po awarii.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-193">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="c8c8b-194">Dodanie obsługi do zarządzania wzbogacaniem komunikatów dla usługi IotHub.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-194">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="c8c8b-195">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-195">New cmdlets are:</span></span>
    - <span data-ttu-id="c8c8b-196">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c8c8b-196">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="c8c8b-197">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c8c8b-197">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="c8c8b-198">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c8c8b-198">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="c8c8b-199">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c8c8b-199">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c8c8b-200">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c8c8b-200">Az.Monitor</span></span>
* <span data-ttu-id="c8c8b-201">Wskazanie najnowszego zestawu Monitor SDK, tj. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="c8c8b-201">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="c8c8b-202">Dodaje zmiany niepowodujące niezgodności do poleceń cmdlet metryk, tj. wyliczenie Unit obsługuje kilka nowych wartości.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-202">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="c8c8b-203">Są to polecenia cmdlet tylko do odczytu, więc nie będzie żadnych zmian w danych wejściowych tych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-203">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="c8c8b-204">Wartość api-version żądań **ActionGroups** to teraz **2019-06-01**, wcześniej było to **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-204">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="c8c8b-205">Testy scenariusza zostały zaktualizowane w celu dostosowania do tej zmiany.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-205">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="c8c8b-206">Konstruktory dla klas **EmailReceiver** i **WebhookReceiver** dodały jeden nowy argument obowiązkowy, tj. wartość logiczną o nazwie **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-206">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="c8c8b-207">Obecnie wartość ta jest stała i równa **false**, aby ukryć tę zmianę powodującą niezgodność przed poleceniami cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-207">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="c8c8b-208">**UWAGA**: Jest to tymczasowa zmiana, która musi być zweryfikowana przez zespół ds. alertów.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-208">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="c8c8b-209">Kolejność argumentów konstruktora klasy **Source** (powiązanej z klasą **ScheduledQueryRuleSource**) zmieniła się od poprzedniego zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-209">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="c8c8b-210">Ta zmiana wymaga naprawienia dwóch testów jednostkowych: kompilowały się, ale nie przechodziły testów.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-210">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="c8c8b-211">Kolejność argumentów konstruktora klasy **AlertingAction** (powiązanej z klasą **ScheduledQueryRuleSource**) została zmieniona od poprzedniego zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-211">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="c8c8b-212">Ta zmiana wymaga naprawienia dwóch testów jednostkowych: kompilowały się, ale nie przechodziły testów.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="c8c8b-213">Obsługa kryteriów progu dynamicznego dla alertu metryki w wersji 2</span><span class="sxs-lookup"><span data-stu-id="c8c8b-213">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="c8c8b-214">New-AzMetricAlertRuleV2Criteria: teraz tworzy kryteria progów dynamicznych</span><span class="sxs-lookup"><span data-stu-id="c8c8b-214">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="c8c8b-215">Add-AzMetricAlertRuleV2: teraz akceptuje kryteria progów dynamicznych</span><span class="sxs-lookup"><span data-stu-id="c8c8b-215">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="c8c8b-216">Ulepszenia poleceń cmdlet reguły zaplanowanego zapytania (SQR)</span><span class="sxs-lookup"><span data-stu-id="c8c8b-216">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="c8c8b-217">Polecenia cmdlet będą akceptować parametr „Location” w obu formatach: jako lokalizację (np. eastus) i jako nazwę wyświetlaną lokalizacji (np. East US)</span><span class="sxs-lookup"><span data-stu-id="c8c8b-217">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="c8c8b-218">Poprawnie zilustrowano parametr „Enabled” w plikach pomocy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-218">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="c8c8b-219">Dodano przykłady dla opcjonalnego parametru „ActionGroup”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-219">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="c8c8b-220">Ogólnie ulepszono pliki pomocy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-220">Overall improved help files</span></span>
* <span data-ttu-id="c8c8b-221">Naprawienie usterki dotyczącej określania typu zakresu dla polecenia „Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-221">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-222">Az.Network</span></span>
* <span data-ttu-id="c8c8b-223">Naprawienie nieprawidłowego przykładu w dokumentacji referencyjnej polecenia „New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-223">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="c8c8b-224">Dodanie w dokumentacji referencyjnej polecenia „Get-AzNetworkWatcherPacketCapture” uwagi dotyczącej pobierania wszystkich właściwości na potrzeby przechwytywania pakietów</span><span class="sxs-lookup"><span data-stu-id="c8c8b-224">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="c8c8b-225">Naprawiono przykład w dokumentacji referencyjnej polecenia „Test-AzNetworkWatcherIPFlow”, aby poprawnie wyliczał karty sieciowe</span><span class="sxs-lookup"><span data-stu-id="c8c8b-225">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="c8c8b-226">Ulepszono analizę wyjątku w chmurze, aby wyświetlane były dodatkowe szczegóły, jeśli są obecne</span><span class="sxs-lookup"><span data-stu-id="c8c8b-226">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="c8c8b-227">Ulepszono analizę wyjątku w chmurze, aby był obsługiwany dodatkowy typ wyjątku zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="c8c8b-227">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="c8c8b-228">Naprawiono niepoprawne mapowanie modeli reguł zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="c8c8b-228">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="c8c8b-229">Dodano właściwości interfejsu sieciowego dla funkcji prywatnego adresu IP</span><span class="sxs-lookup"><span data-stu-id="c8c8b-229">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="c8c8b-230">Dodano właściwość „PrivateEndpoint” jako typ PSResourceId do elementu PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c8c8b-230">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="c8c8b-231">Dodano właściwość „PrivateLinkConnectionProperties” jako typ PSIpConfigurationConnectivityInformation do elementu PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c8b-231">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="c8c8b-232">Dodano nową klasę modelu PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-232">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="c8c8b-233">Dodano nowy typ ApplicationRuleProtocolType „mssql” dla zasobu usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="c8c8b-233">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="c8c8b-234">Obsługa linku wielokrotnego w wirtualnej sieci WAN</span><span class="sxs-lookup"><span data-stu-id="c8c8b-234">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="c8c8b-235">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-235">New cmdlets</span></span>
        - <span data-ttu-id="c8c8b-236">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="c8c8b-236">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="c8c8b-237">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-237">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="c8c8b-238">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-238">Updated cmdlet:</span></span>
        - <span data-ttu-id="c8c8b-239">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="c8c8b-239">New-VpnSite</span></span>
        - <span data-ttu-id="c8c8b-240">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="c8c8b-240">Update-VpnSite</span></span>
        - <span data-ttu-id="c8c8b-241">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-241">New-VpnConnection</span></span>
        - <span data-ttu-id="c8c8b-242">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-242">Update-VpnConnection</span></span>
* <span data-ttu-id="c8c8b-243">Niektóre dokumenty dla przykładów programu PowerShell naprawiono w taki sposób, aby były w nich używane polecenia cmdlet Az zamiast poleceń cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="c8c8b-243">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c8c8b-244">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-244">Az.RecoveryServices</span></span>
* <span data-ttu-id="c8c8b-245">Aktualizacja obiektu AzureVMpolicy o atrybut ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="c8c8b-245">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="c8c8b-246">Dodano testy dotyczące zasad maszyny wirtualnej i przywracania oryginalnego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-246">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-247">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-247">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-248">Naprawienie usterki polegającej na tym, że nie można było wywołać polecenia New-AzRoleAssignment bez parametru Scope.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-248">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c8c8b-249">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c8c8b-249">Az.ServiceFabric</span></span>
* <span data-ttu-id="c8c8b-250">Poprawiono literówkę w przykładzie w dokumentacji referencyjnej polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-250">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="c8c8b-251">Dodanie nowych poleceń cmdlet do zarządzania aplikacją i usługami:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-251">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="c8c8b-252">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c8c8b-252">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c8c8b-253">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c8c8b-253">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="c8c8b-254">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c8c8b-254">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="c8c8b-255">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="c8c8b-255">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="c8c8b-256">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c8c8b-256">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c8c8b-257">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c8c8b-257">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c8c8b-258">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c8c8b-258">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="c8c8b-259">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c8c8b-259">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="c8c8b-260">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="c8c8b-260">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="c8c8b-261">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c8c8b-261">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c8c8b-262">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c8c8b-262">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="c8c8b-263">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c8c8b-263">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="c8c8b-264">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="c8c8b-264">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="c8c8b-265">Uaktualniono zestaw Service Fabric SDK do wersji 1.2.0, która korzysta z dostawcy zasobów usługi Service Fabric o wersji interfejsu API 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-265">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c8c8b-266">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c8c8b-266">Az.SignalR</span></span>
* <span data-ttu-id="c8c8b-267">Dodanie poleceń cmdlet Update, Restart, CheckNameAvailability i GetUsage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-267">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-268">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-268">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-269">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-269">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="c8c8b-270">Dodano przykład dla rdzenia wirtualnego do tworzenia elastycznej puli (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="c8c8b-270">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="c8c8b-271">Usunięcie weryfikacji parametru EmailAddresses i sprawdzania, czy parametr EmailAdmins nie ma wartości false w przypadku, gdy parametr EmailAddresses jest pusty w poleceniach Set-AzSqlServerAdvancedThreatProtectionPolicy i Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-271">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="c8c8b-272">Włączono usuwanie ustawień inspekcji serwera/bazy danych, gdy istnieje wiele ustawień diagnostycznych włączających kategorię inspekcji.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-272">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="c8c8b-273">Naprawa weryfikacji adresów e-mail w wielu poleceniach cmdlet do oceny luk w zabezpieczeniach SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting i Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="c8c8b-273">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c8c8b-274">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-274">Az.Storage</span></span>
* <span data-ttu-id="c8c8b-275">Zaktualizowano przykład w dokumentacji referencyjnej dla polecenia „Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-275">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="c8c8b-276">Obsługa zachowywania w pliku docelowym właściwości SMB pliku źródłowego przy przekazywaniu/pobieraniu pliku platformy Azure (atrybuty pliku, czas utworzenia pliku, czas ostatniego zapisu pliku)</span><span class="sxs-lookup"><span data-stu-id="c8c8b-276">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="c8c8b-277">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c8c8b-277">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="c8c8b-278">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c8c8b-278">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="c8c8b-279">Naprawa awarii przekazywania blokowego obiektu blob z właściwościami/metadanymi dla elementu ImmutabilityPolicy z obsługą kontenerów.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-279">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="c8c8b-280">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c8c8b-280">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="c8c8b-281">Obsługa zarządzania udziałami plików platformy Azure za pomocą interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="c8c8b-281">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="c8c8b-282">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c8c8b-282">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="c8c8b-283">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c8c8b-283">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="c8c8b-284">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c8c8b-284">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="c8c8b-285">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c8c8b-285">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c8c8b-286">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c8c8b-286">Az.Websites</span></span>
* <span data-ttu-id="c8c8b-287">Naprawa problemu powodującego usuwanie tagów aplikacji internetowych podczas migrowania aplikacji do nowego planu ASP</span><span class="sxs-lookup"><span data-stu-id="c8c8b-287">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="c8c8b-288">Naprawa polecenia Publish-AzureWebapp w taki sposób, aby działało w systemach Linux i Windows</span><span class="sxs-lookup"><span data-stu-id="c8c8b-288">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="c8c8b-289">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzWebAppPublishingProfile”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-289">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="c8c8b-290">2.6.0 — sierpień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-290">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="c8c8b-291">Ogólne</span><span class="sxs-lookup"><span data-stu-id="c8c8b-291">General</span></span>
* <span data-ttu-id="c8c8b-292">Naprawiono różne literówki w wielu modułach</span><span class="sxs-lookup"><span data-stu-id="c8c8b-292">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c8c8b-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-293">Az.Accounts</span></span>
* <span data-ttu-id="c8c8b-294">Obsługa pliku MSI przypisanego przez użytkownika w ramach uwierzytelniania usługi Azure Functions (nr 9479)</span><span class="sxs-lookup"><span data-stu-id="c8c8b-294">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="c8c8b-295">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c8c8b-295">Az.Aks</span></span>
* <span data-ttu-id="c8c8b-296">Rozwiązano problem z danymi wyjściowymi polecenia „Get-AzAks”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-296">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="c8c8b-297">Więcej informacji: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="c8c8b-297">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c8c8b-298">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c8c8b-298">Az.ApiManagement</span></span>
* <span data-ttu-id="c8c8b-299">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="c8c8b-299">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="c8c8b-300">Zaktualizowano wersję nuget .net, która nie wymusza ograniczeń dotyczących identyfikatorów productId, apiId, groupId i userId</span><span class="sxs-lookup"><span data-stu-id="c8c8b-300">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="c8c8b-301">**Get-AzApiManagementProduct** — dodano obsługę wysyłania zapytań dotyczących produktów przy użyciu interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-301">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="c8c8b-302">**New-AzApiManagementApiRevision** — poprawka rozwiązująca problem polegający na tym, że wartość ApiRevisionDescription nie była ustawiana podczas tworzenia nowej wersji pomocniczej interfejsu API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="c8c8b-302">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="c8c8b-303">Poprawiono literówkę w modelu „PsApiManagementOAuth2AuthrozationServer” na „PsApiManagementOAuth2AuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-303">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c8c8b-304">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c8c8b-304">Az.Batch</span></span>
* <span data-ttu-id="c8c8b-305">Poprawiono literówkę w komunikacie pomocy i dokumentacji, zmieniając literę w nazwie systemu Windows na wielką</span><span class="sxs-lookup"><span data-stu-id="c8c8b-305">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c8c8b-306">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c8c8b-306">Az.Cdn</span></span>
* <span data-ttu-id="c8c8b-307">Poprawiono literówkę w pomocniku konwersji modułu CDN</span><span class="sxs-lookup"><span data-stu-id="c8c8b-307">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-308">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-308">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-309">Dodanie polecenia VmssId to New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-309">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="c8c8b-310">Dodanie parametrów TerminateScheduledEvents i TerminateScheduledEventNotBeforeTimeoutInMinutes do polecenia New-AzVmssConfig and Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c8c8b-310">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="c8c8b-311">Dodanie właściwości HyperVGeneration do obiektu obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c8c8b-311">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="c8c8b-312">Dodanie funkcji Host i HostGroup</span><span class="sxs-lookup"><span data-stu-id="c8c8b-312">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="c8c8b-313">Nowe polecenia cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="c8c8b-313">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="c8c8b-314">Dodano parametr HostId do poleceń New-AzVMConfig i New-AzVM</span><span class="sxs-lookup"><span data-stu-id="c8c8b-314">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="c8c8b-315">Aktualizacja przykładu w dokumentacji polecenia „Invoke-AzVMRunCommand” w celu użycia poprawnej nazwy parametru</span><span class="sxs-lookup"><span data-stu-id="c8c8b-315">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="c8c8b-316">Aktualizacja opisu parametru „-VolumeType” w dokumentacji referencyjnej poleceń „Set-AzVMDiskEncryptionExtension” i „Set-AzVmssDiskEncryptionExtension”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-316">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c8c8b-317">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c8c8b-317">Az.DataFactory</span></span>
* <span data-ttu-id="c8c8b-318">Poprawiono literówkę w poleceniu „New-AzDataFactoryEncryptValue”, zmieniając literę w nazwie systemu Windows na wielką</span><span class="sxs-lookup"><span data-stu-id="c8c8b-318">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="c8c8b-319">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.2</span><span class="sxs-lookup"><span data-stu-id="c8c8b-319">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="c8c8b-320">Dodanie parametrów „DataProxyIntegrationRuntimeName”, „DataProxyStagingLinkedServiceName” i „DataProxyStagingPath” dla polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime”, aby umożliwić konfigurowanie własnego środowiska Integration Runtime jako serwera proxy dla środowiska SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="c8c8b-320">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="c8c8b-321">Zaktualizowano PSTriggerRun na potrzeby wyświetlania wyzwalanych potoków, komunikatów i właściwości, a także PSActivityRun na potrzeby wyświetlania typu działania</span><span class="sxs-lookup"><span data-stu-id="c8c8b-321">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c8c8b-322">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c8c8b-322">Az.DataLakeStore</span></span>
* <span data-ttu-id="c8c8b-323">Poprawiono wysunięcie polecenia Get-DataLakeStoreDeletedItem pod kątem obsługi błędów lub wyjątków zdalnych.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-323">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c8c8b-324">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c8c8b-324">Az.EventHub</span></span>
* <span data-ttu-id="c8c8b-325">Rozwiązano problem nr 9658: Literówka VirtualNteworkRule w poleceniu Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-325">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="c8c8b-326">Rozwiązano problem nr 9558: Polecenie Set-AzEventHubNamespace używa elementu PATCH zamiast PUT</span><span class="sxs-lookup"><span data-stu-id="c8c8b-326">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="c8c8b-327">dodano parametr EnableKafka do polecenia cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="c8c8b-327">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="c8c8b-328">Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania</span><span class="sxs-lookup"><span data-stu-id="c8c8b-328">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="c8c8b-329">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c8c8b-329">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="c8c8b-330">Poprawiono literówkę w dokumentacji: „Azure” rozpoczynające się małą literą</span><span class="sxs-lookup"><span data-stu-id="c8c8b-330">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c8c8b-331">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c8c8b-331">Az.Monitor</span></span>
* <span data-ttu-id="c8c8b-332">Poprawiono niepoprawną nazwę parametru w dokumentacji pomocy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-332">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-333">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-333">Az.Network</span></span>
* <span data-ttu-id="c8c8b-334">Zaktualizowano polecenie New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-334">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="c8c8b-335">Sklasyfikowano parametr „PublicIpAddress” jako przestarzały, ponieważ nie jest on nigdy używany po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-335">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="c8c8b-336">Dodano jeden opcjonalny parametr „Primary” wskazujący, czy bieżąca konfiguracja IP jest podstawowa, czy nie.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-336">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="c8c8b-337">Ulepszono obsługę wyjątku błędu żądania z zestawu SDK — rozwiązuje to problem polegający na tym, że poprzednio wyjątki zestawu SDK nie były poprawnie obsługiwane, wskutek czego nie były wyświetlane kluczowe szczegóły błędu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-337">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="c8c8b-338">Skorygowano logikę weryfikacji prefiksu IP w wersji IPv6 w celu sprawdzania, czy długość prefiksu IPv6 jest poprawna.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-338">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="c8c8b-339">Zaktualizowano polecenie Get-AzVirtualNetworkSubnetConfig: Dodano parametr ustawiany w celu pobrania identyfikatora zasobu podsieci.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-339">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="c8c8b-340">Zaktualizowano opis parametru Location dla AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="c8c8b-340">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c8c8b-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c8c8b-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="c8c8b-342">Zaktualizowano dokumentację polecenia „New-AzOperationalInsightsLinuxSyslogDataSource”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-342">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="c8c8b-343">Dodano przykład</span><span class="sxs-lookup"><span data-stu-id="c8c8b-343">Added example</span></span>
    - <span data-ttu-id="c8c8b-344">Zaktualizowano opis parametru „-Name”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-344">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="c8c8b-345">Dodano przykład dla polecenia New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="c8c8b-345">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="c8c8b-346">Zaktualizowano opis parametru „-Name” dla polecenia New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="c8c8b-346">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c8c8b-347">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-347">Az.RecoveryServices</span></span>
* <span data-ttu-id="c8c8b-348">Aktualizacja polecenia „Get-AzRecoveryServicesBackupJobDetail.md”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-348">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-349">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-349">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-350">Dodano obsługę nowej wersji interfejsu API (2019-05-10) dla Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="c8c8b-350">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="c8c8b-351">Dodano obsługę „copy.count = 0” dla zmiennych, zasobów i właściwości</span><span class="sxs-lookup"><span data-stu-id="c8c8b-351">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="c8c8b-352">Zasoby z ustawieniami „condition = false” lub „copy.count = 0” będą usuwane w trybie ukończenia</span><span class="sxs-lookup"><span data-stu-id="c8c8b-352">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="c8c8b-353">Dodanie do dokumentu pomocy przykładu przypisywania zasad na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c8c8b-353">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c8c8b-354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c8c8b-354">Az.ServiceBus</span></span>
* <span data-ttu-id="c8c8b-355">Rozwiązano problem nr 9658: Literówka VirtualNetworkRule w poleceniu Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-355">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="c8c8b-356">Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania</span><span class="sxs-lookup"><span data-stu-id="c8c8b-356">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="c8c8b-357">Dodano nowe polecenie „Test-AzServiceBusNameAvailability” do sprawdzania dostępności nazwy dla kolejki i tematu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-357">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="c8c8b-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c8c8b-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="c8c8b-359">Usunięcie usterek poleceń cmdlet dodawania typu węzła:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-359">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="c8c8b-360">Usterka NullReferenceException, gdy grupa zasobów ma inny zestaw VMSS niezwiązany z klastrem usługi Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-360">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="c8c8b-361">Rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="c8c8b-361">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="c8c8b-362">Usunięcie usterki powodującej niepowodzenie polecenia cmdlet, gdy sieć wirtualna znajdowała się w innej grupie zasobów niż klaster.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-362">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="c8c8b-363">rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="c8c8b-363">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="c8c8b-364">Sklasyfikowanie polecenia cmdlet Add-AzServiceFabricApplicationCertificate jako przestarzałego</span><span class="sxs-lookup"><span data-stu-id="c8c8b-364">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-365">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-365">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-366">Aktualizacja dokumentacji starych poleceń cmdlet inspekcji.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-366">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c8c8b-367">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-367">Az.Storage</span></span>
* <span data-ttu-id="c8c8b-368">Aktualizacja pomocy dotyczącej poleceń Get/Close-AzStorageFileHandle, przez dodanie kolejnych scenariuszy do przykładów dotyczących poleceń cmdlet i zaktualizowanie opisów parametrów</span><span class="sxs-lookup"><span data-stu-id="c8c8b-368">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="c8c8b-369">Obsługa StandardBlobTier w ramach przekazywania i kopiowania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="c8c8b-369">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="c8c8b-370">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c8c8b-370">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="c8c8b-371">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-371">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="c8c8b-372">Obsługa priorytetu ponownego wypełniania w ramach kopiowania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="c8c8b-372">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="c8c8b-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-373">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c8c8b-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c8c8b-374">Az.Websites</span></span>
* <span data-ttu-id="c8c8b-375">Dodanie wyjaśnienia do parametru -AppSettings w poleceniach Set-AzWebApp i Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c8c8b-375">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="c8c8b-376">2.5.0 — lipiec 2019</span><span class="sxs-lookup"><span data-stu-id="c8c8b-376">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c8c8b-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-377">Az.Accounts</span></span>
* <span data-ttu-id="c8c8b-378">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="c8c8b-378">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="c8c8b-379">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c8c8b-379">Az.ApplicationInsights</span></span>
* <span data-ttu-id="c8c8b-380">Poprawienie pisowni w przykładzie w dokumentacji polecenia „Remove-AzApplicationInsightsApiKey”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-380">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="c8c8b-381">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-381">Az.Automation</span></span>
* <span data-ttu-id="c8c8b-382">Poprawienie pisowni w ciągu zasobu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-382">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="c8c8b-383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-383">Az.CognitiveServices</span></span>
* <span data-ttu-id="c8c8b-384">Dodano obsługę właściwości NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-384">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-385">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-386">Dodanie brakujących właściwości (ComputerName, OsName, OsVersion i HyperVGeneration) obiektu widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-386">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="c8c8b-387">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c8c8b-387">Az.ContainerRegistry</span></span>
* <span data-ttu-id="c8c8b-388">Poprawienie pisowni parametru Replication w opisie polecenia Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c8c8b-388">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="c8c8b-389">Więcej informacji można znaleźć tutaj: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="c8c8b-389">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c8c8b-390">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c8c8b-390">Az.DataFactory</span></span>
* <span data-ttu-id="c8c8b-391">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.0</span><span class="sxs-lookup"><span data-stu-id="c8c8b-391">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="c8c8b-392">Poprawienie pisowni w dokumentacji dla polecenia „Get-AzDataFactoryV2PipelineRun”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-392">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c8c8b-393">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c8c8b-393">Az.EventHub</span></span>
* <span data-ttu-id="c8c8b-394">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="c8c8b-394">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="c8c8b-395">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-395">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c8c8b-396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c8c8b-396">Az.KeyVault</span></span>
* <span data-ttu-id="c8c8b-397">Dodano obsługę określania rozmiaru klucza dla zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="c8c8b-397">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c8c8b-398">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c8c8b-398">Az.LogicApp</span></span>
* <span data-ttu-id="c8c8b-399">Poprawienie polecenia Get-AzIntegrationAccountMap tak, aby wyświetlało listę wszystkich typów map</span><span class="sxs-lookup"><span data-stu-id="c8c8b-399">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="c8c8b-400">Dodano nowy parametr MapType na potrzeby filtrowania</span><span class="sxs-lookup"><span data-stu-id="c8c8b-400">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="c8c8b-401">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-401">Az.ManagedServices</span></span>
* <span data-ttu-id="c8c8b-402">Dodano obsługę interfejsu API w wersji 2019-06-01 (ogólna dostępność)</span><span class="sxs-lookup"><span data-stu-id="c8c8b-402">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-403">Az.Network</span></span>
* <span data-ttu-id="c8c8b-404">Dodanie obsługi prywatnego punktu końcowego i prywatnej usługi łączenia</span><span class="sxs-lookup"><span data-stu-id="c8c8b-404">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="c8c8b-405">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-405">New cmdlets</span></span>
        - <span data-ttu-id="c8c8b-406">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8c8b-406">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c8c8b-407">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c8c8b-407">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="c8c8b-408">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-408">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c8c8b-409">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-409">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c8c8b-410">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-410">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c8c8b-411">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-411">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c8c8b-412">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="c8c8b-412">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="c8c8b-413">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c8c8b-413">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="c8c8b-414">Zaktualizowano poniższe polecenia dla funkcji: Flaga PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies w podsieci w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c8c8b-414">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="c8c8b-415">Zaktualizowano polecenia New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-415">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="c8c8b-416">Dodano opcjonalny parametr -PrivateEndpointNetworkPoliciesFlag, który konfiguruje, czy stosować zasady sieciowe w prywatnym punkcie końcowym w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-416">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="c8c8b-417">Dodano opcjonalny parametr -PrivateLinkServiceNetworkPoliciesFlag, który konfiguruje, czy stosować zasady sieciowe w usłudze łącza prywatnego w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-417">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="c8c8b-418">Nazwa parametru „ServiceName” polecenia cmdlet AzPrivateLinkService została zmieniona na „Name” z aliasem „ServiceName” w celu zachowania zgodności z poprzednimi wersjami</span><span class="sxs-lookup"><span data-stu-id="c8c8b-418">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="c8c8b-419">Włączenie protokołu ICMP dla konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="c8c8b-419">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="c8c8b-420">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-420">Updated cmdlets</span></span>
        - <span data-ttu-id="c8c8b-421">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-421">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c8c8b-422">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-422">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c8c8b-423">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-423">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="c8c8b-424">Dodanie wartości ConnectionProtocolType (Ikev1/Ikev2) jako konfigurowalnego parametru dla polecenia New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-424">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c8c8b-425">Dodanie parametru PrivateIpAddressVersion w elemencie LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c8b-425">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="c8c8b-426">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-426">Updated cmdlet:</span></span>
        - <span data-ttu-id="c8c8b-427">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-427">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="c8c8b-428">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-428">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="c8c8b-429">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-429">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="c8c8b-430">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig usługi Application Gateway o obsługę portu niestandardowego w sondzie</span><span class="sxs-lookup"><span data-stu-id="c8c8b-430">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="c8c8b-431">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig: Dodano opcjonalny parametr Port, który służy do sondowania serwera zaplecza.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-431">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="c8c8b-432">Ten parametr ma zastosowanie w przypadku jednostek SKU Standard_V2 i WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-432">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c8c8b-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c8c8b-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="c8c8b-434">Zaktualizowano domyślną wersję zapisywanych wyszukiwań na 1.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-434">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="c8c8b-435">Poprawiono obsługę wyrażeń regularnych o wartości null dla dzienników niestandardowych</span><span class="sxs-lookup"><span data-stu-id="c8c8b-435">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c8c8b-436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-436">Az.RecoveryServices</span></span>
* <span data-ttu-id="c8c8b-437">Aktualizacja pliku „Get-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-437">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="c8c8b-438">Aktualizacja pliku „Get-AzRecoveryServicesBackupContainer.md”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-438">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="c8c8b-439">Aktualizacja pliku „Get-AzRecoveryServicesVault.md”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-439">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="c8c8b-440">Aktualizacja pliku „Wait-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-440">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="c8c8b-441">Aktualizacja pliku „Set-AzRecoveryServicesVaultContext.md”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-441">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="c8c8b-442">Aktualizacja pliku „Get-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-442">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="c8c8b-443">Aktualizacja pliku „Get-AzRecoveryServicesBackupRecoveryPoint.md”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-443">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="c8c8b-444">Aktualizacja pliku „Restore-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-444">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="c8c8b-445">Zaktualizowano wywołanie usługi do wyrejestrowywania kontenera dla udziału plików platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c8c8b-445">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="c8c8b-446">Aktualizacja pliku „Set-AzRecoveryServicesAsrAlertSetting.md”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-446">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-447">Az.Resources</span></span>
- <span data-ttu-id="c8c8b-448">Usunięcie brakującego polecenia cmdlet przywoływanego w dokumentacji polecenia „New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-448">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="c8c8b-449">Zaktualizowano polecenia cmdlet zasad w celu używania nowego interfejsu API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="c8c8b-449">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c8c8b-450">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c8c8b-450">Az.ServiceBus</span></span>
* <span data-ttu-id="c8c8b-451">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="c8c8b-451">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="c8c8b-452">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-452">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-453">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-453">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-454">Poprawienie brakujących przykładów dla polecenia cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c8c8b-454">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="c8c8b-455">Poprawienie ustawiania cyklicznego skanowania przez rozszerzenie Ocena luk w zabezpieczeniach bez podawania żadnego adresu e-mail</span><span class="sxs-lookup"><span data-stu-id="c8c8b-455">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="c8c8b-456">Poprawienie pisowni w komunikacie ostrzegawczym.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-456">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c8c8b-457">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-457">Az.Storage</span></span>
* <span data-ttu-id="c8c8b-458">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzStorageAccount” w celu użycia poprawnej nazwy parametru</span><span class="sxs-lookup"><span data-stu-id="c8c8b-458">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c8c8b-459">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c8c8b-459">Az.StorageSync</span></span>
* <span data-ttu-id="c8c8b-460">Dodanie polecenia cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-460">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="c8c8b-461">Rozwiązanie problemu 9551 dotyczącego respektowania wartości TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="c8c8b-461">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c8c8b-462">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c8c8b-462">Az.Websites</span></span>
* <span data-ttu-id="c8c8b-463">Usunięcie usterki polegającej na tym, że niektóre właściwości SiteConfig nie były zwracane przez polecenia Get-AzWebApp i Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c8c8b-463">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="c8c8b-464">Dodanie nowego parametru Location dla poleceń Get-AzDeletedWebApp i Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c8c8b-464">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="c8c8b-465">Usunięcie usterki związanej z klonowaniem miejsc aplikacji internetowych przy użyciu polecenia New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="c8c8b-465">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="c8c8b-466">2.4.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-466">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c8c8b-467">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-467">Az.Accounts</span></span>
* <span data-ttu-id="c8c8b-468">Dodano obsługę poleceń cmdlet profilu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-468">Add support for profile cmdlets</span></span>
* <span data-ttu-id="c8c8b-469">Dodano obsługę środowisk i płaszczyzn danych w generowanych poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-469">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="c8c8b-470">Naprawiono błąd polegający na tym, że w niektórych przypadkach dla poleceń cmdlet płaszczyzny danych w programie Windows PowerShell był używany nieprawidłowy punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-470">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="c8c8b-471">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="c8c8b-471">Az.Advisor</span></span>
* <span data-ttu-id="c8c8b-472">Wersja ogólnodostępna modułu Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="c8c8b-472">GA release of Az.Advisor</span></span>
* <span data-ttu-id="c8c8b-473">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="c8c8b-473">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c8c8b-474">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c8c8b-474">Az.ApiManagement</span></span>
* <span data-ttu-id="c8c8b-475">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="c8c8b-475">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="c8c8b-476">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="c8c8b-476">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="c8c8b-477">Dodano obsługę wykonywania zapytań dotyczących subskrypcji według użytkownika i produktu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-477">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="c8c8b-478">Dodano obsługę wykonywania zapytań przy użyciu zakresu „/”, „/apis”, „/apis/echo-api”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-478">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="c8c8b-479">Rozwiązano problemy https://github.com/Azure/azure-powershell/issues/9307 i https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="c8c8b-479">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="c8c8b-480">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="c8c8b-480">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="c8c8b-481">Dodano obsługę określania właściwości „ApiVersion” i „ApiVersionSetId” podczas importowania interfejsów API</span><span class="sxs-lookup"><span data-stu-id="c8c8b-481">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c8c8b-482">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-482">Az.Automation</span></span>
* <span data-ttu-id="c8c8b-483">Usunięto usterkę polecenia cmdlet Set-AzAutomationConnectionFieldValue w celu obsługi wartości ciągu.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-483">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-484">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-484">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-485">Dodano parametr HyperVGeneration do polecenia New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-485">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c8c8b-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c8c8b-486">Az.DataFactory</span></span>
* <span data-ttu-id="c8c8b-487">Aktualizowanie danych wyjściowych poleceń cmdlet pobierania uruchomień działań, pobierania uruchomień potoków i pobierania uruchomień wyzwalaczy usługi ADF w celu obsługi potoku Select-Object.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-487">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c8c8b-488">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c8c8b-488">Az.EventGrid</span></span>
* <span data-ttu-id="c8c8b-489">Poprawiono literówkę w dokumentacji polecenia New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="c8c8b-489">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c8c8b-490">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c8c8b-490">Az.IotHub</span></span>
* <span data-ttu-id="c8c8b-491">Dodano obsługę ponownego generowania kluczy zasad autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-491">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-492">Az.Network</span></span>
* <span data-ttu-id="c8c8b-493">Dodano właściwość „RoutingPreference” do tagów publicznych adresów IP</span><span class="sxs-lookup"><span data-stu-id="c8c8b-493">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="c8c8b-494">Poprawiono przykłady dla dokumentacji referencyjnej polecenia „Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-494">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c8c8b-495">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c8c8b-495">Az.PolicyInsights</span></span>
* <span data-ttu-id="c8c8b-496">Rozwiązano problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="c8c8b-496">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="c8c8b-497">Więcej informacji: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="c8c8b-497">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c8c8b-498">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c8c8b-498">Az.OperationalInsights</span></span>
* <span data-ttu-id="c8c8b-499">Naprawiono model źródła danych CustomLog zwracany w poleceniu Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c8c8b-499">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c8c8b-500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-500">Az.RecoveryServices</span></span>
* <span data-ttu-id="c8c8b-501">Poprawka dotycząca polecenia get-policy dla maszyn wirtualnych IaaS</span><span class="sxs-lookup"><span data-stu-id="c8c8b-501">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-502">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-502">Az.Resources</span></span>
    - <span data-ttu-id="c8c8b-503">Poprawiono tekst pomocy dotyczącej parametru -Top polecenia Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="c8c8b-503">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="c8c8b-504">Dodano obsługę stronicowania po stronie klienta dla polecenia Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="c8c8b-504">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="c8c8b-505">Dodano nowe parametry dla polecenia Set-AzPolicyAssignment: -PolicyParameters i -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="c8c8b-505">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="c8c8b-506">Aktualizacje dokumentacji i przykładów dla poleceń cmdlet zasad</span><span class="sxs-lookup"><span data-stu-id="c8c8b-506">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c8c8b-507">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c8c8b-507">Az.ServiceBus</span></span>
* <span data-ttu-id="c8c8b-508">Poprawka rozwiązująca problem #4938 — polecenie New-AzureRmServiceBusQueue zwraca wynik BadRequest w przypadku ustawienia właściwości MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="c8c8b-508">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-509">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-510">Dodano polecenia cmdlet grupy trybu failover wystąpienia z wersji zapoznawczej do wersji publicznej</span><span class="sxs-lookup"><span data-stu-id="c8c8b-510">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="c8c8b-511">Obsługa inspekcji w usłudze Azure SQL Server/Database za pomocą nowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-511">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="c8c8b-512">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="c8c8b-512">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="c8c8b-513">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="c8c8b-513">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="c8c8b-514">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="c8c8b-514">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="c8c8b-515">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="c8c8b-515">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="c8c8b-516">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="c8c8b-516">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="c8c8b-517">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="c8c8b-517">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="c8c8b-518">Usunięto ograniczenia wiadomości e-mail z ustawień oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="c8c8b-518">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c8c8b-519">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-519">Az.Storage</span></span>
* <span data-ttu-id="c8c8b-520">Zmieniono dwa parametry: „-IndexDocument” i „-ErrorDocument404Path” z wymaganych na opcjonalne w poleceniu cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-520">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="c8c8b-521">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c8c8b-521">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="c8c8b-522">Zaktualizowano pomoc dotyczącą polecenia Get-AzStorageBlobContent przez dodanie przykładu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-522">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="c8c8b-523">Wyświetlanie dodatkowych informacji o błędzie w przypadku niepowodzenia polecenia cmdlet z powodu wyjątku StorageException</span><span class="sxs-lookup"><span data-stu-id="c8c8b-523">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="c8c8b-524">Obsługa tworzenia i aktualizowania konta magazynu przy użyciu uwierzytelniania usługi AAD DS w usłudze Azure Files</span><span class="sxs-lookup"><span data-stu-id="c8c8b-524">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="c8c8b-525">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8c8b-525">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="c8c8b-526">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8c8b-526">Set-AzStorageAccount</span></span>
* <span data-ttu-id="c8c8b-527">Obsługa wyświetlania listy lub zamykania dojść do plików udziału plików, katalogu plików lub pliku</span><span class="sxs-lookup"><span data-stu-id="c8c8b-527">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="c8c8b-528">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="c8c8b-528">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="c8c8b-529">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="c8c8b-529">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c8c8b-530">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c8c8b-530">Az.StorageSync</span></span>
* <span data-ttu-id="c8c8b-531">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="c8c8b-531">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="c8c8b-532">2.3.2 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-532">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c8c8b-533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-533">Az.Accounts</span></span>
* <span data-ttu-id="c8c8b-534">Usunięto usterkę polegającą na używaniu w niektórych przypadkach niepoprawnego adresu URL w wywołaniach funkcji</span><span class="sxs-lookup"><span data-stu-id="c8c8b-534">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="c8c8b-535">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="c8c8b-535">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="c8c8b-536">Rozwiązano problem z aliasami w poleceniach cmdlet z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="c8c8b-536">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="c8c8b-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c8c8b-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="c8c8b-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="c8c8b-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-539">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-539">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-540">Proste zestawy parametrów New-AzVm i New-AzVmss akceptują teraz parametr „ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-540">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="c8c8b-541">Poprawiono literówkę w dokumentacji referencyjnej polecenia „New-AzVM”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-541">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="c8c8b-542">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="c8c8b-542">Az.Dns</span></span>
* <span data-ttu-id="c8c8b-543">Poprawiono literówkę w przykładach pomocy polecenia „Set-AzDnsZone”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-543">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c8c8b-544">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c8c8b-544">Az.EventGrid</span></span>
* <span data-ttu-id="c8c8b-545">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-545">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="c8c8b-546">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-546">New cmdlets:</span></span>
    - <span data-ttu-id="c8c8b-547">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="c8c8b-547">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="c8c8b-548">Tworzy nową domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-548">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="c8c8b-549">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="c8c8b-549">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="c8c8b-550">Pobiera szczegóły domeny usługi Event Grid lub pobiera listę wszystkich domen usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-550">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="c8c8b-551">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="c8c8b-551">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="c8c8b-552">Usuwa domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-552">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="c8c8b-553">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="c8c8b-553">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="c8c8b-554">Ponownie generuje klucz dostępu współdzielonego dla domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-554">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="c8c8b-555">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="c8c8b-555">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="c8c8b-556">Pobiera klucze dostępu współdzielonego używane do publikowania zdarzeń w domenie usługi Event Grid.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-556">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="c8c8b-557">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-557">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="c8c8b-558">Tworzy nowy temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-558">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="c8c8b-559">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="c8c8b-559">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="c8c8b-560">Pobiera szczegóły tematu domeny usługi Event Grid lub pobiera listę wszystkich tematów domeny usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-560">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="c8c8b-561">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-561">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="c8c8b-562">Usuwa istniejący temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-562">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="c8c8b-563">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-563">Updated cmdlets:</span></span>
    - <span data-ttu-id="c8c8b-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="c8c8b-565">Dodano nowe wymagane parametry do obsługi przesyłania potokowego nowej domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-565">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="c8c8b-566">Dodano nowe wymagane parametry w celu określenia nowej nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-566">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="c8c8b-567">Dodano nowe zestawy parametrów dla domen i tematów domen, aby umożliwić ponowne używanie istniejących parametrów (np. EndPointType, SubjectBeginsWith itp.).</span><span class="sxs-lookup"><span data-stu-id="c8c8b-567">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="c8c8b-568">Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-568">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="c8c8b-569">Data wygaśnięcia subskrypcji zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="c8c8b-569">Event subscription expiration date,</span></span>
            - <span data-ttu-id="c8c8b-570">Zaawansowane parametry filtrowania.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-570">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="c8c8b-571">Dodano nowe wyliczenie dla elementu servicebusqueue jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-571">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="c8c8b-572">Uniemożliwiono użycie elementu „Wszystkie” w opcji -IncludedEventType i zamieniono go na</span><span class="sxs-lookup"><span data-stu-id="c8c8b-572">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="c8c8b-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="c8c8b-574">Dodano nowe opcjonalne parametry (Top, ODataQuery i NextLink) w celu obsługi filtrowania i stronicowania wyników.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-574">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="c8c8b-575">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="c8c8b-575">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="c8c8b-576">Dodano nowe wymagane parametry do obsługi przesyłania potokowego domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-576">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="c8c8b-577">Dodano nowe wymagane parametry w celu określenia nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-577">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c8c8b-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c8c8b-578">Az.FrontDoor</span></span>
* <span data-ttu-id="c8c8b-579">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="c8c8b-579">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="c8c8b-580">Dodano obsługę przekształceń i nową wartość autouzupełniania operatora (wyrażenie regularne)</span><span class="sxs-lookup"><span data-stu-id="c8c8b-580">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="c8c8b-581">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="c8c8b-581">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="c8c8b-582">Dodano nowe wartości autouzupełniania</span><span class="sxs-lookup"><span data-stu-id="c8c8b-582">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-583">Az.Network</span></span>
* <span data-ttu-id="c8c8b-584">Dodano obsługę zasobu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c8c8b-584">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="c8c8b-585">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-585">New cmdlets</span></span>
        - <span data-ttu-id="c8c8b-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="c8c8b-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="c8c8b-587">Dodano element AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="c8c8b-587">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="c8c8b-588">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-588">New cmdlets</span></span> 
        - <span data-ttu-id="c8c8b-589">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="c8c8b-589">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="c8c8b-590">Dodano element PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c8c8b-590">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="c8c8b-591">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-591">New cmdlets</span></span> 
        - <span data-ttu-id="c8c8b-592">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c8c8b-592">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="c8c8b-593">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c8c8b-593">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="c8c8b-594">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c8c8b-594">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="c8c8b-595">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-595">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="c8c8b-596">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-596">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="c8c8b-597">Dodano element PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8c8b-597">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="c8c8b-598">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-598">New cmdlets</span></span>
        - <span data-ttu-id="c8c8b-599">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8c8b-599">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c8c8b-600">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8c8b-600">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c8c8b-601">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8c8b-601">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c8c8b-602">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-602">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="c8c8b-603">Zaktualizowano poniższe polecenia dla funkcji: Flaga UseLocalAzureIpAddress w elemencie VpnConnection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-603">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="c8c8b-604">Zaktualizowano polecenie New-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-604">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="c8c8b-605">Zaktualizowano polecenie Set-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-605">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="c8c8b-606">Dodano pole tylko do odczytu PeeredConnections w komunikacji równorzędnej usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-606">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="c8c8b-607">Dodano pole tylko do odczytu GlobalReachEnabled w usłudze ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-607">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="c8c8b-608">Dodano atrybut zmiany wywołujący zakończenie obsługi pola AllowGlobalReach w modelu ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c8c8b-608">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="c8c8b-609">Rozwiązano problem 8756 podczas używania elementu TargetListenerID z poleceniami cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c8b-609">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="c8c8b-610">Usunięto usterkę w poleceniu New-AzApplicationGatewayPathRuleConfig, która uniemożliwiała ustawienie zestawu reguł regenerowania.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-610">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="c8c8b-611">Rozwiązano problem z wyświetlaniem elementu VirtualNetworkTaps w elemencie NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c8b-611">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="c8c8b-612">Naprawiono polecenia cmdlet pobierania Cortex dla listy wszystkich części</span><span class="sxs-lookup"><span data-stu-id="c8c8b-612">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="c8c8b-613">Naprawiono tworzenie odwołań elementu VirtualHub dla elementu ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="c8c8b-613">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="c8c8b-614">Dodano obsługę stref dostępności w elementach AzureFirewall i NatGateway</span><span class="sxs-lookup"><span data-stu-id="c8c8b-614">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="c8c8b-615">Dodano polecenie cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="c8c8b-615">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="c8c8b-616">Dodano obsługę wielu publicznych adresów IP usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="c8c8b-616">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="c8c8b-617">Zaktualizowano polecenie cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-617">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="c8c8b-618">Dodano parametr -PublicIpAddress, który akceptuje co najmniej jeden obiekt publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="c8c8b-618">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="c8c8b-619">Dodano parametr -VirtualNetwork, który akceptuje obiekt sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c8c8b-619">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="c8c8b-620">Dodano do obiektu zapory metody AddPublicIpAddress i RemovePublicIpAddress, które akceptują obiekt publicznego adresu IP jako dane wejściowe</span><span class="sxs-lookup"><span data-stu-id="c8c8b-620">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="c8c8b-621">Wycofano parametry -PublicIpName i -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c8c8b-621">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="c8c8b-622">Zaktualizowano poniższe polecenia dla funkcji: Ustawiono w opcjach uwierzytelniania usługi AAD elementu VpnClient zasób bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-622">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="c8c8b-623">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-623">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="c8c8b-624">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-624">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="c8c8b-625">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr przełącznika RemoveAadAuthentication w celu usunięcia z bramy opcji uwierzytelniania usługi AAD elementu VpnClient.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-625">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c8c8b-626">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c8c8b-626">Az.OperationalInsights</span></span>
* <span data-ttu-id="c8c8b-627">Włączono warstwę cenową **pergb2018** w poleceniu „New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-627">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-628">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-628">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-629">Obsługa dodatkowych opcji eksportowania szablonu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-629">Support for additional Template Export options</span></span>
    - <span data-ttu-id="c8c8b-630">Dodano parametr „-SkipResourceNameParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c8c8b-630">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="c8c8b-631">Dodano parametr „-SkipAllParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c8c8b-631">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="c8c8b-632">Dodano parametr „-Resource” do polecenia Export-AzResourceGroup w celu filtrowania wyeksportowanych zasobów</span><span class="sxs-lookup"><span data-stu-id="c8c8b-632">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c8c8b-633">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c8c8b-633">Az.ServiceFabric</span></span>
* <span data-ttu-id="c8c8b-634">Usunięto błąd dodawania certyfikatu polegający na pobieraniu przez element ByExistingKeyVault nieprawidłowego odcisku palca w niektórych przypadkach</span><span class="sxs-lookup"><span data-stu-id="c8c8b-634">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-635">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-635">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-636">Naprawiono sufiks punktu końcowego magazynu usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-636">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="c8c8b-637">Rozwiązano problem z usługą Advanced Data Security polegający na przesłanianiu zasad usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-637">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="c8c8b-638">Nowe polecenia cmdlet modułu Management.Sql umożliwiające klientom dodawanie kluczy funkcji TDE i ustawianie funkcji ochrony TDE dla wystąpień zarządzanych</span><span class="sxs-lookup"><span data-stu-id="c8c8b-638">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="c8c8b-639">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c8c8b-639">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="c8c8b-640">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c8c8b-640">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="c8c8b-641">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c8c8b-641">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="c8c8b-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="c8c8b-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="c8c8b-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="c8c8b-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c8c8b-644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-644">Az.Storage</span></span>
* <span data-ttu-id="c8c8b-645">Obsługa rodzajów FileStorage i SkuName Premium_ZRS podczas tworzenia konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-645">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="c8c8b-646">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8c8b-646">New-AzStorageAccount</span></span>
* <span data-ttu-id="c8c8b-647">Opis z wyjaśnieniem polecenia cmdlet niezmienności obiektów blob</span><span class="sxs-lookup"><span data-stu-id="c8c8b-647">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="c8c8b-648">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-648">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c8c8b-649">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c8c8b-649">Az.Websites</span></span>
* <span data-ttu-id="c8c8b-650">Optymalizuje polecenie Get-AzWebAppCertificate w celu filtrowania według grupy zasobów na serwerze zamiast na kliencie</span><span class="sxs-lookup"><span data-stu-id="c8c8b-650">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="c8c8b-651">Dodano parametr przełącznika -UseDisasterRecovery do polecenia Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="c8c8b-651">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="c8c8b-652">2.2.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-652">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="c8c8b-653">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c8c8b-653">Az.Cdn</span></span>
* <span data-ttu-id="c8c8b-654">Zaktualizowano polecenia cmdlet do obsługi funkcji rulesEngine na podstawie interfejsu API w wersji 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-654">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-655">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-656">Dodano parametr `NoWait`, który powoduje rozpoczęcie operacji i natychmiastowy powrót, bez czekania na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-656">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="c8c8b-657">Zaktualizowano następujące polecenia cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="c8c8b-657">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c8c8b-658">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c8c8b-658">Az.EventHub</span></span>
* <span data-ttu-id="c8c8b-659">Poprawka błędu #9231 — polecenie Get-AzEventHubNamespace nie zwraca tagów</span><span class="sxs-lookup"><span data-stu-id="c8c8b-659">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="c8c8b-660">Poprawka błędu #9230 — polecenie Get-AzEventHubNamespace zwraca wartość ResourceGroup zamiast wartości ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8c8b-660">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-661">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-661">Az.Network</span></span>
* <span data-ttu-id="c8c8b-662">Aktualizowanie wartości ResourceId i InputObject dla bramy translatora adresów sieciowych</span><span class="sxs-lookup"><span data-stu-id="c8c8b-662">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="c8c8b-663">Dodawanie aliasów dla wartości ResourceId i InputObject</span><span class="sxs-lookup"><span data-stu-id="c8c8b-663">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c8c8b-664">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c8c8b-664">Az.PolicyInsights</span></span>
* <span data-ttu-id="c8c8b-665">Rozwiązanie problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="c8c8b-665">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c8c8b-666">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-666">Az.RecoveryServices</span></span>
* <span data-ttu-id="c8c8b-667">Minimalny czas przechowywania zasad IaaSVM w dniach zmieniono z 7 na 1</span><span class="sxs-lookup"><span data-stu-id="c8c8b-667">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c8c8b-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c8c8b-668">Az.ServiceBus</span></span>
* <span data-ttu-id="c8c8b-669">Rozwiązanie problemu #9182 — Get-AzServiceBusNamespace zwraca wartość ResourceGroup zamiast ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8c8b-669">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c8c8b-670">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c8c8b-670">Az.ServiceFabric</span></span>
* <span data-ttu-id="c8c8b-671">Poprawienie błędu pisowni w komunikacie o błędzie polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-671">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="c8c8b-672">Poprawienie brakującego znaku w wierszach polecenia usługi Service Fabric</span><span class="sxs-lookup"><span data-stu-id="c8c8b-672">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-673">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-674">Dodanie parametru DnsZonePartner dla polecenia cmdlet New-AzureSqlInstance w celu obsługi funkcji AutoDr dla wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-674">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="c8c8b-675">Wycofanie polecenia cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-675">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="c8c8b-676">Zmiana nazwy poleceń cmdlet z Wykrywanie zagrożeń na Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-676">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="c8c8b-677">Parametry New-AzSqlInstance -StorageSizeInGB i -LicenseType są teraz opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-677">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c8c8b-678">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c8c8b-678">Az.Websites</span></span>
* <span data-ttu-id="c8c8b-679">Rozwiązanie problemu polegającego na tym, że użycie poleceń Set-AzWebApp i Set-AzWebAppSlot z właściwością -WebApp powodowało usunięcie tagów</span><span class="sxs-lookup"><span data-stu-id="c8c8b-679">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="c8c8b-680">2.1.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-680">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="c8c8b-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c8c8b-681">Az.ApiManagement</span></span>
* <span data-ttu-id="c8c8b-682">Utworzono nowe polecenia cmdlet do zarządzania diagnostyką w zakresie globalnym i interfejsu API</span><span class="sxs-lookup"><span data-stu-id="c8c8b-682">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="c8c8b-683">**Get-AzApiManagementDiagnostic** — uzyskiwanie diagnostyki skonfigurowanej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="c8c8b-683">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="c8c8b-684">**New-AzApiManagementDiagnostic** — tworzenie nowej diagnostyki w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="c8c8b-684">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="c8c8b-685">**New-AzApiManagementHttpMessageDiagnostic** — tworzenie ustawienia diagnostyki określającego nagłówki do rejestrowania i rozmiar treści w bajtach</span><span class="sxs-lookup"><span data-stu-id="c8c8b-685">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="c8c8b-686">**New-AzApiManagementPipelineDiagnosticSetting** — tworzenie ustawień diagnostyki dla przychodzących/wychodzących komunikatów HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-686">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="c8c8b-687">**New-AzApiManagementSamplingSetting** — tworzenie ustawienia próbkowania dla żądań i odpowiedzi na potrzeby diagnostyki</span><span class="sxs-lookup"><span data-stu-id="c8c8b-687">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="c8c8b-688">**Remove-AzApiManagementDiagnostic** — usuwanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="c8c8b-688">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="c8c8b-689">**Set-AzApiManagementDiagnostic** — aktualizowanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="c8c8b-689">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="c8c8b-690">Utworzono nowe polecenia cmdlet do zarządzania pamięcią podręczną usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c8c8b-690">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="c8c8b-691">**Get-AzApiManagementCache** — uzyskiwanie szczegółów pamięci podręcznej określonej przez identyfikator lub wszystkich pamięci podręcznych</span><span class="sxs-lookup"><span data-stu-id="c8c8b-691">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="c8c8b-692">**New-AzApiManagementCache** — tworzenie nowej, „domyślnej” pamięci podręcznej lub pamięci podręcznej w konkretnym „regionie” platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c8c8b-692">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="c8c8b-693">**Remove-AzApiManagementCache** — usuwanie pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="c8c8b-693">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="c8c8b-694">**Update-AzApiManagementCache** — aktualizacja pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="c8c8b-694">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="c8c8b-695">Utworzono nowe polecenia cmdlet do zarządzania schematem interfejsu API</span><span class="sxs-lookup"><span data-stu-id="c8c8b-695">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="c8c8b-696">**New-AzApiManagementSchema** — tworzenie nowego schematu dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="c8c8b-696">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="c8c8b-697">**Get-AzApiManagementSchema** — pobieranie schematów skonfigurowanych w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="c8c8b-697">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="c8c8b-698">**Remove-AzApiManagementSchema** — usuwanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="c8c8b-698">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="c8c8b-699">**Set-AzApiManagementSchema** — aktualizowanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="c8c8b-699">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="c8c8b-700">Utworzono nowe polecenie cmdlet do generowania tokenu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-700">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="c8c8b-701">**New-AzApiManagementUserToken** — generowanie nowego tokenu użytkownika ważnego domyślnie przez 8 godzin. Za pomocą tego polecenia cmdlet można wygenerować token dla użytkownika „GIT”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-701">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="c8c8b-702">Utworzono nowe polecenie cmdlet do pobierania stanu sieci.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-702">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="c8c8b-703">**Get-AzApiManagementNetworkStatus** — uzyskiwanie stanu sieci dla łączności z zasobami, od których zależy usługa API Management.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-703">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="c8c8b-704">Jest to przydatne w przypadku wdrażania usługi ApiManagement w sieci wirtualnej i weryfikacji, czy któreś z zależności są uszkodzone.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-704">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="c8c8b-705">Zaktualizowano polecenie cmdlet **New-AzApiManagement** do zarządzania usługą ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c8c8b-705">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="c8c8b-706">Dodano obsługę nowych jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-706">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="c8c8b-707">Dodano obsługę włączania flagi „EnableClientCertificate” dla jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-707">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="c8c8b-708">Nowe polecenie cmdlet **New-AzApiManagementSslSetting** umożliwia skonfigurowanie ustawienia „TLS/SSL” na „Zaplecze” i „Fronton”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-708">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="c8c8b-709">Za jego pomocą można też skonfigurować szyfrowanie, takie jak „3DES”, i protokoły serwera, takie jak „Http2”we frontonie usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-709">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="c8c8b-710">Dodano obsługę konfigurowania nazwy hosta „DeveloperPortal” usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-710">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="c8c8b-711">Zaktualizowano polecenia cmdlet **Get-AzApiManagementSsoToken**, aby przyjmowały jako wejście obiekt „PsApiManagement”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-711">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="c8c8b-712">Zaktualizowano polecenie cmdlet, aby wyświetlało komunikaty o błędach śródwierszowo</span><span class="sxs-lookup"><span data-stu-id="c8c8b-712">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="c8c8b-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Kod błędu: Komunikat o błędzie ValidationError: Co najmniej jedno pole zawiera nieprawidłową wartość: Szczegóły błędu:    [Code=ValidationError, Message=Błąd w elemencie „log-to-eventhub” w wierszu 3, kolumna 10: Nie znaleziono rejestratora, element docelowy=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="c8c8b-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="c8c8b-714">Zaktualizowano polecenie cmdlet **Export-AzApiManagementApi** tak, aby eksportowało interfejsy API w formacie „OpenApi 3.0”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-714">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="c8c8b-715">Zaktualizowano polecenie cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="c8c8b-715">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="c8c8b-716">W celu importowania interfejsu Api z dokumentu ze specyfikacją interfejsu „OpenApi 3.0”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-716">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="c8c8b-717">W celu przesłonięcia właściwości „PsApiManagementSchema” określonej w dowolnym dokumencie („Swagger”, „Wadl”, „Wsdl”, „OpenApi”).</span><span class="sxs-lookup"><span data-stu-id="c8c8b-717">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="c8c8b-718">W celu przesłonięcia właściwości „ServiceUrl” określonej w dowolnym dokumencie.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-718">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="c8c8b-719">Zaktualizowano polecenie cmdlet **Get-AzApiManagementPolicy** tak, aby zwracało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-719">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="c8c8b-720">Zaktualizowano polecenie cmdlet **Set-AzApiManagementPolicy** tak, aby akceptowało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml” i ze zmianą znaczenia Xml przy użyciu formatu „xml”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-720">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="c8c8b-721">Zaktualizowano polecenie cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="c8c8b-721">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="c8c8b-722">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-722">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="c8c8b-723">W celu utworzenia interfejsu API we właściwości ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-723">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="c8c8b-724">W celu sklonowania interfejsu API przy użyciu właściwości „SourceApiId” i „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-724">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="c8c8b-725">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-725">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="c8c8b-726">Zaktualizowano polecenie cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="c8c8b-726">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="c8c8b-727">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-727">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="c8c8b-728">W celu zaktualizowania interfejsu API we właściwości „ApiVersionSet”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-728">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="c8c8b-729">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-729">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="c8c8b-730">Zaktualizowano polecenie cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="c8c8b-730">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="c8c8b-731">W celu klonowania (kopiowanie tagów, produktów, operacji i zasad) istniejącej wersji przy użyciu właściwości „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-731">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="c8c8b-732">Dla nowej wersji przyjmowana jest wartość „ApiId” elementu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-732">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="c8c8b-733">W celu dostarczenia właściwości „ApiRevisionDescription”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-733">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="c8c8b-734">W celu przesłonięcia właściwości „ServiceUrl” podczas klonowania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-734">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="c8c8b-735">Zaktualizowano polecenie cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="c8c8b-735">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="c8c8b-736">W celu skonfigurowania właściwości „AAD” lub „AADB2C” za pomocą właściwości „Authority”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-736">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="c8c8b-737">W celu skonfigurowania właściwości „SignupPolicy”, „SigninPolicy”, „ProfileEditingPolicy” i „PasswordResetPolicy”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-737">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="c8c8b-738">Zaktualizowano polecenie cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="c8c8b-738">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="c8c8b-739">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-739">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="c8c8b-740">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-740">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="c8c8b-741">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-741">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="c8c8b-742">Zaktualizowano polecenie cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="c8c8b-742">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="c8c8b-743">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-743">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="c8c8b-744">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-744">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="c8c8b-745">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-745">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="c8c8b-746">Zaktualizowano następujące polecenia cmdlet do akceptowania właściwości „ResourceId” jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="c8c8b-746">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="c8c8b-747">„New-AzApiManagementContext”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-747">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="c8c8b-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="c8c8b-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="c8c8b-749">„Get-AzApiManagementApiRelease”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-749">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="c8c8b-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="c8c8b-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="c8c8b-751">„Get-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-751">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="c8c8b-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="c8c8b-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="c8c8b-753">„Get-AzApiManagementAuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-753">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="c8c8b-754">„Get-AzApiManagementBackend”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-754">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="c8c8b-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="c8c8b-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="c8c8b-756">„Get-AzApiManagementCertificate”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-756">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="c8c8b-757">„Remove-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-757">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="c8c8b-758">„Remove-AzApiManagementSubscription”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-758">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c8c8b-759">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-759">Az.Automation</span></span>
* <span data-ttu-id="c8c8b-760">Zaktualizowano polecenie Get-AzAutomationJobOutputRecord tak, aby obsługiwało wartości rekordów w postaci kodu JSON i tekstowej.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-760">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="c8c8b-761">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="c8c8b-761">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="c8c8b-762">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="c8c8b-762">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="c8c8b-763">Zmieniono działanie polecenia Start-AzAutomationDscCompilationJob tak, aby tylko uruchamiało zadanie zamiast czekać na jego zakończenie.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-763">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="c8c8b-764">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="c8c8b-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="c8c8b-765">Poprawka dla polecenia Get-AzAutomationDscNode podczas używania opcji -Name zwraca wszystkie węzły.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-765">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="c8c8b-766">Teraz zwraca tylko pasujące węzły.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-766">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-767">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-768">Dodanie parametrów ProtectFromScaleIn i ProtectFromScaleSetAction do polecenia cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-768">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="c8c8b-769">Nowy zestaw parametrów New-AzVM wimple teraz używa domyślnie dostępnej lokalizacji, jeśli region „Wschodnie stany USA” nie jest obsługiwany.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-769">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c8c8b-770">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c8c8b-770">Az.DataLakeStore</span></span>
* <span data-ttu-id="c8c8b-771">Aktualizacja zestawu ADLS SDK do korzystania z klienta httpclient, integrowanie testowania płaszczyzny danych z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c8c8b-771">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c8c8b-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c8c8b-772">Az.Monitor</span></span>
* <span data-ttu-id="c8c8b-773">Naprawiono nieprawidłowe nazwy parametrów w przykładach pomocy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-773">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-774">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-774">Az.Network</span></span>
* <span data-ttu-id="c8c8b-775">Dodanie flagi DisableBgpRoutePropagation do danych wyjściowych obowiązującej tabeli routingu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-775">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="c8c8b-776">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-776">Updated cmdlet:</span></span>
        - <span data-ttu-id="c8c8b-777">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8c8b-777">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="c8c8b-778">Poprawienie podwójnego łącznika w dokumentacji polecenia New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c8c8b-778">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-779">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-780">Dodanie nowego polecenia cmdlet Get-AzureRmDenyAssignment do pobierania przypisań odmowy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-780">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-781">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-781">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-782">Zmiana nazwy poleceń cmdlet usługi Advanced Threat Protection na Advanced Data Security i domyślne włączenie oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="c8c8b-782">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="c8c8b-783">2.0.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-783">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c8c8b-784">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-784">Az.Accounts</span></span>
* <span data-ttu-id="c8c8b-785">Aktualizacja biblioteki uwierzytelniania w celu rozwiązania problemów z usługą ADFS dotyczących uwierzytelniania nazwy użytkownika i hasła</span><span class="sxs-lookup"><span data-stu-id="c8c8b-785">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c8c8b-786">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-786">Az.CognitiveServices</span></span>
* <span data-ttu-id="c8c8b-787">Dla usług wyszukiwania Bing wyświetlane jest tylko zrzeczenie odpowiedzialności usługi Bing.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-787">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="c8c8b-788">Naprawiono błąd polegający na niepomyślnym tworzeniu konta.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-788">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-789">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-790">Funkcja Grupa umieszczania w pobliżu.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-790">Proximity placement group feature.</span></span>
    - <span data-ttu-id="c8c8b-791">Dodano następujące nowe polecenia cmdlet:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c8c8b-791">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="c8c8b-792">Do następujących poleceń cmdlet dodano nowy parametr ProximityPlacementGroupId:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-792">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="c8c8b-793">Do polecenia New-AzGalleryImageVersion dodano parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-793">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="c8c8b-794">Właściwość TargetRegion polecenia New-AzGalleryImageVersion może zawierać parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-794">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="c8c8b-795">Do poleceń Stop-AzVM i Stop-AzVmss dodano parametr przełącznika SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="c8c8b-795">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="c8c8b-796">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="c8c8b-796">Breaking changes</span></span>
    - <span data-ttu-id="c8c8b-797">Polecenie Set-AzVMBootDiagnostics zamieniono na polecenie Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-797">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="c8c8b-798">Polecenie Export-AzLogAnalyticThrottledRequests zamieniono na polecenie Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-798">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="c8c8b-799">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="c8c8b-799">Az.DeploymentManager</span></span>
* <span data-ttu-id="c8c8b-800">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="c8c8b-800">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="c8c8b-801">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="c8c8b-801">Az.Dns</span></span>
* <span data-ttu-id="c8c8b-802">Automatyczne delegowanie serwera nazw systemu DNS</span><span class="sxs-lookup"><span data-stu-id="c8c8b-802">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="c8c8b-803">Polecenie cmdlet tworzenia strefy DNS akceptuje nazwę strefy nadrzędnej jako dodatkowy parametr opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-803">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="c8c8b-804">Dodaje rekordy serwera nazw w strefie nadrzędnej dla nowo utworzonej strefy podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-804">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c8c8b-805">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c8c8b-805">Az.FrontDoor</span></span>
* <span data-ttu-id="c8c8b-806">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c8c8b-806">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="c8c8b-807">Zmiana nazw poleceń cmdlet zapory aplikacji internetowej w celu dołączenia ciągu „Waf”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-807">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="c8c8b-808">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c8c8b-808">Az.HDInsight</span></span>
* <span data-ttu-id="c8c8b-809">Usunięto dwa polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-809">Removed two cmdlets:</span></span>
    - <span data-ttu-id="c8c8b-810">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c8c8b-810">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="c8c8b-811">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c8c8b-811">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="c8c8b-812">Dodano nowe polecenie cmdlet Set-AzHDInsightGatewayCredential w celu zastąpienia polecenia Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c8c8b-812">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="c8c8b-813">Zaktualizowano polecenie cmdlet Get-AzHDInsightJobOutput, aby rozróżnić rolę czytelnika i rolę operatora usługi HDInsight:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-813">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="c8c8b-814">Użytkownicy z rolą czytelnika muszą jawnie określić parametr „DefaultStorageAccountKey” — w przeciwnym razie wystąpi błąd.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-814">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="c8c8b-815">Nie będzie to miało wpływu na użytkowników z rolą operatora usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-815">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c8c8b-816">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c8c8b-816">Az.Monitor</span></span>
* <span data-ttu-id="c8c8b-817">Nowe polecenia cmdlet dla interfejsu API SQR (Scheduled Query Rule, reguła zaplanowanego zapytania)</span><span class="sxs-lookup"><span data-stu-id="c8c8b-817">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="c8c8b-818">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="c8c8b-818">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="c8c8b-819">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="c8c8b-819">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="c8c8b-820">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="c8c8b-820">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="c8c8b-821">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="c8c8b-821">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="c8c8b-822">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="c8c8b-822">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="c8c8b-823">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="c8c8b-823">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="c8c8b-824">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c8c8b-824">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c8c8b-825">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c8c8b-825">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c8c8b-826">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c8c8b-826">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c8c8b-827">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c8c8b-827">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c8c8b-828">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c8c8b-828">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c8c8b-829">[Więcej](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informacji na temat interfejsu API SQR</span><span class="sxs-lookup"><span data-stu-id="c8c8b-829">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="c8c8b-830">Zaktualizowano plik Az.Monitor.md w celu uwzględnienia poleceń cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="c8c8b-830">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-831">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-831">Az.Network</span></span>
* <span data-ttu-id="c8c8b-832">Dodano obsługę dla zasobu usługi NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="c8c8b-832">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="c8c8b-833">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-833">New cmdlets</span></span>
        - <span data-ttu-id="c8c8b-834">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c8c8b-834">New-AzNatGateway</span></span>
        - <span data-ttu-id="c8c8b-835">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c8c8b-835">Get-AzNatGateway</span></span>
        - <span data-ttu-id="c8c8b-836">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c8c8b-836">Set-AzNatGateway</span></span>
        - <span data-ttu-id="c8c8b-837">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c8c8b-837">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="c8c8b-838">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-838">Updated cmdlets</span></span>
        - <span data-ttu-id="c8c8b-839">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="c8c8b-839">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="c8c8b-840">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="c8c8b-840">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="c8c8b-841">Zaktualizowano poniższe polecenia dla funkcji: Ustawianie/usuwanie tras niestandardowych dla bramy Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-841">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="c8c8b-842">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-842">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="c8c8b-843">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-843">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c8c8b-844">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c8c8b-844">Az.PolicyInsights</span></span>
* <span data-ttu-id="c8c8b-845">Obsługa zapytań dotyczących szczegółów oceny zasad.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-845">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="c8c8b-846">Dodano parametr „-Expand” do polecenia Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-846">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="c8c8b-847">Obsługa polecenia „-Expand PolicyEvaluationDetails”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-847">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c8c8b-848">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-848">Az.RecoveryServices</span></span>
* <span data-ttu-id="c8c8b-849">Obsługa odzyskiwania lokacji między subskrypcjami z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-849">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="c8c8b-850">Oznaczanie nadchodzących zmian powodujących niezgodność dla usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-850">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="c8c8b-851">Poprawka zakończenia planu akcji dla planu odzyskiwania usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-851">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="c8c8b-852">Poprawka aktualizacji mapowania sieci usługi Azure Site Recovery z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-852">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="c8c8b-853">Poprawka aktualizacji kierunku ochrony usługi Azure Site Recovery z platformy Azure na platformę Azure dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-853">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="c8c8b-854">Inne drobne poprawki.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-854">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="c8c8b-855">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="c8c8b-855">Az.Relay</span></span>
* <span data-ttu-id="c8c8b-856">Poprawiono błędy pisowni w komunikatach przeznaczonych dla klientów</span><span class="sxs-lookup"><span data-stu-id="c8c8b-856">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c8c8b-857">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c8c8b-857">Az.ServiceBus</span></span>
* <span data-ttu-id="c8c8b-858">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="c8c8b-858">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c8c8b-859">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-859">Az.Storage</span></span>
* <span data-ttu-id="c8c8b-860">Uaktualnienie biblioteki klienta usługi Storage do wersji 10.0.1 (przestrzeń nazw wszystkich obiektów tego zestawu SDK została zmieniona z „Microsoft.WindowsAzure.Storage. *” na „Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="c8c8b-860">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="c8c8b-861">Uaktualnienie do wersji Microsoft.Azure.Management.Storage 11.0.0 w celu obsługi nowego interfejsu API w wersji 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-861">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="c8c8b-862">Domyślny rodzaj konta magazynu w poleceniu Utwórz konto magazynu został zmieniony ze „Storage” na „StorageV2”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-862">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="c8c8b-863">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8c8b-863">New-AzStorageAccount</span></span>
* <span data-ttu-id="c8c8b-864">Zmiana wyjściowego parametru Sku.Name polecenia cmdlet konta magazynu w celu wyrównania z wejściowym parametrem SkuName przez dodanie znaku „-”, na przykład zmiana „StandardLRS” na „Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-864">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="c8c8b-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8c8b-865">New-AzStorageAccount</span></span>
    - <span data-ttu-id="c8c8b-866">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8c8b-866">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="c8c8b-867">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8c8b-867">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c8c8b-868">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c8c8b-868">Az.Websites</span></span>
* <span data-ttu-id="c8c8b-869">Właściwość „Kind” będzie teraz ustawiona dla obiektów PSSite zwracanych przez polecenie Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c8c8b-869">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="c8c8b-870">Polecenia Get-AzWebApp\*Metrics i Get-AzAppServicePlanMetrics oznaczono jako przestarzałe</span><span class="sxs-lookup"><span data-stu-id="c8c8b-870">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="c8c8b-871">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-871">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c8c8b-872">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="c8c8b-872">Highlights since the last major release</span></span>
* <span data-ttu-id="c8c8b-873">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="c8c8b-873">General availability of `Az` module</span></span>
* <span data-ttu-id="c8c8b-874">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="c8c8b-874">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c8c8b-875">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="c8c8b-875">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c8c8b-876">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-876">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c8c8b-877">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="c8c8b-877">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c8c8b-878">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-878">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c8c8b-879">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="c8c8b-879">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c8c8b-880">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-880">Az.Accounts</span></span>
* <span data-ttu-id="c8c8b-881">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="c8c8b-881">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c8c8b-882">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c8c8b-882">Az.Batch</span></span>
* <span data-ttu-id="c8c8b-883">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-883">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c8c8b-884">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c8c8b-884">Az.Cdn</span></span>
* <span data-ttu-id="c8c8b-885">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c8c8b-886">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-886">Az.CognitiveServices</span></span>
* <span data-ttu-id="c8c8b-887">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-888">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-889">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-889">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="c8c8b-890">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c8c8b-891">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="c8c8b-891">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c8c8b-892">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c8c8b-892">Az.DataFactory</span></span>
* <span data-ttu-id="c8c8b-893">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-893">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c8c8b-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c8c8b-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="c8c8b-895">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-895">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c8c8b-896">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c8c8b-896">Az.EventGrid</span></span>
* <span data-ttu-id="c8c8b-897">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-897">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c8c8b-898">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c8c8b-898">Az.EventHub</span></span>
* <span data-ttu-id="c8c8b-899">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="c8c8b-899">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="c8c8b-900">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c8c8b-900">Az.HDInsight</span></span>
* <span data-ttu-id="c8c8b-901">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c8c8b-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c8c8b-902">Az.IotHub</span></span>
* <span data-ttu-id="c8c8b-903">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c8c8b-904">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c8c8b-904">Az.KeyVault</span></span>
* <span data-ttu-id="c8c8b-905">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c8c8b-906">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="c8c8b-906">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="c8c8b-907">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c8c8b-907">Az.MachineLearning</span></span>
* <span data-ttu-id="c8c8b-908">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="c8c8b-909">Az.Media</span><span class="sxs-lookup"><span data-stu-id="c8c8b-909">Az.Media</span></span>
* <span data-ttu-id="c8c8b-910">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c8c8b-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c8c8b-911">Az.Monitor</span></span>
  * <span data-ttu-id="c8c8b-912">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="c8c8b-912">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="c8c8b-913">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="c8c8b-913">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="c8c8b-914">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="c8c8b-914">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="c8c8b-915">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c8c8b-915">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="c8c8b-916">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c8c8b-916">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="c8c8b-917">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c8c8b-917">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="c8c8b-918">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="c8c8b-918">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-919">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-919">Az.Network</span></span>
* <span data-ttu-id="c8c8b-920">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-920">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c8c8b-921">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="c8c8b-921">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="c8c8b-922">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="c8c8b-922">Az.NotificationHubs</span></span>
* <span data-ttu-id="c8c8b-923">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c8c8b-924">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c8c8b-924">Az.OperationalInsights</span></span>
* <span data-ttu-id="c8c8b-925">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="c8c8b-926">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c8c8b-926">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="c8c8b-927">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c8c8b-928">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-928">Az.RecoveryServices</span></span>
* <span data-ttu-id="c8c8b-929">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c8c8b-930">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c8c8b-930">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="c8c8b-931">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="c8c8b-931">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="c8c8b-932">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="c8c8b-932">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c8c8b-933">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c8c8b-933">Az.RedisCache</span></span>
* <span data-ttu-id="c8c8b-934">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-934">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-935">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-936">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="c8c8b-936">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-937">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-938">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="c8c8b-938">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="c8c8b-939">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-939">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c8c8b-940">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-940">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="c8c8b-941">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-941">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="c8c8b-942">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-942">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="c8c8b-943">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-943">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="c8c8b-944">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="c8c8b-944">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c8c8b-945">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c8c8b-945">Az.Websites</span></span>
* <span data-ttu-id="c8c8b-946">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-946">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="c8c8b-947">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-947">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c8c8b-948">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-948">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="c8c8b-949">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-949">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="c8c8b-950">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-950">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c8c8b-951">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="c8c8b-951">Highlights since the last major release</span></span>
* <span data-ttu-id="c8c8b-952">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="c8c8b-952">General availability of `Az` module</span></span>
* <span data-ttu-id="c8c8b-953">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="c8c8b-953">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c8c8b-954">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="c8c8b-954">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c8c8b-955">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-955">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c8c8b-956">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="c8c8b-956">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c8c8b-957">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-957">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c8c8b-958">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="c8c8b-958">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c8c8b-959">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-959">Az.Accounts</span></span>
* <span data-ttu-id="c8c8b-960">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c8c8b-960">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c8c8b-961">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-961">Az.AnalysisServices</span></span>
* <span data-ttu-id="c8c8b-962">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="c8c8b-962">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="c8c8b-963">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="c8c8b-963">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c8c8b-964">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-964">Az.Automation</span></span>
* <span data-ttu-id="c8c8b-965">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-965">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="c8c8b-966">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-966">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="c8c8b-967">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-967">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-968">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-969">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-969">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="c8c8b-970">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-970">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="c8c8b-971">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c8c8b-971">Az.ContainerInstance</span></span>
* <span data-ttu-id="c8c8b-972">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="c8c8b-972">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c8c8b-973">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c8c8b-973">Az.DataFactory</span></span>
* <span data-ttu-id="c8c8b-974">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="c8c8b-974">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="c8c8b-975">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-975">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-976">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-976">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-977">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-977">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="c8c8b-978">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-978">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="c8c8b-979">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="c8c8b-979">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="c8c8b-980">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="c8c8b-980">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="c8c8b-981">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="c8c8b-981">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="c8c8b-982">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="c8c8b-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-983">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-983">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-984">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-984">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c8c8b-985">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-985">Az.Storage</span></span>
* <span data-ttu-id="c8c8b-986">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c8c8b-986">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="c8c8b-987">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c8c8b-987">New-AzStorageContext</span></span>
* <span data-ttu-id="c8c8b-988">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="c8c8b-988">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="c8c8b-989">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c8c8b-989">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="c8c8b-990">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c8c8b-990">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="c8c8b-991">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-991">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="c8c8b-992">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-992">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="c8c8b-993">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="c8c8b-993">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="c8c8b-994">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c8c8b-994">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="c8c8b-995">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c8c8b-995">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="c8c8b-996">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c8c8b-996">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="c8c8b-997">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c8c8b-997">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="c8c8b-998">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="c8c8b-998">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c8c8b-999">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="c8c8b-999">Highlights since the last major release</span></span>
* <span data-ttu-id="c8c8b-1000">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1000">General availability of `Az` module</span></span>
* <span data-ttu-id="c8c8b-1001">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1001">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c8c8b-1002">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1002">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c8c8b-1003">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1003">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c8c8b-1004">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1004">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c8c8b-1005">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1005">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c8c8b-1006">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1006">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c8c8b-1007">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1007">Az.Automation</span></span>
* <span data-ttu-id="c8c8b-1008">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1008">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="c8c8b-1009">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1009">Dynamic grouping</span></span>
    * <span data-ttu-id="c8c8b-1010">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1010">Pre-Post script</span></span>
    * <span data-ttu-id="c8c8b-1011">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1011">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-1012">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1012">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-1013">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1013">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="c8c8b-1014">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1014">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c8c8b-1015">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1015">Az.KeyVault</span></span>
* <span data-ttu-id="c8c8b-1016">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1016">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-1017">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1017">Az.Network</span></span>
* <span data-ttu-id="c8c8b-1018">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1018">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="c8c8b-1019">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1019">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c8c8b-1020">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1020">Az.RecoveryServices</span></span>
* <span data-ttu-id="c8c8b-1021">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1021">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="c8c8b-1022">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1022">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-1023">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1023">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-1024">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1024">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="c8c8b-1025">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1025">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1026">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-1027">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1027">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c8c8b-1028">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1028">Az.Storage</span></span>
* <span data-ttu-id="c8c8b-1029">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1029">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="c8c8b-1030">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1030">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c8c8b-1031">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1031">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c8c8b-1032">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1032">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c8c8b-1033">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1033">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="c8c8b-1034">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1034">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="c8c8b-1035">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1035">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c8c8b-1036">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1036">Az.Websites</span></span>
* <span data-ttu-id="c8c8b-1037">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1037">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="c8c8b-1038">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1038">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c8c8b-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1039">Az.Accounts</span></span>
* <span data-ttu-id="c8c8b-1040">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1040">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="c8c8b-1041">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1041">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c8c8b-1042">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1042">Az.Automation</span></span>
* <span data-ttu-id="c8c8b-1043">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1043">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="c8c8b-1044">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1044">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="c8c8b-1045">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1045">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c8c8b-1046">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1046">Az.Cdn</span></span>
* <span data-ttu-id="c8c8b-1047">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1047">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-1048">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1048">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-1049">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1049">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c8c8b-1050">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1050">Az.DataFactory</span></span>
* <span data-ttu-id="c8c8b-1051">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1051">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c8c8b-1052">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1052">Az.LogicApp</span></span>
* <span data-ttu-id="c8c8b-1053">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1053">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-1054">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1054">Az.Network</span></span>
* <span data-ttu-id="c8c8b-1055">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1055">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c8c8b-1056">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1056">Az.RecoveryServices</span></span>
* <span data-ttu-id="c8c8b-1057">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1057">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="c8c8b-1058">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1058">SDK Update</span></span>
* <span data-ttu-id="c8c8b-1059">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1059">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="c8c8b-1060">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1060">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-1061">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1061">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-1062">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1062">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="c8c8b-1063">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1063">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="c8c8b-1064">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1064">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="c8c8b-1065">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1065">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="c8c8b-1066">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1066">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="c8c8b-1067">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1067">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1068">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-1069">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1069">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="c8c8b-1070">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1070">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c8c8b-1071">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1071">Az.Storage</span></span>
* <span data-ttu-id="c8c8b-1072">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1072">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="c8c8b-1073">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1073">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="c8c8b-1074">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1074">Az.AnalysisServices</span></span>
* <span data-ttu-id="c8c8b-1075">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1075">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c8c8b-1076">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1076">Az.Automation</span></span>
* <span data-ttu-id="c8c8b-1077">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1077">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="c8c8b-1078">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1078">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="c8c8b-1079">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1079">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c8c8b-1080">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1080">Az.CognitiveServices</span></span>
* <span data-ttu-id="c8c8b-1081">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1081">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-1082">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1082">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-1083">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1083">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="c8c8b-1084">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1084">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="c8c8b-1085">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1085">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="c8c8b-1086">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1086">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c8c8b-1087">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1087">Az.DataLakeStore</span></span>
* <span data-ttu-id="c8c8b-1088">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1088">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c8c8b-1089">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1089">Az.EventHub</span></span>
* <span data-ttu-id="c8c8b-1090">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1090">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="c8c8b-1091">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1091">Az.KeyVault</span></span>
* <span data-ttu-id="c8c8b-1092">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1092">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c8c8b-1093">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1093">Az.LogicApp</span></span>
* <span data-ttu-id="c8c8b-1094">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1094">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="c8c8b-1095">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1095">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="c8c8b-1096">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1096">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="c8c8b-1097">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1097">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c8c8b-1098">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1098">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c8c8b-1099">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1099">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c8c8b-1100">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1100">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="c8c8b-1101">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1101">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="c8c8b-1102">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1102">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c8c8b-1103">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1103">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c8c8b-1104">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1104">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c8c8b-1105">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1105">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="c8c8b-1106">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1106">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c8c8b-1107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1107">Az.Monitor</span></span>
* <span data-ttu-id="c8c8b-1108">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1108">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-1109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1109">Az.Network</span></span>
* <span data-ttu-id="c8c8b-1110">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1110">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c8c8b-1111">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1111">Az.OperationalInsights</span></span>
* <span data-ttu-id="c8c8b-1112">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1112">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="c8c8b-1113">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1113">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="c8c8b-1114">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1114">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="c8c8b-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1115">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-1116">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1116">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c8c8b-1117">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1117">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="c8c8b-1118">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="c8c8b-1119">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1119">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-1120">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1120">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-1121">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1121">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="c8c8b-1122">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1122">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c8c8b-1123">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1123">Az.Websites</span></span>
* <span data-ttu-id="c8c8b-1124">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1124">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="c8c8b-1125">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1125">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c8c8b-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1126">Az.Accounts</span></span>
* <span data-ttu-id="c8c8b-1127">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1127">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c8c8b-1128">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1128">Az.AnalysisServices</span></span>
<span data-ttu-id="c8c8b-1129">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1129">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-1130">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1130">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-1131">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1131">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="c8c8b-1132">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1132">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="c8c8b-1133">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1133">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c8c8b-1134">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1134">Az.RecoveryServices</span></span>
<span data-ttu-id="c8c8b-1135">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1135">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1136">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-1137">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1137">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="c8c8b-1138">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1138">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c8c8b-1139">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1139">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="c8c8b-1140">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1140">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-1141">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1141">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-1142">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1142">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="c8c8b-1143">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1143">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="c8c8b-1144">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1144">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="c8c8b-1145">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1145">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c8c8b-1146">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1146">Az.Accounts</span></span>
* <span data-ttu-id="c8c8b-1147">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1147">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c8c8b-1148">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1148">Az.AnalysisServices</span></span>
* <span data-ttu-id="c8c8b-1149">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1149">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c8c8b-1150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1150">Az.RecoveryServices</span></span>
* <span data-ttu-id="c8c8b-1151">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1151">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="c8c8b-1152">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1152">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c8c8b-1153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1153">Az.Accounts</span></span>
* <span data-ttu-id="c8c8b-1154">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1154">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c8c8b-1155">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1155">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c8c8b-1156">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1156">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="c8c8b-1157">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1157">Az.Aks</span></span>
* <span data-ttu-id="c8c8b-1158">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1158">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c8c8b-1159">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1159">Az.Automation</span></span>
* <span data-ttu-id="c8c8b-1160">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1160">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="c8c8b-1161">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1161">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c8c8b-1162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1162">Az.Cdn</span></span>
* <span data-ttu-id="c8c8b-1163">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1163">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-1164">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1164">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-1165">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1165">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="c8c8b-1166">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1166">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="c8c8b-1167">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1167">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="c8c8b-1168">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1168">Az.ContainerRegistry</span></span>
* <span data-ttu-id="c8c8b-1169">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1169">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c8c8b-1170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1170">Az.DataFactory</span></span>
* <span data-ttu-id="c8c8b-1171">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1171">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c8c8b-1172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1172">Az.DataLakeStore</span></span>
* <span data-ttu-id="c8c8b-1173">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1173">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="c8c8b-1174">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1174">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="c8c8b-1175">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1175">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c8c8b-1176">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1176">Az.IotHub</span></span>
* <span data-ttu-id="c8c8b-1177">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1177">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c8c8b-1178">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1178">Az.KeyVault</span></span>
* <span data-ttu-id="c8c8b-1179">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1179">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-1180">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1180">Az.Network</span></span>
* <span data-ttu-id="c8c8b-1181">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1181">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-1182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1182">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-1183">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1183">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="c8c8b-1184">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1184">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="c8c8b-1185">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1185">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="c8c8b-1186">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1186">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="c8c8b-1187">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1187">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="c8c8b-1188">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1188">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="c8c8b-1189">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1189">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c8c8b-1190">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1190">Az.ServiceFabric</span></span>
* <span data-ttu-id="c8c8b-1191">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1191">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="c8c8b-1192">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1192">Fix some error messages.</span></span>
* <span data-ttu-id="c8c8b-1193">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1193">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="c8c8b-1194">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1194">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c8c8b-1195">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1195">Az.SignalR</span></span>
* <span data-ttu-id="c8c8b-1196">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1196">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-1197">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1197">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-1198">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1198">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c8c8b-1199">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1199">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="c8c8b-1200">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1200">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="c8c8b-1201">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1201">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c8c8b-1202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1202">Az.Storage</span></span>
* <span data-ttu-id="c8c8b-1203">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1203">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c8c8b-1204">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1204">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="c8c8b-1205">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1205">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="c8c8b-1206">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1206">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="c8c8b-1207">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1207">Az.TrafficManager</span></span>
* <span data-ttu-id="c8c8b-1208">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1208">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c8c8b-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1209">Az.Websites</span></span>
* <span data-ttu-id="c8c8b-1210">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1210">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c8c8b-1211">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1211">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="c8c8b-1212">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1212">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="c8c8b-1213">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1213">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c8c8b-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1214">Az.Accounts</span></span>
* <span data-ttu-id="c8c8b-1215">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1215">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-1216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1216">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-1217">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1217">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="c8c8b-1218">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1218">Updated the description of ID in help files</span></span>
* <span data-ttu-id="c8c8b-1219">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1219">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c8c8b-1220">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1220">Az.DataLakeStore</span></span>
* <span data-ttu-id="c8c8b-1221">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1221">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="c8c8b-1222">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1222">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c8c8b-1223">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1223">Az.EventGrid</span></span>
* <span data-ttu-id="c8c8b-1224">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1224">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="c8c8b-1225">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1225">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="c8c8b-1226">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1226">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c8c8b-1227">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1227">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c8c8b-1228">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1228">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c8c8b-1229">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1229">Dead letter endpoint.</span></span>
    - <span data-ttu-id="c8c8b-1230">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1230">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c8c8b-1231">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1231">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c8c8b-1232">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1232">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c8c8b-1233">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1233">Dead letter endpoint.</span></span>
* <span data-ttu-id="c8c8b-1234">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1234">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="c8c8b-1235">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1235">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c8c8b-1236">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1236">Az.IotHub</span></span>
* <span data-ttu-id="c8c8b-1237">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1237">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c8c8b-1238">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1238">Az.LogicApp</span></span>
* <span data-ttu-id="c8c8b-1239">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1239">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-1240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1240">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-1241">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1241">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="c8c8b-1242">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1242">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="c8c8b-1243">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1243">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c8c8b-1244">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1244">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="c8c8b-1245">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1245">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="c8c8b-1246">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1246">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c8c8b-1247">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1247">Az.SignalR</span></span>
* <span data-ttu-id="c8c8b-1248">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1248">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-1249">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1249">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-1250">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1250">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c8c8b-1251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1251">Az.Storage</span></span>
* <span data-ttu-id="c8c8b-1252">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1252">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="c8c8b-1253">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1253">New-AzStorageContext</span></span>
* <span data-ttu-id="c8c8b-1254">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1254">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="c8c8b-1255">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1255">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c8c8b-1256">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1256">Az.Websites</span></span>
* <span data-ttu-id="c8c8b-1257">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1257">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="c8c8b-1258">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1258">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="c8c8b-1259">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1259">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="c8c8b-1260">Ogólne</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1260">General</span></span>

- <span data-ttu-id="c8c8b-1261">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1261">General Availability of Az Module</span></span>
- <span data-ttu-id="c8c8b-1262">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1262">Online help for each module</span></span>
- <span data-ttu-id="c8c8b-1263">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1263">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="c8c8b-1264">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1264">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="c8c8b-1265">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1265">Az.Accounts</span></span>
- <span data-ttu-id="c8c8b-1266">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1266">Changed from Az.Profile</span></span>
- <span data-ttu-id="c8c8b-1267">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1267">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c8c8b-1268">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1268">Az.ApiManagement</span></span>
- <span data-ttu-id="c8c8b-1269">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1269">Fixes for #7002</span></span>
- <span data-ttu-id="c8c8b-1270">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1270">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="c8c8b-1271">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1271">Az.Batch</span></span>
- <span data-ttu-id="c8c8b-1272">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1272">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="c8c8b-1273">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1273">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="c8c8b-1274">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1274">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="c8c8b-1275">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1275">Az.Billing</span></span>
- <span data-ttu-id="c8c8b-1276">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1276">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="c8c8b-1277">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1277">Az.CognitivServices</span></span>
- <span data-ttu-id="c8c8b-1278">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1278">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="c8c8b-1279">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1279">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c8c8b-1280">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1280">Az.ContainerInstance</span></span>
- <span data-ttu-id="c8c8b-1281">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1281">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="c8c8b-1282">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1282">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="c8c8b-1283">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1283">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c8c8b-1284">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1284">Az.DataLakeStore</span></span>
- <span data-ttu-id="c8c8b-1285">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="c8c8b-1286">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1286">Az.Monitor</span></span>
- <span data-ttu-id="c8c8b-1287">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1287">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="c8c8b-1288">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1288">Az.KeyVault</span></span>
- <span data-ttu-id="c8c8b-1289">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1289">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="c8c8b-1290">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1290">Az.MachineLearning</span></span>
- <span data-ttu-id="c8c8b-1291">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1291">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="c8c8b-1292">Az.Media</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1292">Az.Media</span></span>
- <span data-ttu-id="c8c8b-1293">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1293">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c8c8b-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1294">Az.Network</span></span>
<span data-ttu-id="c8c8b-1295">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1295">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="c8c8b-1296">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1296">New cmdlets added:</span></span>
        - <span data-ttu-id="c8c8b-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c8c8b-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c8c8b-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c8c8b-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c8c8b-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c8c8b-1302">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1302">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="c8c8b-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="c8c8b-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="c8c8b-1305">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1305">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="c8c8b-1306">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1306">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="c8c8b-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c8c8b-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c8c8b-1309">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1309">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="c8c8b-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="c8c8b-1311">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1311">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="c8c8b-1312">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1312">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="c8c8b-1313">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1313">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c8c8b-1314">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1314">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c8c8b-1315">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1315">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="c8c8b-1316">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1316">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="c8c8b-1317">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1317">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="c8c8b-1318">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1318">Az.OperationalInsights</span></span>
- <span data-ttu-id="c8c8b-1319">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="c8c8b-1320">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1320">Az.Profile</span></span>
- <span data-ttu-id="c8c8b-1321">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1321">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c8c8b-1322">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1322">Az.RecoveryServices</span></span>
- <span data-ttu-id="c8c8b-1323">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1323">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="c8c8b-1324">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1324">Az.Resources</span></span>
- <span data-ttu-id="c8c8b-1325">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c8c8b-1326">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1326">Az.ServiceFabric</span></span>
- <span data-ttu-id="c8c8b-1327">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1327">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="c8c8b-1328">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1328">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="c8c8b-1329">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1329">Az.SIgnalR</span></span>
- <span data-ttu-id="c8c8b-1330">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1330">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="c8c8b-1331">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1331">Az.Sql</span></span>
- <span data-ttu-id="c8c8b-1332">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1332">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="c8c8b-1333">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1333">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="c8c8b-1334">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1334">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="c8c8b-1335">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1335">Az.Storage</span></span>
- <span data-ttu-id="c8c8b-1336">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c8c8b-1337">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1337">Az.Websites</span></span>
- <span data-ttu-id="c8c8b-1338">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="c8c8b-1339">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1339">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="c8c8b-1340">Ogólne</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1340">General</span></span>

* <span data-ttu-id="c8c8b-1341">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1341">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="c8c8b-1342">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1342">Az.Compute</span></span>

* <span data-ttu-id="c8c8b-1343">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1343">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c8c8b-1344">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1344">Az.DataLakeStore</span></span>

* <span data-ttu-id="c8c8b-1345">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1345">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="c8c8b-1346">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1346">Az.FrontDoor</span></span>

* <span data-ttu-id="c8c8b-1347">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1347">Fixed some broken links</span></span>
    - <span data-ttu-id="c8c8b-1348">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1348">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="c8c8b-1349">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1349">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c8c8b-1350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1350">Az.RecoveryServices</span></span>

* <span data-ttu-id="c8c8b-1351">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1351">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="c8c8b-1352">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1352">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="c8c8b-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1353">Az.Resources</span></span>

* <span data-ttu-id="c8c8b-1354">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1354">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="c8c8b-1355">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1355">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="c8c8b-1356">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1356">Az.Sql</span></span>

* <span data-ttu-id="c8c8b-1357">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1357">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="c8c8b-1358">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1358">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="c8c8b-1359">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1359">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="c8c8b-1360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1360">Az.Storage</span></span>

* <span data-ttu-id="c8c8b-1361">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1361">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="c8c8b-1362">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1362">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="c8c8b-1363">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1363">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c8c8b-1364">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1364">Support Static Website configuration</span></span>
    - <span data-ttu-id="c8c8b-1365">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1365">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="c8c8b-1366">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1366">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c8c8b-1367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1367">Az.Websites</span></span>

* <span data-ttu-id="c8c8b-1368">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1368">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="c8c8b-1369">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1369">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="c8c8b-1370">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1370">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="c8c8b-1371">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1371">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c8c8b-1372">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1372">Az.ApiManagement</span></span>
* <span data-ttu-id="c8c8b-1373">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1373">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="c8c8b-1374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1374">Az.Automation</span></span>
* <span data-ttu-id="c8c8b-1375">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1375">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="c8c8b-1376">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1376">Added Update Management cmdlets</span></span>
* <span data-ttu-id="c8c8b-1377">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1377">Added Source Control cmdlets</span></span>
* <span data-ttu-id="c8c8b-1378">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1378">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="c8c8b-1379">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1379">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="c8c8b-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1380">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-1381">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1381">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="c8c8b-1382">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1382">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c8c8b-1383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1383">Az.ContainerInstance</span></span>
* <span data-ttu-id="c8c8b-1384">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1384">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="c8c8b-1385">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1385">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="c8c8b-1386">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1386">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c8c8b-1387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1387">Az.Network</span></span>
* <span data-ttu-id="c8c8b-1388">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1388">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="c8c8b-1389">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1389">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="c8c8b-1390">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1390">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="c8c8b-1391">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1391">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="c8c8b-1392">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1392">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c8c8b-1393">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1393">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="c8c8b-1394">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1394">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="c8c8b-1395">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1395">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c8c8b-1396">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1396">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="c8c8b-1397">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1397">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="c8c8b-1398">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1398">Az.Relay</span></span>
* <span data-ttu-id="c8c8b-1399">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1399">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="c8c8b-1400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1400">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-1401">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1401">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="c8c8b-1402">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1402">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="c8c8b-1403">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1403">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c8c8b-1404">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1404">Az.ServiceFabric</span></span>
* <span data-ttu-id="c8c8b-1405">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1405">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="c8c8b-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1406">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-1407">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1407">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="c8c8b-1408">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1408">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c8c8b-1409">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1409">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c8c8b-1410">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1410">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c8c8b-1411">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1411">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c8c8b-1412">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1412">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c8c8b-1413">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1413">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c8c8b-1414">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1414">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c8c8b-1415">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1415">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="c8c8b-1416">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1416">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="c8c8b-1417">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1417">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="c8c8b-1418">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1418">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="c8c8b-1419">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1419">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c8c8b-1420">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1420">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c8c8b-1421">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1421">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="c8c8b-1422">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1422">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="c8c8b-1423">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1423">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="c8c8b-1424">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1424">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c8c8b-1425">Ogólne</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1425">General</span></span>
* <span data-ttu-id="c8c8b-1426">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1426">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="c8c8b-1427">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1427">Az.Profile</span></span>
* <span data-ttu-id="c8c8b-1428">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1428">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="c8c8b-1429">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1429">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="c8c8b-1430">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1430">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="c8c8b-1431">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1431">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="c8c8b-1432">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1432">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="c8c8b-1433">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1433">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="c8c8b-1434">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1434">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="c8c8b-1435">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1435">Az.CognitiveServices</span></span>
* <span data-ttu-id="c8c8b-1436">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1436">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-1437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1437">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-1438">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1438">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="c8c8b-1439">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1439">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="c8c8b-1440">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1440">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c8c8b-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="c8c8b-1442">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1442">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="c8c8b-1443">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1443">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="c8c8b-1444">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1444">Az.Insights</span></span>
* <span data-ttu-id="c8c8b-1445">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1445">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="c8c8b-1446">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1446">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="c8c8b-1447">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1447">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="c8c8b-1448">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1448">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1449">Az.Network</span></span>
* <span data-ttu-id="c8c8b-1450">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1450">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="c8c8b-1451">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1451">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="c8c8b-1452">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1452">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="c8c8b-1453">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1453">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="c8c8b-1454">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1454">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c8c8b-1455">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1455">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c8c8b-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c8c8b-1457">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1457">Az.PolicyInsights</span></span>
* <span data-ttu-id="c8c8b-1458">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1458">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-1459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1459">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-1460">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1460">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="c8c8b-1461">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1461">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c8c8b-1462">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1462">Az.ServiceBus</span></span>
* <span data-ttu-id="c8c8b-1463">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1463">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c8c8b-1464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1464">Az.ServiceFabric</span></span>
* <span data-ttu-id="c8c8b-1465">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1465">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="c8c8b-1466">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1466">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="c8c8b-1467">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1467">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="c8c8b-1468">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1468">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="c8c8b-1469">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1469">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="c8c8b-1470">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1470">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="c8c8b-1471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1471">Az.Profile</span></span>
* <span data-ttu-id="c8c8b-1472">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1472">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="c8c8b-1473">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1473">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-1474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1474">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-1475">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1475">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="c8c8b-1476">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1476">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c8c8b-1477">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1477">Az.DataLakeStore</span></span>
* <span data-ttu-id="c8c8b-1478">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1478">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="c8c8b-1479">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1479">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="c8c8b-1480">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1480">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c8c8b-1481">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1481">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c8c8b-1482">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1482">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-1483">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1483">Az.Network</span></span>
* <span data-ttu-id="c8c8b-1484">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1484">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="c8c8b-1485">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1485">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-1486">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1486">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-1487">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1487">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="c8c8b-1488">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1488">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="c8c8b-1489">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1489">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="c8c8b-1490">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1490">Azure.Storage</span></span>
* <span data-ttu-id="c8c8b-1491">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1491">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="c8c8b-1492">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1492">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="c8c8b-1493">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1493">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c8c8b-1494">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1494">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="c8c8b-1495">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1495">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="c8c8b-1496">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1496">Az.CognitiveServices</span></span>
* <span data-ttu-id="c8c8b-1497">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1497">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c8c8b-1498">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1498">Az.Compute</span></span>
* <span data-ttu-id="c8c8b-1499">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1499">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="c8c8b-1500">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1500">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="c8c8b-1501">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1501">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="c8c8b-1502">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1502">Az.DataFactoryV2</span></span>
* <span data-ttu-id="c8c8b-1503">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1503">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c8c8b-1504">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1504">Az.Network</span></span>
* <span data-ttu-id="c8c8b-1505">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1505">Added NetworkProfile functionality.</span></span> <span data-ttu-id="c8c8b-1506">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1506">new cmdlets added</span></span>
    - <span data-ttu-id="c8c8b-1507">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1507">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="c8c8b-1508">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1508">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="c8c8b-1509">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1509">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="c8c8b-1510">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1510">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="c8c8b-1511">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1511">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="c8c8b-1512">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1512">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="c8c8b-1513">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1513">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="c8c8b-1514">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1514">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="c8c8b-1515">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1515">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c8c8b-1516">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1516">Az.RedisCache</span></span>
* <span data-ttu-id="c8c8b-1517">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1517">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="c8c8b-1518">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1518">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="c8c8b-1519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1519">Az.Resources</span></span>
* <span data-ttu-id="c8c8b-1520">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1520">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c8c8b-1521">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1521">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="c8c8b-1522">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1522">Az.Sql</span></span>
* <span data-ttu-id="c8c8b-1523">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1523">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c8c8b-1524">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1524">Az.Websites</span></span>
* <span data-ttu-id="c8c8b-1525">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1525">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="c8c8b-1526">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1526">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="c8c8b-1527">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1527">0.2.0 - September 2018</span></span>
 <span data-ttu-id="c8c8b-1528">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="c8c8b-1528">Initial Release</span></span>
