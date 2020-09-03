---
title: Istotne zmiany dotyczące programu Microsoft Azure PowerShell 5.0.0
description: Ten przewodnik po migracji zawiera listę zmian powodujących niezgodność wprowadzonych w programie Azure PowerShell w wersji 5.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 81f52ee8b84f60d59a7f2d53b6675129ac054fd6
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243739"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="5dcbd-103">Istotne zmiany dotyczące programu Microsoft Azure PowerShell 5.0.0</span><span class="sxs-lookup"><span data-stu-id="5dcbd-103">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="5dcbd-104">Ten dokument służy jako przewodnik zarówno po powiadomieniach o istotnych zmianach, jak i migracji dla użytkowników poleceń cmdlet programu Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="5dcbd-105">Każda sekcja opisuje zarówno tempo istotnej zmiany, jak i ścieżkę migracji najmniejszego oporu.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="5dcbd-106">Aby uzyskać szczegółowy kontekst, zapoznaj się z żądaniem ściągnięcia skojarzonym z każdą zmianą.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="5dcbd-107">Spis treści</span><span class="sxs-lookup"><span data-stu-id="5dcbd-107">Table of Contents</span></span>

- [<span data-ttu-id="5dcbd-108">Istotne zmiany w poleceniach cmdlet usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5dcbd-108">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="5dcbd-109">Istotne zmiany w poleceniach cmdlet usługi Batch</span><span class="sxs-lookup"><span data-stu-id="5dcbd-109">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="5dcbd-110">Istotne zmiany w poleceniach cmdlet usługi Compute</span><span class="sxs-lookup"><span data-stu-id="5dcbd-110">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="5dcbd-111">Istotne zmiany w poleceniach cmdlet usługi EventHub</span><span class="sxs-lookup"><span data-stu-id="5dcbd-111">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="5dcbd-112">Istotne zmiany w poleceniach cmdlet usługi Insights</span><span class="sxs-lookup"><span data-stu-id="5dcbd-112">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="5dcbd-113">Istotne zmiany w poleceniach cmdlet usługi Network</span><span class="sxs-lookup"><span data-stu-id="5dcbd-113">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="5dcbd-114">Istotne zmiany w poleceniach cmdlet usługi zasobów</span><span class="sxs-lookup"><span data-stu-id="5dcbd-114">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="5dcbd-115">Istotne zmiany w poleceniach cmdlet usługi ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5dcbd-115">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="5dcbd-116">Istotne zmiany w poleceniach cmdlet usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5dcbd-116">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="5dcbd-117">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-117">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="5dcbd-118">Parametry „UserName” i „Password” są zastępowane na rzecz obiektu PSCredential</span><span class="sxs-lookup"><span data-stu-id="5dcbd-118">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="5dcbd-119">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-119">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="5dcbd-120">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="5dcbd-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="5dcbd-121">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-121">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="5dcbd-122">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="5dcbd-122">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="5dcbd-123">Istotne zmiany w poleceniach cmdlet usługi Batch</span><span class="sxs-lookup"><span data-stu-id="5dcbd-123">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="5dcbd-124">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-124">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="5dcbd-125">Parametr `Password` jest zastępowany na rzecz ciągu zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="5dcbd-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="5dcbd-126">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-126">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="5dcbd-127">Parametr `Password` jest zastępowany na rzecz ciągu zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="5dcbd-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="5dcbd-128">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-128">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="5dcbd-129">Parametr `Password` jest zastępowany na rzecz ciągu zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="5dcbd-129">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="5dcbd-130">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-130">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="5dcbd-131">Usunięto przełącznik `RunElevated` i zastąpiono go właściwością `UserIdentity`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-131">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="5dcbd-132">Wpływa to również na właściwość `RunElevated` w obiektach `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` i `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-132">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="5dcbd-133">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-133">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="5dcbd-134">Konstruktor `PSMultiInstanceSettings` nie przyjmuje wymaganego parametru `numberOfInstances`; zamiast tego przyjmuje wymagany parametr `coordinationCommandLine`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-134">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="5dcbd-135">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-135">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="5dcbd-136">Usunięto właściwość `RunElevated` w elemencie `PSCloudTask`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-136">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="5dcbd-137">Dodano właściwość `UserIdentity` w celu zastąpienia właściwości `RunElevated`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-137">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="5dcbd-138">Wpływa to również na właściwość `RunElevated` w obiektach `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` i `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-138">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="5dcbd-139">**Wiele typów**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-139">**Multiple types**</span></span>

- <span data-ttu-id="5dcbd-140">Nazwa właściwości `SchedulingError` w obiekcie `PSExitConditions` została zmieniona `PreProcessingError`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-140">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="5dcbd-141">**Wiele typów**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-141">**Multiple types**</span></span>

- <span data-ttu-id="5dcbd-142">Nazwa właściwości `SchedulingError` w obiektach `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` i `PSTaskExecutionInformation` została zmieniona na `FailureInformation`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-142">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="5dcbd-143">`FailureInformation` jest zwracany zawsze w przypadku niepowodzenia zadania.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-143">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="5dcbd-144">Obejmuje to wszystkie przypadki błędów planowania, a także kody zakończenia z wartością niezerową oraz błędy przekazywania plików z nowej funkcji plików wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-144">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="5dcbd-145">Struktura jest taka sama jak wcześniej, a więc w przypadku używania tego typu nie są wymagane żadne zmiany kodu.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-145">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="5dcbd-146">Wpływa to również na polecenia: Get-AzureBatchPool, Get-AzureBatchSubtask i Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="5dcbd-146">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="5dcbd-147">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-147">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="5dcbd-148">Usunięto właściwość `TargetDedicated` i zastąpiono ją właściwościami `TargetDedicatedComputeNodes` i `TargetLowPriorityComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-148">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="5dcbd-149">`TargetDedicatedComputeNodes` ma alias `TargetDedicated`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-149">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="5dcbd-150">Ma to również wpływ na polecenia: Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="5dcbd-150">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="5dcbd-151">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-151">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="5dcbd-152">Nazwa właściwości `TargetDedicated` i `CurrentDedicated` w obiekcie `PSCloudPool` została zmieniona na `TargetDedicatedComputeNodes` i `CurrentDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-152">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="5dcbd-153">**Type PSCloudPool**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-153">**Type PSCloudPool**</span></span>

- <span data-ttu-id="5dcbd-154">Zmieniono nazwę `ResizeError` na `ResizeErrors` w obiekcie `PSCloudPool` i teraz jest to kolekcja.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-154">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="5dcbd-155">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-155">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="5dcbd-156">Nazwa właściwości `TargetDedicated` w obiekcie `PSPoolSpecification` została zmieniona na `TargetDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-156">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell-interactive
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="5dcbd-157">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-157">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="5dcbd-158">Usunięto właściwość `Name` i zastąpiono ją właściwością `Path`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-158">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="5dcbd-159">`Path` ma alias `Name`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-159">`Path` has an alias `Name`.</span></span>

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="5dcbd-160">Ma to również wpływ na polecenia: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="5dcbd-160">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="5dcbd-161">Typ **PSNodeFile**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-161">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="5dcbd-162">Nazwa właściwości `Name` w obiekcie `PSNodeFile` została zmieniona na `Path`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-162">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="5dcbd-163">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-163">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="5dcbd-164">Właściwości `PreviousState` i `State` obiektu `PSSubtaskInformation` nie są już typu `TaskState`, lecz typu `SubtaskState`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-164">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="5dcbd-165">W odróżnieniu od typu `TaskState`, typ `SubtaskState` nie ma wartości `Active`, ponieważ podzadania nie mogą być w stanie `Active`.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-165">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="5dcbd-166">Istotne zmiany w poleceniach cmdlet usługi Compute</span><span class="sxs-lookup"><span data-stu-id="5dcbd-166">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="5dcbd-167">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-167">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="5dcbd-168">Parametry „UserName” i „Password” są zastępowane na rzecz obiektu PSCredential</span><span class="sxs-lookup"><span data-stu-id="5dcbd-168">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="5dcbd-169">Istotne zmiany w poleceniach cmdlet usługi EventHub</span><span class="sxs-lookup"><span data-stu-id="5dcbd-169">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="5dcbd-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-171">Polecenie cmdlet „New-AzureRmEventHubNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-171">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-172">Użyj polecenia cmdlet „New-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="5dcbd-172">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>

### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="5dcbd-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-174">Polecenie cmdlet „Get-AzureRmEventHubNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-174">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-175">Użyj polecenia cmdlet „Get-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="5dcbd-175">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>

### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="5dcbd-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-177">Polecenie cmdlet „Set-AzureRmEventHubNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-177">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-178">Użyj polecenia cmdlet „Set-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="5dcbd-178">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>

### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="5dcbd-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-180">Polecenie cmdlet „Remove-AzureRmEventHubNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-180">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-181">Użyj polecenia cmdlet „Remove-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="5dcbd-181">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>

### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="5dcbd-182">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-182">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="5dcbd-183">Polecenie cmdlet „New-AzureRmEventHubNamespaceKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-183">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-184">Użyj polecenia cmdlet „New-AzureRmEventHubKey”</span><span class="sxs-lookup"><span data-stu-id="5dcbd-184">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>

### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="5dcbd-185">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-185">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="5dcbd-186">Polecenie cmdlet „Get-AzureRmEventHubNamespaceKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-186">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-187">Użyj polecenia „Get-AzureRmEventHubKey”</span><span class="sxs-lookup"><span data-stu-id="5dcbd-187">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="5dcbd-188">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-188">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="5dcbd-189">Właściwości „Status” i „Enabled” z atrybutów obszaru nazw zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property
$namespace = Get-AzureRmEventHubNamespace <parameters>
```

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="5dcbd-190">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-190">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="5dcbd-191">Właściwości „Status” i „Enabled” z atrybutów obszaru nazw zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property
$namespace = Get-AzureRmEventHubNamespace <parameters>
```

### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="5dcbd-192">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-192">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="5dcbd-193">Właściwości „Status” i „Enabled” z atrybutów obszaru nazw zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-193">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property
$namespace = Set-AzureRmEventHubNamespace <parameters>
```

### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="5dcbd-194">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-194">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="5dcbd-195">Właściwość „EventHubPath” z elementu ConsumerGroupAttributes zostanie usunięta.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```

### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="5dcbd-196">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-196">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="5dcbd-197">Właściwość „EventHubPath” z elementu ConsumerGroupAttributes zostanie usunięta.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```

### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="5dcbd-198">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-198">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="5dcbd-199">Właściwość „EventHubPath” z elementu ConsumerGroupAttributes zostanie usunięta.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-199">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="5dcbd-200">Istotne zmiany w poleceniach cmdlet usługi Insights</span><span class="sxs-lookup"><span data-stu-id="5dcbd-200">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="5dcbd-201">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-201">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="5dcbd-202">Polecenie cmdlet **Add-AzureRMLogAlertRule** jest przestarzałe</span><span class="sxs-lookup"><span data-stu-id="5dcbd-202">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="5dcbd-203">Po 1 października użycie tego polecenia cmdlet nie będzie miało żadnego efektu, ponieważ ta funkcja zostanie przeniesiona do alertów dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-203">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="5dcbd-204">Aby uzyskać więcej informacji, zobacz https://aka.ms/migratemealerts.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-204">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="5dcbd-205">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-205">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="5dcbd-206">Polecenie **Get-AzureRMUsage** jest przestarzałe</span><span class="sxs-lookup"><span data-stu-id="5dcbd-206">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="5dcbd-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="5dcbd-208">Zmiana danych wyjściowych: pole EventChannels z obiektu EventData (zwracanego przez te polecenia cmdlet) jest przestarzałe, ponieważ obecnie zwraca wartość stałą (Admin,Operation).</span><span class="sxs-lookup"><span data-stu-id="5dcbd-208">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="5dcbd-209">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-209">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="5dcbd-210">Zmiana danych wyjściowych: dane wyjściowe tego polecenia cmdlet zostaną spłaszczone, co oznacza eliminację pola właściwości, aby ulepszyć środowisko użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-210">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled

    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="5dcbd-211">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-211">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="5dcbd-212">Zmiana danych wyjściowych: pole AutoscaleSettingResourceName zostanie wycofane, ponieważ zawsze jest równe polu Nazwa.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-212">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell-interactive
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting

# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="5dcbd-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="5dcbd-214">Zmiana danych wyjściowych: typ danych wyjściowych zmieni się, aby zwracać pojedynczy obiekt zawierający identyfikator żądania i kod stanu.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-214">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell-interactive
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="5dcbd-215">Istotne zmiany w poleceniach cmdlet usługi Network</span><span class="sxs-lookup"><span data-stu-id="5dcbd-215">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="5dcbd-216">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-216">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="5dcbd-217">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="5dcbd-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="5dcbd-218">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-218">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="5dcbd-219">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="5dcbd-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="5dcbd-220">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-220">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="5dcbd-221">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="5dcbd-221">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="5dcbd-222">Istotne zmiany w poleceniach cmdlet zasobów</span><span class="sxs-lookup"><span data-stu-id="5dcbd-222">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="5dcbd-223">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-223">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="5dcbd-224">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="5dcbd-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="5dcbd-225">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-225">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="5dcbd-226">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="5dcbd-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="5dcbd-227">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-227">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="5dcbd-228">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="5dcbd-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="5dcbd-229">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-229">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="5dcbd-230">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="5dcbd-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="5dcbd-231">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-231">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="5dcbd-232">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="5dcbd-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="5dcbd-233">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-233">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="5dcbd-234">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="5dcbd-234">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="5dcbd-235">Istotne zmiany w poleceniach cmdlet usługi ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5dcbd-235">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="5dcbd-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-237">Polecenie cmdlet „Get-AzureRmServiceBusTopicAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-237">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-238">Użyj polecenia cmdlet „Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-238">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="5dcbd-239">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-239">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="5dcbd-240">Polecenie cmdlet „Get-AzureRmServiceBusTopicKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-240">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-241">Użyj polecenia cmdlet „Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-241">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="5dcbd-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-243">Polecenie cmdlet „New-AzureRmServiceBusTopicAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-243">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-244">Użyj polecenia cmdlet „New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-244">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="5dcbd-245">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-245">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="5dcbd-246">Polecenie cmdlet „New-AzureRmServiceBusTopicKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-246">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-247">Użyj polecenia cmdlet „New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-247">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="5dcbd-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-249">Polecenie cmdlet „Remove-AzureRmServiceBusTopicAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-249">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-250">Użyj polecenia cmdlet „Remove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-250">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="5dcbd-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-252">Polecenie cmdlet „Set-AzureRmServiceBusTopicAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-252">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-253">Użyj polecenia cmdlet „Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-253">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="5dcbd-254">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-254">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="5dcbd-255">Polecenie cmdlet „New-AzureRmServiceBusNamespaceKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-255">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-256">Użyj polecenia cmdlet „New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-256">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="5dcbd-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-258">Polecenie cmdlet „Get-AzureRmServiceBusQueueAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-258">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-259">Użyj polecenia cmdlet „Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-259">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="5dcbd-260">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-260">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="5dcbd-261">Polecenie cmdlet „Get-AzureRmServiceBusQueueKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-261">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-262">Użyj polecenia cmdlet „Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-262">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="5dcbd-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-264">Polecenie cmdlet „New-AzureRmServiceBusQueueAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-264">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-265">Użyj polecenia cmdlet „New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-265">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="5dcbd-266">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-266">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="5dcbd-267">Polecenie cmdlet „New-AzureRmServiceBusQueueKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-267">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-268">Użyj polecenia cmdlet „New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-268">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="5dcbd-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-270">Polecenie cmdlet „Remove-AzureRmServiceBusQueueAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-270">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-271">Użyj polecenia cmdlet „GRemove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-271">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="5dcbd-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-273">Polecenie cmdlet „Set-AzureRmServiceBusQueueAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-273">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-274">Użyj polecenia cmdlet „Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-274">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="5dcbd-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-276">Polecenie cmdlet „Get-AzureRmServiceBusNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-276">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-277">Użyj polecenia cmdlet „Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-277">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="5dcbd-278">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-278">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="5dcbd-279">Polecenie cmdlet „Get-AzureRmServiceBusNamespaceKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-279">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-280">Użyj polecenia cmdlet „Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-280">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="5dcbd-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-282">Polecenie cmdlet „New-AzureRmServiceBusNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-282">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-283">Użyj polecenia cmdlet „New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-283">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="5dcbd-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-285">Polecenie cmdlet „Remove-AzureRmServiceBusNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-285">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-286">Użyj polecenia cmdlet „Remove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-286">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="5dcbd-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5dcbd-288">Polecenie cmdlet „Set-AzureRmServiceBusNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-288">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5dcbd-289">Użyj polecenia cmdlet „Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5dcbd-289">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="5dcbd-290">**Typ NamespaceAttributes**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-290">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="5dcbd-291">Usunięto następujące właściwości</span><span class="sxs-lookup"><span data-stu-id="5dcbd-291">The following properties have been removed</span></span>
    - <span data-ttu-id="5dcbd-292">Enabled (Włączony)</span><span class="sxs-lookup"><span data-stu-id="5dcbd-292">Enabled</span></span>
    - <span data-ttu-id="5dcbd-293">Stan</span><span class="sxs-lookup"><span data-stu-id="5dcbd-293">Status</span></span>

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="5dcbd-294">**Typ QueueAttribute**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-294">**Type QueueAttribute**</span></span>
- <span data-ttu-id="5dcbd-295">Następujące właściwości są oznaczone jako przestarzałe:</span><span class="sxs-lookup"><span data-stu-id="5dcbd-295">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="5dcbd-296">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="5dcbd-296">EnableBatchedOperations</span></span>
    - <span data-ttu-id="5dcbd-297">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="5dcbd-297">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="5dcbd-298">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="5dcbd-298">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="5dcbd-299">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="5dcbd-299">SupportOrdering</span></span>

```powershell-interactive
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
```

### <a name="type-topicattribute"></a><span data-ttu-id="5dcbd-300">**Typ TopicAttribute**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-300">**Type TopicAttribute**</span></span>
- <span data-ttu-id="5dcbd-301">Następujące właściwości są oznaczone jako przestarzałe:</span><span class="sxs-lookup"><span data-stu-id="5dcbd-301">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="5dcbd-302">Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5dcbd-302">Location</span></span>
    - <span data-ttu-id="5dcbd-303">IsExpress</span><span class="sxs-lookup"><span data-stu-id="5dcbd-303">IsExpress</span></span>
    - <span data-ttu-id="5dcbd-304">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="5dcbd-304">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="5dcbd-305">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="5dcbd-305">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="5dcbd-306">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="5dcbd-306">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="5dcbd-307">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="5dcbd-307">EntityAvailabilityStatus</span></span>

```powershell-interactive
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$topic = Get-AzureRmServiceBusTopic <parameters>
```

### <a name="type-subscriptionattribute"></a><span data-ttu-id="5dcbd-308">**Typ SubscriptionAttribute**</span><span class="sxs-lookup"><span data-stu-id="5dcbd-308">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="5dcbd-309">Następujące właściwości są oznaczone jako przestarzałe</span><span class="sxs-lookup"><span data-stu-id="5dcbd-309">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="5dcbd-310">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="5dcbd-310">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="5dcbd-311">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="5dcbd-311">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="5dcbd-312">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="5dcbd-312">IsReadOnly</span></span>
    - <span data-ttu-id="5dcbd-313">Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5dcbd-313">Location</span></span>

```powershell-interactive
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
```
