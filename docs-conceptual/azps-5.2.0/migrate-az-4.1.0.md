---
title: Przewodnik migracji dla modułu Az 4.1.0
description: Ten przewodnik migracji zawiera listę zmian powodujących niezgodność wprowadzonych w wersji 4.1.0 modułu Az programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: fe4a2a7c2f1b171b530eef41ac072b2029be1026
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856771"
---
# <a name="migration-guide-for-az-410"></a><span data-ttu-id="2bd22-103">Przewodnik migracji modułu Az 4.1.0</span><span class="sxs-lookup"><span data-stu-id="2bd22-103">Migration Guide for Az 4.1.0</span></span>

<span data-ttu-id="2bd22-104">Ten dokument zawiera opis różnic między wersjami 3.0.0 i 4.1.0 modułu Az.</span><span class="sxs-lookup"><span data-stu-id="2bd22-104">This document describes the changes between the 3.0.0 and 4.1.0 versions of Az.</span></span>

- [<span data-ttu-id="2bd22-105">Przewodnik migracji modułu Az 4.1.0</span><span class="sxs-lookup"><span data-stu-id="2bd22-105">Migration Guide for Az 4.1.0</span></span>](#migration-guide-for-az-410)
  - [<span data-ttu-id="2bd22-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2bd22-106">Az.ApiManagement</span></span>](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [<span data-ttu-id="2bd22-107">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2bd22-107">Az.Batch</span></span>](#azbatch)
    - [<span data-ttu-id="2bd22-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="2bd22-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>](#get-azbatchapplication-new-azbatchapplication)
    - [<span data-ttu-id="2bd22-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="2bd22-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>](#get-azbatchcomputenode-new-azbatchpool)
    - [<span data-ttu-id="2bd22-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="2bd22-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [<span data-ttu-id="2bd22-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2bd22-111">Az.Compute</span></span>](#azcompute)
    - [`Remove-AzVmssDiagnosticsExtension`](#remove-azvmssdiagnosticsextension)
    - [`Get-AzVMImage`](#get-azvmimage)
    - [`New-AzVMConfig`](#new-azvmconfig)
    - [`Update-AzVM`](#update-azvm)
    - [`New-AzProximityPlacementGroup`](#new-azproximityplacementgroup)
    - [`Remove-AzProximityPlacementGroup`](#remove-azproximityplacementgroup)
    - [`Get-AzProximityPlacementGroup`](#get-azproximityplacementgroup)
    - [`Add-AzVmssAdditionalUnattendContent`](#add-azvmssadditionalunattendcontent)
    - [`Add-AzVmssDataDisk`](#add-azvmssdatadisk)
    - [`Add-AzVmssExtension`](#add-azvmssextension)
    - [`Add-AzVmssNetworkInterfaceConfiguration`](#add-azvmssnetworkinterfaceconfiguration)
    - [`Add-AzVmssSecret`](#add-azvmsssecret)
    - [`Add-AzVmssSshPublicKey`](#add-azvmsssshpublickey)
    - [`Add-AzVmssWinRMListener`](#add-azvmsswinrmlistener)
    - [`New-AzVmssConfig`](#new-azvmssconfig)
    - [`Remove-AzVmssDataDisk`](#remove-azvmssdatadisk)
    - [`Remove-AzVmssExtension`](#remove-azvmssextension)
    - [`Remove-AzVmssNetworkInterfaceConfiguration`](#remove-azvmssnetworkinterfaceconfiguration)
    - [`Set-AzVmssBootDiagnostic`](#set-azvmssbootdiagnostic)
    - [`Set-AzVmssOsProfile`](#set-azvmssosprofile)
    - [`Set-AzVmssRollingUpgradePolicy`](#set-azvmssrollingupgradepolicy)
    - [`Set-AzVmssStorageProfile`](#set-azvmssstorageprofile)
    - [`New-AzVmss`](#new-azvmss)
    - [`Repair-AzVmssServiceFabricUpdateDomain`](#repair-azvmssservicefabricupdatedomain)
    - [`Get-AzVmss`](#get-azvmss)
    - [`Set-AzVmssOrchestrationServiceState`](#set-azvmssorchestrationservicestate)
    - [`Update-AzVmss`](#update-azvmss)
    - [`Add-AzVmssDiagnosticsExtension`](#add-azvmssdiagnosticsextension)
    - [`Disable-AzVmssDiskEncryption`](#disable-azvmssdiskencryption)
  - [<span data-ttu-id="2bd22-112">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2bd22-112">Az.KeyVault</span></span>](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [<span data-ttu-id="2bd22-113">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2bd22-113">Az.Monitor</span></span>](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [<span data-ttu-id="2bd22-114">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2bd22-114">Az.Network</span></span>](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [<span data-ttu-id="2bd22-115">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2bd22-115">Az.OperationalInsights</span></span>](#azoperationalinsights)
    - [`Get-AzOperationalInsightsDataSource`](#get-azoperationalinsightsdatasource)
    - [`New-AzOperationalInsightsApplicationInsightsDataSource`](#new-azoperationalinsightsapplicationinsightsdatasource)
    - [`New-AzOperationalInsightsAzureActivityLogDataSource`](#new-azoperationalinsightsazureactivitylogdatasource)
    - [`New-AzOperationalInsightsCustomLogDataSource`](#new-azoperationalinsightscustomlogdatasource)
    - [`New-AzOperationalInsightsLinuxPerformanceObjectDataSource`](#new-azoperationalinsightslinuxperformanceobjectdatasource)
    - [`New-AzOperationalInsightsLinuxSyslogDataSource`](#new-azoperationalinsightslinuxsyslogdatasource)
    - [`New-AzOperationalInsightsWindowsEventDataSource`](#new-azoperationalinsightswindowseventdatasource)
    - [`New-AzOperationalInsightsWindowsPerformanceCounterDataSource`](#new-azoperationalinsightswindowsperformancecounterdatasource)
    - [`Remove-AzOperationalInsightsDataSource`](#remove-azoperationalinsightsdatasource)
    - [`Disable-AzOperationalInsightsIISLogCollection`](#disable-azoperationalinsightsiislogcollection)
    - [`Disable-AzOperationalInsightsLinuxCustomLogCollection`](#disable-azoperationalinsightslinuxcustomlogcollection)
    - [`Disable-AzOperationalInsightsLinuxPerformanceCollection`](#disable-azoperationalinsightslinuxperformancecollection)
    - [`Disable-AzOperationalInsightsLinuxSyslogCollection`](#disable-azoperationalinsightslinuxsyslogcollection)
    - [`Enable-AzOperationalInsightsIISLogCollection`](#enable-azoperationalinsightsiislogcollection)
    - [`Enable-AzOperationalInsightsLinuxCustomLogCollection`](#enable-azoperationalinsightslinuxcustomlogcollection)
    - [`Enable-AzOperationalInsightsLinuxPerformanceCollection`](#enable-azoperationalinsightslinuxperformancecollection)
    - [`Enable-AzOperationalInsightsLinuxSyslogCollection`](#enable-azoperationalinsightslinuxsyslogcollection)
    - [`Get-AzOperationalInsightsSavedSearch`](#get-azoperationalinsightssavedsearch)
    - [`Get-AzOperationalInsightsSavedSearchResult`](#get-azoperationalinsightssavedsearchresult)
    - [`Get-AzOperationalInsightsSearchResult`](#get-azoperationalinsightssearchresult)
    - [`Get-AzOperationalInsightsStorageInsight`](#get-azoperationalinsightsstorageinsight)
    - [`New-AzOperationalInsightsStorageInsight`](#new-azoperationalinsightsstorageinsight)
    - [`Remove-AzOperationalInsightsStorageInsight`](#remove-azoperationalinsightsstorageinsight)
    - [`Set-AzOperationalInsightsStorageInsight`](#set-azoperationalinsightsstorageinsight)
    - [`Get-AzOperationalInsightsLinkTarget`](#get-azoperationalinsightslinktarget)
    - [`Get-AzOperationalInsightsWorkspace`](#get-azoperationalinsightsworkspace)
    - [`New-AzOperationalInsightsWorkspace`](#new-azoperationalinsightsworkspace)
    - [`Set-AzOperationalInsightsWorkspace`](#set-azoperationalinsightsworkspace)
    - [`Invoke-AzOperationalInsightsQuery`](#invoke-azoperationalinsightsquery)
  - [<span data-ttu-id="2bd22-116">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2bd22-116">Az.Resources</span></span>](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [<span data-ttu-id="2bd22-117">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2bd22-117">Az.Storage</span></span>](#azstorage)
    - [<span data-ttu-id="2bd22-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="2bd22-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [<span data-ttu-id="2bd22-119">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="2bd22-119">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>](#new-azstoragetable-get-azstoragetable)
    - [<span data-ttu-id="2bd22-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="2bd22-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [<span data-ttu-id="2bd22-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="2bd22-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [<span data-ttu-id="2bd22-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="2bd22-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a><span data-ttu-id="2bd22-123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2bd22-123">Az.ApiManagement</span></span>

### `Add-AzApiManagementRegion`

<span data-ttu-id="2bd22-124">Typ właściwości `Type` typu `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` został zmieniony z `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` na `System.String`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-124">The type of property `Type` of type `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` has changed from `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` to `System.String`.</span></span>

### `New-AzApiManagement`

- <span data-ttu-id="2bd22-125">Polecenie cmdlet `New-AzApiManagement` nie obsługuje już parametru `AssignIdentity`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="2bd22-125">The cmdlet `New-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="2bd22-126">Zestaw parametrów `__AllParameterSets` dla polecenia cmdlet `New-AzApiManagement` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="2bd22-126">The parameter set `__AllParameterSets` for cmdlet `New-AzApiManagement` has been removed.</span></span>

### `Set-AzApiManagement`

- <span data-ttu-id="2bd22-127">Polecenie cmdlet `Set-AzApiManagement` nie obsługuje już parametru `AssignIdentity`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="2bd22-127">The cmdlet `Set-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="2bd22-128">Zestaw parametrów `__AllParameterSets` dla polecenia cmdlet `Set-AzApiManagement` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="2bd22-128">The parameter set `__AllParameterSets` for cmdlet `Set-AzApiManagement` has been removed.</span></span>

### `Get-AzApiManagementProperty`

<span data-ttu-id="2bd22-129">Polecenie cmdlet `Get-AzApiManagementProperty` zostało zastąpione przez polecenie `Get-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-129">The cmdlet `Get-AzApiManagementProperty` has been replaced by `Get-AzApiManagementNamedValue`.</span></span>

### `New-AzApiManagementProperty`

<span data-ttu-id="2bd22-130">Polecenie cmdlet `New-AzApiManagementProperty` zostało zastąpione przez polecenie `New-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-130">The cmdlet `New-AzApiManagementProperty` has been replaced by `New-AzApiManagementNamedValue`.</span></span>

### `Remove-AzApiManagementProperty`

<span data-ttu-id="2bd22-131">Polecenie cmdlet `Remove-AzApiManagementProperty` zostało zastąpione przez polecenie `Remove-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-131">The cmdlet `Remove-AzApiManagementProperty` has been replaced by `Remove-AzApiManagementNamedValue`.</span></span>

### `Set-AzApiManagementProperty`

<span data-ttu-id="2bd22-132">Polecenie cmdlet `Set-AzApiManagementProperty` zostało zastąpione przez polecenie `Set-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-132">The cmdlet `Set-AzApiManagementProperty` has been replaced by `Set-AzApiManagementNamedValue`.</span></span>

## <a name="azbatch"></a><span data-ttu-id="2bd22-133">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2bd22-133">Az.Batch</span></span>

### <a name="get-azbatchapplication-new-azbatchapplication"></a><span data-ttu-id="2bd22-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="2bd22-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>

<span data-ttu-id="2bd22-135">Właściwość `ApplicationPackages` typu `Microsoft.Azure.Commands.Batch.Models.PSApplication` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-135">The property `ApplicationPackages` of type `Microsoft.Azure.Commands.Batch.Models.PSApplication` has been removed.</span></span>

### <a name="get-azbatchcomputenode-new-azbatchpool"></a><span data-ttu-id="2bd22-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="2bd22-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>

<span data-ttu-id="2bd22-137">Właściwość `PublicIPs` typu `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` została usunięta</span><span class="sxs-lookup"><span data-stu-id="2bd22-137">The property `PublicIPs` of type `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` has been removed</span></span>

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a><span data-ttu-id="2bd22-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="2bd22-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>

<span data-ttu-id="2bd22-139">Typ właściwości `StorageUrlExpiry` typu `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` został zmieniony z `System.DateTime` na `System.DateTime?`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-139">The type of property `StorageUrlExpiry` of type `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` has changed from `System.DateTime` to `System.DateTime?`.</span></span>

## <a name="azcompute"></a><span data-ttu-id="2bd22-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2bd22-140">Az.Compute</span></span>

### `Remove-AzVmssDiagnosticsExtension`

<span data-ttu-id="2bd22-141">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-141">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVMImage`

- <span data-ttu-id="2bd22-142">Polecenie cmdlet `Get-AzVMImage` nie obsługuje już parametru `FilterExpression`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="2bd22-142">The cmdlet `Get-AzVMImage` no longer supports the parameter `FilterExpression` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="2bd22-143">Zestaw parametrów `ListVMImage` dla polecenia cmdlet `Get-AzVMImage` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="2bd22-143">The parameter set `ListVMImage` for cmdlet `Get-AzVMImage` has been removed.</span></span>

### `New-AzVMConfig`

- <span data-ttu-id="2bd22-144">Polecenie cmdlet `New-AzVMConfig` nie obsługuje już parametru `AssignIdentity`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="2bd22-144">The cmdlet `New-AzVMConfig` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="2bd22-145">Zestaw parametrów `AssignIdentityParameterSet` dla polecenia cmdlet `New-AzVMConfig` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="2bd22-145">The parameter set `AssignIdentityParameterSet` for cmdlet `New-AzVMConfig` has been removed.</span></span>

### `Update-AzVM`

- <span data-ttu-id="2bd22-146">Polecenie cmdlet `Update-AzVM` nie obsługuje już parametru `AssignIdentity`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="2bd22-146">The cmdlet `Update-AzVM` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="2bd22-147">Zestaw parametrów `AssignIdentityParameterSet` dla polecenia cmdlet `Update-AzVM` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="2bd22-147">The parameter set `AssignIdentityParameterSet` for cmdlet `Update-AzVM` has been removed.</span></span>

### `New-AzProximityPlacementGroup`

- <span data-ttu-id="2bd22-148">Typ ogólny właściwości `VirtualMachines`, `VirtualMachineScaleSets` i `AvailabilitySets` został zmieniony z `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` na `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-148">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="2bd22-149">Właściwość `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` i `AvailabilitySetsColocationStatus` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-149">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="2bd22-150">Przed</span><span class="sxs-lookup"><span data-stu-id="2bd22-150">Before</span></span>

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="2bd22-151">Po</span><span class="sxs-lookup"><span data-stu-id="2bd22-151">After</span></span>

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Remove-AzProximityPlacementGroup`

- <span data-ttu-id="2bd22-152">Typ ogólny właściwości `VirtualMachines`, `VirtualMachineScaleSets` i `AvailabilitySets` został zmieniony z `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` na `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-152">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="2bd22-153">Właściwość `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` i `AvailabilitySetsColocationStatus` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-153">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="2bd22-154">Przed</span><span class="sxs-lookup"><span data-stu-id="2bd22-154">Before</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="2bd22-155">Po</span><span class="sxs-lookup"><span data-stu-id="2bd22-155">After</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Get-AzProximityPlacementGroup`

- <span data-ttu-id="2bd22-156">Typ ogólny właściwości `VirtualMachines`, `VirtualMachineScaleSets` i `AvailabilitySets` został zmieniony z `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` na `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-156">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="2bd22-157">Właściwość `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` i `AvailabilitySetsColocationStatus` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-157">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="2bd22-158">Przed</span><span class="sxs-lookup"><span data-stu-id="2bd22-158">Before</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="2bd22-159">Po</span><span class="sxs-lookup"><span data-stu-id="2bd22-159">After</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Add-AzVmssAdditionalUnattendContent`

<span data-ttu-id="2bd22-160">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-160">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssDataDisk`

<span data-ttu-id="2bd22-161">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-161">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssExtension`

<span data-ttu-id="2bd22-162">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-162">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="2bd22-163">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-163">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSecret`

<span data-ttu-id="2bd22-164">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-164">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSshPublicKey`

<span data-ttu-id="2bd22-165">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-165">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssWinRMListener`

<span data-ttu-id="2bd22-166">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-166">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmssConfig`

- <span data-ttu-id="2bd22-167">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-167">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="2bd22-168">Nie obsługuje już parametru `AutomaticRepairMaxInstanceRepairsPercent`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="2bd22-168">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="2bd22-169">Nie obsługuje już parametru `AssignIdentity`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="2bd22-169">No longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="2bd22-170">Zestaw parametrów `__AllParameterSets` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="2bd22-170">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="2bd22-171">Zestaw parametrów `ExplicitIdentityParameterSet` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="2bd22-171">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>
- <span data-ttu-id="2bd22-172">Zestaw parametrów `AssignIdentityParameterSet` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="2bd22-172">The parameter set `AssignIdentityParameterSet` has been removed.</span></span>

### `Remove-AzVmssDataDisk`

<span data-ttu-id="2bd22-173">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-173">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssExtension`

<span data-ttu-id="2bd22-174">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-174">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="2bd22-175">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-175">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssBootDiagnostic`

<span data-ttu-id="2bd22-176">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-176">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOsProfile`

<span data-ttu-id="2bd22-177">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-177">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssRollingUpgradePolicy`

<span data-ttu-id="2bd22-178">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-178">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssStorageProfile`

<span data-ttu-id="2bd22-179">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-179">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmss`

<span data-ttu-id="2bd22-180">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-180">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Repair-AzVmssServiceFabricUpdateDomain`

<span data-ttu-id="2bd22-181">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-181">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVmss`

<span data-ttu-id="2bd22-182">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-182">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOrchestrationServiceState`

<span data-ttu-id="2bd22-183">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-183">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Update-AzVmss`

- <span data-ttu-id="2bd22-184">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-184">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="2bd22-185">Nie obsługuje już parametru `AutomaticRepairMaxInstanceRepairsPercent`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="2bd22-185">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="2bd22-186">Zestaw parametrów `__AllParameterSets` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="2bd22-186">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="2bd22-187">Zestaw parametrów `ExplicitIdentityParameterSet` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="2bd22-187">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>

### `Add-AzVmssDiagnosticsExtension`

<span data-ttu-id="2bd22-188">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-188">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Disable-AzVmssDiskEncryption`

<span data-ttu-id="2bd22-189">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-189">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

## <a name="azkeyvault"></a><span data-ttu-id="2bd22-190">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2bd22-190">Az.KeyVault</span></span>

### `New-AzKeyVaultCertificateOrganizationDetail`

<span data-ttu-id="2bd22-191">Alias `New-AzKeyVaultCertificateOrganizationDetails` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="2bd22-191">The alias `New-AzKeyVaultCertificateOrganizationDetails` is removed.</span></span> <span data-ttu-id="2bd22-192">Używaj `New-AzKeyVaultCertificateOrganizationDetail`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-192">Please use `New-AzKeyVaultCertificateOrganizationDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="2bd22-193">Przed</span><span class="sxs-lookup"><span data-stu-id="2bd22-193">Before</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a><span data-ttu-id="2bd22-194">Po</span><span class="sxs-lookup"><span data-stu-id="2bd22-194">After</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

<span data-ttu-id="2bd22-195">Alias `New-AzKeyVaultCertificateAdministratorDetails` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="2bd22-195">The alias `New-AzKeyVaultCertificateAdministratorDetails` is removed.</span></span> <span data-ttu-id="2bd22-196">Używaj `New-AzKeyVaultCertificateAdministratorDetail`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-196">Please use `New-AzKeyVaultCertificateAdministratorDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="2bd22-197">Przed</span><span class="sxs-lookup"><span data-stu-id="2bd22-197">Before</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a><span data-ttu-id="2bd22-198">Po</span><span class="sxs-lookup"><span data-stu-id="2bd22-198">After</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

<span data-ttu-id="2bd22-199">Polecenie `-EnableSoftDelete` jest usuwane, ponieważ usuwanie nietrwałe jest domyślnie włączone.</span><span class="sxs-lookup"><span data-stu-id="2bd22-199">`-EnableSoftDelete` is removed, as soft delete is enabled by default.</span></span> <span data-ttu-id="2bd22-200">Użyj `-DisableSoftDelete`, jeśli nie chcesz tego zachowania.</span><span class="sxs-lookup"><span data-stu-id="2bd22-200">Please use `-DisableSoftDelete` if you do not want this behavior.</span></span>

#### <a name="before"></a><span data-ttu-id="2bd22-201">Przed</span><span class="sxs-lookup"><span data-stu-id="2bd22-201">Before</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="2bd22-202">Po</span><span class="sxs-lookup"><span data-stu-id="2bd22-202">After</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a><span data-ttu-id="2bd22-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2bd22-203">Az.Monitor</span></span>

### `Add-AzLogProfile`

<span data-ttu-id="2bd22-204">Typ właściwości `RetentionPolicy` typu `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` został zmieniony z `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` na `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-204">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `Get-AzLogProfile`

<span data-ttu-id="2bd22-205">Typ właściwości `RetentionPolicy` typu `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` został zmieniony z `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` na `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-205">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `New-AzMetricAlertRuleV2Criteria`

<span data-ttu-id="2bd22-206">Zestaw parametrów `__AllParameterSets` dla polecenia cmdlet `New-AzMetricAlertRuleV2Criteria` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="2bd22-206">The parameter set `__AllParameterSets` for cmdlet `New-AzMetricAlertRuleV2Criteria` has been removed.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="2bd22-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2bd22-207">Az.Network</span></span>

### `Get-AzNetworkWatcherConnectionMonitor`

<span data-ttu-id="2bd22-208">Typ ogólny właściwości `RoundTripTimeMs` został zmieniony z `System.Nullable1[System.Int32]` na `System.Nullable1[System.Double]`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-208">The generic type for property `RoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

<span data-ttu-id="2bd22-209">Typ ogólny parametru `SuccessThresholdRoundTripTimeMs` został zmieniony z `System.Nullable1[System.Int32]` na `System.Nullable1[System.Double]`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-209">The generic type for parameter `SuccessThresholdRoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

## <a name="azoperationalinsights"></a><span data-ttu-id="2bd22-210">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2bd22-210">Az.OperationalInsights</span></span>

### `Get-AzOperationalInsightsDataSource`

<span data-ttu-id="2bd22-211">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-211">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsApplicationInsightsDataSource`

<span data-ttu-id="2bd22-212">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-212">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsAzureActivityLogDataSource`

<span data-ttu-id="2bd22-213">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-213">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsCustomLogDataSource`

<span data-ttu-id="2bd22-214">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-214">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

<span data-ttu-id="2bd22-215">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-215">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxSyslogDataSource`

<span data-ttu-id="2bd22-216">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-216">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsEventDataSource`

<span data-ttu-id="2bd22-217">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-217">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

<span data-ttu-id="2bd22-218">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-218">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsDataSource`

<span data-ttu-id="2bd22-219">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-219">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="2bd22-220">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-220">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="2bd22-221">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-221">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="2bd22-222">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-222">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="2bd22-223">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-223">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="2bd22-224">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-224">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="2bd22-225">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-225">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="2bd22-226">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-226">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="2bd22-227">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-227">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearch`

<span data-ttu-id="2bd22-228">Właściwość `Metadata` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-228">The property `Metadata` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearchResult`

<span data-ttu-id="2bd22-229">Polecenie cmdlet `Get-AzOperationalInsightsSavedSearchResult` nie było już obsługiwane przez zestaw SDK i zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="2bd22-229">The cmdlet `Get-AzOperationalInsightsSavedSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsSearchResult`

<span data-ttu-id="2bd22-230">Polecenie cmdlet `Get-AzOperationalInsightsSearchResult` nie było już obsługiwane przez zestaw SDK i zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="2bd22-230">The cmdlet `Get-AzOperationalInsightsSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsStorageInsight`

<span data-ttu-id="2bd22-231">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-231">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsStorageInsight`

<span data-ttu-id="2bd22-232">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-232">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsStorageInsight`

<span data-ttu-id="2bd22-233">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-233">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsStorageInsight`

<span data-ttu-id="2bd22-234">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-234">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsLinkTarget`

<span data-ttu-id="2bd22-235">Polecenie cmdlet `Get-AzOperationalInsightsLinkTarget` nie było już obsługiwane przez zestaw SDK i zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="2bd22-235">The cmdlet `Get-AzOperationalInsightsLinkTarget` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsWorkspace`

<span data-ttu-id="2bd22-236">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-236">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWorkspace`

- <span data-ttu-id="2bd22-237">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-237">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>
- <span data-ttu-id="2bd22-238">Polecenie cmdlet `New-AzOperationalInsightsWorkspace` nie obsługuje już parametru `CustomerId`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="2bd22-238">The cmdlet `New-AzOperationalInsightsWorkspace` no longer supports the parameter `CustomerId` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="2bd22-239">Zestaw parametrów `__AllParameterSets` dla polecenia cmdlet `New-AzOperationalInsightsWorkspace` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="2bd22-239">The parameter set `__AllParameterSets` for cmdlet `New-AzOperationalInsightsWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsWorkspace`

<span data-ttu-id="2bd22-240">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-240">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Invoke-AzOperationalInsightsQuery`

<span data-ttu-id="2bd22-241">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="2bd22-241">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

## <a name="azresources"></a><span data-ttu-id="2bd22-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2bd22-242">Az.Resources</span></span>

### `Get-AzDeploymentScript`

<span data-ttu-id="2bd22-243">Typ właściwości `Status` typu `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` został zmieniony z `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` na `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-243">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzDeploymentScriptLog`

<span data-ttu-id="2bd22-244">Typ właściwości `Status` typu `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` został zmieniony z `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` na `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-244">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Save-AzDeploymentScriptLog`

<span data-ttu-id="2bd22-245">Typ właściwości `Status` typu `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` został zmieniony z `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` na `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-245">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

<span data-ttu-id="2bd22-246">Parametr `TenantLevel` został usunięty</span><span class="sxs-lookup"><span data-stu-id="2bd22-246">Parameter `TenantLevel` has been removed.</span></span>

### `Get-AzPolicyAlias`

<span data-ttu-id="2bd22-247">Typ ogólny właściwości `Aliases` został zmieniony z `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` na `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-247">The generic type for property `Aliases` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span></span>

### `New-AzPolicyAssignment`

- <span data-ttu-id="2bd22-248">Polecenie cmdlet `New-AzPolicyAssignment` nie obsługuje już typu `System.Management.Automation.PSObject` dla parametru `PolicyDefinition`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-248">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicyDefinition`.</span></span>
- <span data-ttu-id="2bd22-249">Polecenie cmdlet `New-AzPolicyAssignment` nie obsługuje już typu `System.Management.Automation.PSObject` dla parametru `PolicySetDefinition`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-249">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicySetDefinition`.</span></span>

### `Remove-AzDeploymentScript`

<span data-ttu-id="2bd22-250">Typ właściwości `Status` typu `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` został zmieniony z `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` na `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="2bd22-250">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

## <a name="azstorage"></a><span data-ttu-id="2bd22-251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2bd22-251">Az.Storage</span></span>

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a><span data-ttu-id="2bd22-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="2bd22-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>

<span data-ttu-id="2bd22-253">Zmieniono wartość elementu DefaultAction obiektu NetWorkRule z: Zezwól = 1, Odmów = 0, na: Zezwól = 0, Odmów = 1.</span><span class="sxs-lookup"><span data-stu-id="2bd22-253">Changed NetWorkRule DefaultAction value from: Allow = 1, Deny = 0, to: Allow = 0, Deny = 1.</span></span>

### <a name="new-azstoragetable-get-azstoragetable"></a><span data-ttu-id="2bd22-254">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="2bd22-254">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>

<span data-ttu-id="2bd22-255">Dla obiektu wyjściowego AzureStorageTable.CloudTable.ServiceClient usunięto 2 właściwości: ConnectionPolicy, ConsistencyLevel.</span><span class="sxs-lookup"><span data-stu-id="2bd22-255">Output object AzureStorageTable.CloudTable.ServiceClient have 2 properties removed: ConnectionPolicy, ConsistencyLevel.</span></span>

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a><span data-ttu-id="2bd22-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="2bd22-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>

<span data-ttu-id="2bd22-257">Zmieniono typ danych wyjściowych z CloudFile na AzureStorageFile. Oryginalne dane wyjściowe staną się właściwością podrzędną „CloudFile” nowych danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="2bd22-257">Change output type from CloudFile to AzureStorageFile, the original output will become child property "CloudFile" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="2bd22-258">Przed</span><span class="sxs-lookup"><span data-stu-id="2bd22-258">Before</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a><span data-ttu-id="2bd22-259">Po</span><span class="sxs-lookup"><span data-stu-id="2bd22-259">After</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a><span data-ttu-id="2bd22-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="2bd22-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>

<span data-ttu-id="2bd22-261">Zmieniono typ danych wyjściowych z CloudFileDirectory na AzureStorageFileDirectory. Oryginalne dane wyjściowe staną się właściwością podrzędną „CloudFileDirectory” nowych danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="2bd22-261">Change output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become child property "CloudFileDirectory" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="2bd22-262">Przed</span><span class="sxs-lookup"><span data-stu-id="2bd22-262">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="2bd22-263">Po</span><span class="sxs-lookup"><span data-stu-id="2bd22-263">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a><span data-ttu-id="2bd22-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="2bd22-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>

<span data-ttu-id="2bd22-265">Zmieniono typ danych wyjściowych z FileShareProperties na AzureStorageFileShare. Oryginalne dane wyjściowe staną się właściwością podrzędną „CloudFileShare” nowych danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="2bd22-265">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become child property "CloudFileShare" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="2bd22-266">Przed</span><span class="sxs-lookup"><span data-stu-id="2bd22-266">Before</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a><span data-ttu-id="2bd22-267">Po</span><span class="sxs-lookup"><span data-stu-id="2bd22-267">After</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

<span data-ttu-id="2bd22-268">Zmieniono typ danych wyjściowych z FileShareProperties na AzureStorageFileShare. Oryginalne dane wyjściowe staną się pomniejszoną właściwością podrzędną „CloudFileShare.Properties” nowych danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="2bd22-268">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become sub child property ""CloudFileShare.Properties"" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="2bd22-269">Przed</span><span class="sxs-lookup"><span data-stu-id="2bd22-269">Before</span></span>

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a><span data-ttu-id="2bd22-270">Po</span><span class="sxs-lookup"><span data-stu-id="2bd22-270">After</span></span>

```powershell
PS C:\> $share = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $share

   File End Point: https://weiors1.file.core.windows.net/

Name     QuotaGiB LastModified                IsSnapshot SnapshotTime
----     -------- ------------                ---------- ------------
weitest1 100      5/11/2020 3:03:30 PM +00:00 False

PS C:\> $share.CloudFileShare.Properties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

### `Remove-AzStorageDirectory`

<span data-ttu-id="2bd22-271">W przypadku usuwania podkatalogów plików za pomocą nadrzędnego obiektu katalogu i parametru -Path nie można już wprowadzać parametru -Path z potoku z dopasowaniem typu (ciąg).</span><span class="sxs-lookup"><span data-stu-id="2bd22-271">When removing sub File Directories with parent Directory object and -Path, Can't input -Path from pipeline with type (string) match anymore.</span></span>

#### <a name="before"></a><span data-ttu-id="2bd22-272">Przed</span><span class="sxs-lookup"><span data-stu-id="2bd22-272">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="2bd22-273">Po</span><span class="sxs-lookup"><span data-stu-id="2bd22-273">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
