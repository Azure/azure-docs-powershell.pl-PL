---
title: Zmiany powodujące niezgodność dotyczące programu Microsoft Azure PowerShell 6.0.0.
description: Ten przewodnik po migracji zawiera listę zmian powodujących niezgodność wprowadzonych w programie Azure PowerShell w wersji 6.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 72a0e9ca8562dc06a1fe2718658172ce9ee20f0e
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/06/2018
ms.locfileid: "43383944"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a><span data-ttu-id="38cd6-103">Zmiany powodujące niezgodność dotyczące programu Microsoft Azure PowerShell 6.0.0.</span><span class="sxs-lookup"><span data-stu-id="38cd6-103">Breaking changes for Microsoft Azure PowerShell 6.0.0</span></span>

<span data-ttu-id="38cd6-104">Ten dokument służy jako przewodnik zarówno po powiadomieniach o istotnych zmianach, jak i migracji dla użytkowników poleceń cmdlet programu Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="38cd6-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="38cd6-105">Każda sekcja opisuje zarówno tempo istotnej zmiany, jak i ścieżkę migracji najmniejszego oporu.</span><span class="sxs-lookup"><span data-stu-id="38cd6-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="38cd6-106">Aby uzyskać szczegółowy kontekst, zapoznaj się z żądaniem ściągnięcia skojarzonym z każdą zmianą.</span><span class="sxs-lookup"><span data-stu-id="38cd6-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="38cd6-107">Spis treści</span><span class="sxs-lookup"><span data-stu-id="38cd6-107">Table of Contents</span></span>

- [<span data-ttu-id="38cd6-108">Ogólne zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="38cd6-108">General breaking changes</span></span>](#general-breaking-changes)
    - [<span data-ttu-id="38cd6-109">Minimalna wymagana wersja programu PowerShell została podniesiona do wersji 5.0</span><span class="sxs-lookup"><span data-stu-id="38cd6-109">Minimum PowerShell version required bumped to 5.0</span></span>](#minimum-powershell-version-required-bumped-to-50)
    - [<span data-ttu-id="38cd6-110">Automatyczne zapisywanie kontekstu jest domyślnie włączone</span><span class="sxs-lookup"><span data-stu-id="38cd6-110">Context autosaved enabled by default</span></span>](#context-autosave-enabled-by-default)
    - [<span data-ttu-id="38cd6-111">Usunięcie aliasów Tags</span><span class="sxs-lookup"><span data-stu-id="38cd6-111">Removal of Tags alias</span></span>](#removal-of-tags-alias)
- [<span data-ttu-id="38cd6-112">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="38cd6-112">Breaking changes to AzureRM.Compute cmdlets</span></span>](#breaking-changes-to-azurermcompute-cmdlets)
- [<span data-ttu-id="38cd6-113">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Compute AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="38cd6-113">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [<span data-ttu-id="38cd6-114">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Compute AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="38cd6-114">Breaking changes to AzureRM.Dns cmdlets</span></span>](#breaking-changes-to-azurermdns-cmdlets)
- [<span data-ttu-id="38cd6-115">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Compute AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="38cd6-115">Breaking changes to AzureRM.Insights cmdlets</span></span>](#breaking-changes-to-azurerminsights-cmdlets)
- [<span data-ttu-id="38cd6-116">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="38cd6-116">Breaking changes to AzureRM.KeyVault cmdlets</span></span>](#breaking-changes-to-azurermkeyvault-cmdlets)
- [<span data-ttu-id="38cd6-117">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="38cd6-117">Breaking changes to AzureRM.Network cmdlets</span></span>](#breaking-changes-to-azurermnetwork-cmdlets)
- [<span data-ttu-id="38cd6-118">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="38cd6-118">Breaking changes to AzureRM.RedisCache cmdlets</span></span>](#breaking-changes-to-azurermrediscache-cmdlets)
- [<span data-ttu-id="38cd6-119">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="38cd6-119">Breaking changes to AzureRM.Resources cmdlets</span></span>](#breaking-changes-to-azurermresources-cmdlets)
- [<span data-ttu-id="38cd6-120">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="38cd6-120">Breaking changes to AzureRM.Storage cmdlets</span></span>](#breaking-changes-to-azurermstorage-cmdlets)
- [<span data-ttu-id="38cd6-121">Usunięte moduły</span><span class="sxs-lookup"><span data-stu-id="38cd6-121">Removed modules</span></span>](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a><span data-ttu-id="38cd6-122">Ogólne zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="38cd6-122">General breaking changes</span></span>

### <a name="minimum-powershell-version-required-bumped-to-50"></a><span data-ttu-id="38cd6-123">Minimalna wymagana wersja programu PowerShell została podniesiona do wersji 5.0</span><span class="sxs-lookup"><span data-stu-id="38cd6-123">Minimum PowerShell version required bumped to 5.0</span></span>

<span data-ttu-id="38cd6-124">Wcześniej w usłudze Azure PowerShell wymagany był program PowerShell w wersji _co najmniej_ 3.0, aby możliwe było uruchamianie jakichkolwiek poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38cd6-124">Previously, Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.</span></span> <span data-ttu-id="38cd6-125">W przyszłości to wymaganie zostanie podniesione do wersji 5.0 programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="38cd6-125">Moving forward, this requirement will be raised to version 5.0 of PowerShell.</span></span> <span data-ttu-id="38cd6-126">Informacje o uaktualnianiu programu PowerShell 5.0 znajdują się w [tej tabeli](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="38cd6-126">For information on upgrading to PowerShell 5.0, please see [this table](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

### <a name="context-autosave-enabled-by-default"></a><span data-ttu-id="38cd6-127">Automatyczne zapisywanie kontekstu jest domyślnie włączone</span><span class="sxs-lookup"><span data-stu-id="38cd6-127">Context autosave enabled by default</span></span>

<span data-ttu-id="38cd6-128">Automatyczne zapisywanie kontekstu służy do zapisywania na platformie Azure informacji logowania, których można użyć między nowymi i różnymi sesjami programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="38cd6-128">Context autosave is the storage of Azure sign in information that can be used between new and different PowerShell sessions.</span></span> <span data-ttu-id="38cd6-129">Więcej informacji na temat automatycznego zapisywania kontekstu zawiera [ten dokument](https://docs.microsoft.com/en-us/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="38cd6-129">For more information on context autosave, please see [this document](https://docs.microsoft.com/en-us/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="38cd6-130">Wcześniej automatyczne zapisywanie kontekstu było domyślnie wyłączone, co oznacza, że informacje użytkownika dotyczące uwierzytelniania na platformie Azure nie były przechowywane między sesjami, dopóki użytkownik nie uruchomił polecenia cmdlet `Enable-AzureRmContextAutosave` w celu włączenia trwałości kontekstu.</span><span class="sxs-lookup"><span data-stu-id="38cd6-130">Previously by default, context autosave was disabled, which meant the user's Azure authentication information was not stored between sessions until they ran the `Enable-AzureRmContextAutosave` cmdlet to turn on context persistence.</span></span> <span data-ttu-id="38cd6-131">W przyszłości automatyczne zapisywanie kontekstu będzie domyślnie włączone, co oznacza, że dla użytkowników _bez zapisanych ustawień automatycznego zapisywania kontekstu_ kontekst będzie przechowywany do czasu ich następnego zalogowania się.</span><span class="sxs-lookup"><span data-stu-id="38cd6-131">Moving forward, context autosave will be enabled by default, which means that users _with no saved context autosave settings_ will have their context stored the next time they sign in.</span></span> <span data-ttu-id="38cd6-132">Użytkownicy mogą zrezygnować z tej funkcji przy użyciu polecenia cmdlet `Disable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="38cd6-132">Users can opt out of this functionality by using the `Disable-AzureRmContextAutosave` cmdlet.</span></span>

<span data-ttu-id="38cd6-133">_Uwaga_: ta zmiana nie będzie dotyczyła użytkowników, którzy wcześniej wyłączyli automatyczne zapisywanie kontekstu, użytkowników z włączonym automatycznym zapisywaniem kontekstu ani istniejących kontekstów</span><span class="sxs-lookup"><span data-stu-id="38cd6-133">_Note_: users that previously disabled context autosave or users with context autosave enabled and existing contexts will not be affected by this change</span></span>

### <a name="removal-of-tags-alias"></a><span data-ttu-id="38cd6-134">Usunięcie aliasów Tags</span><span class="sxs-lookup"><span data-stu-id="38cd6-134">Removal of Tags alias</span></span>

<span data-ttu-id="38cd6-135">Alias `Tags` dla parametru `Tag` został usunięty z wielu poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38cd6-135">The alias `Tags` for the `Tag` parameter has been removed across numerous cmdlets.</span></span> <span data-ttu-id="38cd6-136">Poniżej przedstawiono listę modułów (i odpowiednich poleceń cmdlet), na które ta zmiana ma wpływ:</span><span class="sxs-lookup"><span data-stu-id="38cd6-136">Below is a list of modules (and the corresponding cmdlets) affected by this:</span></span>

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a><span data-ttu-id="38cd6-137">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="38cd6-137">Breaking changes to AzureRM.Compute cmdlets</span></span>

<span data-ttu-id="38cd6-138">**Różne**</span><span class="sxs-lookup"><span data-stu-id="38cd6-138">**Miscellaneous**</span></span>
- <span data-ttu-id="38cd6-139">Właściwość nazwy jednostki SKU zagnieżdżona w typach `PSDisk` i `PSSnapshot` została zmieniona z wartości `StandardLRS` i `PremiumLRS` odpowiednio na wartości `Standard_LRS` i `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="38cd6-139">The sku name property nested in types `PSDisk` and `PSSnapshot` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- <span data-ttu-id="38cd6-140">Właściwość typu konta magazynu zagnieżdżona w typach `PSVirtualMachine`, `PSVirtualMachineScaleSet` i `PSImage` została zmieniona z wartości `StandardLRS` i `PremiumLRS` odpowiednio na wartości `Standard_LRS` i `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="38cd6-140">The storage account type property nested in types `PSVirtualMachine`, `PSVirtualMachineScaleSet` and `PSImage` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

<span data-ttu-id="38cd6-141">**Add-AzureRmImageDataDisk**</span><span class="sxs-lookup"><span data-stu-id="38cd6-141">**Add-AzureRmImageDataDisk**</span></span>
- <span data-ttu-id="38cd6-142">Dopuszczalne wartości dla parametru `StorageAccountType` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="38cd6-142">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="38cd6-143">**Add-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="38cd6-143">**Add-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="38cd6-144">Dopuszczalne wartości dla parametru `StorageAccountType` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="38cd6-144">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="38cd6-145">**Add-AzureRmVmssDataDisk**</span><span class="sxs-lookup"><span data-stu-id="38cd6-145">**Add-AzureRmVmssDataDisk**</span></span>
- <span data-ttu-id="38cd6-146">Dopuszczalne wartości dla parametru `StorageAccountType` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="38cd6-146">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="38cd6-147">**New-AzureRmAvailabilitySet**</span><span class="sxs-lookup"><span data-stu-id="38cd6-147">**New-AzureRmAvailabilitySet**</span></span>
- <span data-ttu-id="38cd6-148">Parametr `Managed` został usunięty i wprowadzono parametr `Sku`</span><span class="sxs-lookup"><span data-stu-id="38cd6-148">The parameter `Managed` was removed in favor of `Sku`</span></span>

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

<span data-ttu-id="38cd6-149">**New-AzureRmDiskConfig**</span><span class="sxs-lookup"><span data-stu-id="38cd6-149">**New-AzureRmDiskConfig**</span></span>
- <span data-ttu-id="38cd6-150">Dopuszczalne wartości dla parametru `SkuName` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="38cd6-150">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="38cd6-151">**New-AzureRmDiskUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="38cd6-151">**New-AzureRmDiskUpdateConfig**</span></span>
- <span data-ttu-id="38cd6-152">Dopuszczalne wartości dla parametru `SkuName` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="38cd6-152">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="38cd6-153">**New-AzureRmSnapshotConfig**</span><span class="sxs-lookup"><span data-stu-id="38cd6-153">**New-AzureRmSnapshotConfig**</span></span>
- <span data-ttu-id="38cd6-154">Dopuszczalne wartości dla parametru `SkuName` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="38cd6-154">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="38cd6-155">**New-AzureRmSnapshotUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="38cd6-155">**New-AzureRmSnapshotUpdateConfig**</span></span>
- <span data-ttu-id="38cd6-156">Dopuszczalne wartości dla parametru `SkuName` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="38cd6-156">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="38cd6-157">**Set-AzureRmImageOsDisk**</span><span class="sxs-lookup"><span data-stu-id="38cd6-157">**Set-AzureRmImageOsDisk**</span></span>
- <span data-ttu-id="38cd6-158">Dopuszczalne wartości dla parametru `StorageAccountType` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="38cd6-158">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="38cd6-159">**Set-AzureRmVMAEMExtension**</span><span class="sxs-lookup"><span data-stu-id="38cd6-159">**Set-AzureRmVMAEMExtension**</span></span>
- <span data-ttu-id="38cd6-160">Parametr `DisableWAD` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-160">The parameter `DisableWAD` was removed</span></span>
    -  <span data-ttu-id="38cd6-161">Usługa Diagnostyka Microsoft Azure jest domyślnie wyłączona</span><span class="sxs-lookup"><span data-stu-id="38cd6-161">Windows Azure Diagnostics is disabled by default</span></span>

<span data-ttu-id="38cd6-162">**Set-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="38cd6-162">**Set-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="38cd6-163">Dopuszczalne wartości dla parametru `StorageAccountType` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="38cd6-163">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="38cd6-164">**Set-AzureRmVMOSDisk**</span><span class="sxs-lookup"><span data-stu-id="38cd6-164">**Set-AzureRmVMOSDisk**</span></span>
- <span data-ttu-id="38cd6-165">Dopuszczalne wartości dla parametru `StorageAccountType` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="38cd6-165">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="38cd6-166">**Set-AzureRmVmssStorageProfile**</span><span class="sxs-lookup"><span data-stu-id="38cd6-166">**Set-AzureRmVmssStorageProfile**</span></span>
- <span data-ttu-id="38cd6-167">Dopuszczalne wartości dla parametru `ManagedDisk` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="38cd6-167">The accepted values for parameter `ManagedDisk` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="38cd6-168">**Update-AzureRmVmss**</span><span class="sxs-lookup"><span data-stu-id="38cd6-168">**Update-AzureRmVmss**</span></span>
- <span data-ttu-id="38cd6-169">Dopuszczalne wartości dla parametru `ManagedDiskStorageAccountType` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="38cd6-169">The accepted values for parameter `ManagedDiskStorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a><span data-ttu-id="38cd6-170">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="38cd6-170">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>

<span data-ttu-id="38cd6-171">**Export-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="38cd6-171">**Export-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="38cd6-172">Parametry `PerFileThreadCount` i `ConcurrentFileCount` zostały usunięte.</span><span class="sxs-lookup"><span data-stu-id="38cd6-172">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="38cd6-173">W przyszłości użyj parametru `Concurrency`</span><span class="sxs-lookup"><span data-stu-id="38cd6-173">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

<span data-ttu-id="38cd6-174">**Import-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="38cd6-174">**Import-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="38cd6-175">Parametry `PerFileThreadCount` i `ConcurrentFileCount` zostały usunięte.</span><span class="sxs-lookup"><span data-stu-id="38cd6-175">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="38cd6-176">W przyszłości użyj parametru `Concurrency`</span><span class="sxs-lookup"><span data-stu-id="38cd6-176">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

<span data-ttu-id="38cd6-177">**Remove-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="38cd6-177">**Remove-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="38cd6-178">Parametr `Clean` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-178">Parameter `Clean` was removed</span></span>

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a><span data-ttu-id="38cd6-179">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="38cd6-179">Breaking changes to AzureRM.Dns cmdlets</span></span>

<span data-ttu-id="38cd6-180">**New-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="38cd6-180">**New-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="38cd6-181">Parametr `Force` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-181">The parameter `Force` was removed</span></span>

<span data-ttu-id="38cd6-182">**Remove-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="38cd6-182">**Remove-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="38cd6-183">Parametr `Force` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-183">The parameter `Force` was removed</span></span>

<span data-ttu-id="38cd6-184">**Remove-AzureRmDnsZone**</span><span class="sxs-lookup"><span data-stu-id="38cd6-184">**Remove-AzureRmDnsZone**</span></span>
- <span data-ttu-id="38cd6-185">Parametr `Force` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-185">The parameter `Force` was removed</span></span>

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a><span data-ttu-id="38cd6-186">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="38cd6-186">Breaking changes to AzureRM.Insights cmdlets</span></span>

<span data-ttu-id="38cd6-187">**Add-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="38cd6-187">**Add-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="38cd6-188">Aliasy parametrów `AutoscaleProfiles` i `Notifications` zostały usunięte</span><span class="sxs-lookup"><span data-stu-id="38cd6-188">The parameter aliases `AutoscaleProfiles` and `Notifications` were removed</span></span>

<span data-ttu-id="38cd6-189">**Add-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="38cd6-189">**Add-AzureRmLogProfile**</span></span>
- <span data-ttu-id="38cd6-190">Aliasy parametrów `Categories` i `Locations` zostały usunięte</span><span class="sxs-lookup"><span data-stu-id="38cd6-190">The parameter aliases `Categories` and `Locations` were removed</span></span>

<span data-ttu-id="38cd6-191">**Add-AzureRmMetricAlertRule**</span><span class="sxs-lookup"><span data-stu-id="38cd6-191">**Add-AzureRmMetricAlertRule**</span></span>
- <span data-ttu-id="38cd6-192">Alias parametru `Actions` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-192">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="38cd6-193">**Add-AzureRmWebtestAlertRule**</span><span class="sxs-lookup"><span data-stu-id="38cd6-193">**Add-AzureRmWebtestAlertRule**</span></span>
- <span data-ttu-id="38cd6-194">Alias parametru `Actions` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-194">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="38cd6-195">**Get-AzureRmLog**</span><span class="sxs-lookup"><span data-stu-id="38cd6-195">**Get-AzureRmLog**</span></span>
- <span data-ttu-id="38cd6-196">Aliasy parametrów `MaxRecords` i `MaxEvents` zostały usunięte</span><span class="sxs-lookup"><span data-stu-id="38cd6-196">The parameter aliases `MaxRecords` and `MaxEvents` were removed</span></span>

<span data-ttu-id="38cd6-197">**Get-AzureRmMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="38cd6-197">**Get-AzureRmMetricDefinition**</span></span>
- <span data-ttu-id="38cd6-198">Alias parametru `MetricNames` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-198">The parameter alias `MetricNames` was removed</span></span>

<span data-ttu-id="38cd6-199">**New-AzureRmAlertRuleEmail**</span><span class="sxs-lookup"><span data-stu-id="38cd6-199">**New-AzureRmAlertRuleEmail**</span></span>
- <span data-ttu-id="38cd6-200">Aliasy parametrów `CustomEmails` i `SendToServiceOwners` zostały usunięte</span><span class="sxs-lookup"><span data-stu-id="38cd6-200">The parameter aliases `CustomEmails` and `SendToServiceOwners` were removed</span></span>

<span data-ttu-id="38cd6-201">**New-AzureRmAlertRuleWebhook**</span><span class="sxs-lookup"><span data-stu-id="38cd6-201">**New-AzureRmAlertRuleWebhook**</span></span>
- <span data-ttu-id="38cd6-202">Alias parametru `Properties` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-202">The parameter alias `Properties` was removed</span></span>

<span data-ttu-id="38cd6-203">**New-AzureRmAutoscaleNotification**</span><span class="sxs-lookup"><span data-stu-id="38cd6-203">**New-AzureRmAutoscaleNotification**</span></span>
- <span data-ttu-id="38cd6-204">Aliasy parametrów `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` i `Webhooks` zostały usunięte</span><span class="sxs-lookup"><span data-stu-id="38cd6-204">The parameter aliases `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` and `Webhooks` were removed</span></span>

<span data-ttu-id="38cd6-205">**New-AzureRmAutoscaleProfile**</span><span class="sxs-lookup"><span data-stu-id="38cd6-205">**New-AzureRmAutoscaleProfile**</span></span>
- <span data-ttu-id="38cd6-206">Aliasy parametrów `Rules`, `ScheduleDays`, `ScheduleHours` i `ScheduleMinutes` zostały usunięte</span><span class="sxs-lookup"><span data-stu-id="38cd6-206">The parameter aliases `Rules`, `ScheduleDays`, `ScheduleHours` and `ScheduleMinutes` were removed</span></span>

<span data-ttu-id="38cd6-207">**New-AzureRmAutoscaleWebhook**</span><span class="sxs-lookup"><span data-stu-id="38cd6-207">**New-AzureRmAutoscaleWebhook**</span></span>
- <span data-ttu-id="38cd6-208">Alias parametru `Properties` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-208">The parameter alias `Properties` was removed</span></span>

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a><span data-ttu-id="38cd6-209">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="38cd6-209">Breaking changes to AzureRM.KeyVault cmdlets</span></span>

<span data-ttu-id="38cd6-210">**Add-AzureKeyVaultCertificate**</span><span class="sxs-lookup"><span data-stu-id="38cd6-210">**Add-AzureKeyVaultCertificate**</span></span>
- <span data-ttu-id="38cd6-211">Parametr `CertificatePolicy` stał się obowiązkowy.</span><span class="sxs-lookup"><span data-stu-id="38cd6-211">The `CertificatePolicy` parameter has become mandatory.</span></span>

<span data-ttu-id="38cd6-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span><span class="sxs-lookup"><span data-stu-id="38cd6-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span></span>
- <span data-ttu-id="38cd6-213">W poleceniu cmdlet nie są już akceptowane pojedyncze parametry, które tworzą token dostępu. Zamiast tego w poleceniach cmdlet jawne parametry tokenu, takie jak `Service` lub `Permissions`, zostały zastąpione ogólnym parametrem `TemplateUri` odpowiadającym przykładowemu tokenowi dostępu zdefiniowanemu w innym miejscu (prawdopodobnie za pomocą poleceń cmdlet programu PowerShell lub utworzonemu ręcznie zgodnie z dokumentacją usługi Storage) W poleceniu cmdlet zachowano parametr `ValidityPeriod`.</span><span class="sxs-lookup"><span data-stu-id="38cd6-213">The cmdlet no longer accepts individual parameters that compose the access token; instead, the cmdlet replaces explicit token parameters, such as `Service` or `Permissions`, with a generic `TemplateUri` parameter, corresponding to a sample access token defined elsewhere (presumably using Storage PowerShell cmdlets, or composed manually according to the Storage documentation.) The cmdlet retains the `ValidityPeriod` parameter.</span></span>

<span data-ttu-id="38cd6-214">Więcej informacji dotyczących tworzenia tokenów dostępu współdzielonego dla usługi Azure Storage można znaleźć na stronach dokumentacji, czyli odpowiednio:</span><span class="sxs-lookup"><span data-stu-id="38cd6-214">For more information on composing shared access tokens for Azure Storage, please refer to the documentation pages, respectively:</span></span>
- <span data-ttu-id="38cd6-215">[Tworzenie sygnatury dostępu współdzielonego usługi] (https://docs.microsoft.com/en-us/rest/api/storageservices/Constructing-a-Service-SAS)</span><span class="sxs-lookup"><span data-stu-id="38cd6-215">[Constructing a Service SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/Constructing-a-Service-SAS)</span></span>
- <span data-ttu-id="38cd6-216">[Tworzenia sygnatury dostępu współdzielonego konta] (https://docs.microsoft.com/en-us/rest/api/storageservices/constructing-an-account-sas)</span><span class="sxs-lookup"><span data-stu-id="38cd6-216">[Constructing an Account SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/constructing-an-account-sas)</span></span>

```powershell
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

<span data-ttu-id="38cd6-217">**Set-AzureKeyVaultCertificateIssuer**</span><span class="sxs-lookup"><span data-stu-id="38cd6-217">**Set-AzureKeyVaultCertificateIssuer**</span></span>
- <span data-ttu-id="38cd6-218">Parametr `IssuerProvider` stał się obowiązkowy.</span><span class="sxs-lookup"><span data-stu-id="38cd6-218">The `IssuerProvider` parameter has become mandatory.</span></span>

<span data-ttu-id="38cd6-219">**Undo-AzureKeyVaultCertificateRemoval**</span><span class="sxs-lookup"><span data-stu-id="38cd6-219">**Undo-AzureKeyVaultCertificateRemoval**</span></span>
- <span data-ttu-id="38cd6-220">Dane wyjściowe tego polecenia cmdlet zmieniły się z wartości `CertificateBundle` na `PSKeyVaultCertificate`.</span><span class="sxs-lookup"><span data-stu-id="38cd6-220">The output of this cmdlet has changed from `CertificateBundle` to `PSKeyVaultCertificate`.</span></span>

<span data-ttu-id="38cd6-221">**Undo-AzureRmKeyVaultRemoval**</span><span class="sxs-lookup"><span data-stu-id="38cd6-221">**Undo-AzureRmKeyVaultRemoval**</span></span>
- <span data-ttu-id="38cd6-222">Parametr `ResourceGroupName` został usunięty z zestawu parametrów `InputObject` i zamiast tego jest pobierany z właściwości `ResourceId` parametru `InputObject`.</span><span class="sxs-lookup"><span data-stu-id="38cd6-222">`ResourceGroupName` has been removed from the `InputObject` parameter set, and is instead obtained from the `InputObject` parameter's `ResourceId` property.</span></span>

<span data-ttu-id="38cd6-223">**Set-AzureRmKeyVaultAccessPolicy**</span><span class="sxs-lookup"><span data-stu-id="38cd6-223">**Set-AzureRmKeyVaultAccessPolicy**</span></span>
- <span data-ttu-id="38cd6-224">Uprawnienie `all` zostało usunięte z parametrów `PermissionsToKeys`, `PermissionsToSecrets`, i `PermissionsToCertificates`.</span><span class="sxs-lookup"><span data-stu-id="38cd6-224">The `all` permission was removed from `PermissionsToKeys`, `PermissionsToSecrets`, and `PermissionsToCertificates`.</span></span>

<span data-ttu-id="38cd6-225">**Ogólne**</span><span class="sxs-lookup"><span data-stu-id="38cd6-225">**General**</span></span>
- <span data-ttu-id="38cd6-226">Właściwość `ValueFromPipelineByPropertyName` została usunięta ze wszystkich poleceń cmdlet, w których włączone było potokowanie za pomocą parametru `InputObject`.</span><span class="sxs-lookup"><span data-stu-id="38cd6-226">The `ValueFromPipelineByPropertyName` property was removed from all cmdlets where piping by `InputObject` was enabled.</span></span>  <span data-ttu-id="38cd6-227">Polecenia cmdlet, których to dotyczy, są następujące:</span><span class="sxs-lookup"><span data-stu-id="38cd6-227">The cmdlets affected are:</span></span>
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="38cd6-228">Poziomy `ConfirmImpact` zostały usunięte ze wszystkich poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38cd6-228">`ConfirmImpact` levels were removed from all cmdlets.</span></span>  <span data-ttu-id="38cd6-229">Polecenia cmdlet, których to dotyczy, są następujące:</span><span class="sxs-lookup"><span data-stu-id="38cd6-229">The cmdlets affected are:</span></span>
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="38cd6-230">Parametr `IKeyVaultDataServiceClient` został zaktualizowany, więc wszystkie operacje certyfikatu zwracają typy PSTypes zamiast typów SDK.</span><span class="sxs-lookup"><span data-stu-id="38cd6-230">The `IKeyVaultDataServiceClient` was updated so all Certificate operations return PSTypes instead of SDK types.</span></span> <span data-ttu-id="38cd6-231">Obejmuje to:</span><span class="sxs-lookup"><span data-stu-id="38cd6-231">This includes:</span></span>
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a><span data-ttu-id="38cd6-232">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="38cd6-232">Breaking changes to AzureRM.Network cmdlets</span></span>


<span data-ttu-id="38cd6-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="38cd6-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="38cd6-234">Parametr `ProbeEnabled` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-234">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="38cd6-235">**Add-AzureRmVirtualNetworkPeering**</span><span class="sxs-lookup"><span data-stu-id="38cd6-235">**Add-AzureRmVirtualNetworkPeering**</span></span>
- <span data-ttu-id="38cd6-236">Alias parametru `AlloowGatewayTransit` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-236">The parameter alias `AlloowGatewayTransit` was removed</span></span>

<span data-ttu-id="38cd6-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="38cd6-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="38cd6-238">Parametr `ProbeEnabled` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-238">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="38cd6-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="38cd6-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="38cd6-240">Parametr `ProbeEnabled` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-240">The parameter `ProbeEnabled` was removed</span></span>

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a><span data-ttu-id="38cd6-241">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="38cd6-241">Breaking changes to AzureRM.RedisCache cmdlets</span></span>

<span data-ttu-id="38cd6-242">**New-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="38cd6-242">**New-AzureRmRedisCache**</span></span>
- <span data-ttu-id="38cd6-243">Parametry `Subnet` oraz `VirtualNetwork` zostały usunięte i wprowadzono parametr `SubnetId`</span><span class="sxs-lookup"><span data-stu-id="38cd6-243">The parameters `Subnet` and `VirtualNetwork` were removed in favor of `SubnetId`</span></span>
- <span data-ttu-id="38cd6-244">Parametr `RedisVersion` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-244">The parameter `RedisVersion` was removed</span></span>
- <span data-ttu-id="38cd6-245">Parametr `MaxMemoryPolicy` został usunięty i wprowadzono parametr `RedisConfiguration`</span><span class="sxs-lookup"><span data-stu-id="38cd6-245">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

<span data-ttu-id="38cd6-246">**Set-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="38cd6-246">**Set-AzureRmRedisCache**</span></span>
- <span data-ttu-id="38cd6-247">Parametr `MaxMemoryPolicy` został usunięty i wprowadzono parametr `RedisConfiguration`</span><span class="sxs-lookup"><span data-stu-id="38cd6-247">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a><span data-ttu-id="38cd6-248">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="38cd6-248">Breaking changes to AzureRM.Resources cmdlets</span></span>

<span data-ttu-id="38cd6-249">**Find-AzureRmResource**</span><span class="sxs-lookup"><span data-stu-id="38cd6-249">**Find-AzureRmResource**</span></span>
- <span data-ttu-id="38cd6-250">To polecenie cmdlet zostało usunięte, a jego funkcjonalność została przeniesiona do polecenia `Get-AzureRmResource`</span><span class="sxs-lookup"><span data-stu-id="38cd6-250">This cmdlet was removed and the functionality was moved into `Get-AzureRmResource`</span></span>

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

<span data-ttu-id="38cd6-251">**Find-AzureRmResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="38cd6-251">**Find-AzureRmResourceGroup**</span></span>
- <span data-ttu-id="38cd6-252">To polecenie cmdlet zostało usunięte, a jego funkcjonalność została przeniesiona do polecenia `Get-AzureRmResourceGroup`</span><span class="sxs-lookup"><span data-stu-id="38cd6-252">This cmdlet was removed and the functionality was moved into `Get-AzureRmResourceGroup`</span></span>

```powershell
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

<span data-ttu-id="38cd6-253">**Get-AzureRmRoleDefinition**</span><span class="sxs-lookup"><span data-stu-id="38cd6-253">**Get-AzureRmRoleDefinition**</span></span>
- <span data-ttu-id="38cd6-254">Parametr `AtScopeAndBelow` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="38cd6-254">Parameter `AtScopeAndBelow` was removed.</span></span>

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a><span data-ttu-id="38cd6-255">Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="38cd6-255">Breaking changes to AzureRM.Storage cmdlets</span></span>

<span data-ttu-id="38cd6-256">**New-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="38cd6-256">**New-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="38cd6-257">Parametr `EnableEncryptionService` został usunięty</span><span class="sxs-lookup"><span data-stu-id="38cd6-257">The parameter `EnableEncryptionService` was removed</span></span>

<span data-ttu-id="38cd6-258">**Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="38cd6-258">**Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="38cd6-259">Parametry `EnableEncryptionService` i `DisableEncryptionService` zostały usunięte</span><span class="sxs-lookup"><span data-stu-id="38cd6-259">The parameters `EnableEncryptionService` and `DisableEncryptionService` were removed</span></span>

## <a name="removed-modules"></a><span data-ttu-id="38cd6-260">Usunięte moduły</span><span class="sxs-lookup"><span data-stu-id="38cd6-260">Removed modules</span></span>

### `AzureRM.ServerManagement`

<span data-ttu-id="38cd6-261">Usługa Server Management Tools została [wycofana w zeszłym roku](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), w wyniku czego odpowiedni moduł dla usługi SMT, `AzureRM.ServerManagement`, został usunięty z modułu `AzureRM` i nie będzie w przyszłości dostarczany.</span><span class="sxs-lookup"><span data-stu-id="38cd6-261">The Server Management Tools service was [retired last year](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), and as a result, the corresponding module for SMT, `AzureRM.ServerManagement`, was removed from `AzureRM` and will stop shipping moving forward.</span></span>

### `AzureRM.SiteRecovery`

<span data-ttu-id="38cd6-262">Moduł `AzureRM.SiteRecovery` jest zastępowany przez moduł `AzureRM.RecoveryServices.SiteRecovery`, który jest funkcjonalnym nadzbiorem modułu `AzureRM.SiteRecovery` i obejmuje nowy zestaw równoważnych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38cd6-262">The `AzureRM.SiteRecovery` module is being superseded by `AzureRM.RecoveryServices.SiteRecovery`, which is a functional superset of the `AzureRM.SiteRecovery` module and includes a new set of equivalent cmdlets.</span></span> <span data-ttu-id="38cd6-263">Poniżej znajduje się pełna lista mapowań ze starych na nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="38cd6-263">The full list of mappings from old to new cmdlets can be found below:</span></span>

| <span data-ttu-id="38cd6-264">Przestarzałe polecenie cmdlet</span><span class="sxs-lookup"><span data-stu-id="38cd6-264">Deprecated cmdlet</span></span>                                        | <span data-ttu-id="38cd6-265">Równoważne polecenie cmdlet</span><span class="sxs-lookup"><span data-stu-id="38cd6-265">Equivalent cmdlet</span></span>                                                | <span data-ttu-id="38cd6-266">Aliasy</span><span class="sxs-lookup"><span data-stu-id="38cd6-266">Aliases</span></span>                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
