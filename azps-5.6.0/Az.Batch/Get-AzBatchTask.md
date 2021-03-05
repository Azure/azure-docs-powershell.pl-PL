---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: 214ee3b030757da9acf632b2768a94b1ab026cc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012721"
---
# <span data-ttu-id="9e2a7-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="9e2a7-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="9e2a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e2a7-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2a7-103">Pobiera zadania wsadowe dla zadania.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="9e2a7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9e2a7-104">SYNTAX</span></span>

### <span data-ttu-id="9e2a7-105">FiltrDanych OData (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9e2a7-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e2a7-106">Identyfikator</span><span class="sxs-lookup"><span data-stu-id="9e2a7-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e2a7-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="9e2a7-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e2a7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9e2a7-108">DESCRIPTION</span></span>
<span data-ttu-id="9e2a7-109">Polecenie **cmdlet Get-AzBatchTask** pobiera zadania partii platformy Azure dla zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="9e2a7-110">Określ zadanie za pomocą parametru *JobId* lub *parametru Job.*</span><span class="sxs-lookup"><span data-stu-id="9e2a7-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="9e2a7-111">Aby uzyskać jedno zadanie, określ *parametr Id.*</span><span class="sxs-lookup"><span data-stu-id="9e2a7-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="9e2a7-112">Możesz określić parametr *filtru,* aby uzyskać zadania zgodne z filtrem protokołu Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="9e2a7-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="9e2a7-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9e2a7-113">EXAMPLES</span></span>

### <span data-ttu-id="9e2a7-114">Przykład 1. Uzyskiwanie zadania według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="9e2a7-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
AffinityInformation         :
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 7/25/2015 11:24:52 PM
DisplayName                 :
EnvironmentSettings         :
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task03
LastModified                : 7/25/2015 11:24:52 PM
PreviousState               : Running
PreviousStateTransitionTime : 7/25/2015 11:24:59 PM
ResourceFiles               :
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 7/25/2015 11:24:59 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01/tasks/Task03
```

<span data-ttu-id="9e2a7-115">To polecenie pobiera zadanie o identyfikatorze Zadanie03 w obszarze Zadanie01.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="9e2a7-116">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="9e2a7-117">Przykład 2. Uzyskiwanie wszystkich ukończonych zadań z określonego zadania</span><span class="sxs-lookup"><span data-stu-id="9e2a7-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
AffinityInformation         :
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         :
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task17
LastModified                : 3/24/2015 10:21:51 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:22:00 PM
ResourceFiles               :
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 3/24/2015 10:22:00 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task17

AffinityInformation         :
CommandLine                 : cmd /c echo hello > newFile.txt
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         :
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task27
LastModified                : 3/24/2015 10:23:35 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:23:37 PM
ResourceFiles               :
RunElevated                 : True
State                       : Completed
StateTransitionTime         : 3/24/2015 10:23:37 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task27
```

<span data-ttu-id="9e2a7-118">To polecenie pobiera wykonane zadania z zadania o identyfikatorze Zadanie02.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="9e2a7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e2a7-119">PARAMETERS</span></span>

### <span data-ttu-id="9e2a7-120">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="9e2a7-120">-BatchContext</span></span>
<span data-ttu-id="9e2a7-121">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9e2a7-122">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9e2a7-123">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9e2a7-124">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9e2a7-125">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2a7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e2a7-126">-DefaultProfile</span></span>
<span data-ttu-id="9e2a7-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2a7-128">— Rozwiń</span><span class="sxs-lookup"><span data-stu-id="9e2a7-128">-Expand</span></span>
<span data-ttu-id="9e2a7-129">Określa klauzulę rozwijania danych OData.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="9e2a7-130">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej jednostki.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2a7-131">— Filtr</span><span class="sxs-lookup"><span data-stu-id="9e2a7-131">-Filter</span></span>
<span data-ttu-id="9e2a7-132">Określa klauzulę filtru OData dla zadań.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="9e2a7-133">Jeśli filtr nie zostanie określony, to polecenie cmdlet zwróci wszystkie zadania dla konta lub zadania Batch.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2a7-134">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="9e2a7-134">-Id</span></span>
<span data-ttu-id="9e2a7-135">Określa identyfikator zadania, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="9e2a7-136">Nie można określić symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-136">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2a7-137">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="9e2a7-137">-Job</span></span>
<span data-ttu-id="9e2a7-138">Określa zadanie zawierające zadania, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="9e2a7-139">Aby uzyskać obiekt **PSCloudJob,** użyj Get-AzBatchJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2a7-140">- JobId</span><span class="sxs-lookup"><span data-stu-id="9e2a7-140">-JobId</span></span>
<span data-ttu-id="9e2a7-141">Określa identyfikator zadania zawierającego zadania, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2a7-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9e2a7-142">-MaxCount</span></span>
<span data-ttu-id="9e2a7-143">Określa maksymalną liczbę zadań do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="9e2a7-144">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie użyje górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="9e2a7-145">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-145">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2a7-146">— Wybierz</span><span class="sxs-lookup"><span data-stu-id="9e2a7-146">-Select</span></span>
<span data-ttu-id="9e2a7-147">Określa klauzulę wybierania danych OData.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="9e2a7-148">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2a7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2a7-149">CommonParameters</span></span>
<span data-ttu-id="9e2a7-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e2a7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2a7-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e2a7-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2a7-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e2a7-152">INPUTS</span></span>

### <span data-ttu-id="9e2a7-153">System.String</span><span class="sxs-lookup"><span data-stu-id="9e2a7-153">System.String</span></span>

### <span data-ttu-id="9e2a7-154">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="9e2a7-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="9e2a7-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9e2a7-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9e2a7-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e2a7-156">OUTPUTS</span></span>

### <span data-ttu-id="9e2a7-157">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="9e2a7-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="9e2a7-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9e2a7-158">NOTES</span></span>

## <span data-ttu-id="9e2a7-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e2a7-159">RELATED LINKS</span></span>

[<span data-ttu-id="9e2a7-160">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9e2a7-160">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9e2a7-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="9e2a7-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="9e2a7-162">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="9e2a7-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="9e2a7-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="9e2a7-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="9e2a7-164">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="9e2a7-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="9e2a7-165">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="9e2a7-165">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
