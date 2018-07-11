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
ms.openlocfilehash: 255e26aea5ea3cea866faa0d095cdf643c8ef0a8
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406487"
---
# <a name="release-notes"></a><span data-ttu-id="f43fa-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="f43fa-103">Release notes</span></span>

<span data-ttu-id="f43fa-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="f43fa-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="640---july-2018"></a><span data-ttu-id="f43fa-105">6.4.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f43fa-105">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f43fa-106">Ogólne</span><span class="sxs-lookup"><span data-stu-id="f43fa-106">General</span></span>
* <span data-ttu-id="f43fa-107">Naprawiono formatowanie typu OutputType w plikach pomocy dotyczących większości modułów</span><span class="sxs-lookup"><span data-stu-id="f43fa-107">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="f43fa-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f43fa-108">AzureRM.Profile</span></span>
* <span data-ttu-id="f43fa-109">Dodano atrybut Ps1Xml do podstawowych typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="f43fa-109">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f43fa-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f43fa-110">AzureRM.Compute</span></span>
* <span data-ttu-id="f43fa-111">Funkcja tagów adresów IP dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="f43fa-111">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="f43fa-112">Dodano polecenie cmdlet „New-AzureRmVmssIpTagConfig”</span><span class="sxs-lookup"><span data-stu-id="f43fa-112">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="f43fa-113">Dodano parametr IpTag do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="f43fa-113">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="f43fa-114">Funkcja automatycznego wycofywania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="f43fa-114">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="f43fa-115">Dodano parametry DisableAutoRollback do poleceń New-AzureRmVmssConfig i Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f43fa-115">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="f43fa-116">Funkcja historii uaktualniania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="f43fa-116">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="f43fa-117">Dodano parametr przełącznika OSUpgradeHistory do polecenia Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f43fa-117">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="f43fa-118">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f43fa-118">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="f43fa-119">Dodano obsługę list ACL wykazu przy użyciu następujących poleceń:</span><span class="sxs-lookup"><span data-stu-id="f43fa-119">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="f43fa-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f43fa-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="f43fa-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f43fa-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="f43fa-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f43fa-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f43fa-123">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f43fa-123">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f43fa-124">Dodano obsługę anulowania i śledzenia postępu dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="f43fa-124">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="f43fa-125">Dodano obsługę anulowania dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="f43fa-125">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="f43fa-126">Naprawiono opróżnianie komunikatów debugowania dla poleceń cmdlet wykonujących operacje cykliczne</span><span class="sxs-lookup"><span data-stu-id="f43fa-126">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="f43fa-127">Naprawiono lokalizację testu poleceń cmdlet DataLake</span><span class="sxs-lookup"><span data-stu-id="f43fa-127">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f43fa-128">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f43fa-128">AzureRM.EventHub</span></span>
* <span data-ttu-id="f43fa-129">Dodano opcjonalny parametr MaxCount do poleceń cmdlet tworzących listę operacji: Get-AzureRmEventHub i Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="f43fa-129">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="f43fa-130">Rozwiązano problem z poleceniem cmdlet New-AzureRmEventHub polegający na tym, że podczas tworzenia nowego centrum EventHub był wymagany co najmniej jeden parametr.</span><span class="sxs-lookup"><span data-stu-id="f43fa-130">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="f43fa-131">Udostępniono zestaw parametrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="f43fa-131">Provided Default Parameter set.</span></span>
* <span data-ttu-id="f43fa-132">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmEventHubKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="f43fa-132">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f43fa-133">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f43fa-133">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f43fa-134">Rozwiązano problem polegający na tym, że wszystkie zasoby były zwracane przez polecenie Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="f43fa-134">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f43fa-135">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f43fa-135">AzureRM.Network</span></span>
* <span data-ttu-id="f43fa-136">Uwidoczniono nowe jednostki SKU dla strefowo nadmiarowych bram VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="f43fa-136">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="f43fa-137">Dodano nowe polecenia dla funkcji interfejsów API partnerów usługi ExpressRoute za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="f43fa-137">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="f43fa-138">Dodano polecenie Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f43fa-138">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="f43fa-139">Dodano polecenie Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f43fa-139">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="f43fa-140">Dodano polecenie Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f43fa-140">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="f43fa-141">Dodano polecenie Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f43fa-141">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="f43fa-142">Dodano polecenie Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f43fa-142">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="f43fa-143">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f43fa-143">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f43fa-144">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f43fa-144">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f43fa-145">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f43fa-145">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f43fa-146">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f43fa-146">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f43fa-147">Dodano polecenie cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="f43fa-147">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="f43fa-148">To polecenie cmdlet pobiera identyfikator maszyny wirtualnej i sprawdza, czy maszyna wirtualna jest chroniona przez magazyn w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f43fa-148">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="f43fa-149">Jeśli taki magazyn istnieje, polecenie cmdlet wyświetla jego szczegóły.</span><span class="sxs-lookup"><span data-stu-id="f43fa-149">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f43fa-150">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f43fa-150">AzureRM.Resources</span></span>
* <span data-ttu-id="f43fa-151">Zaktualizowano polecenia cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="f43fa-151">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="f43fa-152">Dodano obsługę wyświetlania listy wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="f43fa-152">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="f43fa-153">Dodano obsługę pobierania poszczególnych przydziałów za pomocą wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="f43fa-153">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="f43fa-154">Dodano przełączniki -Effective i -All do parametru kontroli</span><span class="sxs-lookup"><span data-stu-id="f43fa-154">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="f43fa-155">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f43fa-155">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="f43fa-156">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="f43fa-156">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="f43fa-157">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f43fa-157">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="f43fa-158">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f43fa-158">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="f43fa-159">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="f43fa-159">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="f43fa-160">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f43fa-160">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="f43fa-161">Dodano obsługę odwołania do wpisu tajnego KeyVault w parametrach w przypadku używania elementu „TemplateParameterObject” w poleceniu „New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f43fa-161">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="f43fa-162">Rozwiązano problem polegający na tym, że parametr „-EndDate” był ignorowany w poleceniu „New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="f43fa-162">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="f43fa-163">Rozwiązano problem polegający na tym, że w poleceniu „Add-AzureRmADGroupMember” używano nieprawidłowego adres URL podczas zgłaszania żądania</span><span class="sxs-lookup"><span data-stu-id="f43fa-163">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="f43fa-164">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f43fa-164">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f43fa-165">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmServiceBusKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="f43fa-165">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f43fa-166">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f43fa-166">AzureRM.Sql</span></span>
* <span data-ttu-id="f43fa-167">Objaśniono punkty przywracania zdefiniowane przez użytkownika dla usługi SQLDW w pomocy polecenia New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="f43fa-167">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="f43fa-168">Zaktualizowano dokumentację parametru -ComputeGeneration w kilku poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="f43fa-168">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="f43fa-169">6.3.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="f43fa-169">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f43fa-170">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f43fa-170">AzureRM.Profile</span></span>
* <span data-ttu-id="f43fa-171">Zaktualizowano komunikaty o błędach dotyczące polecenia Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="f43fa-171">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="f43fa-172">Tworzenie kontekstu dla każdej subskrypcji w przypadku uruchomienia polecenia „Connect-AzureRmAccount” bez wcześniejszego kontekstu</span><span class="sxs-lookup"><span data-stu-id="f43fa-172">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="f43fa-173">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f43fa-173">Azure.Storage</span></span>
* <span data-ttu-id="f43fa-174">Dodano informacje dotyczące parametru -Permissions w plikach pomocy.</span><span class="sxs-lookup"><span data-stu-id="f43fa-174">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f43fa-175">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f43fa-175">AzureRM.Compute</span></span>
* <span data-ttu-id="f43fa-176">Polecenie „Get-AzureRmVmDiskEncryptionStatus” — rozwiązano problem zaobserwowany w przypadku maszyn wirtualnych bez dysków z danymi</span><span class="sxs-lookup"><span data-stu-id="f43fa-176">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="f43fa-177">Aktualizacja wersji biblioteki klienckiej obliczeń w celu naprawy następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f43fa-177">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="f43fa-178">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f43fa-178">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="f43fa-179">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="f43fa-179">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="f43fa-180">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f43fa-180">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="f43fa-181">Naprawiono następujące polecenia cmdlet w celu poprawnego wyświetlania identyfikatora operacji i stanu operacji:</span><span class="sxs-lookup"><span data-stu-id="f43fa-181">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="f43fa-182">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f43fa-182">Start-AzureRmVM</span></span>
    - <span data-ttu-id="f43fa-183">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f43fa-183">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="f43fa-184">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f43fa-184">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="f43fa-185">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f43fa-185">Set-AzureRmVM</span></span>
    - <span data-ttu-id="f43fa-186">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="f43fa-186">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="f43fa-187">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f43fa-187">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="f43fa-188">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="f43fa-188">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="f43fa-189">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="f43fa-189">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="f43fa-190">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f43fa-190">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="f43fa-191">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f43fa-191">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="f43fa-192">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f43fa-192">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="f43fa-193">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f43fa-193">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="f43fa-194">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="f43fa-194">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="f43fa-195">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="f43fa-195">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="f43fa-196">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="f43fa-196">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="f43fa-197">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f43fa-197">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="f43fa-198">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="f43fa-198">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="f43fa-199">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="f43fa-199">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="f43fa-200">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f43fa-200">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="f43fa-201">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f43fa-201">AzureRM.EventGrid</span></span>
* <span data-ttu-id="f43fa-202">Usunięto warunki weryfikacji ValidateNotNullOrEmpty dla elementów SubjectBeginsWith/SubjectEndsWith w poleceniu cmdlet Update-AzureRmEventGridSubscription w celu umożliwienia zmiany tych parametrów na pusty ciąg w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="f43fa-202">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f43fa-203">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f43fa-203">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f43fa-204">Rozwiązano problem polegający na tym, że nie były zwracane tagi w przypadku uruchomienia polecenia Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="f43fa-204">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="f43fa-205">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f43fa-205">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="f43fa-206">Publiczne udostępnienie poleceń cmdlet usługi Policy Insights</span><span class="sxs-lookup"><span data-stu-id="f43fa-206">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="f43fa-207">Użycie interfejsu API w wersji z 4.04.2018</span><span class="sxs-lookup"><span data-stu-id="f43fa-207">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="f43fa-208">Dodano element PolicyDefinitionReferenceId do wyników polecenia Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="f43fa-208">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f43fa-209">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f43fa-209">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f43fa-210">Dodano parametr -Vault do poleceń cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="f43fa-210">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="f43fa-211">W przypadku przekazania to polecenie przesłania polecenie cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="f43fa-211">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f43fa-212">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f43fa-212">AzureRM.Sql</span></span>
* <span data-ttu-id="f43fa-213">Zaktualizowano przykład w pliku pomocy polecenia Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="f43fa-213">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f43fa-214">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f43fa-214">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f43fa-215">Zaktualizowano plik pomocy polecenia Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f43fa-215">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f43fa-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f43fa-216">AzureRM.Websites</span></span>
* <span data-ttu-id="f43fa-217">Zaktualizowano polecenie „Set-AzureRmWebApp”, aby nie zastępowało elementu AppSettings w przypadku użycia parametru -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f43fa-217">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="f43fa-218">Zaktualizowano polecenie „New-AzureRmWebAppSlot” w celu umożliwienia obsługi parametru AppServicePlan jako parametru opcjonalnego</span><span class="sxs-lookup"><span data-stu-id="f43fa-218">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="f43fa-219">6.2.1 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="f43fa-219">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="f43fa-220">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f43fa-220">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="f43fa-221">Zaktualizowano model PSWorkspace w celu umożliwienia użycia typu jako parametru w sieci</span><span class="sxs-lookup"><span data-stu-id="f43fa-221">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="f43fa-222">6.2.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="f43fa-222">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f43fa-223">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f43fa-223">AzureRM.Profile</span></span>
* <span data-ttu-id="f43fa-224">Naprawiono problem, który polegał na tym, że wersja 10.0.3 pliku Newtonsoft.Json nie była ładowana podczas importowania modułu</span><span class="sxs-lookup"><span data-stu-id="f43fa-224">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f43fa-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f43fa-225">AzureRM.Compute</span></span>
* <span data-ttu-id="f43fa-226">Funkcja aktualizacji maszyny wirtualnej usługi VMSS</span><span class="sxs-lookup"><span data-stu-id="f43fa-226">VMSS VM Update feature</span></span>
    - <span data-ttu-id="f43fa-227">Dodano polecenia cmdlet „Update-AzureRmVmssVM” i „New-AzureRmVMDataDisk”</span><span class="sxs-lookup"><span data-stu-id="f43fa-227">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="f43fa-228">Dodano parametr VirtualMachineScaleSetVM do polecenia cmdlet „Add-AzureRmVMDataDisk” w celu obsługi dodawania dysku danych do maszyny wirtualnej usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="f43fa-228">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f43fa-229">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f43fa-229">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f43fa-230">Zaktualizowano zestaw ADF .Net SDK do wersji 0.8.0-preview zawierającej następujące zmiany:</span><span class="sxs-lookup"><span data-stu-id="f43fa-230">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="f43fa-231">Dodano operację repozytorium do konfigurowania fabryki</span><span class="sxs-lookup"><span data-stu-id="f43fa-231">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="f43fa-232">Zaktualizowano usługę QuickBooks LinkedService w celu ujawnienia właściwości consumerKey i consumerSecret</span><span class="sxs-lookup"><span data-stu-id="f43fa-232">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="f43fa-233">Zaktualizowano wiele typów modeli, od SecretBase do Object</span><span class="sxs-lookup"><span data-stu-id="f43fa-233">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="f43fa-234">Dodano wyzwalacz zdarzeń obiektów blob</span><span class="sxs-lookup"><span data-stu-id="f43fa-234">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="f43fa-235">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f43fa-235">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f43fa-236">Zaktualizowano dokumentację o przykładowe dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="f43fa-236">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="f43fa-237">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f43fa-237">AzureRM.Network</span></span>
* <span data-ttu-id="f43fa-238">Parametry włączania analizy ruchu w poleceniach cmdlet narzędzia Network Watcher</span><span class="sxs-lookup"><span data-stu-id="f43fa-238">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f43fa-239">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f43fa-239">AzureRM.Resources</span></span>
* <span data-ttu-id="f43fa-240">Rozwiązano problem z właściwością „Properties” obiektu „PSResource” zwracanego z polecenia „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="f43fa-240">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="f43fa-241">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="f43fa-241">AzureRM.Scheduler</span></span>
* <span data-ttu-id="f43fa-242">Rozwiązano problem z aktualizacją ServiceBusQueueJob, która nie ustawiała nowych wartości uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="f43fa-242">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="f43fa-243">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f43fa-243">AzureRM.Sql</span></span>
* <span data-ttu-id="f43fa-244">Zaktualizowano następujące polecenia cmdlet o opcjonalny parametr LicenseType</span><span class="sxs-lookup"><span data-stu-id="f43fa-244">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="f43fa-245">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f43fa-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="f43fa-246">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f43fa-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="f43fa-247">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f43fa-247">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="f43fa-248">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f43fa-248">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="f43fa-249">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f43fa-249">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f43fa-250">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f43fa-250">AzureRM.Websites</span></span>
* <span data-ttu-id="f43fa-251">Polecenie „New-AzureRMWebApp” zostało zaktualizowane w celu używania typowych algorytmów z biblioteki strategii.</span><span class="sxs-lookup"><span data-stu-id="f43fa-251">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="f43fa-252">6.1.0 — maj 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f43fa-252">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f43fa-253">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f43fa-253">AzureRM.Profile</span></span>
* <span data-ttu-id="f43fa-254">Rozwiązano problem polegający na tym, że po uruchomieniu polecenia „Clear-AzureRmContext” pozostawał pusty kontekst o nazwie takiej jak poprzedni kontekst domyślny, co uniemożliwiało użytkownikowi utworzenie nowego kontekstu ze starą nazwą</span><span class="sxs-lookup"><span data-stu-id="f43fa-254">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="f43fa-255">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f43fa-255">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="f43fa-256">Włączono operacje kojarzenia/usuwania skojarzenia bramy w usłudze AS.</span><span class="sxs-lookup"><span data-stu-id="f43fa-256">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f43fa-257">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f43fa-257">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f43fa-258">Dodano obsługę elementów ApiVersion, ApiRelease oraz ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f43fa-258">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="f43fa-259">Dodano obsługę zaplecza ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f43fa-259">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="f43fa-260">Dodano obsługę rejestratora usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="f43fa-260">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="f43fa-261">Dodano obsługę rozpoznawania jednostki SKU „Podstawowa” jako prawidłowej jednostki SKU usługi API Management</span><span class="sxs-lookup"><span data-stu-id="f43fa-261">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="f43fa-262">Dodano obsługę instalowania certyfikatów wystawionych przez prywatny urząd certyfikacji jako certyfikatów głównych lub certyfikatów urzędu certyfikacji</span><span class="sxs-lookup"><span data-stu-id="f43fa-262">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="f43fa-263">Dodano obsługę akceptowania niestandardowych certyfikatów SSL za pomocą magazynu kluczy i wielu nazw hostów serwera proxy</span><span class="sxs-lookup"><span data-stu-id="f43fa-263">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="f43fa-264">Dodano obsługę tożsamości MSI</span><span class="sxs-lookup"><span data-stu-id="f43fa-264">Added support for MSI identity</span></span>
* <span data-ttu-id="f43fa-265">Dodano obsługę akceptowania zasad za pomocą adresu URL. UWAGA: następujące polecenia cmdlet staną się przestarzałe w przyszłym wydaniu</span><span class="sxs-lookup"><span data-stu-id="f43fa-265">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="f43fa-266">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="f43fa-266">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="f43fa-267">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f43fa-267">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="f43fa-268">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="f43fa-268">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="f43fa-269">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="f43fa-269">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="f43fa-270">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="f43fa-270">AzureRM.Batch</span></span>
* <span data-ttu-id="f43fa-271">Wydano nowe polecenie cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="f43fa-271">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="f43fa-272">Wydano nowe polecenie cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="f43fa-272">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="f43fa-273">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="f43fa-273">AzureRM.Consumption</span></span>
* <span data-ttu-id="f43fa-274">Dodano nowe parametry polecenia cmdlet Get-AzureRmConsumptionUsageDetail: Expand, ResourceGroup, InstanceName, InstanceId, Tags oraz Top</span><span class="sxs-lookup"><span data-stu-id="f43fa-274">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f43fa-275">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f43fa-275">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f43fa-276">Poprawiono przykład dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="f43fa-276">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="f43fa-277">Rozwiązano problem powodujący wyjątek parametru o wartości null dla przypadku Recurse w poleceniu Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f43fa-277">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="f43fa-278">Poprawiono pliki pomocy dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl oraz Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f43fa-278">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="f43fa-279">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f43fa-279">AzureRM.Network</span></span>
* <span data-ttu-id="f43fa-280">Podniesiono wersję zestawu SDK sieci z 18.0.0-preview do 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="f43fa-280">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="f43fa-281">Dodano polecenie cmdlet służące do tworzenia konfiguracji protokołu</span><span class="sxs-lookup"><span data-stu-id="f43fa-281">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="f43fa-282">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f43fa-282">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="f43fa-283">Dodano polecenie cmdlet służące do dodawania nowego połączenia obwodu do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f43fa-283">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="f43fa-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f43fa-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="f43fa-285">Dodano polecenie cmdlet służące do usuwania połączenia obwodu z istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f43fa-285">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="f43fa-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f43fa-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="f43fa-287">Dodano polecenie cmdlet służące do pobierania połączenia obwodu</span><span class="sxs-lookup"><span data-stu-id="f43fa-287">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="f43fa-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f43fa-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f43fa-289">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f43fa-289">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f43fa-290">Naprawiono użycie uwierzytelniania serwera za pomocą wygenerowanych certyfikatów (problem nr 5998)</span><span class="sxs-lookup"><span data-stu-id="f43fa-290">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f43fa-291">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f43fa-291">AzureRM.Sql</span></span>
* <span data-ttu-id="f43fa-292">Zaktualizowano polecenia cmdlet inspekcji w celu umożliwienia usuwania elementów AuditAction lub AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="f43fa-292">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="f43fa-293">Rozwiązano problem z poleceniem Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, który powodował zakończenie polecenia niepowodzeniem podczas ustawiania nowych, elastycznych zasad przechowywania oraz zwrócenie komunikatu „Konfigurowanie zasad przechowywania długoterminowego za pomocą magazynu usługi Azure Recovery Service i zasad nie jest już obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="f43fa-293">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="f43fa-294">Prześlij żądanie z nowymi, elastycznymi zasadami przechowywania”.</span><span class="sxs-lookup"><span data-stu-id="f43fa-294">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="f43fa-295">Zaktualizowano wszystkie polecenia cmdlet służące do tworzenia/aktualizowania elastycznej puli/bazy danych usługi Azure SQL Database w taki sposób, aby korzystały z nowego interfejsu API bazy danych, który obsługuje właściwość SKU na potrzeby właściwości powiązanych ze skalowaniem i warstwą.</span><span class="sxs-lookup"><span data-stu-id="f43fa-295">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="f43fa-296">Zaktualizowane polecenia cmdlet to:</span><span class="sxs-lookup"><span data-stu-id="f43fa-296">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="f43fa-297">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f43fa-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="f43fa-298">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f43fa-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="f43fa-299">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f43fa-299">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="f43fa-300">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f43fa-300">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="f43fa-301">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f43fa-301">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f43fa-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f43fa-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f43fa-303">Zaktualizowano parametry polecenia „Get-AzureRmTrafficManagerProfile”, aby parametr -ResourceGroupName był wymagany, gdy został podany parametr -Name.</span><span class="sxs-lookup"><span data-stu-id="f43fa-303">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>