---
title: Przewodnik migracji dla modułu Az 5.0.0
description: Ten przewodnik migracji zawiera listę zmian powodujących niezgodność wprowadzonych w wersji 5.0.0 modułu Az programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 3a82e738bcb652ddc38886f7064e7373b5fb8cc1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92754125"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="8d14e-103">Przewodnik migracji dla modułu Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="8d14e-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="8d14e-104">Ten dokument zawiera opis różnic między wersjami 4.0.0 i 5.0.0 modułu Az.</span><span class="sxs-lookup"><span data-stu-id="8d14e-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="8d14e-105">Przewodnik migracji dla modułu Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="8d14e-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="8d14e-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8d14e-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="8d14e-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="8d14e-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="8d14e-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="8d14e-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="8d14e-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8d14e-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="8d14e-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8d14e-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="8d14e-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="8d14e-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="8d14e-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="8d14e-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="8d14e-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="8d14e-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="8d14e-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d14e-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="8d14e-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d14e-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="8d14e-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d14e-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="8d14e-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8d14e-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="8d14e-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8d14e-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="8d14e-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="8d14e-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="8d14e-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="8d14e-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="8d14e-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="8d14e-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="8d14e-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="8d14e-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="8d14e-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="8d14e-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="8d14e-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="8d14e-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8d14e-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="8d14e-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="8d14e-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8d14e-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="8d14e-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8d14e-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="8d14e-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="8d14e-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8d14e-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="8d14e-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="8d14e-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="8d14e-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="8d14e-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="8d14e-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="8d14e-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="8d14e-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8d14e-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="8d14e-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8d14e-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="8d14e-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8d14e-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="8d14e-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="8d14e-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="8d14e-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="8d14e-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="8d14e-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="8d14e-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="8d14e-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="8d14e-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8d14e-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="8d14e-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8d14e-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="8d14e-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="8d14e-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="8d14e-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8d14e-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="8d14e-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="8d14e-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="8d14e-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8d14e-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="8d14e-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8d14e-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="8d14e-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d14e-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="8d14e-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8d14e-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="8d14e-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="8d14e-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="8d14e-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8d14e-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="8d14e-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8d14e-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="8d14e-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d14e-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="8d14e-162">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d14e-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="8d14e-163">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d14e-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="8d14e-164">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d14e-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="8d14e-165">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d14e-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="8d14e-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d14e-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="8d14e-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="8d14e-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="8d14e-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8d14e-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="8d14e-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="8d14e-169">New-AzAksCluster</span></span>

- <span data-ttu-id="8d14e-170">Nie obsługuje już parametru `NodeOsType`, a alias nazwy oryginalnego parametru nie został znaleziony, zawsze będzie to `Linux`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="8d14e-171">Nie obsługuje już aliasu `ClientIdAndSecret` dla parametru `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="8d14e-172">Wartość domyślna parametru `NodeVmSetType` została zmieniona z `AvailabilitySet` na `VirtualMachineScaleSets`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="8d14e-173">Wartość domyślna parametru `NetworkPlugin` została zmieniona z `none` na `azure`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-174">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="8d14e-175">Nowy adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="8d14e-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="8d14e-176">Set-AzAksCluster</span></span>

<span data-ttu-id="8d14e-177">Nie obsługuje już aliasu `ClientIdAndSecret` dla parametru `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-178">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="8d14e-179">Nowy adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="8d14e-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8d14e-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="8d14e-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8d14e-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="8d14e-182">Nie obsługuje już parametru `StorageAccountName`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="8d14e-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-183">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="8d14e-184">Nowy adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-184">After</span></span>

<span data-ttu-id="8d14e-185">Element `Classic` został uznany za przestarzały i parametr `StorageAccountName` został usunięty, ponieważ działa tylko z klasycznym rejestrem kontenerów.</span><span class="sxs-lookup"><span data-stu-id="8d14e-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="8d14e-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="8d14e-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="8d14e-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="8d14e-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="8d14e-188">Usunięto parametr przełącznika `IncludeSlot` ze wszystkich zestawów parametrów oprócz jednego: `Get-AzFunctionApp`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="8d14e-189">Polecenie cmdlet obsługuje teraz pobieranie miejsc wdrożenia w wynikach, gdy określono `-IncludeSlot`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="8d14e-190">Ta funkcja była uszkodzona w poprzedniej wersji polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d14e-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="8d14e-191">Jednak teraz jest to naprawione.</span><span class="sxs-lookup"><span data-stu-id="8d14e-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="8d14e-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="8d14e-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="8d14e-193">Naprawiono opcję `-DisableApplicationInsights` w poleceniu `New-AzFunctionApp`, dzięki czemu nie jest tworzony projekt usługi Application Insights, gdy określono tę opcję.</span><span class="sxs-lookup"><span data-stu-id="8d14e-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="8d14e-194">Usunięto obsługę tworzenia aplikacji funkcji programu PowerShell 6.2, ponieważ okres obsługi programu PowerShell 6.2 został zakończony.</span><span class="sxs-lookup"><span data-stu-id="8d14e-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="8d14e-195">Bieżącą wytyczną dla klientów jest utworzenie zamiast tego aplikacji funkcji programu PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="8d14e-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="8d14e-196">Zmieniono domyślną wersję środowiska uruchomieniowego w usłudze Functions w wersji 3 w systemie Windows dla aplikacji funkcji programu PowerShell z 6.2 na 7.0, gdy nie określono parametru `RuntimeVersion`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="8d14e-197">Zmieniono domyślną wersję środowiska uruchomieniowego w usłudze Functions w wersji 3 w systemach Windows i Linux dla aplikacji funkcji programu Node z 10 na 12, gdy nie określono parametru `RuntimeVersion`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="8d14e-198">Jednak użytkownicy nadal mogą tworzyć aplikacje funkcji Node 10, określając elementy `-Runtime Node` i `-RuntimeVersion 10`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="8d14e-199">Zmieniono domyślną wersję środowiska uruchomieniowego w usłudze Functions w wersji 3 w systemie Linux dla aplikacji funkcji języka Python z 3.7 na 3.8, gdy nie określono parametru `RuntimeVersion`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="8d14e-200">Jednak użytkownicy mogą nadal tworzyć aplikacje funkcji języka Python 3.7, określając elementy `-Runtime Python` i `-RuntimeVersion 3.7`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-201">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-201">Before</span></span>

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python
```

#### <a name="after"></a><span data-ttu-id="8d14e-202">Nowy adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-202">After</span></span>

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node `
                  -RuntimeVersion 10

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python `
                  -RuntimeVersion 3.7
```

## <a name="azkeyvault"></a><span data-ttu-id="8d14e-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d14e-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="8d14e-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d14e-204">New-AzKeyVault</span></span>

<span data-ttu-id="8d14e-205">Nie obsługuje już parametru `DisableSoftDelete`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="8d14e-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-206">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="8d14e-207">Nowy adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-207">After</span></span>

<span data-ttu-id="8d14e-208">Możliwość aktualizowania ustawienia usuwania nietrwałego jest przestarzała w module Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="8d14e-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="8d14e-209">Dowiedz się więcej: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="8d14e-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="8d14e-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d14e-210">Update-AzKeyVault</span></span>

<span data-ttu-id="8d14e-211">Nie obsługuje już parametru `EnableSoftDelete`, `SoftDeleteRetentionInDays`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="8d14e-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-212">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="8d14e-213">Nowy adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-213">After</span></span>

<span data-ttu-id="8d14e-214">Możliwość aktualizowania ustawienia usuwania nietrwałego jest przestarzała w module Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="8d14e-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="8d14e-215">Dowiedz się więcej: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="8d14e-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="8d14e-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8d14e-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="8d14e-217">Właściwość `SecretValueText` typu `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="8d14e-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="8d14e-218">Właściwość `SecretValueText` została zastąpiona właściwością `SecretValue`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-218">The `SecretValueText` property has been replaced with `SecretValue`.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-219">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="8d14e-220">Nowy adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-220">After</span></span>

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a><span data-ttu-id="8d14e-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8d14e-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="8d14e-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="8d14e-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="8d14e-223">Nie obsługuje już parametru `ResourceId`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="8d14e-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-224">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="8d14e-225">Nowy adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="8d14e-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="8d14e-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="8d14e-227">Nie obsługuje już parametru `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="8d14e-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-228">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="8d14e-229">Nowy adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="8d14e-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="8d14e-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="8d14e-231">Nie obsługuje już parametru `Id`, `ResourceId` a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="8d14e-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-232">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="8d14e-233">Nowy adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="8d14e-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="8d14e-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="8d14e-235">Nie obsługuje już parametru `Id`, `ResourceId` a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="8d14e-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-236">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="8d14e-237">Nowy adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="8d14e-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="8d14e-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="8d14e-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="8d14e-240">Nie obsługuje już parametru `ApiVersion`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="8d14e-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-241">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="8d14e-242">Nowy adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="8d14e-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8d14e-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="8d14e-244">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="8d14e-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-245">Get-AzDeployment</span></span>

<span data-ttu-id="8d14e-246">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="8d14e-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8d14e-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="8d14e-248">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="8d14e-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8d14e-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="8d14e-250">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="8d14e-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="8d14e-252">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="8d14e-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8d14e-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="8d14e-254">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="8d14e-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="8d14e-256">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="8d14e-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-257">New-AzDeployment</span></span>

<span data-ttu-id="8d14e-258">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="8d14e-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="8d14e-260">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="8d14e-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="8d14e-262">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="8d14e-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-263">Remove-AzDeployment</span></span>

<span data-ttu-id="8d14e-264">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="8d14e-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="8d14e-266">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="8d14e-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8d14e-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="8d14e-268">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="8d14e-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8d14e-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="8d14e-270">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="8d14e-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8d14e-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="8d14e-272">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="8d14e-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="8d14e-274">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="8d14e-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-275">Stop-AzDeployment</span></span>

<span data-ttu-id="8d14e-276">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="8d14e-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="8d14e-278">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="8d14e-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="8d14e-280">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="8d14e-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-281">Test-AzDeployment</span></span>

<span data-ttu-id="8d14e-282">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="8d14e-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="8d14e-284">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="8d14e-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="8d14e-286">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="8d14e-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8d14e-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="8d14e-288">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="8d14e-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8d14e-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="8d14e-290">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="8d14e-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="8d14e-292">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="8d14e-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="8d14e-294">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="8d14e-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8d14e-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="8d14e-296">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="8d14e-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="8d14e-298">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="8d14e-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d14e-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="8d14e-300">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="8d14e-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8d14e-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="8d14e-302">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="8d14e-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8d14e-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="8d14e-304">Taki sam jak `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="8d14e-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d14e-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="8d14e-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8d14e-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="8d14e-307">Nie obsługuje już parametru `IsAzureADOnlyAuthentication`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="8d14e-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-308">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="8d14e-309">Nowy adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="8d14e-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="8d14e-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="8d14e-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8d14e-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="8d14e-312">Nie obsługuje już parametru `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="8d14e-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-313">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="8d14e-314">Nowy adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="8d14e-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8d14e-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="8d14e-316">Nie obsługuje już parametru `Suspend`, `Resume`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="8d14e-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="8d14e-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d14e-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="8d14e-318">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d14e-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="8d14e-319">Nie obsługuje już parametru `PrivateLinkResourceType`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="8d14e-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-320">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="8d14e-321">Nowy adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="8d14e-322">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d14e-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="8d14e-323">Taki sam jak `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="8d14e-324">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d14e-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="8d14e-325">Taki sam jak `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="8d14e-326">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d14e-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="8d14e-327">Taki sam jak `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="8d14e-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d14e-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="8d14e-329">Taki sam jak `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="8d14e-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="8d14e-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="8d14e-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="8d14e-331">Nie obsługuje już parametru `FilterType`, `FilterItem`, a alias nazwy oryginalnego parametru nie został znaleziony.</span><span class="sxs-lookup"><span data-stu-id="8d14e-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8d14e-332">Stary adres</span><span class="sxs-lookup"><span data-stu-id="8d14e-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="8d14e-333">Po</span><span class="sxs-lookup"><span data-stu-id="8d14e-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
