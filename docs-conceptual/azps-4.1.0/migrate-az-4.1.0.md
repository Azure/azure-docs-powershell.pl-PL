---
ms.openlocfilehash: 636fd0432d421f74fa74f3275abbc31ec5dc0b5c
ms.sourcegitcommit: 31f4facf815c2e25dc44e2fde0e1d2bd690bfc54
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/20/2020
ms.locfileid: "83688530"
---
# <a name="migration-guide-for-az-410"></a><span data-ttu-id="0b65d-101">Przewodnik migracji modułu Az 4.1.0</span><span class="sxs-lookup"><span data-stu-id="0b65d-101">Migration Guide for Az 4.1.0</span></span>

<span data-ttu-id="0b65d-102">Ten dokument zawiera opis różnic między wersjami 3.0.0 i 4.1.0 modułu Az.</span><span class="sxs-lookup"><span data-stu-id="0b65d-102">This document describes the changes between the 3.0.0 and 4.1.0 versions of Az.</span></span>

- [<span data-ttu-id="0b65d-103">Przewodnik migracji modułu Az 4.1.0</span><span class="sxs-lookup"><span data-stu-id="0b65d-103">Migration Guide for Az 4.1.0</span></span>](#migration-guide-for-az-410)
  - [<span data-ttu-id="0b65d-104">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b65d-104">Az.ApiManagement</span></span>](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [<span data-ttu-id="0b65d-105">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0b65d-105">Az.Batch</span></span>](#azbatch)
    - [<span data-ttu-id="0b65d-106">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="0b65d-106">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>](#get-azbatchapplication-new-azbatchapplication)
    - [<span data-ttu-id="0b65d-107">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="0b65d-107">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>](#get-azbatchcomputenode-new-azbatchpool)
    - [<span data-ttu-id="0b65d-108">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="0b65d-108">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [<span data-ttu-id="0b65d-109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b65d-109">Az.Compute</span></span>](#azcompute)
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
  - [<span data-ttu-id="0b65d-110">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b65d-110">Az.KeyVault</span></span>](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [<span data-ttu-id="0b65d-111">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0b65d-111">Az.Monitor</span></span>](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [<span data-ttu-id="0b65d-112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b65d-112">Az.Network</span></span>](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [<span data-ttu-id="0b65d-113">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0b65d-113">Az.OperationalInsights</span></span>](#azoperationalinsights)
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
  - [<span data-ttu-id="0b65d-114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b65d-114">Az.Resources</span></span>](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [<span data-ttu-id="0b65d-115">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b65d-115">Az.Storage</span></span>](#azstorage)
    - [<span data-ttu-id="0b65d-116">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="0b65d-116">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [<span data-ttu-id="0b65d-117">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="0b65d-117">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>](#new-azstoragetable-get-azstoragetable)
    - [<span data-ttu-id="0b65d-118">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="0b65d-118">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [<span data-ttu-id="0b65d-119">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="0b65d-119">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [<span data-ttu-id="0b65d-120">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="0b65d-120">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a><span data-ttu-id="0b65d-121">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b65d-121">Az.ApiManagement</span></span>

### `Add-AzApiManagementRegion`

<span data-ttu-id="0b65d-122">Typ właściwości `Type` typu `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` został zmieniony z `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` na `System.String`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-122">The type of property `Type` of type `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` has changed from `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` to `System.String`.</span></span>

### `New-AzApiManagement`

- <span data-ttu-id="0b65d-123">Polecenie cmdlet `New-AzApiManagement` nie obsługuje już parametru `AssignIdentity`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-123">The cmdlet `New-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="0b65d-124">Zestaw parametrów `__AllParameterSets` dla polecenia cmdlet `New-AzApiManagement` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="0b65d-124">The parameter set `__AllParameterSets` for cmdlet `New-AzApiManagement` has been removed.</span></span>

### `Set-AzApiManagement`

- <span data-ttu-id="0b65d-125">Polecenie cmdlet `Set-AzApiManagement` nie obsługuje już parametru `AssignIdentity`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-125">The cmdlet `Set-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="0b65d-126">Zestaw parametrów `__AllParameterSets` dla polecenia cmdlet `Set-AzApiManagement` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="0b65d-126">The parameter set `__AllParameterSets` for cmdlet `Set-AzApiManagement` has been removed.</span></span>

### `Get-AzApiManagementProperty`

<span data-ttu-id="0b65d-127">Polecenie cmdlet `Get-AzApiManagementProperty` zostało usunięte, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-127">The cmdlet `Get-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

### `New-AzApiManagementProperty`

<span data-ttu-id="0b65d-128">Polecenie cmdlet `New-AzApiManagementProperty` zostało usunięte, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-128">The cmdlet `New-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Remove-AzApiManagementProperty`

<span data-ttu-id="0b65d-129">Polecenie cmdlet `Remove-AzApiManagementProperty` zostało usunięte, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-129">The cmdlet `Remove-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Set-AzApiManagementProperty`

<span data-ttu-id="0b65d-130">Polecenie cmdlet `Set-AzApiManagementProperty` zostało usunięte, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-130">The cmdlet `Set-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

## <a name="azbatch"></a><span data-ttu-id="0b65d-131">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0b65d-131">Az.Batch</span></span>

### <a name="get-azbatchapplication-new-azbatchapplication"></a><span data-ttu-id="0b65d-132">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="0b65d-132">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>

<span data-ttu-id="0b65d-133">Właściwość `ApplicationPackages` typu `Microsoft.Azure.Commands.Batch.Models.PSApplication` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-133">The property `ApplicationPackages` of type `Microsoft.Azure.Commands.Batch.Models.PSApplication` has been removed.</span></span>

### <a name="get-azbatchcomputenode-new-azbatchpool"></a><span data-ttu-id="0b65d-134">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="0b65d-134">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>

<span data-ttu-id="0b65d-135">Właściwość `PublicIPs` typu `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` została usunięta</span><span class="sxs-lookup"><span data-stu-id="0b65d-135">The property `PublicIPs` of type `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` has been removed</span></span>

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a><span data-ttu-id="0b65d-136">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="0b65d-136">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>

<span data-ttu-id="0b65d-137">Typ właściwości `StorageUrlExpiry` typu `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` został zmieniony z `System.DateTime` na `System.DateTime?`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-137">The type of property `StorageUrlExpiry` of type `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` has changed from `System.DateTime` to `System.DateTime?`.</span></span>

## <a name="azcompute"></a><span data-ttu-id="0b65d-138">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b65d-138">Az.Compute</span></span>

### `Remove-AzVmssDiagnosticsExtension`

<span data-ttu-id="0b65d-139">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-139">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVMImage`

- <span data-ttu-id="0b65d-140">Polecenie cmdlet `Get-AzVMImage` nie obsługuje już parametru `FilterExpression`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-140">The cmdlet `Get-AzVMImage` no longer supports the parameter `FilterExpression` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="0b65d-141">Zestaw parametrów `ListVMImage` dla polecenia cmdlet `Get-AzVMImage` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="0b65d-141">The parameter set `ListVMImage` for cmdlet `Get-AzVMImage` has been removed.</span></span>

### `New-AzVMConfig`

- <span data-ttu-id="0b65d-142">Polecenie cmdlet `New-AzVMConfig` nie obsługuje już parametru `AssignIdentity`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-142">The cmdlet `New-AzVMConfig` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="0b65d-143">Zestaw parametrów `AssignIdentityParameterSet` dla polecenia cmdlet `New-AzVMConfig` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="0b65d-143">The parameter set `AssignIdentityParameterSet` for cmdlet `New-AzVMConfig` has been removed.</span></span>

### `Update-AzVM`

- <span data-ttu-id="0b65d-144">Polecenie cmdlet `Update-AzVM` nie obsługuje już parametru `AssignIdentity`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-144">The cmdlet `Update-AzVM` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="0b65d-145">Zestaw parametrów `AssignIdentityParameterSet` dla polecenia cmdlet `Update-AzVM` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="0b65d-145">The parameter set `AssignIdentityParameterSet` for cmdlet `Update-AzVM` has been removed.</span></span>

### `New-AzProximityPlacementGroup`

- <span data-ttu-id="0b65d-146">Typ ogólny właściwości `VirtualMachines`, `VirtualMachineScaleSets` i `AvailabilitySets` został zmieniony z `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` na `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-146">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="0b65d-147">Właściwość `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` i `AvailabilitySetsColocationStatus` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-147">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="0b65d-148">Przed</span><span class="sxs-lookup"><span data-stu-id="0b65d-148">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="0b65d-149">Po</span><span class="sxs-lookup"><span data-stu-id="0b65d-149">After</span></span>

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

- <span data-ttu-id="0b65d-150">Typ ogólny właściwości `VirtualMachines`, `VirtualMachineScaleSets` i `AvailabilitySets` został zmieniony z `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` na `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-150">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="0b65d-151">Właściwość `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` i `AvailabilitySetsColocationStatus` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-151">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="0b65d-152">Przed</span><span class="sxs-lookup"><span data-stu-id="0b65d-152">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="0b65d-153">Po</span><span class="sxs-lookup"><span data-stu-id="0b65d-153">After</span></span>

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

- <span data-ttu-id="0b65d-154">Typ ogólny właściwości `VirtualMachines`, `VirtualMachineScaleSets` i `AvailabilitySets` został zmieniony z `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` na `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-154">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="0b65d-155">Właściwość `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` i `AvailabilitySetsColocationStatus` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-155">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="0b65d-156">Przed</span><span class="sxs-lookup"><span data-stu-id="0b65d-156">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="0b65d-157">Po</span><span class="sxs-lookup"><span data-stu-id="0b65d-157">After</span></span>

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

<span data-ttu-id="0b65d-158">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-158">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssDataDisk`

<span data-ttu-id="0b65d-159">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-159">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssExtension`

<span data-ttu-id="0b65d-160">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-160">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="0b65d-161">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-161">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSecret`

<span data-ttu-id="0b65d-162">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-162">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSshPublicKey`

<span data-ttu-id="0b65d-163">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-163">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssWinRMListener`

<span data-ttu-id="0b65d-164">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-164">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmssConfig`

- <span data-ttu-id="0b65d-165">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-165">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="0b65d-166">Nie obsługuje już parametru `AutomaticRepairMaxInstanceRepairsPercent`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-166">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="0b65d-167">Nie obsługuje już parametru `AssignIdentity`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-167">No longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="0b65d-168">Zestaw parametrów `__AllParameterSets` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="0b65d-168">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="0b65d-169">Zestaw parametrów `ExplicitIdentityParameterSet` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="0b65d-169">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>
- <span data-ttu-id="0b65d-170">Zestaw parametrów `AssignIdentityParameterSet` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="0b65d-170">The parameter set `AssignIdentityParameterSet` has been removed.</span></span>

### `Remove-AzVmssDataDisk`

<span data-ttu-id="0b65d-171">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-171">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssExtension`

<span data-ttu-id="0b65d-172">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-172">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="0b65d-173">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-173">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssBootDiagnostic`

<span data-ttu-id="0b65d-174">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-174">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOsProfile`

<span data-ttu-id="0b65d-175">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-175">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssRollingUpgradePolicy`

<span data-ttu-id="0b65d-176">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-176">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssStorageProfile`

<span data-ttu-id="0b65d-177">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-177">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmss`

<span data-ttu-id="0b65d-178">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-178">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Repair-AzVmssServiceFabricUpdateDomain`

<span data-ttu-id="0b65d-179">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-179">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVmss`

<span data-ttu-id="0b65d-180">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-180">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOrchestrationServiceState`

<span data-ttu-id="0b65d-181">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-181">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Update-AzVmss`

- <span data-ttu-id="0b65d-182">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-182">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="0b65d-183">Nie obsługuje już parametru `AutomaticRepairMaxInstanceRepairsPercent`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-183">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="0b65d-184">Zestaw parametrów `__AllParameterSets` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="0b65d-184">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="0b65d-185">Zestaw parametrów `ExplicitIdentityParameterSet` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="0b65d-185">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>

### `Add-AzVmssDiagnosticsExtension`

<span data-ttu-id="0b65d-186">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-186">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Disable-AzVmssDiskEncryption`

<span data-ttu-id="0b65d-187">Typ właściwości `AutomaticRepairsPolicy` typu `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` został zmieniony z `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` na `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-187">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

## <a name="azkeyvault"></a><span data-ttu-id="0b65d-188">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b65d-188">Az.KeyVault</span></span>

### `New-AzKeyVaultCertificateOrganizationDetail`

<span data-ttu-id="0b65d-189">Alias `New-AzKeyVaultCertificateOrganizationDetails` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="0b65d-189">The alias `New-AzKeyVaultCertificateOrganizationDetails` is removed.</span></span> <span data-ttu-id="0b65d-190">Używaj `New-AzKeyVaultCertificateOrganizationDetail`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-190">Please use `New-AzKeyVaultCertificateOrganizationDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="0b65d-191">Przed</span><span class="sxs-lookup"><span data-stu-id="0b65d-191">Before</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a><span data-ttu-id="0b65d-192">Po</span><span class="sxs-lookup"><span data-stu-id="0b65d-192">After</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

<span data-ttu-id="0b65d-193">Alias `New-AzKeyVaultCertificateAdministratorDetails` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="0b65d-193">The alias `New-AzKeyVaultCertificateAdministratorDetails` is removed.</span></span> <span data-ttu-id="0b65d-194">Używaj `New-AzKeyVaultCertificateAdministratorDetail`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-194">Please use `New-AzKeyVaultCertificateAdministratorDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="0b65d-195">Przed</span><span class="sxs-lookup"><span data-stu-id="0b65d-195">Before</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a><span data-ttu-id="0b65d-196">Po</span><span class="sxs-lookup"><span data-stu-id="0b65d-196">After</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

<span data-ttu-id="0b65d-197">Polecenie `-EnableSoftDelete` jest usuwane, ponieważ usuwanie nietrwałe jest domyślnie włączone.</span><span class="sxs-lookup"><span data-stu-id="0b65d-197">`-EnableSoftDelete` is removed, as soft delete is enabled by default.</span></span> <span data-ttu-id="0b65d-198">Użyj `-DisableSoftDelete`, jeśli nie chcesz tego zachowania.</span><span class="sxs-lookup"><span data-stu-id="0b65d-198">Please use `-DisableSoftDelete` if you do not want this behavior.</span></span>

#### <a name="before"></a><span data-ttu-id="0b65d-199">Przed</span><span class="sxs-lookup"><span data-stu-id="0b65d-199">Before</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="0b65d-200">Po</span><span class="sxs-lookup"><span data-stu-id="0b65d-200">After</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a><span data-ttu-id="0b65d-201">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0b65d-201">Az.Monitor</span></span>

### `Add-AzLogProfile`

<span data-ttu-id="0b65d-202">Typ właściwości `RetentionPolicy` typu `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` został zmieniony z `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` na `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-202">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `Get-AzLogProfile`

<span data-ttu-id="0b65d-203">Typ właściwości `RetentionPolicy` typu `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` został zmieniony z `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` na `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-203">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `New-AzMetricAlertRuleV2Criteria`

<span data-ttu-id="0b65d-204">Zestaw parametrów `__AllParameterSets` dla polecenia cmdlet `New-AzMetricAlertRuleV2Criteria` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="0b65d-204">The parameter set `__AllParameterSets` for cmdlet `New-AzMetricAlertRuleV2Criteria` has been removed.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="0b65d-205">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b65d-205">Az.Network</span></span>

### `Get-AzNetworkWatcherConnectionMonitor`

<span data-ttu-id="0b65d-206">Typ ogólny właściwości `RoundTripTimeMs` został zmieniony z `System.Nullable1[System.Int32]` na `System.Nullable1[System.Double]`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-206">The generic type for property `RoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

<span data-ttu-id="0b65d-207">Typ ogólny parametru `SuccessThresholdRoundTripTimeMs` został zmieniony z `System.Nullable1[System.Int32]` na `System.Nullable1[System.Double]`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-207">The generic type for parameter `SuccessThresholdRoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

## <a name="azoperationalinsights"></a><span data-ttu-id="0b65d-208">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0b65d-208">Az.OperationalInsights</span></span>

### `Get-AzOperationalInsightsDataSource`

<span data-ttu-id="0b65d-209">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-209">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsApplicationInsightsDataSource`

<span data-ttu-id="0b65d-210">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-210">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsAzureActivityLogDataSource`

<span data-ttu-id="0b65d-211">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-211">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsCustomLogDataSource`

<span data-ttu-id="0b65d-212">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-212">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

<span data-ttu-id="0b65d-213">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-213">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxSyslogDataSource`

<span data-ttu-id="0b65d-214">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-214">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsEventDataSource`

<span data-ttu-id="0b65d-215">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-215">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

<span data-ttu-id="0b65d-216">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-216">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsDataSource`

<span data-ttu-id="0b65d-217">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-217">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="0b65d-218">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-218">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="0b65d-219">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-219">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="0b65d-220">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-220">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="0b65d-221">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-221">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="0b65d-222">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-222">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="0b65d-223">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-223">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="0b65d-224">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-224">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="0b65d-225">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-225">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearch`

<span data-ttu-id="0b65d-226">Właściwość `Metadata` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-226">The property `Metadata` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearchResult`

<span data-ttu-id="0b65d-227">Polecenie cmdlet `Get-AzOperationalInsightsSavedSearchResult` zostało usunięte, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-227">The cmdlet `Get-AzOperationalInsightsSavedSearchResult` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Get-AzOperationalInsightsSearchResult`

<span data-ttu-id="0b65d-228">Polecenie cmdlet `Get-AzOperationalInsightsSearchResult` zostało usunięte, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-228">The cmdlet `Get-AzOperationalInsightsSearchResult` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Get-AzOperationalInsightsStorageInsight`

<span data-ttu-id="0b65d-229">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-229">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsStorageInsight`

<span data-ttu-id="0b65d-230">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-230">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsStorageInsight`

<span data-ttu-id="0b65d-231">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-231">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsStorageInsight`

<span data-ttu-id="0b65d-232">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-232">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsLinkTarget`

<span data-ttu-id="0b65d-233">Polecenie cmdlet `Get-AzOperationalInsightsLinkTarget` zostało usunięte, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-233">The cmdlet `Get-AzOperationalInsightsLinkTarget` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Get-AzOperationalInsightsWorkspace`

<span data-ttu-id="0b65d-234">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-234">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWorkspace`

- <span data-ttu-id="0b65d-235">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-235">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>
- <span data-ttu-id="0b65d-236">Polecenie cmdlet `New-AzOperationalInsightsWorkspace` nie obsługuje już parametru `CustomerId`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="0b65d-236">The cmdlet `New-AzOperationalInsightsWorkspace` no longer supports the parameter `CustomerId` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="0b65d-237">Zestaw parametrów `__AllParameterSets` dla polecenia cmdlet `New-AzOperationalInsightsWorkspace` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="0b65d-237">The parameter set `__AllParameterSets` for cmdlet `New-AzOperationalInsightsWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsWorkspace`

<span data-ttu-id="0b65d-238">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-238">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Invoke-AzOperationalInsightsQuery`

<span data-ttu-id="0b65d-239">Właściwość `PortalUrl` typu `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b65d-239">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

## <a name="azresources"></a><span data-ttu-id="0b65d-240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b65d-240">Az.Resources</span></span>

### `Get-AzDeploymentScript`

<span data-ttu-id="0b65d-241">Typ właściwości `Status` typu `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` został zmieniony z `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` na `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-241">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzDeploymentScriptLog`

<span data-ttu-id="0b65d-242">Typ właściwości `Status` typu `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` został zmieniony z `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` na `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-242">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Save-AzDeploymentScriptLog`

<span data-ttu-id="0b65d-243">Typ właściwości `Status` typu `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` został zmieniony z `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` na `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-243">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

<span data-ttu-id="0b65d-244">Parametr `TenantLevel` został usunięty</span><span class="sxs-lookup"><span data-stu-id="0b65d-244">Parameter `TenantLevel` has been removed.</span></span>

### `Get-AzPolicyAlias`

<span data-ttu-id="0b65d-245">Typ ogólny właściwości `Aliases` został zmieniony z `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` na `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-245">The generic type for property `Aliases` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span></span>

### `New-AzPolicyAssignment`

- <span data-ttu-id="0b65d-246">Polecenie cmdlet `New-AzPolicyAssignment` nie obsługuje już typu `System.Management.Automation.PSObject` dla parametru `PolicyDefinition`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-246">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicyDefinition`.</span></span>
- <span data-ttu-id="0b65d-247">Polecenie cmdlet `New-AzPolicyAssignment` nie obsługuje już typu `System.Management.Automation.PSObject` dla parametru `PolicySetDefinition`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-247">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicySetDefinition`.</span></span>

### `Remove-AzDeploymentScript`

<span data-ttu-id="0b65d-248">Typ właściwości `Status` typu `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` został zmieniony z `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` na `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="0b65d-248">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

## <a name="azstorage"></a><span data-ttu-id="0b65d-249">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b65d-249">Az.Storage</span></span>

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a><span data-ttu-id="0b65d-250">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="0b65d-250">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>

<span data-ttu-id="0b65d-251">Zmieniono wartość elementu DefaultAction obiektu NetWorkRule z: Zezwól = 1, Odmów = 0, na: Zezwól = 0, Odmów = 1.</span><span class="sxs-lookup"><span data-stu-id="0b65d-251">Changed NetWorkRule DefaultAction value from: Allow = 1, Deny = 0, to: Allow = 0, Deny = 1.</span></span>

### <a name="new-azstoragetable-get-azstoragetable"></a><span data-ttu-id="0b65d-252">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="0b65d-252">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>

<span data-ttu-id="0b65d-253">Dla obiektu wyjściowego AzureStorageTable.CloudTable.ServiceClient usunięto 2 właściwości: ConnectionPolicy, ConsistencyLevel.</span><span class="sxs-lookup"><span data-stu-id="0b65d-253">Output object AzureStorageTable.CloudTable.ServiceClient have 2 properties removed: ConnectionPolicy, ConsistencyLevel.</span></span>

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a><span data-ttu-id="0b65d-254">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="0b65d-254">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>

<span data-ttu-id="0b65d-255">Zmieniono typ danych wyjściowych z CloudFile na AzureStorageFile. Oryginalne dane wyjściowe staną się właściwością podrzędną „CloudFile” nowych danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="0b65d-255">Change output type from CloudFile to AzureStorageFile, the original output will become child property "CloudFile" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="0b65d-256">Przed</span><span class="sxs-lookup"><span data-stu-id="0b65d-256">Before</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a><span data-ttu-id="0b65d-257">Po</span><span class="sxs-lookup"><span data-stu-id="0b65d-257">After</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a><span data-ttu-id="0b65d-258">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="0b65d-258">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>

<span data-ttu-id="0b65d-259">Zmieniono typ danych wyjściowych z CloudFileDirectory na AzureStorageFileDirectory. Oryginalne dane wyjściowe staną się właściwością podrzędną „CloudFileDirectory” nowych danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="0b65d-259">Change output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become child property "CloudFileDirectory" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="0b65d-260">Przed</span><span class="sxs-lookup"><span data-stu-id="0b65d-260">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="0b65d-261">Po</span><span class="sxs-lookup"><span data-stu-id="0b65d-261">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a><span data-ttu-id="0b65d-262">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="0b65d-262">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>

<span data-ttu-id="0b65d-263">Zmieniono typ danych wyjściowych z FileShareProperties na AzureStorageFileShare. Oryginalne dane wyjściowe staną się właściwością podrzędną „CloudFileShare” nowych danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="0b65d-263">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become child property "CloudFileShare" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="0b65d-264">Przed</span><span class="sxs-lookup"><span data-stu-id="0b65d-264">Before</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a><span data-ttu-id="0b65d-265">Po</span><span class="sxs-lookup"><span data-stu-id="0b65d-265">After</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

<span data-ttu-id="0b65d-266">Zmieniono typ danych wyjściowych z FileShareProperties na AzureStorageFileShare. Oryginalne dane wyjściowe staną się pomniejszoną właściwością podrzędną „CloudFileShare.Properties” nowych danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="0b65d-266">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become sub child property ""CloudFileShare.Properties"" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="0b65d-267">Przed</span><span class="sxs-lookup"><span data-stu-id="0b65d-267">Before</span></span>

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a><span data-ttu-id="0b65d-268">Po</span><span class="sxs-lookup"><span data-stu-id="0b65d-268">After</span></span>

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

<span data-ttu-id="0b65d-269">W przypadku usuwania podkatalogów plików za pomocą nadrzędnego obiektu katalogu i parametru -Path nie można już wprowadzać parametru -Path z potoku z dopasowaniem typu (ciąg).</span><span class="sxs-lookup"><span data-stu-id="0b65d-269">When removing sub File Directories with parent Directory object and -Path, Can't input -Path from pipeline with type (string) match anymore.</span></span>

#### <a name="before"></a><span data-ttu-id="0b65d-270">Przed</span><span class="sxs-lookup"><span data-stu-id="0b65d-270">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="0b65d-271">Po</span><span class="sxs-lookup"><span data-stu-id="0b65d-271">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
