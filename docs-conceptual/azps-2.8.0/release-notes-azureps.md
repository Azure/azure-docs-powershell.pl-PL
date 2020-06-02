---
title: Informacje o wersji programu Azure PowerShell
description: Uzyskaj informacje na temat wszystkich najnowszych aktualizacji modułów programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: bcbb78809c2db63d665dc0c3d05e0614acce6045
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/28/2020
ms.locfileid: "84122157"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="57040-103">Informacje o wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="57040-103">Azure PowerShell release notes</span></span>
## <a name="280---october-2019"></a><span data-ttu-id="57040-104">2.8.0 — październik 2019 r.</span><span class="sxs-lookup"><span data-stu-id="57040-104">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="57040-105">Ogólne</span><span class="sxs-lookup"><span data-stu-id="57040-105">General</span></span>
* <span data-ttu-id="57040-106">Wydanie Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="57040-106">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="57040-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-107">Az.Accounts</span></span>
* <span data-ttu-id="57040-108">Aktualizacja telemetrii i ponowne zapisywanie adresów URL dla wygenerowanych modułów oraz naprawa testów jednostkowych systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="57040-108">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="57040-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="57040-109">Az.ApiManagement</span></span>
* <span data-ttu-id="57040-110">**Set-AzApiManagementApi** — Dodano obsługę aktualizowania interfejsu API do właściwości ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="57040-110">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="57040-111">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="57040-111">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="57040-112">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="57040-112">Az.Automation</span></span>
* <span data-ttu-id="57040-113">Naprawiono parametr ponownego uruchamiania polecenia cmdlet New-AzureAutomationSoftwareUpdateConfiguration dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="57040-113">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="57040-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="57040-114">Az.Batch</span></span>
* <span data-ttu-id="57040-115">Polecenie **Get-AzBatchNodeAgentSku** jest przestarzałe i zostanie zastąpione poleceniem **Get-AzBatchSupportImage** w wersji 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="57040-115">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-116">Az.Compute</span></span>
* <span data-ttu-id="57040-117">Dodano parametry Priority, EvictionPolicy i MaxPrice do poleceń cmdlet New-AzVM i New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="57040-117">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="57040-118">Naprawiono komunikat ostrzegawczy i dokumentację pomocy dla poleceń Add-AzVMAdditionalUnattendContent i Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="57040-118">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="57040-119">Naprawiono wyjątek -skipVmBackup dla maszyn wirtualnych z systemem Linux z dyskami zarządzanymi dla polecenia Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="57040-119">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="57040-120">Naprawiono usterkę w ustawieniach szyfrowania aktualizacji w scenariuszu dwuprzebiegowym polecenia Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="57040-120">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="57040-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="57040-121">Az.DataFactory</span></span>
* <span data-ttu-id="57040-122">Dodano polecenia CRUD dla przepływu danych usługi ADF w wersji 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow i Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="57040-122">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="57040-123">Dodano polecenia akcji dla sesji debugowania przepływu danych usługi ADF w wersji 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand i Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="57040-123">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="57040-124">Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.2.0</span><span class="sxs-lookup"><span data-stu-id="57040-124">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="57040-125">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="57040-125">Az.DataLakeStore</span></span>
* <span data-ttu-id="57040-126">Naprawiono weryfikację kont, aby umożliwić przekazywanie kont ze znakiem „-” bez domeny</span><span class="sxs-lookup"><span data-stu-id="57040-126">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="57040-127">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="57040-127">Az.HealthcareApis</span></span>
* <span data-ttu-id="57040-128">Zaktualizowano program PowerShell do wersji 1.0.0</span><span class="sxs-lookup"><span data-stu-id="57040-128">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="57040-129">Zaktualizowano zestaw SDK do wersji 1.0.2</span><span class="sxs-lookup"><span data-stu-id="57040-129">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="57040-130">Zaktualizowano testy, aby odwoływały się do nowej wersji zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="57040-130">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="57040-131">Zaktualizowano strukturę wyjściową z zagnieżdżonej do spłaszczonej.</span><span class="sxs-lookup"><span data-stu-id="57040-131">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="57040-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="57040-132">Az.IotHub</span></span>
* <span data-ttu-id="57040-133">Dodano nowe źródło routingu: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="57040-133">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="57040-134">Drobna poprawka usterki: Polecenie Get-AzIothub nie zwraca wartości subscriptionId</span><span class="sxs-lookup"><span data-stu-id="57040-134">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="57040-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="57040-135">Az.Monitor</span></span>
* <span data-ttu-id="57040-136">Dodano nowe odbiorniki grupy akcji dla polecenia cmdlet New-AzActionGroupReceiver: -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="57040-136">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="57040-137">Włączono korzystanie z typowych schematów alertów dla odbiorników.</span><span class="sxs-lookup"><span data-stu-id="57040-137">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="57040-138">Nie dotyczy to odbiorników wiadomości SMS, powiadomień push usługi Azure App , narzędzia ITSM i połączeń głosowych</span><span class="sxs-lookup"><span data-stu-id="57040-138">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="57040-139">Elementy webhook obsługują teraz uwierzytelnianie za pomocą usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="57040-139">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-140">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-140">Az.Network</span></span>
* <span data-ttu-id="57040-141">Dodano nowe polecenie cmdlet Get-AzAvailableServiceAlias, które można wywołać, aby pobrać aliasy do użytku z zasadami punktu końcowego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="57040-141">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="57040-142">Dodano obsługę dodawania selektorów ruchu do połączeń bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="57040-142">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="57040-143">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="57040-143">New cmdlets added:</span></span>
        - <span data-ttu-id="57040-144">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="57040-144">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="57040-145">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -TrafficSelectorPolicies</span><span class="sxs-lookup"><span data-stu-id="57040-145">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="57040-146">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="57040-146">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="57040-147">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="57040-147">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="57040-148">Dodano obsługę protokołów ESP i AH do konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="57040-148">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="57040-149">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="57040-149">Updated cmdlets:</span></span>
        - <span data-ttu-id="57040-150">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57040-150">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="57040-151">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57040-151">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="57040-152">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57040-152">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="57040-153">Poprawiono obsługę wyjątków w poleceniach cmdlet usługi Cortex</span><span class="sxs-lookup"><span data-stu-id="57040-153">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="57040-154">Dodano nowe generacje i jednostki SKU dla elementów VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57040-154">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="57040-155">Wprowadzono nowe generacje dla elementów VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="57040-155">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="57040-156">Wprowadzono nowe jednostki SKU o wysokiej przepływności dla elementów VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="57040-156">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="57040-157">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="57040-157">Az.RedisCache</span></span>
* <span data-ttu-id="57040-158">Zaktualizowano dokumentację referencyjną polecenia „Set-AzRedisCache” w celu uwzględnienia brakujących wartości parametru „-Size”</span><span class="sxs-lookup"><span data-stu-id="57040-158">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-159">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-159">Az.Sql</span></span>
* <span data-ttu-id="57040-160">Dodano obsługę ustawiania administratora usługi Active Directory w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="57040-160">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="57040-161">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="57040-161">Az.Storage</span></span>
* <span data-ttu-id="57040-162">Uaktualniono bibliotekę klienta usługi Azure Storage do wersji 11.1.0</span><span class="sxs-lookup"><span data-stu-id="57040-162">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="57040-163">Utworzenie listy kontenerów przy użyciu interfejsu API płaszczyzny zarządzania spowoduje wyświetlenie listy przy użyciu właściwości NextPageLink</span><span class="sxs-lookup"><span data-stu-id="57040-163">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="57040-164">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="57040-164">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="57040-165">Utworzenie listy kont magazynu z subskrypcji spowoduje wyświetlenie listy przy użyciu właściwości NextPageLink</span><span class="sxs-lookup"><span data-stu-id="57040-165">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="57040-166">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57040-166">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="57040-167">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="57040-167">Az.StorageSync</span></span>
* <span data-ttu-id="57040-168">Naprawiono problem 9810 w poleceniu Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="57040-168">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="57040-169">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="57040-169">Az.Websites</span></span>
* <span data-ttu-id="57040-170">Aktualizowanie elementu ASP aplikacji przy użyciu polecenia Set-AzWebApp kończyło się niepowodzeniem</span><span class="sxs-lookup"><span data-stu-id="57040-170">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="57040-171">2.7.0 — wrzesień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="57040-171">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="57040-172">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="57040-172">Az.ApiManagement</span></span>
* <span data-ttu-id="57040-173">Aktualizacja opisu parametru „-Format” w dokumentacji referencyjnej polecenia „Set-AzApiManagementPolicy”</span><span class="sxs-lookup"><span data-stu-id="57040-173">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="57040-174">Usunięto z dokumentacji referencyjnej odwołania do przestarzałego polecenia cmdlet „Update-AzApiManagementDeployment”.</span><span class="sxs-lookup"><span data-stu-id="57040-174">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="57040-175">Zamiast niego należy używać polecenia „Set-AzApiManagement”.</span><span class="sxs-lookup"><span data-stu-id="57040-175">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="57040-176">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="57040-176">Az.Automation</span></span>
* <span data-ttu-id="57040-177">Poprawiono literówkę w przykładzie w dokumentacji referencyjnej polecenia „Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="57040-177">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="57040-178">Dodano wyjaśnienie dotyczące ograniczeń systemu operacyjnego dla polecenia Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="57040-178">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="57040-179">Naprawiono wyjątek odwołania o wartości null dla opcji -Wait polecenia cmdlet Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="57040-179">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-180">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-180">Az.Compute</span></span>
* <span data-ttu-id="57040-181">Dodanie parametru UploadSizeInBytes do polecenia New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="57040-181">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="57040-182">Dodanie parametru Incremental do polecenia New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="57040-182">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="57040-183">Dodanie funkcji maszyny wirtualnej o niskim priorytecie:</span><span class="sxs-lookup"><span data-stu-id="57040-183">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="57040-184">do polecenia New-AzVMConfig dodano parametry MaxPrice, EvictionPolicy i Priority.</span><span class="sxs-lookup"><span data-stu-id="57040-184">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="57040-185">Parametr MaxPrice został dodany do poleceń cmdlet New-AzVmssConfig, Update-AzVM i Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="57040-185">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="57040-186">Rozwiązanie problemu z odwołaniem do maszyny wirtualnej dla polecenia cmdlet Get-AzAvailabilitySet, gdy wyświetla listę wszystkich zestawów dostępności w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="57040-186">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="57040-187">Naprawienie wyjątku o wartości null dla polecenia Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="57040-187">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="57040-188">Naprawienie metody przeszukiwania wirtualnego dysku twardego dla pozycji względem końca.</span><span class="sxs-lookup"><span data-stu-id="57040-188">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="57040-189">Rozwiązanie problemu z dyskami UltraSSD dla poleceń New-AzVM i Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="57040-189">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="57040-190">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="57040-190">Az.DataFactory</span></span>
* <span data-ttu-id="57040-191">Dodanie 3 nowych poleceń do usługi ADF w wersji 2 — Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription i Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="57040-191">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="57040-192">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.3</span><span class="sxs-lookup"><span data-stu-id="57040-192">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="57040-193">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="57040-193">Az.HDInsight</span></span>
* <span data-ttu-id="57040-194">Wywołanie zmian powodujących niezgodność</span><span class="sxs-lookup"><span data-stu-id="57040-194">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="57040-195">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="57040-195">Az.IotHub</span></span>
* <span data-ttu-id="57040-196">Dodanie obsługi w celu wywołania trybu failover dla usługi IotHub do sparowanego geograficznie regionu odzyskiwania po awarii.</span><span class="sxs-lookup"><span data-stu-id="57040-196">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="57040-197">Dodanie obsługi do zarządzania wzbogacaniem komunikatów dla usługi IotHub.</span><span class="sxs-lookup"><span data-stu-id="57040-197">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="57040-198">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="57040-198">New cmdlets are:</span></span>
    - <span data-ttu-id="57040-199">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="57040-199">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="57040-200">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="57040-200">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="57040-201">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="57040-201">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="57040-202">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="57040-202">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="57040-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="57040-203">Az.Monitor</span></span>
* <span data-ttu-id="57040-204">Wskazanie najnowszego zestawu Monitor SDK, tj. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="57040-204">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="57040-205">Dodaje zmiany niepowodujące niezgodności do poleceń cmdlet metryk, tj. wyliczenie Unit obsługuje kilka nowych wartości.</span><span class="sxs-lookup"><span data-stu-id="57040-205">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="57040-206">Są to polecenia cmdlet tylko do odczytu, więc nie będzie żadnych zmian w danych wejściowych tych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57040-206">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="57040-207">Wartość api-version żądań **ActionGroups** to teraz **2019-06-01**, wcześniej było to **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="57040-207">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="57040-208">Testy scenariusza zostały zaktualizowane w celu dostosowania do tej zmiany.</span><span class="sxs-lookup"><span data-stu-id="57040-208">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="57040-209">Konstruktory dla klas **EmailReceiver** i **WebhookReceiver** dodały jeden nowy argument obowiązkowy, tj. wartość logiczną o nazwie **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="57040-209">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="57040-210">Obecnie wartość ta jest stała i równa **false**, aby ukryć tę zmianę powodującą niezgodność przed poleceniami cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57040-210">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="57040-211">**UWAGA**: Jest to tymczasowa zmiana, która musi być zweryfikowana przez zespół ds. alertów.</span><span class="sxs-lookup"><span data-stu-id="57040-211">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="57040-212">Kolejność argumentów konstruktora klasy **Source** (powiązanej z klasą **ScheduledQueryRuleSource**) zmieniła się od poprzedniego zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="57040-212">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="57040-213">Ta zmiana wymaga naprawienia dwóch testów jednostkowych: kompilowały się, ale nie przechodziły testów.</span><span class="sxs-lookup"><span data-stu-id="57040-213">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="57040-214">Kolejność argumentów konstruktora klasy **AlertingAction** (powiązanej z klasą **ScheduledQueryRuleSource**) została zmieniona od poprzedniego zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="57040-214">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="57040-215">Ta zmiana wymaga naprawienia dwóch testów jednostkowych: kompilowały się, ale nie przechodziły testów.</span><span class="sxs-lookup"><span data-stu-id="57040-215">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="57040-216">Obsługa kryteriów progu dynamicznego dla alertu metryki w wersji 2</span><span class="sxs-lookup"><span data-stu-id="57040-216">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="57040-217">New-AzMetricAlertRuleV2Criteria: teraz tworzy kryteria progów dynamicznych</span><span class="sxs-lookup"><span data-stu-id="57040-217">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="57040-218">Add-AzMetricAlertRuleV2: teraz akceptuje kryteria progów dynamicznych</span><span class="sxs-lookup"><span data-stu-id="57040-218">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="57040-219">Ulepszenia poleceń cmdlet reguły zaplanowanego zapytania (SQR)</span><span class="sxs-lookup"><span data-stu-id="57040-219">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="57040-220">Polecenia cmdlet będą akceptować parametr „Location” w obu formatach: jako lokalizację (np. eastus) i jako nazwę wyświetlaną lokalizacji (np. East US)</span><span class="sxs-lookup"><span data-stu-id="57040-220">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="57040-221">Poprawnie zilustrowano parametr „Enabled” w plikach pomocy</span><span class="sxs-lookup"><span data-stu-id="57040-221">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="57040-222">Dodano przykłady dla opcjonalnego parametru „ActionGroup”</span><span class="sxs-lookup"><span data-stu-id="57040-222">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="57040-223">Ogólnie ulepszono pliki pomocy</span><span class="sxs-lookup"><span data-stu-id="57040-223">Overall improved help files</span></span>
* <span data-ttu-id="57040-224">Naprawienie usterki dotyczącej określania typu zakresu dla polecenia „Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="57040-224">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-225">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-225">Az.Network</span></span>
* <span data-ttu-id="57040-226">Naprawienie nieprawidłowego przykładu w dokumentacji referencyjnej polecenia „New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="57040-226">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="57040-227">Dodanie w dokumentacji referencyjnej polecenia „Get-AzNetworkWatcherPacketCapture” uwagi dotyczącej pobierania wszystkich właściwości na potrzeby przechwytywania pakietów</span><span class="sxs-lookup"><span data-stu-id="57040-227">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="57040-228">Naprawiono przykład w dokumentacji referencyjnej polecenia „Test-AzNetworkWatcherIPFlow”, aby poprawnie wyliczał karty sieciowe</span><span class="sxs-lookup"><span data-stu-id="57040-228">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="57040-229">Ulepszono analizę wyjątku w chmurze, aby wyświetlane były dodatkowe szczegóły, jeśli są obecne</span><span class="sxs-lookup"><span data-stu-id="57040-229">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="57040-230">Ulepszono analizę wyjątku w chmurze, aby był obsługiwany dodatkowy typ wyjątku zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="57040-230">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="57040-231">Naprawiono niepoprawne mapowanie modeli reguł zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="57040-231">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="57040-232">Dodano właściwości interfejsu sieciowego dla funkcji prywatnego adresu IP</span><span class="sxs-lookup"><span data-stu-id="57040-232">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="57040-233">Dodano właściwość „PrivateEndpoint” jako typ PSResourceId do elementu PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="57040-233">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="57040-234">Dodano właściwość „PrivateLinkConnectionProperties” jako typ PSIpConfigurationConnectivityInformation do elementu PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="57040-234">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="57040-235">Dodano nową klasę modelu PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="57040-235">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="57040-236">Dodano nowy typ ApplicationRuleProtocolType „mssql” dla zasobu usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="57040-236">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="57040-237">Obsługa linku wielokrotnego w wirtualnej sieci WAN</span><span class="sxs-lookup"><span data-stu-id="57040-237">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="57040-238">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="57040-238">New cmdlets</span></span>
        - <span data-ttu-id="57040-239">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="57040-239">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="57040-240">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="57040-240">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="57040-241">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="57040-241">Updated cmdlet:</span></span>
        - <span data-ttu-id="57040-242">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="57040-242">New-VpnSite</span></span>
        - <span data-ttu-id="57040-243">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="57040-243">Update-VpnSite</span></span>
        - <span data-ttu-id="57040-244">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="57040-244">New-VpnConnection</span></span>
        - <span data-ttu-id="57040-245">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="57040-245">Update-VpnConnection</span></span>
* <span data-ttu-id="57040-246">Niektóre dokumenty dla przykładów programu PowerShell naprawiono w taki sposób, aby były w nich używane polecenia cmdlet Az zamiast poleceń cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="57040-246">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="57040-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="57040-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="57040-248">Aktualizacja obiektu AzureVMpolicy o atrybut ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="57040-248">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="57040-249">Dodano testy dotyczące zasad maszyny wirtualnej i przywracania oryginalnego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="57040-249">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-250">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-250">Az.Resources</span></span>
* <span data-ttu-id="57040-251">Naprawienie usterki polegającej na tym, że nie można było wywołać polecenia New-AzRoleAssignment bez parametru Scope.</span><span class="sxs-lookup"><span data-stu-id="57040-251">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="57040-252">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="57040-252">Az.ServiceFabric</span></span>
* <span data-ttu-id="57040-253">Poprawiono literówkę w przykładzie w dokumentacji referencyjnej polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="57040-253">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="57040-254">Dodanie nowych poleceń cmdlet do zarządzania aplikacją i usługami:</span><span class="sxs-lookup"><span data-stu-id="57040-254">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="57040-255">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="57040-255">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="57040-256">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="57040-256">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="57040-257">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="57040-257">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="57040-258">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="57040-258">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="57040-259">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="57040-259">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="57040-260">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="57040-260">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="57040-261">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="57040-261">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="57040-262">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="57040-262">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="57040-263">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="57040-263">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="57040-264">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="57040-264">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="57040-265">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="57040-265">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="57040-266">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="57040-266">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="57040-267">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="57040-267">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="57040-268">Uaktualniono zestaw Service Fabric SDK do wersji 1.2.0, która korzysta z dostawcy zasobów usługi Service Fabric o wersji interfejsu API 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="57040-268">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="57040-269">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="57040-269">Az.SignalR</span></span>
* <span data-ttu-id="57040-270">Dodanie poleceń cmdlet Update, Restart, CheckNameAvailability i GetUsage</span><span class="sxs-lookup"><span data-stu-id="57040-270">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-271">Az.Sql</span></span>
* <span data-ttu-id="57040-272">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="57040-272">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="57040-273">Dodano przykład dla rdzenia wirtualnego do tworzenia elastycznej puli (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="57040-273">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="57040-274">Usunięcie weryfikacji parametru EmailAddresses i sprawdzania, czy parametr EmailAdmins nie ma wartości false w przypadku, gdy parametr EmailAddresses jest pusty w poleceniach Set-AzSqlServerAdvancedThreatProtectionPolicy i Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="57040-274">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="57040-275">Włączono usuwanie ustawień inspekcji serwera/bazy danych, gdy istnieje wiele ustawień diagnostycznych włączających kategorię inspekcji.</span><span class="sxs-lookup"><span data-stu-id="57040-275">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="57040-276">Naprawa weryfikacji adresów e-mail w wielu poleceniach cmdlet do oceny luk w zabezpieczeniach SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting i Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="57040-276">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="57040-277">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="57040-277">Az.Storage</span></span>
* <span data-ttu-id="57040-278">Zaktualizowano przykład w dokumentacji referencyjnej dla polecenia „Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="57040-278">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="57040-279">Obsługa zachowywania w pliku docelowym właściwości SMB pliku źródłowego przy przekazywaniu/pobieraniu pliku platformy Azure (atrybuty pliku, czas utworzenia pliku, czas ostatniego zapisu pliku)</span><span class="sxs-lookup"><span data-stu-id="57040-279">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="57040-280">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="57040-280">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="57040-281">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="57040-281">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="57040-282">Naprawa awarii przekazywania blokowego obiektu blob z właściwościami/metadanymi dla elementu ImmutabilityPolicy z obsługą kontenerów.</span><span class="sxs-lookup"><span data-stu-id="57040-282">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="57040-283">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="57040-283">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="57040-284">Obsługa zarządzania udziałami plików platformy Azure za pomocą interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="57040-284">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="57040-285">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="57040-285">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="57040-286">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="57040-286">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="57040-287">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="57040-287">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="57040-288">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="57040-288">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="57040-289">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="57040-289">Az.Websites</span></span>
* <span data-ttu-id="57040-290">Naprawa problemu powodującego usuwanie tagów aplikacji internetowych podczas migrowania aplikacji do nowego planu ASP</span><span class="sxs-lookup"><span data-stu-id="57040-290">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="57040-291">Naprawa polecenia Publish-AzureWebapp w taki sposób, aby działało w systemach Linux i Windows</span><span class="sxs-lookup"><span data-stu-id="57040-291">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="57040-292">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzWebAppPublishingProfile”</span><span class="sxs-lookup"><span data-stu-id="57040-292">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="57040-293">2.6.0 — sierpień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="57040-293">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="57040-294">Ogólne</span><span class="sxs-lookup"><span data-stu-id="57040-294">General</span></span>
* <span data-ttu-id="57040-295">Naprawiono różne literówki w wielu modułach</span><span class="sxs-lookup"><span data-stu-id="57040-295">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="57040-296">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-296">Az.Accounts</span></span>
* <span data-ttu-id="57040-297">Obsługa pliku MSI przypisanego przez użytkownika w ramach uwierzytelniania usługi Azure Functions (nr 9479)</span><span class="sxs-lookup"><span data-stu-id="57040-297">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="57040-298">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="57040-298">Az.Aks</span></span>
* <span data-ttu-id="57040-299">Rozwiązano problem z danymi wyjściowymi polecenia „Get-AzAks”</span><span class="sxs-lookup"><span data-stu-id="57040-299">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="57040-300">Więcej informacji: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="57040-300">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="57040-301">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="57040-301">Az.ApiManagement</span></span>
* <span data-ttu-id="57040-302">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="57040-302">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="57040-303">Zaktualizowano wersję nuget .net, która nie wymusza ograniczeń dotyczących identyfikatorów productId, apiId, groupId i userId</span><span class="sxs-lookup"><span data-stu-id="57040-303">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="57040-304">**Get-AzApiManagementProduct** — dodano obsługę wysyłania zapytań dotyczących produktów przy użyciu interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="57040-304">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="57040-305">**New-AzApiManagementApiRevision** — poprawka rozwiązująca problem polegający na tym, że wartość ApiRevisionDescription nie była ustawiana podczas tworzenia nowej wersji pomocniczej interfejsu API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="57040-305">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="57040-306">Poprawiono literówkę w modelu „PsApiManagementOAuth2AuthrozationServer” na „PsApiManagementOAuth2AuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="57040-306">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="57040-307">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="57040-307">Az.Batch</span></span>
* <span data-ttu-id="57040-308">Poprawiono literówkę w komunikacie pomocy i dokumentacji, zmieniając literę w nazwie systemu Windows na wielką</span><span class="sxs-lookup"><span data-stu-id="57040-308">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="57040-309">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="57040-309">Az.Cdn</span></span>
* <span data-ttu-id="57040-310">Poprawiono literówkę w pomocniku konwersji modułu CDN</span><span class="sxs-lookup"><span data-stu-id="57040-310">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-311">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-311">Az.Compute</span></span>
* <span data-ttu-id="57040-312">Dodanie polecenia VmssId to New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="57040-312">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="57040-313">Dodanie parametrów TerminateScheduledEvents i TerminateScheduledEventNotBeforeTimeoutInMinutes do polecenia New-AzVmssConfig and Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="57040-313">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="57040-314">Dodanie właściwości HyperVGeneration do obiektu obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="57040-314">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="57040-315">Dodanie funkcji Host i HostGroup</span><span class="sxs-lookup"><span data-stu-id="57040-315">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="57040-316">Nowe polecenia cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="57040-316">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="57040-317">Dodano parametr HostId do poleceń New-AzVMConfig i New-AzVM</span><span class="sxs-lookup"><span data-stu-id="57040-317">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="57040-318">Aktualizacja przykładu w dokumentacji polecenia „Invoke-AzVMRunCommand” w celu użycia poprawnej nazwy parametru</span><span class="sxs-lookup"><span data-stu-id="57040-318">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="57040-319">Aktualizacja opisu parametru „-VolumeType” w dokumentacji referencyjnej poleceń „Set-AzVMDiskEncryptionExtension” i „Set-AzVmssDiskEncryptionExtension”</span><span class="sxs-lookup"><span data-stu-id="57040-319">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="57040-320">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="57040-320">Az.DataFactory</span></span>
* <span data-ttu-id="57040-321">Poprawiono literówkę w poleceniu „New-AzDataFactoryEncryptValue”, zmieniając literę w nazwie systemu Windows na wielką</span><span class="sxs-lookup"><span data-stu-id="57040-321">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="57040-322">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.2</span><span class="sxs-lookup"><span data-stu-id="57040-322">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="57040-323">Dodanie parametrów „DataProxyIntegrationRuntimeName”, „DataProxyStagingLinkedServiceName” i „DataProxyStagingPath” dla polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime”, aby umożliwić konfigurowanie własnego środowiska Integration Runtime jako serwera proxy dla środowiska SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="57040-323">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="57040-324">Zaktualizowano PSTriggerRun na potrzeby wyświetlania wyzwalanych potoków, komunikatów i właściwości, a także PSActivityRun na potrzeby wyświetlania typu działania</span><span class="sxs-lookup"><span data-stu-id="57040-324">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="57040-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="57040-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="57040-326">Poprawiono wysunięcie polecenia Get-DataLakeStoreDeletedItem pod kątem obsługi błędów lub wyjątków zdalnych.</span><span class="sxs-lookup"><span data-stu-id="57040-326">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="57040-327">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="57040-327">Az.EventHub</span></span>
* <span data-ttu-id="57040-328">Rozwiązano problem nr 9658: Literówka VirtualNteworkRule w poleceniu Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="57040-328">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="57040-329">Rozwiązano problem nr 9558: Polecenie Set-AzEventHubNamespace używa elementu PATCH zamiast PUT</span><span class="sxs-lookup"><span data-stu-id="57040-329">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="57040-330">dodano parametr EnableKafka do polecenia cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="57040-330">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="57040-331">Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania</span><span class="sxs-lookup"><span data-stu-id="57040-331">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="57040-332">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="57040-332">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="57040-333">Poprawiono literówkę w dokumentacji: „Azure” rozpoczynające się małą literą</span><span class="sxs-lookup"><span data-stu-id="57040-333">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="57040-334">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="57040-334">Az.Monitor</span></span>
* <span data-ttu-id="57040-335">Poprawiono niepoprawną nazwę parametru w dokumentacji pomocy</span><span class="sxs-lookup"><span data-stu-id="57040-335">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-336">Az.Network</span></span>
* <span data-ttu-id="57040-337">Zaktualizowano polecenie New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="57040-337">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="57040-338">Sklasyfikowano parametr „PublicIpAddress” jako przestarzały, ponieważ nie jest on nigdy używany po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="57040-338">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="57040-339">Dodano jeden opcjonalny parametr „Primary” wskazujący, czy bieżąca konfiguracja IP jest podstawowa, czy nie.</span><span class="sxs-lookup"><span data-stu-id="57040-339">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="57040-340">Ulepszono obsługę wyjątku błędu żądania z zestawu SDK — rozwiązuje to problem polegający na tym, że poprzednio wyjątki zestawu SDK nie były poprawnie obsługiwane, wskutek czego nie były wyświetlane kluczowe szczegóły błędu</span><span class="sxs-lookup"><span data-stu-id="57040-340">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="57040-341">Skorygowano logikę weryfikacji prefiksu IP w wersji IPv6 w celu sprawdzania, czy długość prefiksu IPv6 jest poprawna.</span><span class="sxs-lookup"><span data-stu-id="57040-341">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="57040-342">Zaktualizowano polecenie Get-AzVirtualNetworkSubnetConfig: Dodano parametr ustawiany w celu pobrania identyfikatora zasobu podsieci.</span><span class="sxs-lookup"><span data-stu-id="57040-342">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="57040-343">Zaktualizowano opis parametru Location dla AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="57040-343">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="57040-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="57040-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="57040-345">Zaktualizowano dokumentację polecenia „New-AzOperationalInsightsLinuxSyslogDataSource”</span><span class="sxs-lookup"><span data-stu-id="57040-345">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="57040-346">Dodano przykład</span><span class="sxs-lookup"><span data-stu-id="57040-346">Added example</span></span>
    - <span data-ttu-id="57040-347">Zaktualizowano opis parametru „-Name”</span><span class="sxs-lookup"><span data-stu-id="57040-347">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="57040-348">Dodano przykład dla polecenia New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="57040-348">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="57040-349">Zaktualizowano opis parametru „-Name” dla polecenia New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="57040-349">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="57040-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="57040-350">Az.RecoveryServices</span></span>
* <span data-ttu-id="57040-351">Aktualizacja polecenia „Get-AzRecoveryServicesBackupJobDetail.md”</span><span class="sxs-lookup"><span data-stu-id="57040-351">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-352">Az.Resources</span></span>
* <span data-ttu-id="57040-353">Dodano obsługę nowej wersji interfejsu API (2019-05-10) dla Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="57040-353">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="57040-354">Dodano obsługę „copy.count = 0” dla zmiennych, zasobów i właściwości</span><span class="sxs-lookup"><span data-stu-id="57040-354">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="57040-355">Zasoby z ustawieniami „condition = false” lub „copy.count = 0” będą usuwane w trybie ukończenia</span><span class="sxs-lookup"><span data-stu-id="57040-355">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="57040-356">Dodanie do dokumentu pomocy przykładu przypisywania zasad na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="57040-356">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="57040-357">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="57040-357">Az.ServiceBus</span></span>
* <span data-ttu-id="57040-358">Rozwiązano problem nr 9658: Literówka VirtualNetworkRule w poleceniu Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="57040-358">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="57040-359">Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania</span><span class="sxs-lookup"><span data-stu-id="57040-359">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="57040-360">Dodano nowe polecenie „Test-AzServiceBusNameAvailability” do sprawdzania dostępności nazwy dla kolejki i tematu</span><span class="sxs-lookup"><span data-stu-id="57040-360">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="57040-361">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="57040-361">Az.ServiceFabric</span></span>
* <span data-ttu-id="57040-362">Usunięcie usterek poleceń cmdlet dodawania typu węzła:</span><span class="sxs-lookup"><span data-stu-id="57040-362">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="57040-363">Usterka NullReferenceException, gdy grupa zasobów ma inny zestaw VMSS niezwiązany z klastrem usługi Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="57040-363">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="57040-364">Rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="57040-364">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="57040-365">Usunięcie usterki powodującej niepowodzenie polecenia cmdlet, gdy sieć wirtualna znajdowała się w innej grupie zasobów niż klaster.</span><span class="sxs-lookup"><span data-stu-id="57040-365">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="57040-366">rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="57040-366">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="57040-367">Sklasyfikowanie polecenia cmdlet Add-AzServiceFabricApplicationCertificate jako przestarzałego</span><span class="sxs-lookup"><span data-stu-id="57040-367">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-368">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-368">Az.Sql</span></span>
* <span data-ttu-id="57040-369">Aktualizacja dokumentacji starych poleceń cmdlet inspekcji.</span><span class="sxs-lookup"><span data-stu-id="57040-369">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="57040-370">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="57040-370">Az.Storage</span></span>
* <span data-ttu-id="57040-371">Aktualizacja pomocy dotyczącej poleceń Get/Close-AzStorageFileHandle, przez dodanie kolejnych scenariuszy do przykładów dotyczących poleceń cmdlet i zaktualizowanie opisów parametrów</span><span class="sxs-lookup"><span data-stu-id="57040-371">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="57040-372">Obsługa StandardBlobTier w ramach przekazywania i kopiowania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="57040-372">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="57040-373">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="57040-373">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="57040-374">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="57040-374">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="57040-375">Obsługa priorytetu ponownego wypełniania w ramach kopiowania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="57040-375">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="57040-376">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="57040-376">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="57040-377">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="57040-377">Az.Websites</span></span>
* <span data-ttu-id="57040-378">Dodanie wyjaśnienia do parametru -AppSettings w poleceniach Set-AzWebApp i Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57040-378">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="57040-379">2.5.0 — lipiec 2019</span><span class="sxs-lookup"><span data-stu-id="57040-379">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="57040-380">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-380">Az.Accounts</span></span>
* <span data-ttu-id="57040-381">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="57040-381">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="57040-382">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="57040-382">Az.ApplicationInsights</span></span>
* <span data-ttu-id="57040-383">Poprawienie pisowni w przykładzie w dokumentacji polecenia „Remove-AzApplicationInsightsApiKey”</span><span class="sxs-lookup"><span data-stu-id="57040-383">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="57040-384">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="57040-384">Az.Automation</span></span>
* <span data-ttu-id="57040-385">Poprawienie pisowni w ciągu zasobu</span><span class="sxs-lookup"><span data-stu-id="57040-385">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="57040-386">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="57040-386">Az.CognitiveServices</span></span>
* <span data-ttu-id="57040-387">Dodano obsługę właściwości NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="57040-387">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-388">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-388">Az.Compute</span></span>
* <span data-ttu-id="57040-389">Dodanie brakujących właściwości (ComputerName, OsName, OsVersion i HyperVGeneration) obiektu widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57040-389">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="57040-390">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="57040-390">Az.ContainerRegistry</span></span>
* <span data-ttu-id="57040-391">Poprawienie pisowni parametru Replication w opisie polecenia Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="57040-391">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="57040-392">Więcej informacji można znaleźć tutaj: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="57040-392">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="57040-393">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="57040-393">Az.DataFactory</span></span>
* <span data-ttu-id="57040-394">Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.0</span><span class="sxs-lookup"><span data-stu-id="57040-394">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="57040-395">Poprawienie pisowni w dokumentacji dla polecenia „Get-AzDataFactoryV2PipelineRun”</span><span class="sxs-lookup"><span data-stu-id="57040-395">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="57040-396">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="57040-396">Az.EventHub</span></span>
* <span data-ttu-id="57040-397">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="57040-397">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="57040-398">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="57040-398">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="57040-399">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="57040-399">Az.KeyVault</span></span>
* <span data-ttu-id="57040-400">Dodano obsługę określania rozmiaru klucza dla zasad certyfikatów</span><span class="sxs-lookup"><span data-stu-id="57040-400">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="57040-401">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="57040-401">Az.LogicApp</span></span>
* <span data-ttu-id="57040-402">Poprawienie polecenia Get-AzIntegrationAccountMap tak, aby wyświetlało listę wszystkich typów map</span><span class="sxs-lookup"><span data-stu-id="57040-402">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="57040-403">Dodano nowy parametr MapType na potrzeby filtrowania</span><span class="sxs-lookup"><span data-stu-id="57040-403">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="57040-404">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="57040-404">Az.ManagedServices</span></span>
* <span data-ttu-id="57040-405">Dodano obsługę interfejsu API w wersji 2019-06-01 (ogólna dostępność)</span><span class="sxs-lookup"><span data-stu-id="57040-405">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-406">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-406">Az.Network</span></span>
* <span data-ttu-id="57040-407">Dodanie obsługi prywatnego punktu końcowego i prywatnej usługi łączenia</span><span class="sxs-lookup"><span data-stu-id="57040-407">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="57040-408">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="57040-408">New cmdlets</span></span>
        - <span data-ttu-id="57040-409">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="57040-409">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="57040-410">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="57040-410">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="57040-411">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="57040-411">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="57040-412">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="57040-412">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="57040-413">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="57040-413">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="57040-414">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="57040-414">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="57040-415">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="57040-415">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="57040-416">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="57040-416">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="57040-417">Zaktualizowano poniższe polecenia dla funkcji: Flaga PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies w podsieci w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="57040-417">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="57040-418">Zaktualizowano polecenia New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="57040-418">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="57040-419">Dodano opcjonalny parametr -PrivateEndpointNetworkPoliciesFlag, który konfiguruje, czy stosować zasady sieciowe w prywatnym punkcie końcowym w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="57040-419">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="57040-420">Dodano opcjonalny parametr -PrivateLinkServiceNetworkPoliciesFlag, który konfiguruje, czy stosować zasady sieciowe w usłudze łącza prywatnego w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="57040-420">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="57040-421">Nazwa parametru „ServiceName” polecenia cmdlet AzPrivateLinkService została zmieniona na „Name” z aliasem „ServiceName” w celu zachowania zgodności z poprzednimi wersjami</span><span class="sxs-lookup"><span data-stu-id="57040-421">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="57040-422">Włączenie protokołu ICMP dla konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="57040-422">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="57040-423">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="57040-423">Updated cmdlets</span></span>
        - <span data-ttu-id="57040-424">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57040-424">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="57040-425">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57040-425">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="57040-426">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57040-426">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="57040-427">Dodanie wartości ConnectionProtocolType (Ikev1/Ikev2) jako konfigurowalnego parametru dla polecenia New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="57040-427">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="57040-428">Dodanie parametru PrivateIpAddressVersion w elemencie LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="57040-428">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="57040-429">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="57040-429">Updated cmdlet:</span></span>
        - <span data-ttu-id="57040-430">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="57040-430">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="57040-431">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="57040-431">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="57040-432">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="57040-432">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="57040-433">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig usługi Application Gateway o obsługę portu niestandardowego w sondzie</span><span class="sxs-lookup"><span data-stu-id="57040-433">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="57040-434">Aktualizacja polecenia New-AzApplicationGatewayProbeConfig: Dodano opcjonalny parametr Port, który służy do sondowania serwera zaplecza.</span><span class="sxs-lookup"><span data-stu-id="57040-434">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="57040-435">Ten parametr ma zastosowanie w przypadku jednostek SKU Standard_V2 i WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="57040-435">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="57040-436">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="57040-436">Az.OperationalInsights</span></span>
* <span data-ttu-id="57040-437">Zaktualizowano domyślną wersję zapisywanych wyszukiwań na 1.</span><span class="sxs-lookup"><span data-stu-id="57040-437">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="57040-438">Poprawiono obsługę wyrażeń regularnych o wartości null dla dzienników niestandardowych</span><span class="sxs-lookup"><span data-stu-id="57040-438">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="57040-439">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="57040-439">Az.RecoveryServices</span></span>
* <span data-ttu-id="57040-440">Aktualizacja pliku „Get-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="57040-440">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="57040-441">Aktualizacja pliku „Get-AzRecoveryServicesBackupContainer.md”</span><span class="sxs-lookup"><span data-stu-id="57040-441">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="57040-442">Aktualizacja pliku „Get-AzRecoveryServicesVault.md”</span><span class="sxs-lookup"><span data-stu-id="57040-442">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="57040-443">Aktualizacja pliku „Wait-AzRecoveryServicesBackupJob.md”</span><span class="sxs-lookup"><span data-stu-id="57040-443">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="57040-444">Aktualizacja pliku „Set-AzRecoveryServicesVaultContext.md”</span><span class="sxs-lookup"><span data-stu-id="57040-444">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="57040-445">Aktualizacja pliku „Get-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="57040-445">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="57040-446">Aktualizacja pliku „Get-AzRecoveryServicesBackupRecoveryPoint.md”</span><span class="sxs-lookup"><span data-stu-id="57040-446">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="57040-447">Aktualizacja pliku „Restore-AzRecoveryServicesBackupItem.md”</span><span class="sxs-lookup"><span data-stu-id="57040-447">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="57040-448">Zaktualizowano wywołanie usługi do wyrejestrowywania kontenera dla udziału plików platformy Azure</span><span class="sxs-lookup"><span data-stu-id="57040-448">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="57040-449">Aktualizacja pliku „Set-AzRecoveryServicesAsrAlertSetting.md”</span><span class="sxs-lookup"><span data-stu-id="57040-449">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-450">Az.Resources</span></span>
- <span data-ttu-id="57040-451">Usunięcie brakującego polecenia cmdlet przywoływanego w dokumentacji polecenia „New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="57040-451">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="57040-452">Zaktualizowano polecenia cmdlet zasad w celu używania nowego interfejsu API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="57040-452">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="57040-453">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="57040-453">Az.ServiceBus</span></span>
* <span data-ttu-id="57040-454">Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="57040-454">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="57040-455">Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”</span><span class="sxs-lookup"><span data-stu-id="57040-455">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-456">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-456">Az.Sql</span></span>
* <span data-ttu-id="57040-457">Poprawienie brakujących przykładów dla polecenia cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="57040-457">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="57040-458">Poprawienie ustawiania cyklicznego skanowania przez rozszerzenie Ocena luk w zabezpieczeniach bez podawania żadnego adresu e-mail</span><span class="sxs-lookup"><span data-stu-id="57040-458">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="57040-459">Poprawienie pisowni w komunikacie ostrzegawczym.</span><span class="sxs-lookup"><span data-stu-id="57040-459">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="57040-460">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="57040-460">Az.Storage</span></span>
* <span data-ttu-id="57040-461">Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzStorageAccount” w celu użycia poprawnej nazwy parametru</span><span class="sxs-lookup"><span data-stu-id="57040-461">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="57040-462">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="57040-462">Az.StorageSync</span></span>
* <span data-ttu-id="57040-463">Dodanie polecenia cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="57040-463">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="57040-464">Rozwiązanie problemu 9551 dotyczącego respektowania wartości TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="57040-464">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="57040-465">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="57040-465">Az.Websites</span></span>
* <span data-ttu-id="57040-466">Usunięcie usterki polegającej na tym, że niektóre właściwości SiteConfig nie były zwracane przez polecenia Get-AzWebApp i Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="57040-466">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="57040-467">Dodanie nowego parametru Location dla poleceń Get-AzDeletedWebApp i Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="57040-467">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="57040-468">Usunięcie usterki związanej z klonowaniem miejsc aplikacji internetowych przy użyciu polecenia New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="57040-468">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="57040-469">2.4.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="57040-469">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="57040-470">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-470">Az.Accounts</span></span>
* <span data-ttu-id="57040-471">Dodano obsługę poleceń cmdlet profilu</span><span class="sxs-lookup"><span data-stu-id="57040-471">Add support for profile cmdlets</span></span>
* <span data-ttu-id="57040-472">Dodano obsługę środowisk i płaszczyzn danych w generowanych poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="57040-472">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="57040-473">Naprawiono błąd polegający na tym, że w niektórych przypadkach dla poleceń cmdlet płaszczyzny danych w programie Windows PowerShell był używany nieprawidłowy punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="57040-473">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="57040-474">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="57040-474">Az.Advisor</span></span>
* <span data-ttu-id="57040-475">Wersja ogólnodostępna modułu Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="57040-475">GA release of Az.Advisor</span></span>
* <span data-ttu-id="57040-476">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="57040-476">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="57040-477">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="57040-477">Az.ApiManagement</span></span>
* <span data-ttu-id="57040-478">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="57040-478">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="57040-479">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="57040-479">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="57040-480">Dodano obsługę wykonywania zapytań dotyczących subskrypcji według użytkownika i produktu</span><span class="sxs-lookup"><span data-stu-id="57040-480">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="57040-481">Dodano obsługę wykonywania zapytań przy użyciu zakresu „/”, „/apis”, „/apis/echo-api”</span><span class="sxs-lookup"><span data-stu-id="57040-481">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="57040-482">Rozwiązano problemy https://github.com/Azure/azure-powershell/issues/9307 i https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="57040-482">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="57040-483">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="57040-483">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="57040-484">Dodano obsługę określania właściwości „ApiVersion” i „ApiVersionSetId” podczas importowania interfejsów API</span><span class="sxs-lookup"><span data-stu-id="57040-484">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="57040-485">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="57040-485">Az.Automation</span></span>
* <span data-ttu-id="57040-486">Usunięto usterkę polecenia cmdlet Set-AzAutomationConnectionFieldValue w celu obsługi wartości ciągu.</span><span class="sxs-lookup"><span data-stu-id="57040-486">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-487">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-487">Az.Compute</span></span>
* <span data-ttu-id="57040-488">Dodano parametr HyperVGeneration do polecenia New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="57040-488">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="57040-489">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="57040-489">Az.DataFactory</span></span>
* <span data-ttu-id="57040-490">Aktualizowanie danych wyjściowych poleceń cmdlet pobierania uruchomień działań, pobierania uruchomień potoków i pobierania uruchomień wyzwalaczy usługi ADF w celu obsługi potoku Select-Object.</span><span class="sxs-lookup"><span data-stu-id="57040-490">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="57040-491">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="57040-491">Az.EventGrid</span></span>
* <span data-ttu-id="57040-492">Poprawiono literówkę w dokumentacji polecenia New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="57040-492">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="57040-493">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="57040-493">Az.IotHub</span></span>
* <span data-ttu-id="57040-494">Dodano obsługę ponownego generowania kluczy zasad autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="57040-494">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-495">Az.Network</span></span>
* <span data-ttu-id="57040-496">Dodano właściwość „RoutingPreference” do tagów publicznych adresów IP</span><span class="sxs-lookup"><span data-stu-id="57040-496">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="57040-497">Poprawiono przykłady dla dokumentacji referencyjnej polecenia „Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="57040-497">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="57040-498">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="57040-498">Az.PolicyInsights</span></span>
* <span data-ttu-id="57040-499">Rozwiązano problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="57040-499">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="57040-500">Więcej informacji: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="57040-500">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="57040-501">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="57040-501">Az.OperationalInsights</span></span>
* <span data-ttu-id="57040-502">Naprawiono model źródła danych CustomLog zwracany w poleceniu Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="57040-502">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="57040-503">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="57040-503">Az.RecoveryServices</span></span>
* <span data-ttu-id="57040-504">Poprawka dotycząca polecenia get-policy dla maszyn wirtualnych IaaS</span><span class="sxs-lookup"><span data-stu-id="57040-504">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-505">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-505">Az.Resources</span></span>
    - <span data-ttu-id="57040-506">Poprawiono tekst pomocy dotyczącej parametru -Top polecenia Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="57040-506">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="57040-507">Dodano obsługę stronicowania po stronie klienta dla polecenia Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="57040-507">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="57040-508">Dodano nowe parametry dla polecenia Set-AzPolicyAssignment: -PolicyParameters i -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="57040-508">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="57040-509">Aktualizacje dokumentacji i przykładów dla poleceń cmdlet zasad</span><span class="sxs-lookup"><span data-stu-id="57040-509">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="57040-510">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="57040-510">Az.ServiceBus</span></span>
* <span data-ttu-id="57040-511">Poprawka rozwiązująca problem #4938 — polecenie New-AzureRmServiceBusQueue zwraca wynik BadRequest w przypadku ustawienia właściwości MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="57040-511">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-512">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-512">Az.Sql</span></span>
* <span data-ttu-id="57040-513">Dodano polecenia cmdlet grupy trybu failover wystąpienia z wersji zapoznawczej do wersji publicznej</span><span class="sxs-lookup"><span data-stu-id="57040-513">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="57040-514">Obsługa inspekcji w usłudze Azure SQL Server/Database za pomocą nowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57040-514">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="57040-515">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="57040-515">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="57040-516">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="57040-516">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="57040-517">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="57040-517">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="57040-518">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="57040-518">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="57040-519">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="57040-519">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="57040-520">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="57040-520">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="57040-521">Usunięto ograniczenia wiadomości e-mail z ustawień oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="57040-521">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="57040-522">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="57040-522">Az.Storage</span></span>
* <span data-ttu-id="57040-523">Zmieniono dwa parametry: „-IndexDocument” i „-ErrorDocument404Path” z wymaganych na opcjonalne w poleceniu cmdlet:</span><span class="sxs-lookup"><span data-stu-id="57040-523">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="57040-524">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="57040-524">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="57040-525">Zaktualizowano pomoc dotyczącą polecenia Get-AzStorageBlobContent przez dodanie przykładu</span><span class="sxs-lookup"><span data-stu-id="57040-525">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="57040-526">Wyświetlanie dodatkowych informacji o błędzie w przypadku niepowodzenia polecenia cmdlet z powodu wyjątku StorageException</span><span class="sxs-lookup"><span data-stu-id="57040-526">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="57040-527">Obsługa tworzenia i aktualizowania konta magazynu przy użyciu uwierzytelniania usługi AAD DS w usłudze Azure Files</span><span class="sxs-lookup"><span data-stu-id="57040-527">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="57040-528">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57040-528">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="57040-529">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57040-529">Set-AzStorageAccount</span></span>
* <span data-ttu-id="57040-530">Obsługa wyświetlania listy lub zamykania dojść do plików udziału plików, katalogu plików lub pliku</span><span class="sxs-lookup"><span data-stu-id="57040-530">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="57040-531">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="57040-531">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="57040-532">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="57040-532">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="57040-533">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="57040-533">Az.StorageSync</span></span>
* <span data-ttu-id="57040-534">Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`</span><span class="sxs-lookup"><span data-stu-id="57040-534">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="57040-535">2.3.2 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="57040-535">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="57040-536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-536">Az.Accounts</span></span>
* <span data-ttu-id="57040-537">Usunięto usterkę polegającą na używaniu w niektórych przypadkach niepoprawnego adresu URL w wywołaniach funkcji</span><span class="sxs-lookup"><span data-stu-id="57040-537">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="57040-538">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="57040-538">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="57040-539">Rozwiązano problem z aliasami w poleceniach cmdlet z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="57040-539">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="57040-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="57040-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="57040-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="57040-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-542">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-542">Az.Compute</span></span>
* <span data-ttu-id="57040-543">Proste zestawy parametrów New-AzVm i New-AzVmss akceptują teraz parametr „ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="57040-543">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="57040-544">Poprawiono literówkę w dokumentacji referencyjnej polecenia „New-AzVM”</span><span class="sxs-lookup"><span data-stu-id="57040-544">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="57040-545">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="57040-545">Az.Dns</span></span>
* <span data-ttu-id="57040-546">Poprawiono literówkę w przykładach pomocy polecenia „Set-AzDnsZone”.</span><span class="sxs-lookup"><span data-stu-id="57040-546">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="57040-547">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="57040-547">Az.EventGrid</span></span>
* <span data-ttu-id="57040-548">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="57040-548">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="57040-549">Nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="57040-549">New cmdlets:</span></span>
    - <span data-ttu-id="57040-550">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="57040-550">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="57040-551">Tworzy nową domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="57040-551">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="57040-552">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="57040-552">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="57040-553">Pobiera szczegóły domeny usługi Event Grid lub pobiera listę wszystkich domen usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="57040-553">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="57040-554">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="57040-554">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="57040-555">Usuwa domenę usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="57040-555">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="57040-556">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="57040-556">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="57040-557">Ponownie generuje klucz dostępu współdzielonego dla domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="57040-557">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="57040-558">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="57040-558">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="57040-559">Pobiera klucze dostępu współdzielonego używane do publikowania zdarzeń w domenie usługi Event Grid.</span><span class="sxs-lookup"><span data-stu-id="57040-559">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="57040-560">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="57040-560">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="57040-561">Tworzy nowy temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="57040-561">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="57040-562">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="57040-562">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="57040-563">Pobiera szczegóły tematu domeny usługi Event Grid lub pobiera listę wszystkich tematów domeny usługi Event Grid w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="57040-563">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="57040-564">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="57040-564">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="57040-565">Usuwa istniejący temat domeny usługi Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="57040-565">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="57040-566">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="57040-566">Updated cmdlets:</span></span>
    - <span data-ttu-id="57040-567">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="57040-567">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="57040-568">Dodano nowe wymagane parametry do obsługi przesyłania potokowego nowej domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="57040-568">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="57040-569">Dodano nowe wymagane parametry w celu określenia nowej nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="57040-569">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="57040-570">Dodano nowe zestawy parametrów dla domen i tematów domen, aby umożliwić ponowne używanie istniejących parametrów (np. EndPointType, SubjectBeginsWith itp.).</span><span class="sxs-lookup"><span data-stu-id="57040-570">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="57040-571">Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="57040-571">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="57040-572">Data wygaśnięcia subskrypcji zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="57040-572">Event subscription expiration date,</span></span>
            - <span data-ttu-id="57040-573">Zaawansowane parametry filtrowania.</span><span class="sxs-lookup"><span data-stu-id="57040-573">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="57040-574">Dodano nowe wyliczenie dla elementu servicebusqueue jako miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="57040-574">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="57040-575">Uniemożliwiono użycie elementu „Wszystkie” w opcji -IncludedEventType i zamieniono go na</span><span class="sxs-lookup"><span data-stu-id="57040-575">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="57040-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="57040-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="57040-577">Dodano nowe opcjonalne parametry (Top, ODataQuery i NextLink) w celu obsługi filtrowania i stronicowania wyników.</span><span class="sxs-lookup"><span data-stu-id="57040-577">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="57040-578">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="57040-578">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="57040-579">Dodano nowe wymagane parametry do obsługi przesyłania potokowego domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="57040-579">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="57040-580">Dodano nowe wymagane parametry w celu określenia nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.</span><span class="sxs-lookup"><span data-stu-id="57040-580">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="57040-581">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="57040-581">Az.FrontDoor</span></span>
* <span data-ttu-id="57040-582">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="57040-582">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="57040-583">Dodano obsługę przekształceń i nową wartość autouzupełniania operatora (wyrażenie regularne)</span><span class="sxs-lookup"><span data-stu-id="57040-583">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="57040-584">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="57040-584">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="57040-585">Dodano nowe wartości autouzupełniania</span><span class="sxs-lookup"><span data-stu-id="57040-585">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-586">Az.Network</span></span>
* <span data-ttu-id="57040-587">Dodano obsługę zasobu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="57040-587">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="57040-588">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="57040-588">New cmdlets</span></span>
        - <span data-ttu-id="57040-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="57040-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="57040-590">Dodano element AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="57040-590">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="57040-591">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="57040-591">New cmdlets</span></span>
        - <span data-ttu-id="57040-592">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="57040-592">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="57040-593">Dodano element PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="57040-593">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="57040-594">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="57040-594">New cmdlets</span></span>
        - <span data-ttu-id="57040-595">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="57040-595">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="57040-596">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="57040-596">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="57040-597">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="57040-597">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="57040-598">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="57040-598">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="57040-599">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="57040-599">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="57040-600">Dodano element PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="57040-600">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="57040-601">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="57040-601">New cmdlets</span></span>
        - <span data-ttu-id="57040-602">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="57040-602">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="57040-603">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="57040-603">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="57040-604">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="57040-604">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="57040-605">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="57040-605">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="57040-606">Zaktualizowano poniższe polecenia dla funkcji: Flaga UseLocalAzureIpAddress w elemencie VpnConnection</span><span class="sxs-lookup"><span data-stu-id="57040-606">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="57040-607">Zaktualizowano polecenie New-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="57040-607">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="57040-608">Zaktualizowano polecenie Set-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="57040-608">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="57040-609">Dodano pole tylko do odczytu PeeredConnections w komunikacji równorzędnej usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="57040-609">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="57040-610">Dodano pole tylko do odczytu GlobalReachEnabled w usłudze ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="57040-610">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="57040-611">Dodano atrybut zmiany wywołujący zakończenie obsługi pola AllowGlobalReach w modelu ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="57040-611">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="57040-612">Rozwiązano problem 8756 podczas używania elementu TargetListenerID z poleceniami cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="57040-612">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="57040-613">Usunięto usterkę w poleceniu New-AzApplicationGatewayPathRuleConfig, która uniemożliwiała ustawienie zestawu reguł regenerowania.</span><span class="sxs-lookup"><span data-stu-id="57040-613">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="57040-614">Rozwiązano problem z wyświetlaniem elementu VirtualNetworkTaps w elemencie NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="57040-614">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="57040-615">Naprawiono polecenia cmdlet pobierania Cortex dla listy wszystkich części</span><span class="sxs-lookup"><span data-stu-id="57040-615">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="57040-616">Naprawiono tworzenie odwołań elementu VirtualHub dla elementu ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="57040-616">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="57040-617">Dodano obsługę stref dostępności w elementach AzureFirewall i NatGateway</span><span class="sxs-lookup"><span data-stu-id="57040-617">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="57040-618">Dodano polecenie cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="57040-618">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="57040-619">Dodano obsługę wielu publicznych adresów IP usługi Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="57040-619">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="57040-620">Zaktualizowano polecenie cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="57040-620">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="57040-621">Dodano parametr -PublicIpAddress, który akceptuje co najmniej jeden obiekt publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="57040-621">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="57040-622">Dodano parametr -VirtualNetwork, który akceptuje obiekt sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="57040-622">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="57040-623">Dodano do obiektu zapory metody AddPublicIpAddress i RemovePublicIpAddress, które akceptują obiekt publicznego adresu IP jako dane wejściowe</span><span class="sxs-lookup"><span data-stu-id="57040-623">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="57040-624">Wycofano parametry -PublicIpName i -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="57040-624">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="57040-625">Zaktualizowano poniższe polecenia dla funkcji: Ustawiono w opcjach uwierzytelniania usługi AAD elementu VpnClient zasób bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57040-625">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="57040-626">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="57040-626">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="57040-627">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.</span><span class="sxs-lookup"><span data-stu-id="57040-627">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="57040-628">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr przełącznika RemoveAadAuthentication w celu usunięcia z bramy opcji uwierzytelniania usługi AAD elementu VpnClient.</span><span class="sxs-lookup"><span data-stu-id="57040-628">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="57040-629">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="57040-629">Az.OperationalInsights</span></span>
* <span data-ttu-id="57040-630">Włączono warstwę cenową **pergb2018** w poleceniu „New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="57040-630">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-631">Az.Resources</span></span>
* <span data-ttu-id="57040-632">Obsługa dodatkowych opcji eksportowania szablonu</span><span class="sxs-lookup"><span data-stu-id="57040-632">Support for additional Template Export options</span></span>
    - <span data-ttu-id="57040-633">Dodano parametr „-SkipResourceNameParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="57040-633">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="57040-634">Dodano parametr „-SkipAllParameterization” do polecenia Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="57040-634">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="57040-635">Dodano parametr „-Resource” do polecenia Export-AzResourceGroup w celu filtrowania wyeksportowanych zasobów</span><span class="sxs-lookup"><span data-stu-id="57040-635">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="57040-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="57040-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="57040-637">Usunięto błąd dodawania certyfikatu polegający na pobieraniu przez element ByExistingKeyVault nieprawidłowego odcisku palca w niektórych przypadkach</span><span class="sxs-lookup"><span data-stu-id="57040-637">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-638">Az.Sql</span></span>
* <span data-ttu-id="57040-639">Naprawiono sufiks punktu końcowego magazynu usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="57040-639">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="57040-640">Rozwiązano problem z usługą Advanced Data Security polegający na przesłanianiu zasad usługi Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="57040-640">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="57040-641">Nowe polecenia cmdlet modułu Management.Sql umożliwiające klientom dodawanie kluczy funkcji TDE i ustawianie funkcji ochrony TDE dla wystąpień zarządzanych</span><span class="sxs-lookup"><span data-stu-id="57040-641">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="57040-642">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="57040-642">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="57040-643">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="57040-643">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="57040-644">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="57040-644">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="57040-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="57040-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="57040-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="57040-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="57040-647">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="57040-647">Az.Storage</span></span>
* <span data-ttu-id="57040-648">Obsługa rodzajów FileStorage i SkuName Premium_ZRS podczas tworzenia konta magazynu</span><span class="sxs-lookup"><span data-stu-id="57040-648">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="57040-649">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57040-649">New-AzStorageAccount</span></span>
* <span data-ttu-id="57040-650">Opis z wyjaśnieniem polecenia cmdlet niezmienności obiektów blob</span><span class="sxs-lookup"><span data-stu-id="57040-650">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="57040-651">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="57040-651">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="57040-652">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="57040-652">Az.Websites</span></span>
* <span data-ttu-id="57040-653">Optymalizuje polecenie Get-AzWebAppCertificate w celu filtrowania według grupy zasobów na serwerze zamiast na kliencie</span><span class="sxs-lookup"><span data-stu-id="57040-653">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="57040-654">Dodano parametr przełącznika -UseDisasterRecovery do polecenia Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="57040-654">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="57040-655">2.2.0 — czerwiec 2019 r.</span><span class="sxs-lookup"><span data-stu-id="57040-655">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="57040-656">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="57040-656">Az.Cdn</span></span>
* <span data-ttu-id="57040-657">Zaktualizowano polecenia cmdlet do obsługi funkcji rulesEngine na podstawie interfejsu API w wersji 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="57040-657">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-658">Az.Compute</span></span>
* <span data-ttu-id="57040-659">Dodano parametr `NoWait`, który powoduje rozpoczęcie operacji i natychmiastowy powrót, bez czekania na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="57040-659">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="57040-660">Zaktualizowano następujące polecenia cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="57040-660">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="57040-661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="57040-661">Az.EventHub</span></span>
* <span data-ttu-id="57040-662">Poprawka błędu #9231 — polecenie Get-AzEventHubNamespace nie zwraca tagów</span><span class="sxs-lookup"><span data-stu-id="57040-662">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="57040-663">Poprawka błędu #9230 — polecenie Get-AzEventHubNamespace zwraca wartość ResourceGroup zamiast wartości ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57040-663">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-664">Az.Network</span></span>
* <span data-ttu-id="57040-665">Aktualizowanie wartości ResourceId i InputObject dla bramy translatora adresów sieciowych</span><span class="sxs-lookup"><span data-stu-id="57040-665">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="57040-666">Dodawanie aliasów dla wartości ResourceId i InputObject</span><span class="sxs-lookup"><span data-stu-id="57040-666">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="57040-667">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="57040-667">Az.PolicyInsights</span></span>
* <span data-ttu-id="57040-668">Rozwiązanie problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="57040-668">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="57040-669">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="57040-669">Az.RecoveryServices</span></span>
* <span data-ttu-id="57040-670">Minimalny czas przechowywania zasad IaaSVM w dniach zmieniono z 7 na 1</span><span class="sxs-lookup"><span data-stu-id="57040-670">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="57040-671">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="57040-671">Az.ServiceBus</span></span>
* <span data-ttu-id="57040-672">Rozwiązanie problemu #9182 — Get-AzServiceBusNamespace zwraca wartość ResourceGroup zamiast ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57040-672">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="57040-673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="57040-673">Az.ServiceFabric</span></span>
* <span data-ttu-id="57040-674">Poprawienie błędu pisowni w komunikacie o błędzie polecenia „Update-AzServiceFabricReliability”</span><span class="sxs-lookup"><span data-stu-id="57040-674">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="57040-675">Poprawienie brakującego znaku w wierszach polecenia usługi Service Fabric</span><span class="sxs-lookup"><span data-stu-id="57040-675">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-676">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-676">Az.Sql</span></span>
* <span data-ttu-id="57040-677">Dodanie parametru DnsZonePartner dla polecenia cmdlet New-AzureSqlInstance w celu obsługi funkcji AutoDr dla wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="57040-677">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="57040-678">Wycofanie polecenia cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="57040-678">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="57040-679">Zmiana nazwy poleceń cmdlet z Wykrywanie zagrożeń na Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="57040-679">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="57040-680">Parametry New-AzSqlInstance -StorageSizeInGB i -LicenseType są teraz opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="57040-680">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="57040-681">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="57040-681">Az.Websites</span></span>
* <span data-ttu-id="57040-682">Rozwiązanie problemu polegającego na tym, że użycie poleceń Set-AzWebApp i Set-AzWebAppSlot z właściwością -WebApp powodowało usunięcie tagów</span><span class="sxs-lookup"><span data-stu-id="57040-682">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="57040-683">2.1.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="57040-683">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="57040-684">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="57040-684">Az.ApiManagement</span></span>
* <span data-ttu-id="57040-685">Utworzono nowe polecenia cmdlet do zarządzania diagnostyką w zakresie globalnym i interfejsu API</span><span class="sxs-lookup"><span data-stu-id="57040-685">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="57040-686">**Get-AzApiManagementDiagnostic** — uzyskiwanie diagnostyki skonfigurowanej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="57040-686">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="57040-687">**New-AzApiManagementDiagnostic** — tworzenie nowej diagnostyki w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="57040-687">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="57040-688">**New-AzApiManagementHttpMessageDiagnostic** — tworzenie ustawienia diagnostyki określającego nagłówki do rejestrowania i rozmiar treści w bajtach</span><span class="sxs-lookup"><span data-stu-id="57040-688">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="57040-689">**New-AzApiManagementPipelineDiagnosticSetting** — tworzenie ustawień diagnostyki dla przychodzących/wychodzących komunikatów HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="57040-689">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="57040-690">**New-AzApiManagementSamplingSetting** — tworzenie ustawienia próbkowania dla żądań i odpowiedzi na potrzeby diagnostyki</span><span class="sxs-lookup"><span data-stu-id="57040-690">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="57040-691">**Remove-AzApiManagementDiagnostic** — usuwanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="57040-691">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="57040-692">**Set-AzApiManagementDiagnostic** — aktualizowanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API</span><span class="sxs-lookup"><span data-stu-id="57040-692">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="57040-693">Utworzono nowe polecenia cmdlet do zarządzania pamięcią podręczną usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="57040-693">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="57040-694">**Get-AzApiManagementCache** — uzyskiwanie szczegółów pamięci podręcznej określonej przez identyfikator lub wszystkich pamięci podręcznych</span><span class="sxs-lookup"><span data-stu-id="57040-694">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="57040-695">**New-AzApiManagementCache** — tworzenie nowej, „domyślnej” pamięci podręcznej lub pamięci podręcznej w konkretnym „regionie” platformy Azure</span><span class="sxs-lookup"><span data-stu-id="57040-695">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="57040-696">**Remove-AzApiManagementCache** — usuwanie pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="57040-696">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="57040-697">**Update-AzApiManagementCache** — aktualizacja pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="57040-697">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="57040-698">Utworzono nowe polecenia cmdlet do zarządzania schematem interfejsu API</span><span class="sxs-lookup"><span data-stu-id="57040-698">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="57040-699">**New-AzApiManagementSchema** — tworzenie nowego schematu dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="57040-699">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="57040-700">**Get-AzApiManagementSchema** — pobieranie schematów skonfigurowanych w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="57040-700">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="57040-701">**Remove-AzApiManagementSchema** — usuwanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="57040-701">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="57040-702">**Set-AzApiManagementSchema** — aktualizowanie schematu skonfigurowanego w interfejsie API</span><span class="sxs-lookup"><span data-stu-id="57040-702">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="57040-703">Utworzono nowe polecenie cmdlet do generowania tokenu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="57040-703">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="57040-704">**New-AzApiManagementUserToken** — generowanie nowego tokenu użytkownika ważnego domyślnie przez 8 godzin. Za pomocą tego polecenia cmdlet można wygenerować token dla użytkownika „GIT”.</span><span class="sxs-lookup"><span data-stu-id="57040-704">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="57040-705">Utworzono nowe polecenie cmdlet do pobierania stanu sieci.</span><span class="sxs-lookup"><span data-stu-id="57040-705">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="57040-706">**Get-AzApiManagementNetworkStatus** — uzyskiwanie stanu sieci dla łączności z zasobami, od których zależy usługa API Management.</span><span class="sxs-lookup"><span data-stu-id="57040-706">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="57040-707">Jest to przydatne w przypadku wdrażania usługi ApiManagement w sieci wirtualnej i weryfikacji, czy któreś z zależności są uszkodzone.</span><span class="sxs-lookup"><span data-stu-id="57040-707">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="57040-708">Zaktualizowano polecenie cmdlet **New-AzApiManagement** do zarządzania usługą ApiManagement</span><span class="sxs-lookup"><span data-stu-id="57040-708">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="57040-709">Dodano obsługę nowych jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="57040-709">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="57040-710">Dodano obsługę włączania flagi „EnableClientCertificate” dla jednostek SKU „Zużycie”</span><span class="sxs-lookup"><span data-stu-id="57040-710">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="57040-711">Nowe polecenie cmdlet **New-AzApiManagementSslSetting** umożliwia skonfigurowanie ustawienia „TLS/SSL” na „Zaplecze” i „Fronton”.</span><span class="sxs-lookup"><span data-stu-id="57040-711">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="57040-712">Za jego pomocą można też skonfigurować szyfrowanie, takie jak „3DES”, i protokoły serwera, takie jak „Http2”we frontonie usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="57040-712">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="57040-713">Dodano obsługę konfigurowania nazwy hosta „DeveloperPortal” usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="57040-713">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="57040-714">Zaktualizowano polecenia cmdlet **Get-AzApiManagementSsoToken**, aby przyjmowały jako wejście obiekt „PsApiManagement”</span><span class="sxs-lookup"><span data-stu-id="57040-714">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="57040-715">Zaktualizowano polecenie cmdlet, aby wyświetlało komunikaty o błędach śródwierszowo</span><span class="sxs-lookup"><span data-stu-id="57040-715">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="57040-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Kod błędu: Komunikat o błędzie ValidationError: Co najmniej jedno pole zawiera nieprawidłową wartość: Szczegóły błędu:    [Code=ValidationError, Message=Błąd w elemencie „log-to-eventhub” w wierszu 3, kolumna 10: Nie znaleziono rejestratora, element docelowy=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="57040-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="57040-717">Zaktualizowano polecenie cmdlet **Export-AzApiManagementApi** tak, aby eksportowało interfejsy API w formacie „OpenApi 3.0”</span><span class="sxs-lookup"><span data-stu-id="57040-717">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="57040-718">Zaktualizowano polecenie cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="57040-718">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="57040-719">W celu importowania interfejsu Api z dokumentu ze specyfikacją interfejsu „OpenApi 3.0”.</span><span class="sxs-lookup"><span data-stu-id="57040-719">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="57040-720">W celu przesłonięcia właściwości „PsApiManagementSchema” określonej w dowolnym dokumencie („Swagger”, „Wadl”, „Wsdl”, „OpenApi”).</span><span class="sxs-lookup"><span data-stu-id="57040-720">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="57040-721">W celu przesłonięcia właściwości „ServiceUrl” określonej w dowolnym dokumencie.</span><span class="sxs-lookup"><span data-stu-id="57040-721">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="57040-722">Zaktualizowano polecenie cmdlet **Get-AzApiManagementPolicy** tak, aby zwracało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml”</span><span class="sxs-lookup"><span data-stu-id="57040-722">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="57040-723">Zaktualizowano polecenie cmdlet **Set-AzApiManagementPolicy** tak, aby akceptowało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml” i ze zmianą znaczenia Xml przy użyciu formatu „xml”</span><span class="sxs-lookup"><span data-stu-id="57040-723">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="57040-724">Zaktualizowano polecenie cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="57040-724">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="57040-725">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="57040-725">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="57040-726">W celu utworzenia interfejsu API we właściwości ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="57040-726">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="57040-727">W celu sklonowania interfejsu API przy użyciu właściwości „SourceApiId” i „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="57040-727">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="57040-728">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="57040-728">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="57040-729">Zaktualizowano polecenie cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="57040-729">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="57040-730">W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.</span><span class="sxs-lookup"><span data-stu-id="57040-730">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="57040-731">W celu zaktualizowania interfejsu API we właściwości „ApiVersionSet”.</span><span class="sxs-lookup"><span data-stu-id="57040-731">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="57040-732">Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="57040-732">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="57040-733">Zaktualizowano polecenie cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="57040-733">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="57040-734">W celu klonowania (kopiowanie tagów, produktów, operacji i zasad) istniejącej wersji przy użyciu właściwości „SourceApiRevision”.</span><span class="sxs-lookup"><span data-stu-id="57040-734">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="57040-735">Dla nowej wersji przyjmowana jest wartość „ApiId” elementu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="57040-735">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="57040-736">W celu dostarczenia właściwości „ApiRevisionDescription”.</span><span class="sxs-lookup"><span data-stu-id="57040-736">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="57040-737">W celu przesłonięcia właściwości „ServiceUrl” podczas klonowania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="57040-737">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="57040-738">Zaktualizowano polecenie cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="57040-738">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="57040-739">W celu skonfigurowania właściwości „AAD” lub „AADB2C” za pomocą właściwości „Authority”.</span><span class="sxs-lookup"><span data-stu-id="57040-739">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="57040-740">W celu skonfigurowania właściwości „SignupPolicy”, „SigninPolicy”, „ProfileEditingPolicy” i „PasswordResetPolicy”.</span><span class="sxs-lookup"><span data-stu-id="57040-740">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="57040-741">Zaktualizowano polecenie cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="57040-741">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="57040-742">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="57040-742">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="57040-743">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="57040-743">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="57040-744">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="57040-744">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="57040-745">Zaktualizowano polecenie cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="57040-745">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="57040-746">W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="57040-746">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="57040-747">W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.</span><span class="sxs-lookup"><span data-stu-id="57040-747">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="57040-748">Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="57040-748">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="57040-749">Zaktualizowano następujące polecenia cmdlet do akceptowania właściwości „ResourceId” jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="57040-749">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="57040-750">„New-AzApiManagementContext”</span><span class="sxs-lookup"><span data-stu-id="57040-750">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="57040-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="57040-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="57040-752">„Get-AzApiManagementApiRelease”</span><span class="sxs-lookup"><span data-stu-id="57040-752">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="57040-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="57040-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="57040-754">„Get-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="57040-754">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="57040-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="57040-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="57040-756">„Get-AzApiManagementAuthorizationServer”</span><span class="sxs-lookup"><span data-stu-id="57040-756">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="57040-757">„Get-AzApiManagementBackend”</span><span class="sxs-lookup"><span data-stu-id="57040-757">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="57040-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="57040-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="57040-759">„Get-AzApiManagementCertificate”</span><span class="sxs-lookup"><span data-stu-id="57040-759">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="57040-760">„Remove-AzApiManagementApiVersionSet”</span><span class="sxs-lookup"><span data-stu-id="57040-760">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="57040-761">„Remove-AzApiManagementSubscription”</span><span class="sxs-lookup"><span data-stu-id="57040-761">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="57040-762">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="57040-762">Az.Automation</span></span>
* <span data-ttu-id="57040-763">Zaktualizowano polecenie Get-AzAutomationJobOutputRecord tak, aby obsługiwało wartości rekordów w postaci kodu JSON i tekstowej.</span><span class="sxs-lookup"><span data-stu-id="57040-763">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="57040-764">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="57040-764">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="57040-765">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="57040-765">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="57040-766">Zmieniono działanie polecenia Start-AzAutomationDscCompilationJob tak, aby tylko uruchamiało zadanie zamiast czekać na jego zakończenie.</span><span class="sxs-lookup"><span data-stu-id="57040-766">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="57040-767">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="57040-767">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="57040-768">Poprawka dla polecenia Get-AzAutomationDscNode podczas używania opcji -Name zwraca wszystkie węzły.</span><span class="sxs-lookup"><span data-stu-id="57040-768">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="57040-769">Teraz zwraca tylko pasujące węzły.</span><span class="sxs-lookup"><span data-stu-id="57040-769">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-770">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-770">Az.Compute</span></span>
* <span data-ttu-id="57040-771">Dodanie parametrów ProtectFromScaleIn i ProtectFromScaleSetAction do polecenia cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="57040-771">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="57040-772">Nowy zestaw parametrów New-AzVM wimple teraz używa domyślnie dostępnej lokalizacji, jeśli region „Wschodnie stany USA” nie jest obsługiwany.</span><span class="sxs-lookup"><span data-stu-id="57040-772">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="57040-773">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="57040-773">Az.DataLakeStore</span></span>
* <span data-ttu-id="57040-774">Aktualizacja zestawu ADLS SDK do korzystania z klienta httpclient, integrowanie testowania płaszczyzny danych z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="57040-774">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="57040-775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="57040-775">Az.Monitor</span></span>
* <span data-ttu-id="57040-776">Naprawiono nieprawidłowe nazwy parametrów w przykładach pomocy</span><span class="sxs-lookup"><span data-stu-id="57040-776">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-777">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-777">Az.Network</span></span>
* <span data-ttu-id="57040-778">Dodanie flagi DisableBgpRoutePropagation do danych wyjściowych obowiązującej tabeli routingu</span><span class="sxs-lookup"><span data-stu-id="57040-778">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="57040-779">Zaktualizowano polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="57040-779">Updated cmdlet:</span></span>
        - <span data-ttu-id="57040-780">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="57040-780">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="57040-781">Poprawienie podwójnego łącznika w dokumentacji polecenia New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="57040-781">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-782">Az.Resources</span></span>
* <span data-ttu-id="57040-783">Dodanie nowego polecenia cmdlet Get-AzureRmDenyAssignment do pobierania przypisań odmowy</span><span class="sxs-lookup"><span data-stu-id="57040-783">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-784">Az.Sql</span></span>
* <span data-ttu-id="57040-785">Zmiana nazwy poleceń cmdlet usługi Advanced Threat Protection na Advanced Data Security i domyślne włączenie oceny luk w zabezpieczeniach</span><span class="sxs-lookup"><span data-stu-id="57040-785">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="57040-786">2.0.0 — maj 2019 r.</span><span class="sxs-lookup"><span data-stu-id="57040-786">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="57040-787">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-787">Az.Accounts</span></span>
* <span data-ttu-id="57040-788">Aktualizacja biblioteki uwierzytelniania w celu rozwiązania problemów z usługą ADFS dotyczących uwierzytelniania nazwy użytkownika i hasła</span><span class="sxs-lookup"><span data-stu-id="57040-788">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="57040-789">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="57040-789">Az.CognitiveServices</span></span>
* <span data-ttu-id="57040-790">Dla usług wyszukiwania Bing wyświetlane jest tylko zrzeczenie odpowiedzialności usługi Bing.</span><span class="sxs-lookup"><span data-stu-id="57040-790">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="57040-791">Naprawiono błąd polegający na niepomyślnym tworzeniu konta.</span><span class="sxs-lookup"><span data-stu-id="57040-791">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-792">Az.Compute</span></span>
* <span data-ttu-id="57040-793">Funkcja Grupa umieszczania w pobliżu.</span><span class="sxs-lookup"><span data-stu-id="57040-793">Proximity placement group feature.</span></span>
    - <span data-ttu-id="57040-794">Dodano następujące nowe polecenia cmdlet:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="57040-794">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="57040-795">Do następujących poleceń cmdlet dodano nowy parametr ProximityPlacementGroupId:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="57040-795">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="57040-796">Do polecenia New-AzGalleryImageVersion dodano parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="57040-796">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="57040-797">Właściwość TargetRegion polecenia New-AzGalleryImageVersion może zawierać parametr StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="57040-797">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="57040-798">Do poleceń Stop-AzVM i Stop-AzVmss dodano parametr przełącznika SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="57040-798">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="57040-799">Zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="57040-799">Breaking changes</span></span>
    - <span data-ttu-id="57040-800">Polecenie Set-AzVMBootDiagnostics zamieniono na polecenie Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="57040-800">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="57040-801">Polecenie Export-AzLogAnalyticThrottledRequests zamieniono na polecenie Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="57040-801">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="57040-802">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="57040-802">Az.DeploymentManager</span></span>
* <span data-ttu-id="57040-803">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="57040-803">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="57040-804">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="57040-804">Az.Dns</span></span>
* <span data-ttu-id="57040-805">Automatyczne delegowanie serwera nazw systemu DNS</span><span class="sxs-lookup"><span data-stu-id="57040-805">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="57040-806">Polecenie cmdlet tworzenia strefy DNS akceptuje nazwę strefy nadrzędnej jako dodatkowy parametr opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="57040-806">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="57040-807">Dodaje rekordy serwera nazw w strefie nadrzędnej dla nowo utworzonej strefy podrzędnej.</span><span class="sxs-lookup"><span data-stu-id="57040-807">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="57040-808">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="57040-808">Az.FrontDoor</span></span>
* <span data-ttu-id="57040-809">Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="57040-809">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="57040-810">Zmiana nazw poleceń cmdlet zapory aplikacji internetowej w celu dołączenia ciągu „Waf”</span><span class="sxs-lookup"><span data-stu-id="57040-810">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="57040-811">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="57040-811">Az.HDInsight</span></span>
* <span data-ttu-id="57040-812">Usunięto dwa polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="57040-812">Removed two cmdlets:</span></span>
    - <span data-ttu-id="57040-813">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="57040-813">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="57040-814">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="57040-814">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="57040-815">Dodano nowe polecenie cmdlet Set-AzHDInsightGatewayCredential w celu zastąpienia polecenia Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="57040-815">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="57040-816">Zaktualizowano polecenie cmdlet Get-AzHDInsightJobOutput, aby rozróżnić rolę czytelnika i rolę operatora usługi HDInsight:</span><span class="sxs-lookup"><span data-stu-id="57040-816">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="57040-817">Użytkownicy z rolą czytelnika muszą jawnie określić parametr „DefaultStorageAccountKey” — w przeciwnym razie wystąpi błąd.</span><span class="sxs-lookup"><span data-stu-id="57040-817">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="57040-818">Nie będzie to miało wpływu na użytkowników z rolą operatora usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="57040-818">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="57040-819">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="57040-819">Az.Monitor</span></span>
* <span data-ttu-id="57040-820">Nowe polecenia cmdlet dla interfejsu API SQR (Scheduled Query Rule, reguła zaplanowanego zapytania)</span><span class="sxs-lookup"><span data-stu-id="57040-820">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="57040-821">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="57040-821">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="57040-822">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="57040-822">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="57040-823">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="57040-823">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="57040-824">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="57040-824">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="57040-825">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="57040-825">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="57040-826">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="57040-826">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="57040-827">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="57040-827">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="57040-828">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="57040-828">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="57040-829">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="57040-829">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="57040-830">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="57040-830">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="57040-831">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="57040-831">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="57040-832">[Więcej](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informacji na temat interfejsu API SQR</span><span class="sxs-lookup"><span data-stu-id="57040-832">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="57040-833">Zaktualizowano plik Az.Monitor.md w celu uwzględnienia poleceń cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="57040-833">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-834">Az.Network</span></span>
* <span data-ttu-id="57040-835">Dodano obsługę dla zasobu usługi NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="57040-835">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="57040-836">Nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="57040-836">New cmdlets</span></span>
        - <span data-ttu-id="57040-837">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="57040-837">New-AzNatGateway</span></span>
        - <span data-ttu-id="57040-838">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="57040-838">Get-AzNatGateway</span></span>
        - <span data-ttu-id="57040-839">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="57040-839">Set-AzNatGateway</span></span>
        - <span data-ttu-id="57040-840">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="57040-840">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="57040-841">Zaktualizowano następujące polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="57040-841">Updated cmdlets</span></span>
        - <span data-ttu-id="57040-842">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="57040-842">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="57040-843">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="57040-843">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="57040-844">Zaktualizowano poniższe polecenia dla funkcji: Ustawianie/usuwanie tras niestandardowych dla bramy Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="57040-844">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="57040-845">Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="57040-845">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="57040-846">Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.</span><span class="sxs-lookup"><span data-stu-id="57040-846">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="57040-847">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="57040-847">Az.PolicyInsights</span></span>
* <span data-ttu-id="57040-848">Obsługa zapytań dotyczących szczegółów oceny zasad.</span><span class="sxs-lookup"><span data-stu-id="57040-848">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="57040-849">Dodano parametr „-Expand” do polecenia Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="57040-849">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="57040-850">Obsługa polecenia „-Expand PolicyEvaluationDetails”.</span><span class="sxs-lookup"><span data-stu-id="57040-850">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="57040-851">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="57040-851">Az.RecoveryServices</span></span>
* <span data-ttu-id="57040-852">Obsługa odzyskiwania lokacji między subskrypcjami z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="57040-852">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="57040-853">Oznaczanie nadchodzących zmian powodujących niezgodność dla usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="57040-853">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="57040-854">Poprawka zakończenia planu akcji dla planu odzyskiwania usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="57040-854">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="57040-855">Poprawka aktualizacji mapowania sieci usługi Azure Site Recovery z platformy Azure na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="57040-855">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="57040-856">Poprawka aktualizacji kierunku ochrony usługi Azure Site Recovery z platformy Azure na platformę Azure dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="57040-856">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="57040-857">Inne drobne poprawki.</span><span class="sxs-lookup"><span data-stu-id="57040-857">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="57040-858">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="57040-858">Az.Relay</span></span>
* <span data-ttu-id="57040-859">Poprawiono błędy pisowni w komunikatach przeznaczonych dla klientów</span><span class="sxs-lookup"><span data-stu-id="57040-859">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="57040-860">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="57040-860">Az.ServiceBus</span></span>
* <span data-ttu-id="57040-861">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="57040-861">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="57040-862">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="57040-862">Az.Storage</span></span>
* <span data-ttu-id="57040-863">Uaktualnienie biblioteki klienta usługi Storage do wersji 10.0.1 (przestrzeń nazw wszystkich obiektów tego zestawu SDK została zmieniona z „Microsoft.WindowsAzure.Storage. *” na „Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="57040-863">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="57040-864">Uaktualnienie do wersji Microsoft.Azure.Management.Storage 11.0.0 w celu obsługi nowego interfejsu API w wersji 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="57040-864">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="57040-865">Domyślny rodzaj konta magazynu w poleceniu Utwórz konto magazynu został zmieniony ze „Storage” na „StorageV2”</span><span class="sxs-lookup"><span data-stu-id="57040-865">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="57040-866">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57040-866">New-AzStorageAccount</span></span>
* <span data-ttu-id="57040-867">Zmiana wyjściowego parametru Sku.Name polecenia cmdlet konta magazynu w celu wyrównania z wejściowym parametrem SkuName przez dodanie znaku „-”, na przykład zmiana „StandardLRS” na „Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="57040-867">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="57040-868">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57040-868">New-AzStorageAccount</span></span>
    - <span data-ttu-id="57040-869">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57040-869">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="57040-870">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57040-870">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="57040-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="57040-871">Az.Websites</span></span>
* <span data-ttu-id="57040-872">Właściwość „Kind” będzie teraz ustawiona dla obiektów PSSite zwracanych przez polecenie Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="57040-872">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="57040-873">Polecenia Get-AzWebApp\*Metrics i Get-AzAppServicePlanMetrics oznaczono jako przestarzałe</span><span class="sxs-lookup"><span data-stu-id="57040-873">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="57040-874">1.8.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="57040-874">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="57040-875">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="57040-875">Highlights since the last major release</span></span>
* <span data-ttu-id="57040-876">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="57040-876">General availability of `Az` module</span></span>
* <span data-ttu-id="57040-877">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="57040-877">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="57040-878">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="57040-878">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="57040-879">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-879">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="57040-880">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="57040-880">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="57040-881">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="57040-881">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="57040-882">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="57040-882">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="57040-883">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-883">Az.Accounts</span></span>
* <span data-ttu-id="57040-884">Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac</span><span class="sxs-lookup"><span data-stu-id="57040-884">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="57040-885">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="57040-885">Az.Batch</span></span>
* <span data-ttu-id="57040-886">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-886">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="57040-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="57040-887">Az.Cdn</span></span>
* <span data-ttu-id="57040-888">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-888">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="57040-889">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="57040-889">Az.CognitiveServices</span></span>
* <span data-ttu-id="57040-890">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-891">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-891">Az.Compute</span></span>
* <span data-ttu-id="57040-892">Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu</span><span class="sxs-lookup"><span data-stu-id="57040-892">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="57040-893">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-893">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="57040-894">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="57040-894">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="57040-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="57040-895">Az.DataFactory</span></span>
* <span data-ttu-id="57040-896">Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="57040-896">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="57040-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="57040-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="57040-898">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-898">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="57040-899">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="57040-899">Az.EventGrid</span></span>
* <span data-ttu-id="57040-900">Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="57040-900">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="57040-901">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="57040-901">Az.EventHub</span></span>
* <span data-ttu-id="57040-902">Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="57040-902">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="57040-903">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="57040-903">Az.HDInsight</span></span>
* <span data-ttu-id="57040-904">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-904">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="57040-905">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="57040-905">Az.IotHub</span></span>
* <span data-ttu-id="57040-906">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-906">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="57040-907">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="57040-907">Az.KeyVault</span></span>
* <span data-ttu-id="57040-908">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="57040-909">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="57040-909">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="57040-910">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="57040-910">Az.MachineLearning</span></span>
* <span data-ttu-id="57040-911">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="57040-912">Az.Media</span><span class="sxs-lookup"><span data-stu-id="57040-912">Az.Media</span></span>
* <span data-ttu-id="57040-913">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-913">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="57040-914">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="57040-914">Az.Monitor</span></span>
  * <span data-ttu-id="57040-915">Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)</span><span class="sxs-lookup"><span data-stu-id="57040-915">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="57040-916">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="57040-916">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="57040-917">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="57040-917">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="57040-918">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="57040-918">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="57040-919">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="57040-919">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="57040-920">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="57040-920">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="57040-921">Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="57040-921">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-922">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-922">Az.Network</span></span>
* <span data-ttu-id="57040-923">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="57040-924">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="57040-924">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="57040-925">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="57040-925">Az.NotificationHubs</span></span>
* <span data-ttu-id="57040-926">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="57040-927">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="57040-927">Az.OperationalInsights</span></span>
* <span data-ttu-id="57040-928">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-928">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="57040-929">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="57040-929">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="57040-930">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-930">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="57040-931">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="57040-931">Az.RecoveryServices</span></span>
* <span data-ttu-id="57040-932">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-932">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="57040-933">Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="57040-933">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="57040-934">Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="57040-934">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="57040-935">Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową</span><span class="sxs-lookup"><span data-stu-id="57040-935">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="57040-936">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="57040-936">Az.RedisCache</span></span>
* <span data-ttu-id="57040-937">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-937">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-938">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-938">Az.Resources</span></span>
* <span data-ttu-id="57040-939">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="57040-939">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-940">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-940">Az.Sql</span></span>
* <span data-ttu-id="57040-941">Zamiana zależności od zestawu Monitor SDK na typowy kod</span><span class="sxs-lookup"><span data-stu-id="57040-941">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="57040-942">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-942">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="57040-943">Rozszerzony proces klasyfikowania wielu kolumn.</span><span class="sxs-lookup"><span data-stu-id="57040-943">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="57040-944">Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.</span><span class="sxs-lookup"><span data-stu-id="57040-944">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="57040-945">Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.</span><span class="sxs-lookup"><span data-stu-id="57040-945">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="57040-946">Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="57040-946">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="57040-947">Poprawiono informacje o symbolach wieloznacznych w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="57040-947">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="57040-948">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="57040-948">Az.Websites</span></span>
* <span data-ttu-id="57040-949">Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu</span><span class="sxs-lookup"><span data-stu-id="57040-949">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="57040-950">Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="57040-950">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="57040-951">Zaktualizowano zestaw WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="57040-951">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="57040-952">Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="57040-952">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="57040-953">1.7.0 — kwiecień 2019 r.</span><span class="sxs-lookup"><span data-stu-id="57040-953">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="57040-954">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="57040-954">Highlights since the last major release</span></span>
* <span data-ttu-id="57040-955">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="57040-955">General availability of `Az` module</span></span>
* <span data-ttu-id="57040-956">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="57040-956">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="57040-957">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="57040-957">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="57040-958">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-958">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="57040-959">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="57040-959">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="57040-960">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="57040-960">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="57040-961">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="57040-961">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="57040-962">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-962">Az.Accounts</span></span>
* <span data-ttu-id="57040-963">Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="57040-963">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="57040-964">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="57040-964">Az.AnalysisServices</span></span>
* <span data-ttu-id="57040-965">Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="57040-965">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="57040-966">Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność</span><span class="sxs-lookup"><span data-stu-id="57040-966">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="57040-967">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="57040-967">Az.Automation</span></span>
* <span data-ttu-id="57040-968">Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień.</span><span class="sxs-lookup"><span data-stu-id="57040-968">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="57040-969">Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.</span><span class="sxs-lookup"><span data-stu-id="57040-969">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="57040-970">Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="57040-970">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-971">Az.Compute</span></span>
* <span data-ttu-id="57040-972">Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="57040-972">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="57040-973">Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="57040-973">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="57040-974">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="57040-974">Az.ContainerInstance</span></span>
* <span data-ttu-id="57040-975">Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego</span><span class="sxs-lookup"><span data-stu-id="57040-975">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="57040-976">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="57040-976">Az.DataFactory</span></span>
* <span data-ttu-id="57040-977">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2</span><span class="sxs-lookup"><span data-stu-id="57040-977">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="57040-978">Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="57040-978">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-979">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-979">Az.Resources</span></span>
* <span data-ttu-id="57040-980">Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="57040-980">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="57040-981">Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="57040-981">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="57040-982">Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia</span><span class="sxs-lookup"><span data-stu-id="57040-982">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="57040-983">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="57040-983">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="57040-984">Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań</span><span class="sxs-lookup"><span data-stu-id="57040-984">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="57040-985">Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="57040-985">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-986">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-986">Az.Sql</span></span>
* <span data-ttu-id="57040-987">Dodano obsługę klasyfikacji danych bazy danych.</span><span class="sxs-lookup"><span data-stu-id="57040-987">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="57040-988">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="57040-988">Az.Storage</span></span>
* <span data-ttu-id="57040-989">Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="57040-989">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="57040-990">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="57040-990">New-AzStorageContext</span></span>
* <span data-ttu-id="57040-991">Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania</span><span class="sxs-lookup"><span data-stu-id="57040-991">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="57040-992">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="57040-992">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="57040-993">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="57040-993">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="57040-994">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="57040-994">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="57040-995">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="57040-995">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="57040-996">Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików</span><span class="sxs-lookup"><span data-stu-id="57040-996">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="57040-997">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="57040-997">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="57040-998">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="57040-998">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="57040-999">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="57040-999">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="57040-1000">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="57040-1000">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="57040-1001">1.6.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="57040-1001">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="57040-1002">Najważniejsze zmiany od ostatniej wersji głównej</span><span class="sxs-lookup"><span data-stu-id="57040-1002">Highlights since the last major release</span></span>
* <span data-ttu-id="57040-1003">Ogólna dostępność modułu `Az`</span><span class="sxs-lookup"><span data-stu-id="57040-1003">General availability of `Az` module</span></span>
* <span data-ttu-id="57040-1004">Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="57040-1004">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="57040-1005">Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="57040-1005">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="57040-1006">Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-1006">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="57040-1007">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="57040-1007">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="57040-1008">Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation</span><span class="sxs-lookup"><span data-stu-id="57040-1008">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="57040-1009">Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="57040-1009">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="57040-1010">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="57040-1010">Az.Automation</span></span>
* <span data-ttu-id="57040-1011">Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:</span><span class="sxs-lookup"><span data-stu-id="57040-1011">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="57040-1012">Grupowanie dynamiczne</span><span class="sxs-lookup"><span data-stu-id="57040-1012">Dynamic grouping</span></span>
    * <span data-ttu-id="57040-1013">Działania przed napisaniem skryptu i po napisaniu skryptu</span><span class="sxs-lookup"><span data-stu-id="57040-1013">Pre-Post script</span></span>
    * <span data-ttu-id="57040-1014">Ustawienie ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="57040-1014">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-1015">Az.Compute</span></span>
* <span data-ttu-id="57040-1016">Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="57040-1016">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="57040-1017">Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="57040-1017">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="57040-1018">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="57040-1018">Az.KeyVault</span></span>
* <span data-ttu-id="57040-1019">Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault</span><span class="sxs-lookup"><span data-stu-id="57040-1019">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-1020">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-1020">Az.Network</span></span>
* <span data-ttu-id="57040-1021">Dodano obsługę analizy zagrożeń w usłudze Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="57040-1021">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="57040-1022">Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe</span><span class="sxs-lookup"><span data-stu-id="57040-1022">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="57040-1023">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="57040-1023">Az.RecoveryServices</span></span>
* <span data-ttu-id="57040-1024">Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP</span><span class="sxs-lookup"><span data-stu-id="57040-1024">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="57040-1025">Dodano obsługę potoków do wyrejestrowania kontenera</span><span class="sxs-lookup"><span data-stu-id="57040-1025">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-1026">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-1026">Az.Resources</span></span>
* <span data-ttu-id="57040-1027">Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="57040-1027">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="57040-1028">Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM</span><span class="sxs-lookup"><span data-stu-id="57040-1028">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-1029">Az.Sql</span></span>
* <span data-ttu-id="57040-1030">Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.</span><span class="sxs-lookup"><span data-stu-id="57040-1030">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="57040-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="57040-1031">Az.Storage</span></span>
* <span data-ttu-id="57040-1032">Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="57040-1032">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="57040-1033">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="57040-1033">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="57040-1034">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="57040-1034">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="57040-1035">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="57040-1035">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="57040-1036">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="57040-1036">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="57040-1037">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="57040-1037">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="57040-1038">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="57040-1038">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="57040-1039">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="57040-1039">Az.Websites</span></span>
* <span data-ttu-id="57040-1040">Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="57040-1040">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="57040-1041">1.5.0 — marzec 2019</span><span class="sxs-lookup"><span data-stu-id="57040-1041">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="57040-1042">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-1042">Az.Accounts</span></span>
* <span data-ttu-id="57040-1043">Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest</span><span class="sxs-lookup"><span data-stu-id="57040-1043">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="57040-1044">Zaktualizowano przykłady polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="57040-1044">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="57040-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="57040-1045">Az.Automation</span></span>
* <span data-ttu-id="57040-1046">Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="57040-1046">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="57040-1047">Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode.</span><span class="sxs-lookup"><span data-stu-id="57040-1047">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="57040-1048">Teraz polecenie zwraca wszystkie węzły</span><span class="sxs-lookup"><span data-stu-id="57040-1048">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="57040-1049">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="57040-1049">Az.Cdn</span></span>
* <span data-ttu-id="57040-1050">Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia</span><span class="sxs-lookup"><span data-stu-id="57040-1050">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-1051">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-1051">Az.Compute</span></span>
* <span data-ttu-id="57040-1052">Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania</span><span class="sxs-lookup"><span data-stu-id="57040-1052">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="57040-1053">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="57040-1053">Az.DataFactory</span></span>
* <span data-ttu-id="57040-1054">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1</span><span class="sxs-lookup"><span data-stu-id="57040-1054">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="57040-1055">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="57040-1055">Az.LogicApp</span></span>
* <span data-ttu-id="57040-1056">Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows</span><span class="sxs-lookup"><span data-stu-id="57040-1056">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-1057">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-1057">Az.Network</span></span>
* <span data-ttu-id="57040-1058">Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci</span><span class="sxs-lookup"><span data-stu-id="57040-1058">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="57040-1059">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="57040-1059">Az.RecoveryServices</span></span>
* <span data-ttu-id="57040-1060">Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="57040-1060">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="57040-1061">Aktualizacja zestawu SDK</span><span class="sxs-lookup"><span data-stu-id="57040-1061">SDK Update</span></span>
* <span data-ttu-id="57040-1062">Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="57040-1062">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="57040-1063">Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="57040-1063">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-1064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-1064">Az.Resources</span></span>
* <span data-ttu-id="57040-1065">Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania</span><span class="sxs-lookup"><span data-stu-id="57040-1065">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="57040-1066">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="57040-1066">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="57040-1067">Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="57040-1067">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="57040-1068">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="57040-1068">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="57040-1069">Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="57040-1069">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="57040-1070">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="57040-1070">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-1071">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-1071">Az.Sql</span></span>
* <span data-ttu-id="57040-1072">Zaktualizowano element AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="57040-1072">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="57040-1073">Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="57040-1073">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="57040-1074">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="57040-1074">Az.Storage</span></span>
* <span data-ttu-id="57040-1075">Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57040-1075">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="57040-1076">1.4.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="57040-1076">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="57040-1077">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="57040-1077">Az.AnalysisServices</span></span>
* <span data-ttu-id="57040-1078">Przestarzałe polecenie cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="57040-1078">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="57040-1079">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="57040-1079">Az.Automation</span></span>
* <span data-ttu-id="57040-1080">Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="57040-1080">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="57040-1081">Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="57040-1081">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="57040-1082">Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="57040-1082">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="57040-1083">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="57040-1083">Az.CognitiveServices</span></span>
* <span data-ttu-id="57040-1084">Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.</span><span class="sxs-lookup"><span data-stu-id="57040-1084">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-1085">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-1085">Az.Compute</span></span>
* <span data-ttu-id="57040-1086">Naprawiono błąd z zestawami parametrów identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="57040-1086">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="57040-1087">Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany</span><span class="sxs-lookup"><span data-stu-id="57040-1087">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="57040-1088">Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="57040-1088">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="57040-1089">Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="57040-1089">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="57040-1090">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="57040-1090">Az.DataLakeStore</span></span>
* <span data-ttu-id="57040-1091">Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL</span><span class="sxs-lookup"><span data-stu-id="57040-1091">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="57040-1092">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="57040-1092">Az.EventHub</span></span>
* <span data-ttu-id="57040-1093">Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub</span><span class="sxs-lookup"><span data-stu-id="57040-1093">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="57040-1094">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="57040-1094">Az.KeyVault</span></span>
* <span data-ttu-id="57040-1095">Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="57040-1095">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="57040-1096">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="57040-1096">Az.LogicApp</span></span>
* <span data-ttu-id="57040-1097">Dodano podstawową jednostkę SKU na potrzeby kont integracji</span><span class="sxs-lookup"><span data-stu-id="57040-1097">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="57040-1098">Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid</span><span class="sxs-lookup"><span data-stu-id="57040-1098">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="57040-1099">Nowe polecenia cmdlet dla zestawów kont integracji</span><span class="sxs-lookup"><span data-stu-id="57040-1099">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="57040-1100">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="57040-1100">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="57040-1101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="57040-1101">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="57040-1102">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="57040-1102">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="57040-1103">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="57040-1103">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="57040-1104">Nowe polecenia cmdlet dla konfiguracji partii konta integracji</span><span class="sxs-lookup"><span data-stu-id="57040-1104">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="57040-1105">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="57040-1105">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="57040-1106">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="57040-1106">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="57040-1107">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="57040-1107">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="57040-1108">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="57040-1108">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="57040-1109">Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0</span><span class="sxs-lookup"><span data-stu-id="57040-1109">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="57040-1110">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="57040-1110">Az.Monitor</span></span>
* <span data-ttu-id="57040-1111">Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="57040-1111">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-1112">Az.Network</span></span>
* <span data-ttu-id="57040-1113">Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="57040-1113">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="57040-1114">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="57040-1114">Az.OperationalInsights</span></span>
* <span data-ttu-id="57040-1115">Dodatkowa obsługa źródła danych New i Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="57040-1115">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="57040-1116">Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="57040-1116">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="57040-1117">Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.</span><span class="sxs-lookup"><span data-stu-id="57040-1117">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-1118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-1118">Az.Resources</span></span>
* <span data-ttu-id="57040-1119">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="57040-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="57040-1120">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="57040-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="57040-1121">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="57040-1121">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="57040-1122">Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="57040-1122">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-1123">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-1123">Az.Sql</span></span>
* <span data-ttu-id="57040-1124">Dodano obsługę warstwy Hiperskala bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="57040-1124">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="57040-1125">Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania</span><span class="sxs-lookup"><span data-stu-id="57040-1125">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="57040-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="57040-1126">Az.Websites</span></span>
* <span data-ttu-id="57040-1127">Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="57040-1127">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="57040-1128">1.3.0 — luty 2019 r.</span><span class="sxs-lookup"><span data-stu-id="57040-1128">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="57040-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-1129">Az.Accounts</span></span>
* <span data-ttu-id="57040-1130">Zaktualizowano do najnowszej wersji środowiska ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="57040-1130">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="57040-1131">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="57040-1131">Az.AnalysisServices</span></span>
<span data-ttu-id="57040-1132">Ogólna dostępność modułu Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="57040-1132">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-1133">Az.Compute</span></span>
* <span data-ttu-id="57040-1134">Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80</span><span class="sxs-lookup"><span data-stu-id="57040-1134">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="57040-1135">Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="57040-1135">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="57040-1136">Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="57040-1136">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="57040-1137">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="57040-1137">Az.RecoveryServices</span></span>
<span data-ttu-id="57040-1138">Ogólna dostępność modułu Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="57040-1138">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-1139">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-1139">Az.Resources</span></span>
* <span data-ttu-id="57040-1140">Poprawiono tagowanie dla grup zasobów</span><span class="sxs-lookup"><span data-stu-id="57040-1140">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="57040-1141">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="57040-1141">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="57040-1142">Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="57040-1142">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="57040-1143">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="57040-1143">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-1144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-1144">Az.Sql</span></span>
* <span data-ttu-id="57040-1145">Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="57040-1145">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="57040-1146">Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL</span><span class="sxs-lookup"><span data-stu-id="57040-1146">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="57040-1147">Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="57040-1147">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="57040-1148">1.2.1 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="57040-1148">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="57040-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-1149">Az.Accounts</span></span>
* <span data-ttu-id="57040-1150">Wersja z poprawną wersją uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="57040-1150">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="57040-1151">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="57040-1151">Az.AnalysisServices</span></span>
* <span data-ttu-id="57040-1152">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="57040-1152">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="57040-1153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="57040-1153">Az.RecoveryServices</span></span>
* <span data-ttu-id="57040-1154">Wersja ze zaktualizowaną zależnością uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="57040-1154">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="57040-1155">1.2.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="57040-1155">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="57040-1156">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-1156">Az.Accounts</span></span>
* <span data-ttu-id="57040-1157">Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="57040-1157">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="57040-1158">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="57040-1158">Update incorrect online help URLs</span></span>
* <span data-ttu-id="57040-1159">Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="57040-1159">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="57040-1160">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="57040-1160">Az.Aks</span></span>
* <span data-ttu-id="57040-1161">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="57040-1161">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="57040-1162">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="57040-1162">Az.Automation</span></span>
* <span data-ttu-id="57040-1163">Dodano obsługę elementów runbook języka Python 2</span><span class="sxs-lookup"><span data-stu-id="57040-1163">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="57040-1164">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="57040-1164">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="57040-1165">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="57040-1165">Az.Cdn</span></span>
* <span data-ttu-id="57040-1166">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="57040-1166">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-1167">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-1167">Az.Compute</span></span>
* <span data-ttu-id="57040-1168">Dodano polecenie cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="57040-1168">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="57040-1169">Dodano parametr TempDisk do polecenia Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="57040-1169">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="57040-1170">Poprawiono komunikat ostrzegawczy polecenia New-AzVM</span><span class="sxs-lookup"><span data-stu-id="57040-1170">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="57040-1171">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="57040-1171">Az.ContainerRegistry</span></span>
* <span data-ttu-id="57040-1172">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="57040-1172">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="57040-1173">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="57040-1173">Az.DataFactory</span></span>
* <span data-ttu-id="57040-1174">Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0</span><span class="sxs-lookup"><span data-stu-id="57040-1174">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="57040-1175">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="57040-1175">Az.DataLakeStore</span></span>
* <span data-ttu-id="57040-1176">Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="57040-1176">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="57040-1177">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="57040-1177">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="57040-1178">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="57040-1178">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="57040-1179">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="57040-1179">Az.IotHub</span></span>
* <span data-ttu-id="57040-1180">Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="57040-1180">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="57040-1181">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="57040-1181">Az.KeyVault</span></span>
* <span data-ttu-id="57040-1182">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="57040-1182">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-1183">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-1183">Az.Network</span></span>
* <span data-ttu-id="57040-1184">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="57040-1184">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-1185">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-1185">Az.Resources</span></span>
* <span data-ttu-id="57040-1186">Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="57040-1186">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="57040-1187">Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="57040-1187">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="57040-1188">Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="57040-1188">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="57040-1189">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="57040-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="57040-1190">Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="57040-1190">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="57040-1191">Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="57040-1191">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="57040-1192">Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="57040-1192">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="57040-1193">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="57040-1193">Az.ServiceFabric</span></span>
* <span data-ttu-id="57040-1194">Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="57040-1194">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="57040-1195">Poprawiono niektóre komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="57040-1195">Fix some error messages.</span></span>
* <span data-ttu-id="57040-1196">Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="57040-1196">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="57040-1197">Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="57040-1197">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="57040-1198">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="57040-1198">Az.SignalR</span></span>
* <span data-ttu-id="57040-1199">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="57040-1199">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-1200">Az.Sql</span></span>
* <span data-ttu-id="57040-1201">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="57040-1201">Update incorrect online help URLs</span></span>
* <span data-ttu-id="57040-1202">Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości</span><span class="sxs-lookup"><span data-stu-id="57040-1202">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="57040-1203">Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość</span><span class="sxs-lookup"><span data-stu-id="57040-1203">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="57040-1204">Obsługa niestandardowego sortowania w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="57040-1204">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="57040-1205">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="57040-1205">Az.Storage</span></span>
* <span data-ttu-id="57040-1206">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="57040-1206">Update incorrect online help URLs</span></span>
* <span data-ttu-id="57040-1207">Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.</span><span class="sxs-lookup"><span data-stu-id="57040-1207">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="57040-1208">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="57040-1208">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="57040-1209">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="57040-1209">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="57040-1210">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="57040-1210">Az.TrafficManager</span></span>
* <span data-ttu-id="57040-1211">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="57040-1211">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="57040-1212">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="57040-1212">Az.Websites</span></span>
* <span data-ttu-id="57040-1213">Zaktualizowano nieprawidłowe adresy URL pomocy online</span><span class="sxs-lookup"><span data-stu-id="57040-1213">Update incorrect online help URLs</span></span>
* <span data-ttu-id="57040-1214">Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.</span><span class="sxs-lookup"><span data-stu-id="57040-1214">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="57040-1215">Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją</span><span class="sxs-lookup"><span data-stu-id="57040-1215">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="57040-1216">1.1.0 — styczeń 2019 r.</span><span class="sxs-lookup"><span data-stu-id="57040-1216">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="57040-1217">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-1217">Az.Accounts</span></span>
* <span data-ttu-id="57040-1218">Dodano zakres „Local” do polecenia Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="57040-1218">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-1219">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-1219">Az.Compute</span></span>
* <span data-ttu-id="57040-1220">Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="57040-1220">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="57040-1221">Zaktualizowano opis identyfikatora w plikach Pomocy</span><span class="sxs-lookup"><span data-stu-id="57040-1221">Updated the description of ID in help files</span></span>
* <span data-ttu-id="57040-1222">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-1222">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="57040-1223">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="57040-1223">Az.DataLakeStore</span></span>
* <span data-ttu-id="57040-1224">Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="57040-1224">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="57040-1225">Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego</span><span class="sxs-lookup"><span data-stu-id="57040-1225">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="57040-1226">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="57040-1226">Az.EventGrid</span></span>
* <span data-ttu-id="57040-1227">Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="57040-1227">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="57040-1228">Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="57040-1228">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="57040-1229">New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="57040-1229">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="57040-1230">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="57040-1230">Event Time-To-Live,</span></span>
        - <span data-ttu-id="57040-1231">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="57040-1231">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="57040-1232">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="57040-1232">Dead letter endpoint.</span></span>
    - <span data-ttu-id="57040-1233">Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:</span><span class="sxs-lookup"><span data-stu-id="57040-1233">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="57040-1234">czas wygaśnięcia zdarzenia,</span><span class="sxs-lookup"><span data-stu-id="57040-1234">Event Time-To-Live,</span></span>
        - <span data-ttu-id="57040-1235">maksymalna liczba prób dostarczenia dla zdarzeń,</span><span class="sxs-lookup"><span data-stu-id="57040-1235">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="57040-1236">punkt końcowy utraconych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="57040-1236">Dead letter endpoint.</span></span>
* <span data-ttu-id="57040-1237">Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="57040-1237">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="57040-1238">Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.</span><span class="sxs-lookup"><span data-stu-id="57040-1238">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="57040-1239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="57040-1239">Az.IotHub</span></span>
* <span data-ttu-id="57040-1240">Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub</span><span class="sxs-lookup"><span data-stu-id="57040-1240">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="57040-1241">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="57040-1241">Az.LogicApp</span></span>
* <span data-ttu-id="57040-1242">Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy</span><span class="sxs-lookup"><span data-stu-id="57040-1242">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-1243">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-1243">Az.Resources</span></span>
* <span data-ttu-id="57040-1244">Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="57040-1244">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="57040-1245">Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="57040-1245">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="57040-1246">Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="57040-1246">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="57040-1247">Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="57040-1247">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="57040-1248">Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”</span><span class="sxs-lookup"><span data-stu-id="57040-1248">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="57040-1249">Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="57040-1249">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="57040-1250">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="57040-1250">Az.SignalR</span></span>
* <span data-ttu-id="57040-1251">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-1251">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-1252">Az.Sql</span></span>
* <span data-ttu-id="57040-1253">Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="57040-1253">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="57040-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="57040-1254">Az.Storage</span></span>
* <span data-ttu-id="57040-1255">Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous</span><span class="sxs-lookup"><span data-stu-id="57040-1255">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="57040-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="57040-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="57040-1257">Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki</span><span class="sxs-lookup"><span data-stu-id="57040-1257">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="57040-1258">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="57040-1258">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="57040-1259">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="57040-1259">Az.Websites</span></span>
* <span data-ttu-id="57040-1260">Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="57040-1260">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="57040-1261">Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-1261">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="57040-1262">1.0.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="57040-1262">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="57040-1263">Ogólne</span><span class="sxs-lookup"><span data-stu-id="57040-1263">General</span></span>

- <span data-ttu-id="57040-1264">Ogólna dostępność modułu Az</span><span class="sxs-lookup"><span data-stu-id="57040-1264">General Availability of Az Module</span></span>
- <span data-ttu-id="57040-1265">Pomoc online dla każdego modułu</span><span class="sxs-lookup"><span data-stu-id="57040-1265">Online help for each module</span></span>
- <span data-ttu-id="57040-1266">Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="57040-1266">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="57040-1267">Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="57040-1267">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="57040-1268">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-1268">Az.Accounts</span></span>
- <span data-ttu-id="57040-1269">Zmiana z modułu Az.Profile</span><span class="sxs-lookup"><span data-stu-id="57040-1269">Changed from Az.Profile</span></span>
- <span data-ttu-id="57040-1270">Poprawiono formaty tabel dla typów profili i kontekstu</span><span class="sxs-lookup"><span data-stu-id="57040-1270">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="57040-1271">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="57040-1271">Az.ApiManagement</span></span>
- <span data-ttu-id="57040-1272">Poprawki dotyczące usterki nr 7002</span><span class="sxs-lookup"><span data-stu-id="57040-1272">Fixes for #7002</span></span>
- <span data-ttu-id="57040-1273">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="57040-1273">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="57040-1274">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="57040-1274">Az.Batch</span></span>
- <span data-ttu-id="57040-1275">Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="57040-1275">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="57040-1276">Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.</span><span class="sxs-lookup"><span data-stu-id="57040-1276">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="57040-1277">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="57040-1277">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="57040-1278">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="57040-1278">Az.Billing</span></span>
- <span data-ttu-id="57040-1279">Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="57040-1279">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="57040-1280">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="57040-1280">Az.CognitivServices</span></span>
- <span data-ttu-id="57040-1281">Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="57040-1281">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="57040-1282">Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="57040-1282">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="57040-1283">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="57040-1283">Az.ContainerInstance</span></span>
- <span data-ttu-id="57040-1284">Dodano obsługę elementu ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="57040-1284">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="57040-1285">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="57040-1285">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="57040-1286">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="57040-1286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="57040-1287">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="57040-1287">Az.DataLakeStore</span></span>
- <span data-ttu-id="57040-1288">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="57040-1288">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="57040-1289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="57040-1289">Az.Monitor</span></span>
- <span data-ttu-id="57040-1290">Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="57040-1290">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="57040-1291">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="57040-1291">Az.KeyVault</span></span>
- <span data-ttu-id="57040-1292">Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="57040-1292">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="57040-1293">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="57040-1293">Az.MachineLearning</span></span>
- <span data-ttu-id="57040-1294">Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="57040-1294">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="57040-1295">Az.Media</span><span class="sxs-lookup"><span data-stu-id="57040-1295">Az.Media</span></span>
- <span data-ttu-id="57040-1296">Usunięto przestarzały alias -Tags z polecenia New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="57040-1296">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="57040-1297">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-1297">Az.Network</span></span>
<span data-ttu-id="57040-1298">Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="57040-1298">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="57040-1299">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="57040-1299">New cmdlets added:</span></span>
        - <span data-ttu-id="57040-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57040-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="57040-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57040-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="57040-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57040-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="57040-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57040-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="57040-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57040-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="57040-1305">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="57040-1305">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="57040-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="57040-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="57040-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="57040-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="57040-1308">Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57040-1308">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="57040-1309">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57040-1309">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="57040-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="57040-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="57040-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="57040-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="57040-1312">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57040-1312">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="57040-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="57040-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="57040-1314">New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="57040-1314">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="57040-1315">Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="57040-1315">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="57040-1316">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="57040-1316">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="57040-1317">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="57040-1317">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="57040-1318">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="57040-1318">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="57040-1319">Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="57040-1319">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="57040-1320">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="57040-1320">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="57040-1321">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="57040-1321">Az.OperationalInsights</span></span>
- <span data-ttu-id="57040-1322">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="57040-1322">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="57040-1323">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="57040-1323">Az.Profile</span></span>
- <span data-ttu-id="57040-1324">Zmieniono nazwę modułu na Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="57040-1324">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="57040-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="57040-1325">Az.RecoveryServices</span></span>
- <span data-ttu-id="57040-1326">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="57040-1326">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="57040-1327">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-1327">Az.Resources</span></span>
- <span data-ttu-id="57040-1328">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="57040-1328">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="57040-1329">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="57040-1329">Az.ServiceFabric</span></span>
- <span data-ttu-id="57040-1330">Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca</span><span class="sxs-lookup"><span data-stu-id="57040-1330">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="57040-1331">Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="57040-1331">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="57040-1332">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="57040-1332">Az.SIgnalR</span></span>
- <span data-ttu-id="57040-1333">Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR</span><span class="sxs-lookup"><span data-stu-id="57040-1333">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="57040-1334">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-1334">Az.Sql</span></span>
- <span data-ttu-id="57040-1335">Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń</span><span class="sxs-lookup"><span data-stu-id="57040-1335">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="57040-1336">Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="57040-1336">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="57040-1337">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="57040-1337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="57040-1338">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="57040-1338">Az.Storage</span></span>
- <span data-ttu-id="57040-1339">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="57040-1339">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="57040-1340">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="57040-1340">Az.Websites</span></span>
- <span data-ttu-id="57040-1341">Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="57040-1341">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="57040-1342">0.7.0 — grudzień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="57040-1342">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="57040-1343">Ogólne</span><span class="sxs-lookup"><span data-stu-id="57040-1343">General</span></span>

* <span data-ttu-id="57040-1344">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="57040-1344">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="57040-1345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-1345">Az.Compute</span></span>

* <span data-ttu-id="57040-1346">Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="57040-1346">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="57040-1347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="57040-1347">Az.DataLakeStore</span></span>

* <span data-ttu-id="57040-1348">Poprawiono końcowy ukośnik w domenie konta usługi ADLS</span><span class="sxs-lookup"><span data-stu-id="57040-1348">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="57040-1349">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="57040-1349">Az.FrontDoor</span></span>

* <span data-ttu-id="57040-1350">Poprawiono kilka przerwanych hiperlinków</span><span class="sxs-lookup"><span data-stu-id="57040-1350">Fixed some broken links</span></span>
    - <span data-ttu-id="57040-1351">W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="57040-1351">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="57040-1352">W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="57040-1352">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="57040-1353">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="57040-1353">Az.RecoveryServices</span></span>

* <span data-ttu-id="57040-1354">Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="57040-1354">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="57040-1355">Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="57040-1355">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="57040-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-1356">Az.Resources</span></span>

* <span data-ttu-id="57040-1357">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="57040-1357">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="57040-1358">Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.</span><span class="sxs-lookup"><span data-stu-id="57040-1358">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="57040-1359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-1359">Az.Sql</span></span>

* <span data-ttu-id="57040-1360">Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="57040-1360">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="57040-1361">Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core</span><span class="sxs-lookup"><span data-stu-id="57040-1361">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="57040-1362">Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.</span><span class="sxs-lookup"><span data-stu-id="57040-1362">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="57040-1363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="57040-1363">Az.Storage</span></span>

* <span data-ttu-id="57040-1364">Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57040-1364">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="57040-1365">Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext</span><span class="sxs-lookup"><span data-stu-id="57040-1365">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="57040-1366">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="57040-1366">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="57040-1367">Obsługa konfiguracji statycznej witryny internetowej</span><span class="sxs-lookup"><span data-stu-id="57040-1367">Support Static Website configuration</span></span>
    - <span data-ttu-id="57040-1368">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="57040-1368">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="57040-1369">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="57040-1369">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="57040-1370">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="57040-1370">Az.Websites</span></span>

* <span data-ttu-id="57040-1371">Set-AzureRmWebApp i Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57040-1371">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="57040-1372">Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="57040-1372">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="57040-1373">Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="57040-1373">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="57040-1374">0.6.1 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="57040-1374">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="57040-1375">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="57040-1375">Az.ApiManagement</span></span>
* <span data-ttu-id="57040-1376">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="57040-1376">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="57040-1377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="57040-1377">Az.Automation</span></span>
* <span data-ttu-id="57040-1378">Polecenia cmdlet usługi Azure Automation oparte na programie Swagger</span><span class="sxs-lookup"><span data-stu-id="57040-1378">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="57040-1379">Dodano polecenia cmdlet rozwiązania Update Management</span><span class="sxs-lookup"><span data-stu-id="57040-1379">Added Update Management cmdlets</span></span>
* <span data-ttu-id="57040-1380">Dodano polecenia cmdlet kontroli kodu źródłowego</span><span class="sxs-lookup"><span data-stu-id="57040-1380">Added Source Control cmdlets</span></span>
* <span data-ttu-id="57040-1381">Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="57040-1381">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="57040-1382">Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła</span><span class="sxs-lookup"><span data-stu-id="57040-1382">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="57040-1383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-1383">Az.Compute</span></span>
* <span data-ttu-id="57040-1384">Rozwiązano problem dotyczący tożsamości SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="57040-1384">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="57040-1385">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="57040-1385">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="57040-1386">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="57040-1386">Az.ContainerInstance</span></span>
* <span data-ttu-id="57040-1387">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="57040-1387">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="57040-1388">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="57040-1388">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="57040-1389">Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace</span><span class="sxs-lookup"><span data-stu-id="57040-1389">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="57040-1390">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-1390">Az.Network</span></span>
* <span data-ttu-id="57040-1391">Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="57040-1391">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="57040-1392">Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="57040-1392">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="57040-1393">Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.</span><span class="sxs-lookup"><span data-stu-id="57040-1393">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="57040-1394">Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="57040-1394">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="57040-1395">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="57040-1395">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="57040-1396">Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="57040-1396">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="57040-1397">Przekonwertowano strefę czasową zasad na wielkie litery.</span><span class="sxs-lookup"><span data-stu-id="57040-1397">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="57040-1398">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="57040-1398">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="57040-1399">Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="57040-1399">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="57040-1400">Aktualizacja zależności w związku z problemem dotyczącym mapowania typów</span><span class="sxs-lookup"><span data-stu-id="57040-1400">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="57040-1401">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="57040-1401">Az.Relay</span></span>
* <span data-ttu-id="57040-1402">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="57040-1402">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="57040-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-1403">Az.Resources</span></span>
* <span data-ttu-id="57040-1404">Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="57040-1404">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="57040-1405">Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata</span><span class="sxs-lookup"><span data-stu-id="57040-1405">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="57040-1406">Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="57040-1406">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="57040-1407">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="57040-1407">Az.ServiceFabric</span></span>
* <span data-ttu-id="57040-1408">Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność</span><span class="sxs-lookup"><span data-stu-id="57040-1408">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="57040-1409">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-1409">Az.Sql</span></span>
* <span data-ttu-id="57040-1410">Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="57040-1410">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="57040-1411">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="57040-1411">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="57040-1412">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="57040-1412">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="57040-1413">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="57040-1413">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="57040-1414">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="57040-1414">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="57040-1415">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="57040-1415">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="57040-1416">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="57040-1416">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="57040-1417">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="57040-1417">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="57040-1418">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="57040-1418">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="57040-1419">Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="57040-1419">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="57040-1420">Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="57040-1420">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="57040-1421">Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.</span><span class="sxs-lookup"><span data-stu-id="57040-1421">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="57040-1422">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="57040-1422">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="57040-1423">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="57040-1423">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="57040-1424">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="57040-1424">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="57040-1425">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="57040-1425">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="57040-1426">Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="57040-1426">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="57040-1427">0.5.0 — listopad 2018 r.</span><span class="sxs-lookup"><span data-stu-id="57040-1427">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="57040-1428">Ogólne</span><span class="sxs-lookup"><span data-stu-id="57040-1428">General</span></span>
* <span data-ttu-id="57040-1429">Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="57040-1429">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="57040-1430">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="57040-1430">Az.Profile</span></span>
* <span data-ttu-id="57040-1431">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="57040-1431">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="57040-1432">Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId</span><span class="sxs-lookup"><span data-stu-id="57040-1432">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="57040-1433">Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="57040-1433">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="57040-1434">Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy</span><span class="sxs-lookup"><span data-stu-id="57040-1434">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="57040-1435">Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie</span><span class="sxs-lookup"><span data-stu-id="57040-1435">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="57040-1436">Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej</span><span class="sxs-lookup"><span data-stu-id="57040-1436">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="57040-1437">Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia</span><span class="sxs-lookup"><span data-stu-id="57040-1437">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="57040-1438">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="57040-1438">Az.CognitiveServices</span></span>
* <span data-ttu-id="57040-1439">Dodano operację Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="57040-1439">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-1440">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-1440">Az.Compute</span></span>
* <span data-ttu-id="57040-1441">Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="57040-1441">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="57040-1442">Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="57040-1442">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="57040-1443">Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="57040-1443">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="57040-1444">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="57040-1444">Az.DataLakeStore</span></span>
* <span data-ttu-id="57040-1445">Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="57040-1445">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="57040-1446">Dodano domyślną współbieżność do operacji wielowątkowych.</span><span class="sxs-lookup"><span data-stu-id="57040-1446">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="57040-1447">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="57040-1447">Az.Insights</span></span>
* <span data-ttu-id="57040-1448">Rozwiązano problem nr 7267 (obszar autoskalowania)</span><span class="sxs-lookup"><span data-stu-id="57040-1448">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="57040-1449">Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).</span><span class="sxs-lookup"><span data-stu-id="57040-1449">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="57040-1450">Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia</span><span class="sxs-lookup"><span data-stu-id="57040-1450">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="57040-1451">Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji</span><span class="sxs-lookup"><span data-stu-id="57040-1451">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-1452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-1452">Az.Network</span></span>
* <span data-ttu-id="57040-1453">Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="57040-1453">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="57040-1454">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="57040-1454">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="57040-1455">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="57040-1455">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="57040-1456">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="57040-1456">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="57040-1457">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="57040-1457">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="57040-1458">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="57040-1458">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="57040-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="57040-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="57040-1460">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="57040-1460">Az.PolicyInsights</span></span>
* <span data-ttu-id="57040-1461">Dodano polecenia cmdlet korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="57040-1461">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-1462">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-1462">Az.Resources</span></span>
* <span data-ttu-id="57040-1463">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="57040-1463">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="57040-1464">Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="57040-1464">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="57040-1465">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="57040-1465">Az.ServiceBus</span></span>
* <span data-ttu-id="57040-1466">Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.</span><span class="sxs-lookup"><span data-stu-id="57040-1466">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="57040-1467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="57040-1467">Az.ServiceFabric</span></span>
* <span data-ttu-id="57040-1468">Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="57040-1468">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="57040-1469">Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="57040-1469">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="57040-1470">Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="57040-1470">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="57040-1471">Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="57040-1471">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="57040-1472">Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="57040-1472">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="57040-1473">0.4.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="57040-1473">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="57040-1474">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="57040-1474">Az.Profile</span></span>
* <span data-ttu-id="57040-1475">Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell</span><span class="sxs-lookup"><span data-stu-id="57040-1475">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="57040-1476">Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta</span><span class="sxs-lookup"><span data-stu-id="57040-1476">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-1477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-1477">Az.Compute</span></span>
* <span data-ttu-id="57040-1478">Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="57040-1478">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="57040-1479">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57040-1479">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="57040-1480">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="57040-1480">Az.DataLakeStore</span></span>
* <span data-ttu-id="57040-1481">Dodawanie obsługi dla reguł sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="57040-1481">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="57040-1482">Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="57040-1482">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="57040-1483">Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="57040-1483">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="57040-1484">Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="57040-1484">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="57040-1485">Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="57040-1485">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-1486">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-1486">Az.Network</span></span>
* <span data-ttu-id="57040-1487">Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="57040-1487">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="57040-1488">Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57040-1488">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-1489">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-1489">Az.Resources</span></span>
* <span data-ttu-id="57040-1490">Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza.</span><span class="sxs-lookup"><span data-stu-id="57040-1490">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="57040-1491">Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.</span><span class="sxs-lookup"><span data-stu-id="57040-1491">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="57040-1492">0.3.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="57040-1492">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="57040-1493">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="57040-1493">Azure.Storage</span></span>
* <span data-ttu-id="57040-1494">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="57040-1494">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="57040-1495">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="57040-1495">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="57040-1496">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="57040-1496">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="57040-1497">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="57040-1497">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="57040-1498">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="57040-1498">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="57040-1499">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="57040-1499">Az.CognitiveServices</span></span>
* <span data-ttu-id="57040-1500">Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="57040-1500">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="57040-1501">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="57040-1501">Az.Compute</span></span>
* <span data-ttu-id="57040-1502">Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="57040-1502">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="57040-1503">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="57040-1503">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="57040-1504">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="57040-1504">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="57040-1505">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="57040-1505">Az.DataFactoryV2</span></span>
* <span data-ttu-id="57040-1506">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="57040-1506">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="57040-1507">Az.Network</span><span class="sxs-lookup"><span data-stu-id="57040-1507">Az.Network</span></span>
* <span data-ttu-id="57040-1508">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="57040-1508">Added NetworkProfile functionality.</span></span> <span data-ttu-id="57040-1509">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="57040-1509">new cmdlets added</span></span>
    - <span data-ttu-id="57040-1510">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="57040-1510">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="57040-1511">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="57040-1511">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="57040-1512">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="57040-1512">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="57040-1513">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="57040-1513">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="57040-1514">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="57040-1514">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="57040-1515">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="57040-1515">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="57040-1516">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="57040-1516">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="57040-1517">Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="57040-1517">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="57040-1518">Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="57040-1518">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="57040-1519">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="57040-1519">Az.RedisCache</span></span>
* <span data-ttu-id="57040-1520">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="57040-1520">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="57040-1521">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="57040-1521">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="57040-1522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="57040-1522">Az.Resources</span></span>
* <span data-ttu-id="57040-1523">Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="57040-1523">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="57040-1524">Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="57040-1524">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="57040-1525">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="57040-1525">Az.Sql</span></span>
* <span data-ttu-id="57040-1526">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="57040-1526">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="57040-1527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="57040-1527">Az.Websites</span></span>
* <span data-ttu-id="57040-1528">Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="57040-1528">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="57040-1529">Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="57040-1529">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="57040-1530">0.2.0 — Wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="57040-1530">0.2.0 - September 2018</span></span>
 <span data-ttu-id="57040-1531">Wersja początkowa</span><span class="sxs-lookup"><span data-stu-id="57040-1531">Initial Release</span></span>
