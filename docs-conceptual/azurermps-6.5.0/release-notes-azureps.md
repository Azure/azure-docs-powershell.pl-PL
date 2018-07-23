---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: e9fa2d75c1c4e6ffaa2f7dd8e400f5b13dd4527d
ms.sourcegitcommit: 8b882d1c27d9e323447ff85f56d11bbf5e244d7f
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2018
ms.locfileid: "39110487"
---
# <a name="release-notes"></a><span data-ttu-id="b7101-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="b7101-103">Release notes</span></span>

<span data-ttu-id="b7101-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="b7101-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="650---july-2018"></a><span data-ttu-id="b7101-105">6.5.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b7101-105">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b7101-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b7101-106">AzureRM.Profile</span></span>
* <span data-ttu-id="b7101-107">Zaktualizowano pomoc dotyczącą polecenia „Get-AzureRmContextAutosaveSetting”</span><span class="sxs-lookup"><span data-stu-id="b7101-107">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b7101-108">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b7101-108">Azure.Storage</span></span>
* <span data-ttu-id="b7101-109">Dodano obsługę przekazywania obiektu blob lub pliku z tokenem sygnatury dostępu współdzielonego tylko do odczytu</span><span class="sxs-lookup"><span data-stu-id="b7101-109">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="b7101-110">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b7101-110">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="b7101-111">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b7101-111">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b7101-112">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b7101-112">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b7101-113">Dodano wymaganą właściwość ResourceGroupName do usługi AS.</span><span class="sxs-lookup"><span data-stu-id="b7101-113">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="b7101-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="b7101-114">AzureRM.Automation</span></span>
* <span data-ttu-id="b7101-115">Zaktualizowano pomoc i dodano przykład polecenia „New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="b7101-115">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b7101-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b7101-116">AzureRM.Compute</span></span>
* <span data-ttu-id="b7101-117">Dodano parametr -Tag do polecenia Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b7101-117">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="b7101-118">Dodano przykład polecenia „Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="b7101-118">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="b7101-119">Dodano przykłady polecenia „Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="b7101-119">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="b7101-120">Zaktualizowano pomoc dotyczącą polecenia „Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="b7101-120">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="b7101-121">Zaktualizowano atrybut SimpleParameterSet dla polecenia New-AzureRmVmss, aby domyślnie ustawiał parametr SinglePlacementGroup na wartość false oraz dodano parametr przełącznika „SinglePlacementGroup” umożliwiający użytkownikowi tworzenie zestawów VMSS w pojedynczej grupie umieszczania.</span><span class="sxs-lookup"><span data-stu-id="b7101-121">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b7101-122">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b7101-122">AzureRM.EventHub</span></span>
* <span data-ttu-id="b7101-123">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSEventHubDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="b7101-123">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b7101-124">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7101-124">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b7101-125">Zaktualizowano komunikat o błędzie dla polecenia Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b7101-125">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="b7101-126">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b7101-126">AzureRM.LogicApp</span></span>
* <span data-ttu-id="b7101-127">Naprawiono błąd „nie można rozpoznać zestawu parametrów” w poleceniu New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="b7101-127">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b7101-128">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b7101-128">AzureRM.Network</span></span>
* <span data-ttu-id="b7101-129">Włączono komunikację równorzędną między sieciami wirtualnymi w wielu dzierżawach dla polecenia Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b7101-129">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="b7101-130">Zaktualizowano poniższe polecenia cmdlet usługi Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b7101-130">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="b7101-131">New-AzureRmApplicationGateway: dodano obsługę flagi EnableFIPS i stref</span><span class="sxs-lookup"><span data-stu-id="b7101-131">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="b7101-132">New-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="b7101-132">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="b7101-133">Set-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="b7101-133">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="b7101-134">Ponownie wygenerowano polecenia cmdlet RouteTable z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="b7101-134">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="b7101-135">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="b7101-135">AzureRM.Relay</span></span>
* <span data-ttu-id="b7101-136">Zaktualizowano pliki markdown, naprawiono problem z nazwą parametru w przykładzie</span><span class="sxs-lookup"><span data-stu-id="b7101-136">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b7101-137">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b7101-137">AzureRM.Resources</span></span>
* <span data-ttu-id="b7101-138">Zaktualizowano polecenia cmdlet Roleassignment i roledefinition:</span><span class="sxs-lookup"><span data-stu-id="b7101-138">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="b7101-139">Usunięto dodatkowe wywołania polecenia roledefinition wykonywane w ramach stronicowania.</span><span class="sxs-lookup"><span data-stu-id="b7101-139">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="b7101-140">Naprawiono polecenie cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b7101-140">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="b7101-141">Naprawiono funkcjonalność parametru polecenia -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="b7101-141">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="b7101-142">Rozwiązano problem z poleceniem „Get-AzureRmResource”, który polegał na tym, że w parametrze „-ResourceType” była uwzględniana wielkość liter</span><span class="sxs-lookup"><span data-stu-id="b7101-142">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b7101-143">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b7101-143">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b7101-144">Dodano parametry top i skip do poleceń cmdlet „list”</span><span class="sxs-lookup"><span data-stu-id="b7101-144">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="b7101-145">Dodano polecenia cmdlet migracji przestrzeni nazw z warstwy Standardowa do warstwy Premium:</span><span class="sxs-lookup"><span data-stu-id="b7101-145">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="b7101-146">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b7101-146">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b7101-147">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b7101-147">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b7101-148">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b7101-148">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b7101-149">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b7101-149">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b7101-150">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b7101-150">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="b7101-151">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSServiceBusDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="b7101-151">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b7101-152">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7101-152">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b7101-153">Zaktualizowano przykład dotyczący polecenia „New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="b7101-153">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b7101-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b7101-154">AzureRM.Sql</span></span>
* <span data-ttu-id="b7101-155">Dodano nowe polecenia cmdlet dla przestrzeni nazw Management.Sql, aby umożliwić klientom dodawanie certyfikatu TDE do wystąpienia programu SQL Server lub wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="b7101-155">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="b7101-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="b7101-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="b7101-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="b7101-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b7101-158">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b7101-158">AzureRM.Websites</span></span>
* <span data-ttu-id="b7101-159">Polecenia `Set-AzureRmWebApp -AssignIdentity` i `Set-AzureRmWebAppSlot -AssignIdentity` po ustawieniu na wartość false spowodują teraz usunięcie właściwości Identity z obiektu lokacji. Usuwany jest także tag podglądu.</span><span class="sxs-lookup"><span data-stu-id="b7101-159">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="b7101-160">Zaktualizowano przykład dotyczący poleceń `Get-AzureRmWebAppMetrics` i `Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="b7101-160">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="b7101-161">Polecenie `Set-AzureRmWebApp -PhpVersion` obsługuje wartość off jako prawidłową wersję języka PHP</span><span class="sxs-lookup"><span data-stu-id="b7101-161">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="b7101-162">6.4.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b7101-162">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b7101-163">Ogólne</span><span class="sxs-lookup"><span data-stu-id="b7101-163">General</span></span>
* <span data-ttu-id="b7101-164">Naprawiono formatowanie typu OutputType w plikach pomocy dotyczących większości modułów</span><span class="sxs-lookup"><span data-stu-id="b7101-164">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b7101-165">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b7101-165">AzureRM.Profile</span></span>
* <span data-ttu-id="b7101-166">Dodano atrybut Ps1Xml do podstawowych typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="b7101-166">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b7101-167">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b7101-167">AzureRM.Compute</span></span>
* <span data-ttu-id="b7101-168">Funkcja tagów adresów IP dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="b7101-168">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="b7101-169">Dodano polecenie cmdlet „New-AzureRmVmssIpTagConfig”</span><span class="sxs-lookup"><span data-stu-id="b7101-169">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="b7101-170">Dodano parametr IpTag do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7101-170">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="b7101-171">Funkcja automatycznego wycofywania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="b7101-171">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="b7101-172">Dodano parametry DisableAutoRollback do poleceń New-AzureRmVmssConfig i Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7101-172">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="b7101-173">Funkcja historii uaktualniania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="b7101-173">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="b7101-174">Dodano parametr przełącznika OSUpgradeHistory do polecenia Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7101-174">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="b7101-175">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b7101-175">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="b7101-176">Dodano obsługę list ACL wykazu przy użyciu następujących poleceń:</span><span class="sxs-lookup"><span data-stu-id="b7101-176">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="b7101-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b7101-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="b7101-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b7101-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="b7101-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b7101-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b7101-180">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7101-180">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b7101-181">Dodano obsługę anulowania i śledzenia postępu dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="b7101-181">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="b7101-182">Dodano obsługę anulowania dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="b7101-182">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="b7101-183">Naprawiono opróżnianie komunikatów debugowania dla poleceń cmdlet wykonujących operacje cykliczne</span><span class="sxs-lookup"><span data-stu-id="b7101-183">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="b7101-184">Naprawiono lokalizację testu poleceń cmdlet DataLake</span><span class="sxs-lookup"><span data-stu-id="b7101-184">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b7101-185">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b7101-185">AzureRM.EventHub</span></span>
* <span data-ttu-id="b7101-186">Dodano opcjonalny parametr MaxCount do poleceń cmdlet tworzących listę operacji: Get-AzureRmEventHub i Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b7101-186">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="b7101-187">Rozwiązano problem z poleceniem cmdlet New-AzureRmEventHub polegający na tym, że podczas tworzenia nowego centrum EventHub był wymagany co najmniej jeden parametr.</span><span class="sxs-lookup"><span data-stu-id="b7101-187">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="b7101-188">Udostępniono zestaw parametrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="b7101-188">Provided Default Parameter set.</span></span>
* <span data-ttu-id="b7101-189">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmEventHubKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="b7101-189">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b7101-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7101-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b7101-191">Rozwiązano problem polegający na tym, że wszystkie zasoby były zwracane przez polecenie Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="b7101-191">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b7101-192">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b7101-192">AzureRM.Network</span></span>
* <span data-ttu-id="b7101-193">Uwidoczniono nowe jednostki SKU dla strefowo nadmiarowych bram VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="b7101-193">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="b7101-194">Dodano nowe polecenia dla funkcji interfejsów API partnerów usługi ExpressRoute za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="b7101-194">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="b7101-195">Dodano polecenie Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b7101-195">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="b7101-196">Dodano polecenie Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b7101-196">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="b7101-197">Dodano polecenie Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="b7101-197">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b7101-198">Dodano polecenie Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="b7101-198">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b7101-199">Dodano polecenie Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="b7101-199">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b7101-200">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="b7101-200">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b7101-201">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b7101-201">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b7101-202">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b7101-202">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b7101-203">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b7101-203">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b7101-204">Dodano polecenie cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="b7101-204">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="b7101-205">To polecenie cmdlet pobiera identyfikator maszyny wirtualnej i sprawdza, czy maszyna wirtualna jest chroniona przez magazyn w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b7101-205">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="b7101-206">Jeśli taki magazyn istnieje, polecenie cmdlet wyświetla jego szczegóły.</span><span class="sxs-lookup"><span data-stu-id="b7101-206">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b7101-207">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b7101-207">AzureRM.Resources</span></span>
* <span data-ttu-id="b7101-208">Zaktualizowano polecenia cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="b7101-208">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="b7101-209">Dodano obsługę wyświetlania listy wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="b7101-209">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="b7101-210">Dodano obsługę pobierania poszczególnych przydziałów za pomocą wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="b7101-210">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="b7101-211">Dodano przełączniki -Effective i -All do parametru kontroli</span><span class="sxs-lookup"><span data-stu-id="b7101-211">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="b7101-212">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b7101-212">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="b7101-213">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="b7101-213">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="b7101-214">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b7101-214">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="b7101-215">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b7101-215">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="b7101-216">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="b7101-216">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="b7101-217">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b7101-217">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="b7101-218">Dodano obsługę odwołania do wpisu tajnego KeyVault w parametrach w przypadku używania elementu „TemplateParameterObject” w poleceniu „New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="b7101-218">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="b7101-219">Rozwiązano problem polegający na tym, że parametr „-EndDate” był ignorowany w poleceniu „New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="b7101-219">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="b7101-220">Rozwiązano problem polegający na tym, że w poleceniu „Add-AzureRmADGroupMember” używano nieprawidłowego adres URL podczas zgłaszania żądania</span><span class="sxs-lookup"><span data-stu-id="b7101-220">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="b7101-221">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b7101-221">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b7101-222">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmServiceBusKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="b7101-222">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b7101-223">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b7101-223">AzureRM.Sql</span></span>
* <span data-ttu-id="b7101-224">Objaśniono punkty przywracania zdefiniowane przez użytkownika dla usługi SQLDW w pomocy polecenia New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="b7101-224">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="b7101-225">Zaktualizowano dokumentację parametru -ComputeGeneration w kilku poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7101-225">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="b7101-226">6.3.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="b7101-226">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b7101-227">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b7101-227">AzureRM.Profile</span></span>
* <span data-ttu-id="b7101-228">Zaktualizowano komunikaty o błędach dotyczące polecenia Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="b7101-228">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="b7101-229">Tworzenie kontekstu dla każdej subskrypcji w przypadku uruchomienia polecenia „Connect-AzureRmAccount” bez wcześniejszego kontekstu</span><span class="sxs-lookup"><span data-stu-id="b7101-229">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b7101-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b7101-230">Azure.Storage</span></span>
* <span data-ttu-id="b7101-231">Dodano informacje dotyczące parametru -Permissions w plikach pomocy.</span><span class="sxs-lookup"><span data-stu-id="b7101-231">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b7101-232">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b7101-232">AzureRM.Compute</span></span>
* <span data-ttu-id="b7101-233">Polecenie „Get-AzureRmVmDiskEncryptionStatus” — rozwiązano problem zaobserwowany w przypadku maszyn wirtualnych bez dysków z danymi</span><span class="sxs-lookup"><span data-stu-id="b7101-233">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="b7101-234">Aktualizacja wersji biblioteki klienckiej obliczeń w celu naprawy następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b7101-234">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="b7101-235">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b7101-235">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="b7101-236">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b7101-236">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="b7101-237">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b7101-237">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="b7101-238">Naprawiono następujące polecenia cmdlet w celu poprawnego wyświetlania identyfikatora operacji i stanu operacji:</span><span class="sxs-lookup"><span data-stu-id="b7101-238">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="b7101-239">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b7101-239">Start-AzureRmVM</span></span>
    - <span data-ttu-id="b7101-240">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b7101-240">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="b7101-241">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b7101-241">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="b7101-242">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b7101-242">Set-AzureRmVM</span></span>
    - <span data-ttu-id="b7101-243">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="b7101-243">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="b7101-244">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7101-244">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="b7101-245">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="b7101-245">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="b7101-246">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="b7101-246">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="b7101-247">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7101-247">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="b7101-248">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7101-248">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="b7101-249">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7101-249">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="b7101-250">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7101-250">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="b7101-251">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="b7101-251">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="b7101-252">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b7101-252">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="b7101-253">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="b7101-253">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="b7101-254">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b7101-254">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="b7101-255">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="b7101-255">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="b7101-256">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b7101-256">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="b7101-257">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b7101-257">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="b7101-258">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b7101-258">AzureRM.EventGrid</span></span>
* <span data-ttu-id="b7101-259">Usunięto warunki weryfikacji ValidateNotNullOrEmpty dla elementów SubjectBeginsWith/SubjectEndsWith w poleceniu cmdlet Update-AzureRmEventGridSubscription w celu umożliwienia zmiany tych parametrów na pusty ciąg w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="b7101-259">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b7101-260">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7101-260">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b7101-261">Rozwiązano problem polegający na tym, że nie były zwracane tagi w przypadku uruchomienia polecenia Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="b7101-261">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="b7101-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b7101-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="b7101-263">Publiczne udostępnienie poleceń cmdlet usługi Policy Insights</span><span class="sxs-lookup"><span data-stu-id="b7101-263">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="b7101-264">Użycie interfejsu API w wersji z 4.04.2018</span><span class="sxs-lookup"><span data-stu-id="b7101-264">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="b7101-265">Dodano element PolicyDefinitionReferenceId do wyników polecenia Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="b7101-265">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b7101-266">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b7101-266">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b7101-267">Dodano parametr -Vault do poleceń cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="b7101-267">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="b7101-268">W przypadku przekazania to polecenie przesłania polecenie cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="b7101-268">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b7101-269">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b7101-269">AzureRM.Sql</span></span>
* <span data-ttu-id="b7101-270">Zaktualizowano przykład w pliku pomocy polecenia Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="b7101-270">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b7101-271">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b7101-271">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b7101-272">Zaktualizowano plik pomocy polecenia Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b7101-272">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b7101-273">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b7101-273">AzureRM.Websites</span></span>
* <span data-ttu-id="b7101-274">Zaktualizowano polecenie „Set-AzureRmWebApp”, aby nie zastępowało elementu AppSettings w przypadku użycia parametru -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b7101-274">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="b7101-275">Zaktualizowano polecenie „New-AzureRmWebAppSlot” w celu umożliwienia obsługi parametru AppServicePlan jako parametru opcjonalnego</span><span class="sxs-lookup"><span data-stu-id="b7101-275">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="b7101-276">6.2.1 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="b7101-276">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="b7101-277">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b7101-277">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="b7101-278">Zaktualizowano model PSWorkspace w celu umożliwienia użycia typu jako parametru w sieci</span><span class="sxs-lookup"><span data-stu-id="b7101-278">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="b7101-279">6.2.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="b7101-279">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b7101-280">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b7101-280">AzureRM.Profile</span></span>
* <span data-ttu-id="b7101-281">Naprawiono problem, który polegał na tym, że wersja 10.0.3 pliku Newtonsoft.Json nie była ładowana podczas importowania modułu</span><span class="sxs-lookup"><span data-stu-id="b7101-281">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b7101-282">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b7101-282">AzureRM.Compute</span></span>
* <span data-ttu-id="b7101-283">Funkcja aktualizacji maszyny wirtualnej usługi VMSS</span><span class="sxs-lookup"><span data-stu-id="b7101-283">VMSS VM Update feature</span></span>
    - <span data-ttu-id="b7101-284">Dodano polecenia cmdlet „Update-AzureRmVmssVM” i „New-AzureRmVMDataDisk”</span><span class="sxs-lookup"><span data-stu-id="b7101-284">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="b7101-285">Dodano parametr VirtualMachineScaleSetVM do polecenia cmdlet „Add-AzureRmVMDataDisk” w celu obsługi dodawania dysku danych do maszyny wirtualnej usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="b7101-285">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b7101-286">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b7101-286">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b7101-287">Zaktualizowano zestaw ADF .Net SDK do wersji 0.8.0-preview zawierającej następujące zmiany:</span><span class="sxs-lookup"><span data-stu-id="b7101-287">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="b7101-288">Dodano operację repozytorium do konfigurowania fabryki</span><span class="sxs-lookup"><span data-stu-id="b7101-288">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="b7101-289">Zaktualizowano usługę QuickBooks LinkedService w celu ujawnienia właściwości consumerKey i consumerSecret</span><span class="sxs-lookup"><span data-stu-id="b7101-289">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="b7101-290">Zaktualizowano wiele typów modeli, od SecretBase do Object</span><span class="sxs-lookup"><span data-stu-id="b7101-290">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="b7101-291">Dodano wyzwalacz zdarzeń obiektów blob</span><span class="sxs-lookup"><span data-stu-id="b7101-291">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="b7101-292">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7101-292">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b7101-293">Zaktualizowano dokumentację o przykładowe dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="b7101-293">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="b7101-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b7101-294">AzureRM.Network</span></span>
* <span data-ttu-id="b7101-295">Parametry włączania analizy ruchu w poleceniach cmdlet narzędzia Network Watcher</span><span class="sxs-lookup"><span data-stu-id="b7101-295">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b7101-296">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b7101-296">AzureRM.Resources</span></span>
* <span data-ttu-id="b7101-297">Rozwiązano problem z właściwością „Properties” obiektu „PSResource” zwracanego z polecenia „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="b7101-297">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="b7101-298">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="b7101-298">AzureRM.Scheduler</span></span>
* <span data-ttu-id="b7101-299">Rozwiązano problem z aktualizacją ServiceBusQueueJob, która nie ustawiała nowych wartości uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="b7101-299">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="b7101-300">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b7101-300">AzureRM.Sql</span></span>
* <span data-ttu-id="b7101-301">Zaktualizowano następujące polecenia cmdlet o opcjonalny parametr LicenseType</span><span class="sxs-lookup"><span data-stu-id="b7101-301">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="b7101-302">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b7101-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="b7101-303">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b7101-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="b7101-304">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b7101-304">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="b7101-305">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b7101-305">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="b7101-306">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b7101-306">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b7101-307">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b7101-307">AzureRM.Websites</span></span>
* <span data-ttu-id="b7101-308">Polecenie „New-AzureRMWebApp” zostało zaktualizowane w celu używania typowych algorytmów z biblioteki strategii.</span><span class="sxs-lookup"><span data-stu-id="b7101-308">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="b7101-309">6.1.0 — maj 2018 r.</span><span class="sxs-lookup"><span data-stu-id="b7101-309">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b7101-310">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b7101-310">AzureRM.Profile</span></span>
* <span data-ttu-id="b7101-311">Rozwiązano problem polegający na tym, że po uruchomieniu polecenia „Clear-AzureRmContext” pozostawał pusty kontekst o nazwie takiej jak poprzedni kontekst domyślny, co uniemożliwiało użytkownikowi utworzenie nowego kontekstu ze starą nazwą</span><span class="sxs-lookup"><span data-stu-id="b7101-311">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b7101-312">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b7101-312">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b7101-313">Włączono operacje kojarzenia/usuwania skojarzenia bramy w usłudze AS.</span><span class="sxs-lookup"><span data-stu-id="b7101-313">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b7101-314">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b7101-314">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b7101-315">Dodano obsługę elementów ApiVersion, ApiRelease oraz ApiRevision</span><span class="sxs-lookup"><span data-stu-id="b7101-315">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="b7101-316">Dodano obsługę zaplecza ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7101-316">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="b7101-317">Dodano obsługę rejestratora usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="b7101-317">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="b7101-318">Dodano obsługę rozpoznawania jednostki SKU „Podstawowa” jako prawidłowej jednostki SKU usługi API Management</span><span class="sxs-lookup"><span data-stu-id="b7101-318">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="b7101-319">Dodano obsługę instalowania certyfikatów wystawionych przez prywatny urząd certyfikacji jako certyfikatów głównych lub certyfikatów urzędu certyfikacji</span><span class="sxs-lookup"><span data-stu-id="b7101-319">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="b7101-320">Dodano obsługę akceptowania niestandardowych certyfikatów SSL za pomocą magazynu kluczy i wielu nazw hostów serwera proxy</span><span class="sxs-lookup"><span data-stu-id="b7101-320">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="b7101-321">Dodano obsługę tożsamości MSI</span><span class="sxs-lookup"><span data-stu-id="b7101-321">Added support for MSI identity</span></span>
* <span data-ttu-id="b7101-322">Dodano obsługę akceptowania zasad za pomocą adresu URL. UWAGA: następujące polecenia cmdlet staną się przestarzałe w przyszłym wydaniu</span><span class="sxs-lookup"><span data-stu-id="b7101-322">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="b7101-323">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="b7101-323">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="b7101-324">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7101-324">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="b7101-325">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="b7101-325">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="b7101-326">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="b7101-326">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="b7101-327">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="b7101-327">AzureRM.Batch</span></span>
* <span data-ttu-id="b7101-328">Wydano nowe polecenie cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="b7101-328">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="b7101-329">Wydano nowe polecenie cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="b7101-329">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="b7101-330">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="b7101-330">AzureRM.Consumption</span></span>
* <span data-ttu-id="b7101-331">Dodano nowe parametry polecenia cmdlet Get-AzureRmConsumptionUsageDetail: Expand, ResourceGroup, InstanceName, InstanceId, Tags oraz Top</span><span class="sxs-lookup"><span data-stu-id="b7101-331">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b7101-332">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7101-332">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b7101-333">Poprawiono przykład dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="b7101-333">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="b7101-334">Rozwiązano problem powodujący wyjątek parametru o wartości null dla przypadku Recurse w poleceniu Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b7101-334">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="b7101-335">Poprawiono pliki pomocy dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl oraz Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b7101-335">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="b7101-336">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b7101-336">AzureRM.Network</span></span>
* <span data-ttu-id="b7101-337">Podniesiono wersję zestawu SDK sieci z 18.0.0-preview do 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="b7101-337">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="b7101-338">Dodano polecenie cmdlet służące do tworzenia konfiguracji protokołu</span><span class="sxs-lookup"><span data-stu-id="b7101-338">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="b7101-339">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7101-339">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="b7101-340">Dodano polecenie cmdlet służące do dodawania nowego połączenia obwodu do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="b7101-340">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="b7101-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7101-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="b7101-342">Dodano polecenie cmdlet służące do usuwania połączenia obwodu z istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="b7101-342">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="b7101-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7101-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="b7101-344">Dodano polecenie cmdlet służące do pobierania połączenia obwodu</span><span class="sxs-lookup"><span data-stu-id="b7101-344">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="b7101-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7101-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b7101-346">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7101-346">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b7101-347">Naprawiono użycie uwierzytelniania serwera za pomocą wygenerowanych certyfikatów (problem nr 5998)</span><span class="sxs-lookup"><span data-stu-id="b7101-347">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b7101-348">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b7101-348">AzureRM.Sql</span></span>
* <span data-ttu-id="b7101-349">Zaktualizowano polecenia cmdlet inspekcji w celu umożliwienia usuwania elementów AuditAction lub AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="b7101-349">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="b7101-350">Rozwiązano problem z poleceniem Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, który powodował zakończenie polecenia niepowodzeniem podczas ustawiania nowych, elastycznych zasad przechowywania oraz zwrócenie komunikatu „Konfigurowanie zasad przechowywania długoterminowego za pomocą magazynu usługi Azure Recovery Service i zasad nie jest już obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="b7101-350">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="b7101-351">Prześlij żądanie z nowymi, elastycznymi zasadami przechowywania”.</span><span class="sxs-lookup"><span data-stu-id="b7101-351">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="b7101-352">Zaktualizowano wszystkie polecenia cmdlet służące do tworzenia/aktualizowania elastycznej puli/bazy danych usługi Azure SQL Database w taki sposób, aby korzystały z nowego interfejsu API bazy danych, który obsługuje właściwość SKU na potrzeby właściwości powiązanych ze skalowaniem i warstwą.</span><span class="sxs-lookup"><span data-stu-id="b7101-352">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="b7101-353">Zaktualizowane polecenia cmdlet to:</span><span class="sxs-lookup"><span data-stu-id="b7101-353">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="b7101-354">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b7101-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="b7101-355">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b7101-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="b7101-356">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b7101-356">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="b7101-357">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b7101-357">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="b7101-358">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b7101-358">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b7101-359">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b7101-359">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b7101-360">Zaktualizowano parametry polecenia „Get-AzureRmTrafficManagerProfile”, aby parametr -ResourceGroupName był wymagany, gdy został podany parametr -Name.</span><span class="sxs-lookup"><span data-stu-id="b7101-360">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>