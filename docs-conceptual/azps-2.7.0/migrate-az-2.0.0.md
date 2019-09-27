---
title: Przewodnik migracji modułu Az 2.0.0
description: Ten przewodnik migracji zawiera listę zmian powodujących niezgodność wprowadzonych w wersji 2.0 modułu Az programu Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.openlocfilehash: 5f15d1a4f1e8416d7214aceb78494867fe4aad52
ms.sourcegitcommit: 92722d603b60dc769660e7517da60110133d9959
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/24/2019
ms.locfileid: "71226222"
---
# <a name="migration-guide-for-az-200"></a><span data-ttu-id="f1c4d-103">Przewodnik migracji modułu Az 2.0.0</span><span class="sxs-lookup"><span data-stu-id="f1c4d-103">Migration Guide for Az 2.0.0</span></span>

<span data-ttu-id="f1c4d-104">Ten dokument zawiera opis różnic między wersjami 1.0.0 i 2.0.0 modułu Az</span><span class="sxs-lookup"><span data-stu-id="f1c4d-104">This document describes the changes between the 1.0.0 and 2.0.0 versions of Az</span></span> 

## <a name="table-of-contents"></a><span data-ttu-id="f1c4d-105">Spis treści</span><span class="sxs-lookup"><span data-stu-id="f1c4d-105">Table of Contents</span></span>
- [<span data-ttu-id="f1c4d-106">Zmiany powodujące niezgodność modułów</span><span class="sxs-lookup"><span data-stu-id="f1c4d-106">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="f1c4d-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1c4d-107">Az.Compute</span></span>](#azcompute)
  - [<span data-ttu-id="f1c4d-108">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1c4d-108">Az.HDInsight</span></span>](#azhdinsight)
  - [<span data-ttu-id="f1c4d-109">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1c4d-109">Az.Storage</span></span>](#azstorage)

## <a name="module-breaking-changes"></a><span data-ttu-id="f1c4d-110">Zmiany powodujące niezgodność modułów</span><span class="sxs-lookup"><span data-stu-id="f1c4d-110">Module breaking changes</span></span>

### <a name="azcompute"></a><span data-ttu-id="f1c4d-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1c4d-111">Az.Compute</span></span>

- <span data-ttu-id="f1c4d-112">Usunięto parametr `Managed` z poleceń cmdlet `New-AzAvailabilitySet` i `Update-AzAvailabilitySet` na rzecz parametru ```Sku = Aligned```</span><span class="sxs-lookup"><span data-stu-id="f1c4d-112">Removed `Managed` Parameter from `New-AzAvailabilitySet` and `Update-AzAvailabilitySet` cmdlets in favor of using ```Sku = Aligned```</span></span>

  #### <a name="before"></a><span data-ttu-id="f1c4d-113">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-113">Before</span></span>

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a><span data-ttu-id="f1c4d-114">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-114">After</span></span>

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- <span data-ttu-id="f1c4d-115">W celu zapewnienia spójności usunięto parametr `Image` z zestawu parametrów „ByName” i „ByResourceId” w poleceniu `Update-AzImage`</span><span class="sxs-lookup"><span data-stu-id="f1c4d-115">For consistency, removed `Image` parameter from 'ByName' and 'ByResourceId' parameter sets in `Update-AzImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="f1c4d-116">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-116">Before</span></span>

  <span data-ttu-id="f1c4d-117">Pamiętaj, że poniższy kod będzie działać, ale przekazany parametr ImageName nie jest używany, więc jego usunięcie nie ma żadnego wpływu na funkcjonalność.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-117">Note that the below code is functional, but the passed-in ImageName is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a><span data-ttu-id="f1c4d-118">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-118">After</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- <span data-ttu-id="f1c4d-119">W celu zapewnienia spójności usunięto parametr `Name` z zestawów parametrów „ByObject” i „ByResourceId” w poleceniu `Restart-AzVM`</span><span class="sxs-lookup"><span data-stu-id="f1c4d-119">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Restart-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="f1c4d-120">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-120">Before</span></span>

  <span data-ttu-id="f1c4d-121">Pamiętaj, że poniższy kod będzie działać, ale przekazany parametr Name nie jest używany, więc jego usunięcie nie ma żadnego wpływu na funkcjonalność.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-121">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="f1c4d-122">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-122">After</span></span>

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="f1c4d-123">W celu zapewnienia spójności usunięto parametr `Name` z zestawów parametrów „ByObject” i „ByResourceId” w poleceniu `Start-AzVM`</span><span class="sxs-lookup"><span data-stu-id="f1c4d-123">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Start-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="f1c4d-124">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-124">Before</span></span>

  <span data-ttu-id="f1c4d-125">Pamiętaj, że poniższy kod będzie działać, ale przekazany parametr Name nie jest używany, więc jego usunięcie nie ma żadnego wpływu na funkcjonalność.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-125">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="f1c4d-126">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-126">After</span></span>

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="f1c4d-127">W celu zapewnienia spójności usunięto parametr `Name` z zestawów parametrów „ByObject” i „ByResourceId” w poleceniu `Stop-AzVM`</span><span class="sxs-lookup"><span data-stu-id="f1c4d-127">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Stop-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="f1c4d-128">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-128">Before</span></span>

  <span data-ttu-id="f1c4d-129">Pamiętaj, że poniższy kod będzie działać, ale przekazany parametr Name nie jest używany, więc jego usunięcie nie ma żadnego wpływu na funkcjonalność.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-129">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="f1c4d-130">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-130">After</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="f1c4d-131">W celu zapewnienia spójności usunięto parametr `Name` z zestawów parametrów „ByObject” i „ByResourceId” w poleceniu `Remove-AzVM`</span><span class="sxs-lookup"><span data-stu-id="f1c4d-131">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Remove-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="f1c4d-132">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-132">Before</span></span>

  <span data-ttu-id="f1c4d-133">Pamiętaj, że poniższy kod będzie działać, ale przekazany parametr Name nie jest używany, więc jego usunięcie nie ma żadnego wpływu na funkcjonalność.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-133">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a><span data-ttu-id="f1c4d-134">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-134">After</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- <span data-ttu-id="f1c4d-135">W celu zapewnienia spójności usunięto parametr `Name` z zestawów parametrów „ByObject” i „ByResourceId” w poleceniu `Set-AzVM`</span><span class="sxs-lookup"><span data-stu-id="f1c4d-135">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Set-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="f1c4d-136">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-136">Before</span></span>

  <span data-ttu-id="f1c4d-137">Pamiętaj, że poniższy kod będzie działać, ale przekazany parametr Name nie jest używany, więc jego usunięcie nie ma żadnego wpływu na funkcjonalność.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-137">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a><span data-ttu-id="f1c4d-138">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-138">After</span></span>

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- <span data-ttu-id="f1c4d-139">W celu zapewnienia spójności usunięto parametr `Name` z zestawów parametrów „ByObject” i „ByResourceId” w poleceniu `Save-AzVMImage`</span><span class="sxs-lookup"><span data-stu-id="f1c4d-139">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Save-AzVMImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="f1c4d-140">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-140">Before</span></span>
  <span data-ttu-id="f1c4d-141">Pamiętaj, że poniższy kod będzie działać, ale przekazany parametr Name nie jest używany, więc jego usunięcie nie ma żadnego wpływu na funkcjonalność.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-141">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a><span data-ttu-id="f1c4d-142">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-142">After</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- <span data-ttu-id="f1c4d-143">Dodano właściwość ProtectionPolicy w celu hermetyzacji właściwości `ProtectFromScaleIn` w klasie `PSVirtualMachineScaleSetVM`</span><span class="sxs-lookup"><span data-stu-id="f1c4d-143">Added ProtectionPolicy property to encapsulate `ProtectFromScaleIn` property in `PSVirtualMachineScaleSetVM`</span></span>

  #### <a name="before"></a><span data-ttu-id="f1c4d-144">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-144">Before</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a><span data-ttu-id="f1c4d-145">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-145">After</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- <span data-ttu-id="f1c4d-146">Dodano właściwość ```EncryptionSettingsCollection``` w celu objęcia właściwości `EncryptionSettings` w klasie `PSDisk`</span><span class="sxs-lookup"><span data-stu-id="f1c4d-146">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSDisk`</span></span>

  #### <a name="before"></a><span data-ttu-id="f1c4d-147">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-147">Before</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="f1c4d-148">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-148">After</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="f1c4d-149">Dodano właściwość ```EncryptionSettingsCollection``` w celu objęcia właściwości `EncryptionSettings` w klasie `PSSnapshot`</span><span class="sxs-lookup"><span data-stu-id="f1c4d-149">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSSnapshot`</span></span>

  #### <a name="before"></a><span data-ttu-id="f1c4d-150">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-150">Before</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="f1c4d-151">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-151">After</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="f1c4d-152">Usunięto właściwość `VirtualMachineProfile` z klasy `PSVirtualMachineScaleSet`</span><span class="sxs-lookup"><span data-stu-id="f1c4d-152">Removed `VirtualMachineProfile` property from `PSVirtualMachineScaleSet`</span></span>

  #### <a name="before"></a><span data-ttu-id="f1c4d-153">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-153">Before</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a><span data-ttu-id="f1c4d-154">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-154">After</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- <span data-ttu-id="f1c4d-155">W przypadku polecenia cmdlet `Set-AzVMBootDiagnostic` usunięto alias polecenia cmdlet `Set-AzVMBootDiagnostics`</span><span class="sxs-lookup"><span data-stu-id="f1c4d-155">Cmdlet `Set-AzVMBootDiagnostic` removed alias to `Set-AzVMBootDiagnostics`</span></span>

  #### <a name="before"></a><span data-ttu-id="f1c4d-156">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-156">Before</span></span>

  <span data-ttu-id="f1c4d-157">Użycie przestarzałego aliasu</span><span class="sxs-lookup"><span data-stu-id="f1c4d-157">Using deprecated alias</span></span>

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a><span data-ttu-id="f1c4d-158">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-158">After</span></span>

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- <span data-ttu-id="f1c4d-159">W przypadku polecenia cmdlet `Export-AzLogAnalyticThrottledRequest` usunięto alias polecenia cmdlet `Export-AzLogAnalyticThrottledRequests`</span><span class="sxs-lookup"><span data-stu-id="f1c4d-159">Cmdlet `Export-AzLogAnalyticThrottledRequest` removed alias to `Export-AzLogAnalyticThrottledRequests`</span></span>

  #### <a name="before"></a><span data-ttu-id="f1c4d-160">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-160">Before</span></span>

  <span data-ttu-id="f1c4d-161">Użycie przestarzałego aliasu</span><span class="sxs-lookup"><span data-stu-id="f1c4d-161">Using deprectaed alias</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a><span data-ttu-id="f1c4d-162">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-162">After</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a><span data-ttu-id="f1c4d-163">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1c4d-163">Az.HDInsight</span></span>

- <span data-ttu-id="f1c4d-164">Usunięto polecenia cmdlet `Grant-AzHDInsightHttpServicesAccess` i `Revoke-AzHDInsightHttpServicesAccess`.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-164">Removed the `Grant-AzHDInsightHttpServicesAccess` and `Revoke-AzHDInsightHttpServicesAccess` cmdlets.</span></span> <span data-ttu-id="f1c4d-165">Nie są one już potrzebne, ponieważ dostęp HTTP jest zawsze włączony na wszystkich klastrach HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-165">These are no longer necessary because HTTP access is always enabled on all HDInsight clusters.</span></span>
- <span data-ttu-id="f1c4d-166">Dodano nowe polecenie cmdlet `Set-AzHDInsightGatewayCredential`.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-166">Added a new `Set-AzHDInsightGatewayCredential`  cmdlet.</span></span> <span data-ttu-id="f1c4d-167">Za pomocą tego polecenia cmdlet można zmienić nazwę i hasło użytkownika HTTP bramy (zastępuje polecenie cmdlet `Grant-AzHDInsightHttpServicesAccess`).</span><span class="sxs-lookup"><span data-stu-id="f1c4d-167">Use this cmdlet to change the gateway HTTP username and password (replaces `Grant-AzHDInsightHttpServicesAccess`).</span></span>
- <span data-ttu-id="f1c4d-168">Zaktualizowano polecenie cmdlet `Get-AzHDInsightJobOutput` tak, aby obsługiwało szczegółowy dostęp na podstawie ról do klucza magazynu.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-168">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
    - <span data-ttu-id="f1c4d-169">Nie ma to wpływu na użytkowników mających rolę Operator, Współautor lub Właściciel w klastrze usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-169">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
    - <span data-ttu-id="f1c4d-170">Użytkownicy mający tylko rolę Czytelnik będą musieli jawnie określać parametr `DefaultStorageAccountKey`.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-170">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

<span data-ttu-id="f1c4d-171">Aby uzyskać więcej informacji o tych zmianach dostępu na podstawie ról, zobacz [aka.ms/hdi-config-update](http://aka.ms/hdi-config-update)</span><span class="sxs-lookup"><span data-stu-id="f1c4d-171">For more information about these role-based access changes, see [aka.ms/hdi-config-update](http://aka.ms/hdi-config-update)</span></span>

  #### <a name="before"></a><span data-ttu-id="f1c4d-172">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-172">Before</span></span>

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a><span data-ttu-id="f1c4d-173">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-173">After</span></span>

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a><span data-ttu-id="f1c4d-174">Polecenie cmdlet Get-AzHDInsightJobOutput w przypadku użytkowników mających tylko rolę Czytelnik</span><span class="sxs-lookup"><span data-stu-id="f1c4d-174">Users with only Reader role for cmdlet Get-AzHDInsightJobOutput</span></span>

  ####  <a name="before"></a><span data-ttu-id="f1c4d-175">Przed</span><span class="sxs-lookup"><span data-stu-id="f1c4d-175">Before</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a><span data-ttu-id="f1c4d-176">Po</span><span class="sxs-lookup"><span data-stu-id="f1c4d-176">After</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a><span data-ttu-id="f1c4d-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1c4d-177">Az.Storage</span></span>

- <span data-ttu-id="f1c4d-178">Przestrzenie nazw dla typów zwracanych przez polecenia cmdlet Blob, Queue i File zostały zmienione z `Microsoft.WindowsAzure.Storage` na `Microsoft.Azure.Storage`.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-178">Namespaces for types returned from Blob, Queue, and File cmdlets have changed their namespace from `Microsoft.WindowsAzure.Storage` to `Microsoft.Azure.Storage`.</span></span>  <span data-ttu-id="f1c4d-179">Chociaż w zasadzie nie jest to zmiana powodująca niezgodność zgodnie z zasadami zmian powodujących niezgodność, może spowodować konieczność wprowadzenia pewnych zmian w kodzie, który używa metod z zestawu .Net SDK magazynu do interakcji z obiektami zwracanymi przez te polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-179">While this is not technically a breaking change according to the breaking change policy, it may require some changes in code that uses the methods from the Storage .Net SDK to interact with the objects returned from these cmdlets.</span></span>

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a><span data-ttu-id="f1c4d-180">Przykład 1:  Dodawanie komunikatu do kolejki (zmiana przestrzeni nazw obiektu CloudQueueMessage)</span><span class="sxs-lookup"><span data-stu-id="f1c4d-180">Example 1:  Add a message to a Queue (change CloudQueueMessage object namespace)</span></span>

  <span data-ttu-id="f1c4d-181">Przed:</span><span class="sxs-lookup"><span data-stu-id="f1c4d-181">Before:</span></span> 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  <span data-ttu-id="f1c4d-182">Po:</span><span class="sxs-lookup"><span data-stu-id="f1c4d-182">After:</span></span>

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a><span data-ttu-id="f1c4d-183">Przykład 2:  Pobieranie atrybutów obiektu blob/pliku przy użyciu obiektu AccessCondition (zmiana przestrzeni nazw obiektu AccessCondition)</span><span class="sxs-lookup"><span data-stu-id="f1c4d-183">Example 2:  Fetch Blob/File Attributes with AccessCondition (change AccessCondition object namespace)</span></span>

  <span data-ttu-id="f1c4d-184">Przed:</span><span class="sxs-lookup"><span data-stu-id="f1c4d-184">Before:</span></span> 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  <span data-ttu-id="f1c4d-185">Po:</span><span class="sxs-lookup"><span data-stu-id="f1c4d-185">After:</span></span>

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- <span data-ttu-id="f1c4d-186">Chociaż w zasadzie nie jest to zmiana powodująca niezgodność, zauważysz następujące różnice w danych wyjściowych właściwości Sku.Name kont magazynu zwracanych przez polecenie `New/Get/Set-AzStorageAccount`.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-186">While not technically a breaking change, you will notice output differences in the Sku.Name property of Storage Accounts returned from  `New/Get/Set-AzStorageAccount` changes are as follows.</span></span> <span data-ttu-id="f1c4d-187">(Po zmianie wyjściowa i wejściowa wartość SkuName będą zgodne).</span><span class="sxs-lookup"><span data-stu-id="f1c4d-187">(After the change, output and input SkuName are aligned.)</span></span>
  - <span data-ttu-id="f1c4d-188">„StandardLRS” -> „Standard_LRS”;</span><span class="sxs-lookup"><span data-stu-id="f1c4d-188">"StandardLRS" -> "Standard_LRS";</span></span>
  - <span data-ttu-id="f1c4d-189">„StandardGRS” -> „Standard_GRS”;</span><span class="sxs-lookup"><span data-stu-id="f1c4d-189">"StandardGRS" -> "Standard_GRS";</span></span>
  - <span data-ttu-id="f1c4d-190">„StandardRAGRS” -> „Standard_RAGRS”;</span><span class="sxs-lookup"><span data-stu-id="f1c4d-190">"StandardRAGRS" -> "Standard_RAGRS";</span></span>
  - <span data-ttu-id="f1c4d-191">„StandardZRS” -> „Standard_ZRS”;</span><span class="sxs-lookup"><span data-stu-id="f1c4d-191">"StandardZRS" -> "Standard_ZRS";</span></span>
  - <span data-ttu-id="f1c4d-192">„PremiumLRS” -> „Premium_LRS”;</span><span class="sxs-lookup"><span data-stu-id="f1c4d-192">"PremiumLRS" -> "Premium_LRS";</span></span>

- <span data-ttu-id="f1c4d-193">Zmieniono domyślne zachowanie usługi podczas tworzenia konta magazynu bez określania rodzaju.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-193">The default service behavior when creating a storage account withous specifying a Kind has changed.</span></span>  <span data-ttu-id="f1c4d-194">W poprzednich wersjach, gdy konto magazynu zostało utworzone bez określenia parametru `Kind`, używany był rodzaj konta magazynu `Storage`. W nowej wersji `StorageV2` to wartość domyślna parametru `Kind`.</span><span class="sxs-lookup"><span data-stu-id="f1c4d-194">In previous versions, when a storage account was created with no `Kind` specified, the Storage account Kind of `Storage` was used, in the new version `StorageV2` is the default `Kind` value.</span></span> <span data-ttu-id="f1c4d-195">Jeśli chcesz utworzyć konto magazynu w wersji 1 o rodzaju „Storage”, dodaj parametr „-Kind Storage”</span><span class="sxs-lookup"><span data-stu-id="f1c4d-195">If you need to create a V1 Storage account with Kind 'Storage', add parameter '-Kind Storage'</span></span>

  #### <a name="example--create-a-storage-account-default-kind-change"></a><span data-ttu-id="f1c4d-196">Przykład: Tworzenie konta magazynu (zmiana domyślnego rodzaju)</span><span class="sxs-lookup"><span data-stu-id="f1c4d-196">Example : Create a storage Account (Default Kind change)</span></span>  

  <span data-ttu-id="f1c4d-197">Przed:</span><span class="sxs-lookup"><span data-stu-id="f1c4d-197">Before:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  <span data-ttu-id="f1c4d-198">Po:</span><span class="sxs-lookup"><span data-stu-id="f1c4d-198">After:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```