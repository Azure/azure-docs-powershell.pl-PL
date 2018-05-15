# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="33522-101">Istotne zmiany dotyczące programu Microsoft Azure PowerShell 5.0.0</span><span class="sxs-lookup"><span data-stu-id="33522-101">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

<span data-ttu-id="33522-102">Ten dokument służy jako przewodnik zarówno po powiadomieniach o istotnych zmianach, jak i migracji dla użytkowników poleceń cmdlet programu Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33522-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="33522-103">Każda sekcja opisuje zarówno tempo istotnej zmiany, jak i ścieżkę migracji najmniejszego oporu.</span><span class="sxs-lookup"><span data-stu-id="33522-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="33522-104">Aby uzyskać szczegółowy kontekst, zapoznaj się z żądaniem ściągnięcia skojarzonym z każdą zmianą.</span><span class="sxs-lookup"><span data-stu-id="33522-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="33522-105">Spis treści</span><span class="sxs-lookup"><span data-stu-id="33522-105">Table of Contents</span></span>

- [<span data-ttu-id="33522-106">Istotne zmiany w poleceniach cmdlet usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="33522-106">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="33522-107">Istotne zmiany w poleceniach cmdlet usługi Batch</span><span class="sxs-lookup"><span data-stu-id="33522-107">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="33522-108">Istotne zmiany w poleceniach cmdlet usługi Compute</span><span class="sxs-lookup"><span data-stu-id="33522-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="33522-109">Istotne zmiany w poleceniach cmdlet usługi EventHub</span><span class="sxs-lookup"><span data-stu-id="33522-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="33522-110">Istotne zmiany w poleceniach cmdlet usługi Insights</span><span class="sxs-lookup"><span data-stu-id="33522-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="33522-111">Istotne zmiany w poleceniach cmdlet usługi Network</span><span class="sxs-lookup"><span data-stu-id="33522-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="33522-112">Istotne zmiany w poleceniach cmdlet usługi zasobów</span><span class="sxs-lookup"><span data-stu-id="33522-112">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="33522-113">Istotne zmiany w poleceniach cmdlet usługi ServiceBus</span><span class="sxs-lookup"><span data-stu-id="33522-113">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="33522-114">Istotne zmiany w poleceniach cmdlet usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="33522-114">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="33522-115">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="33522-115">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="33522-116">Parametry „UserName” i „Password” są zastępowane na rzecz obiektu PSCredential</span><span class="sxs-lookup"><span data-stu-id="33522-116">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="33522-117">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="33522-117">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="33522-118">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="33522-118">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="33522-119">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="33522-119">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="33522-120">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="33522-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="33522-121">Istotne zmiany w poleceniach cmdlet usługi Batch</span><span class="sxs-lookup"><span data-stu-id="33522-121">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="33522-122">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="33522-122">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="33522-123">Parametr `Password` jest zastępowany na rzecz ciągu zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="33522-123">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="33522-124">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="33522-124">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="33522-125">Parametr `Password` jest zastępowany na rzecz ciągu zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="33522-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="33522-126">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="33522-126">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="33522-127">Parametr `Password` jest zastępowany na rzecz ciągu zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="33522-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="33522-128">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="33522-128">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="33522-129">Usunięto przełącznik `RunElevated` i zastąpiono go właściwością `UserIdentity`.</span><span class="sxs-lookup"><span data-stu-id="33522-129">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="33522-130">Wpływa to również na właściwość `RunElevated` w obiektach `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` i `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="33522-130">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="33522-131">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="33522-131">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="33522-132">Konstruktor `PSMultiInstanceSettings` nie przyjmuje wymaganego parametru `numberOfInstances`; zamiast tego przyjmuje wymagany parametr `coordinationCommandLine`.</span><span class="sxs-lookup"><span data-stu-id="33522-132">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="33522-133">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="33522-133">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="33522-134">Usunięto właściwość `RunElevated` w elemencie `PSCloudTask`.</span><span class="sxs-lookup"><span data-stu-id="33522-134">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="33522-135">Dodano właściwość `UserIdentity` w celu zastąpienia właściwości `RunElevated`.</span><span class="sxs-lookup"><span data-stu-id="33522-135">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="33522-136">Wpływa to również na właściwość `RunElevated` w obiektach `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` i `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="33522-136">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="33522-137">**Wiele typów**</span><span class="sxs-lookup"><span data-stu-id="33522-137">**Multiple types**</span></span>

- <span data-ttu-id="33522-138">Nazwa właściwości `SchedulingError` w obiekcie `PSExitConditions` została zmieniona `PreProcessingError`.</span><span class="sxs-lookup"><span data-stu-id="33522-138">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="33522-139">**Wiele typów**</span><span class="sxs-lookup"><span data-stu-id="33522-139">**Multiple types**</span></span>

- <span data-ttu-id="33522-140">Nazwa właściwości `SchedulingError` w obiektach `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` i `PSTaskExecutionInformation` została zmieniona na `FailureInformation`.</span><span class="sxs-lookup"><span data-stu-id="33522-140">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="33522-141">`FailureInformation` jest zwracany zawsze w przypadku niepowodzenia zadania.</span><span class="sxs-lookup"><span data-stu-id="33522-141">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="33522-142">Obejmuje to wszystkie przypadki błędów planowania, a także kody zakończenia z wartością niezerową oraz błędy przekazywania plików z nowej funkcji plików wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="33522-142">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="33522-143">Struktura jest taka sama jak wcześniej, a więc w przypadku używania tego typu nie są wymagane żadne zmiany kodu.</span><span class="sxs-lookup"><span data-stu-id="33522-143">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="33522-144">Wpływa to również na polecenia Get-AzureBatchPool, Get-AzureBatchSubtask i Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="33522-144">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="33522-145">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="33522-145">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="33522-146">Usunięto właściwość `TargetDedicated` i zastąpiono ją właściwościami `TargetDedicatedComputeNodes` i `TargetLowPriorityComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="33522-146">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="33522-147">`TargetDedicatedComputeNodes` ma alias `TargetDedicated`.</span><span class="sxs-lookup"><span data-stu-id="33522-147">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="33522-148">Ma to również wpływ na polecenie Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="33522-148">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="33522-149">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="33522-149">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="33522-150">Nazwa właściwości `TargetDedicated` i `CurrentDedicated` w obiekcie `PSCloudPool` została zmieniona na `TargetDedicatedComputeNodes` i `CurrentDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="33522-150">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="33522-151">**Type PSCloudPool**</span><span class="sxs-lookup"><span data-stu-id="33522-151">**Type PSCloudPool**</span></span>

- <span data-ttu-id="33522-152">Zmieniono nazwę `ResizeError` na `ResizeErrors` w obiekcie `PSCloudPool` i teraz jest to kolekcja.</span><span class="sxs-lookup"><span data-stu-id="33522-152">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="33522-153">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="33522-153">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="33522-154">Nazwa właściwości `TargetDedicated` w obiekcie `PSPoolSpecification` została zmieniona na `TargetDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="33522-154">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell
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

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="33522-155">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="33522-155">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="33522-156">Usunięto właściwość `Name` i zastąpiono ją właściwością `Path`.</span><span class="sxs-lookup"><span data-stu-id="33522-156">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="33522-157">`Path` ma alias `Name`.</span><span class="sxs-lookup"><span data-stu-id="33522-157">`Path` has an alias `Name`.</span></span>

```powershell
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="33522-158">Ma również wpływ na polecenia Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="33522-158">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="33522-159">Typ **PSNodeFile**</span><span class="sxs-lookup"><span data-stu-id="33522-159">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="33522-160">Nazwa właściwości `Name` w obiekcie `PSNodeFile` została zmieniona na `Path`.</span><span class="sxs-lookup"><span data-stu-id="33522-160">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="33522-161">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="33522-161">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="33522-162">Właściwości `PreviousState` i `State` obiektu `PSSubtaskInformation` nie są już typu `TaskState`, lecz typu `SubtaskState`.</span><span class="sxs-lookup"><span data-stu-id="33522-162">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="33522-163">W odróżnieniu od typu `TaskState`, typ `SubtaskState` nie ma wartości `Active`, ponieważ podzadania nie mogą być w stanie `Active`.</span><span class="sxs-lookup"><span data-stu-id="33522-163">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="33522-164">Istotne zmiany w poleceniach cmdlet usługi Compute</span><span class="sxs-lookup"><span data-stu-id="33522-164">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="33522-165">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="33522-165">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="33522-166">Parametry „UserName” i „Password” są zastępowane na rzecz obiektu PSCredential</span><span class="sxs-lookup"><span data-stu-id="33522-166">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="33522-167">Istotne zmiany w poleceniach cmdlet usługi EventHub</span><span class="sxs-lookup"><span data-stu-id="33522-167">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="33522-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="33522-169">Polecenie cmdlet „New-AzureRmEventHubNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-169">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-170">Użyj polecenia cmdlet „New-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="33522-170">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="33522-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="33522-172">Polecenie cmdlet „Get-AzureRmEventHubNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-172">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-173">Użyj polecenia cmdlet „Get-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="33522-173">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="33522-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="33522-175">Polecenie cmdlet „Set-AzureRmEventHubNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-175">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-176">Użyj polecenia cmdlet „Set-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="33522-176">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="33522-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="33522-178">Polecenie cmdlet „Remove-AzureRmEventHubNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-178">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-179">Użyj polecenia cmdlet „Remove-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="33522-179">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="33522-180">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="33522-180">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="33522-181">Polecenie cmdlet „New-AzureRmEventHubNamespaceKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-181">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="33522-182">Użyj polecenia cmdlet „New-AzureRmEventHubKey”</span><span class="sxs-lookup"><span data-stu-id="33522-182">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="33522-183">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="33522-183">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="33522-184">Polecenie cmdlet „Get-AzureRmEventHubNamespaceKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-184">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="33522-185">Użyj polecenia „Get-AzureRmEventHubKey”</span><span class="sxs-lookup"><span data-stu-id="33522-185">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="33522-186">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="33522-186">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="33522-187">Właściwości „Status” i „Enabled” z atrybutów obszaru nazw zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-187">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="33522-188">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="33522-188">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="33522-189">Właściwości „Status” i „Enabled” z atrybutów obszaru nazw zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="33522-190">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="33522-190">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="33522-191">Właściwości „Status” i „Enabled” z atrybutów obszaru nazw zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="33522-192">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="33522-192">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="33522-193">Właściwość „EventHubPath” z elementu ConsumerGroupAttributes zostanie usunięta.</span><span class="sxs-lookup"><span data-stu-id="33522-193">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="33522-194">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="33522-194">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="33522-195">Właściwość „EventHubPath” z elementu ConsumerGroupAttributes zostanie usunięta.</span><span class="sxs-lookup"><span data-stu-id="33522-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="33522-196">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="33522-196">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="33522-197">Właściwość „EventHubPath” z elementu ConsumerGroupAttributes zostanie usunięta.</span><span class="sxs-lookup"><span data-stu-id="33522-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="33522-198">Istotne zmiany w poleceniach cmdlet usługi Insights</span><span class="sxs-lookup"><span data-stu-id="33522-198">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="33522-199">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="33522-199">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="33522-200">Polecenie cmdlet **Add-AzureRMLogAlertRule** jest przestarzałe</span><span class="sxs-lookup"><span data-stu-id="33522-200">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="33522-201">Po 1 października użycie tego polecenia cmdlet nie będzie miało żadnego efektu, ponieważ ta funkcja zostanie przeniesiona do alertów dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="33522-201">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="33522-202">Aby uzyskać więcej informacji, zobacz https://aka.ms/migratemealerts.</span><span class="sxs-lookup"><span data-stu-id="33522-202">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="33522-203">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="33522-203">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="33522-204">Polecenie **Get-AzureRMUsage** jest przestarzałe</span><span class="sxs-lookup"><span data-stu-id="33522-204">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="33522-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="33522-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="33522-206">Zmiana danych wyjściowych: pole EventChannels z obiektu EventData (zwracanego przez te polecenia cmdlet) jest przestarzałe, ponieważ obecnie zwraca wartość stałą (Admin,Operation).</span><span class="sxs-lookup"><span data-stu-id="33522-206">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="33522-207">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="33522-207">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="33522-208">Zmiana danych wyjściowych: dane wyjściowe tego polecenia cmdlet zostaną spłaszczone, co oznacza eliminację pola właściwości, aby ulepszyć środowisko użytkownika.</span><span class="sxs-lookup"><span data-stu-id="33522-208">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell
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

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="33522-209">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="33522-209">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="33522-210">Zmiana danych wyjściowych: pole AutoscaleSettingResourceName zostanie wycofane, ponieważ zawsze jest równe polu Nazwa.</span><span class="sxs-lookup"><span data-stu-id="33522-210">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell
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

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="33522-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="33522-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="33522-212">Zmiana danych wyjściowych: typ danych wyjściowych zmieni się, aby zwracać pojedynczy obiekt zawierający identyfikator żądania i kod stanu.</span><span class="sxs-lookup"><span data-stu-id="33522-212">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell
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

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="33522-213">Istotne zmiany w poleceniach cmdlet usługi Network</span><span class="sxs-lookup"><span data-stu-id="33522-213">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="33522-214">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="33522-214">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="33522-215">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="33522-215">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="33522-216">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="33522-216">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="33522-217">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="33522-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="33522-218">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="33522-218">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="33522-219">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="33522-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="33522-220">Istotne zmiany w poleceniach cmdlet zasobów</span><span class="sxs-lookup"><span data-stu-id="33522-220">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="33522-221">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="33522-221">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="33522-222">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="33522-222">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="33522-223">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="33522-223">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="33522-224">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="33522-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="33522-225">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="33522-225">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="33522-226">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="33522-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="33522-227">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="33522-227">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="33522-228">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="33522-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="33522-229">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="33522-229">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="33522-230">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="33522-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="33522-231">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="33522-231">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="33522-232">Parametr „Password” jest zastępowany na rzecz obiektu SecureString</span><span class="sxs-lookup"><span data-stu-id="33522-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="33522-233">Istotne zmiany w poleceniach cmdlet usługi ServiceBus</span><span class="sxs-lookup"><span data-stu-id="33522-233">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="33522-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="33522-235">Polecenie cmdlet „Get-AzureRmServiceBusTopicAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-235">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-236">Użyj polecenia cmdlet „Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="33522-236">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="33522-237">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="33522-237">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="33522-238">Polecenie cmdlet „Get-AzureRmServiceBusTopicKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-238">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="33522-239">Użyj polecenia cmdlet „Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="33522-239">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="33522-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="33522-241">Polecenie cmdlet „New-AzureRmServiceBusTopicAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-241">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-242">Użyj polecenia cmdlet „New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="33522-242">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="33522-243">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="33522-243">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="33522-244">Polecenie cmdlet „New-AzureRmServiceBusTopicKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-244">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="33522-245">Użyj polecenia cmdlet „New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="33522-245">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="33522-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="33522-247">Polecenie cmdlet „Remove-AzureRmServiceBusTopicAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-247">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-248">Użyj polecenia cmdlet „Remove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="33522-248">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="33522-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="33522-250">Polecenie cmdlet „Set-AzureRmServiceBusTopicAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-250">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-251">Użyj polecenia cmdlet „Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="33522-251">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="33522-252">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="33522-252">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="33522-253">Polecenie cmdlet „New-AzureRmServiceBusNamespaceKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-253">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="33522-254">Użyj polecenia cmdlet „New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="33522-254">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="33522-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="33522-256">Polecenie cmdlet „Get-AzureRmServiceBusQueueAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-256">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-257">Użyj polecenia cmdlet „Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="33522-257">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="33522-258">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="33522-258">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="33522-259">Polecenie cmdlet „Get-AzureRmServiceBusQueueKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-259">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="33522-260">Użyj polecenia cmdlet „Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="33522-260">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="33522-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="33522-262">Polecenie cmdlet „New-AzureRmServiceBusQueueAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-262">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-263">Użyj polecenia cmdlet „New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="33522-263">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="33522-264">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="33522-264">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="33522-265">Polecenie cmdlet „New-AzureRmServiceBusQueueKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-265">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="33522-266">Użyj polecenia cmdlet „New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="33522-266">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="33522-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="33522-268">Polecenie cmdlet „Remove-AzureRmServiceBusQueueAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-268">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-269">Użyj polecenia cmdlet „GRemove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="33522-269">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="33522-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="33522-271">Polecenie cmdlet „Set-AzureRmServiceBusQueueAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-271">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-272">Użyj polecenia cmdlet „Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="33522-272">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="33522-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="33522-274">Polecenie cmdlet „Get-AzureRmServiceBusNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-274">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-275">Użyj polecenia cmdlet „Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="33522-275">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="33522-276">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="33522-276">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="33522-277">Polecenie cmdlet „Get-AzureRmServiceBusNamespaceKey” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-277">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="33522-278">Użyj polecenia cmdlet „Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="33522-278">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="33522-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="33522-280">Polecenie cmdlet „New-AzureRmServiceBusNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-280">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-281">Użyj polecenia cmdlet „New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="33522-281">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="33522-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="33522-283">Polecenie cmdlet „Remove-AzureRmServiceBusNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-283">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-284">Użyj polecenia cmdlet „Remove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="33522-284">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="33522-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="33522-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="33522-286">Polecenie cmdlet „Set-AzureRmServiceBusNamespaceAuthorizationRule” zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33522-286">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="33522-287">Użyj polecenia cmdlet „Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="33522-287">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="33522-288">**Typ NamespaceAttributes**</span><span class="sxs-lookup"><span data-stu-id="33522-288">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="33522-289">Usunięto następujące właściwości</span><span class="sxs-lookup"><span data-stu-id="33522-289">The following properties have been removed</span></span>
    - <span data-ttu-id="33522-290">Enabled (Włączony)</span><span class="sxs-lookup"><span data-stu-id="33522-290">Enabled</span></span>
    - <span data-ttu-id="33522-291">Stan</span><span class="sxs-lookup"><span data-stu-id="33522-291">Status</span></span>
   
```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="33522-292">**Typ QueueAttribute**</span><span class="sxs-lookup"><span data-stu-id="33522-292">**Type QueueAttribute**</span></span>
- <span data-ttu-id="33522-293">Następujące właściwości są oznaczone jako przestarzałe:</span><span class="sxs-lookup"><span data-stu-id="33522-293">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="33522-294">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="33522-294">EnableBatchedOperations</span></span>
    - <span data-ttu-id="33522-295">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="33522-295">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="33522-296">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="33522-296">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="33522-297">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="33522-297">SupportOrdering</span></span>

```powershell
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
   
### <a name="type-topicattribute"></a><span data-ttu-id="33522-298">**Typ TopicAttribute**</span><span class="sxs-lookup"><span data-stu-id="33522-298">**Type TopicAttribute**</span></span>
- <span data-ttu-id="33522-299">Następujące właściwości są oznaczone jako przestarzałe:</span><span class="sxs-lookup"><span data-stu-id="33522-299">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="33522-300">Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="33522-300">Location</span></span>
    - <span data-ttu-id="33522-301">IsExpress</span><span class="sxs-lookup"><span data-stu-id="33522-301">IsExpress</span></span>
    - <span data-ttu-id="33522-302">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="33522-302">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="33522-303">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="33522-303">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="33522-304">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="33522-304">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="33522-305">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="33522-305">EntityAvailabilityStatus</span></span>

```powershell
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
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="33522-306">**Typ SubscriptionAttribute**</span><span class="sxs-lookup"><span data-stu-id="33522-306">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="33522-307">Następujące właściwości są oznaczone jako przestarzałe</span><span class="sxs-lookup"><span data-stu-id="33522-307">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="33522-308">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="33522-308">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="33522-309">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="33522-309">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="33522-310">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="33522-310">IsReadOnly</span></span>
    - <span data-ttu-id="33522-311">Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="33522-311">Location</span></span>
   
```powershell
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