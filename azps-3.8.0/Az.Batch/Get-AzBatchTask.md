---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: a0c6952b86485d6ec8417e6399e8f8348cd6f9a4
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "94061735"
---
# <span data-ttu-id="d0cc0-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d0cc0-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="d0cc0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="d0cc0-103">Pobiera zadania wsadowe dla zadania.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="d0cc0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0cc0-104">SYNTAX</span></span>

### <span data-ttu-id="d0cc0-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d0cc0-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0cc0-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="d0cc0-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0cc0-107">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="d0cc0-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0cc0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d0cc0-108">DESCRIPTION</span></span>
<span data-ttu-id="d0cc0-109">Polecenie cmdlet **Get-AzBatchTask** pobiera zadania wsadowe Azure Batch dla zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="d0cc0-110">Zadanie należy określić za pomocą parametru *JobID* lub parametru *zadania* .</span><span class="sxs-lookup"><span data-stu-id="d0cc0-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="d0cc0-111">Aby uzyskać jedno zadanie, określ parametr *ID* .</span><span class="sxs-lookup"><span data-stu-id="d0cc0-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="d0cc0-112">Możesz określić parametr *Filter* , aby uzyskać zadania zgodne z filtrem Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="d0cc0-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="d0cc0-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0cc0-113">EXAMPLES</span></span>

### <span data-ttu-id="d0cc0-114">Przykład 1. Uzyskaj zadanie według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="d0cc0-114">Example 1: Get a task by ID</span></span>
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

<span data-ttu-id="d0cc0-115">To polecenie pobiera zadanie z IDENTYFIKATORem Task03 w obszarze zadanie Job01.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="d0cc0-116">Użyj polecenia cmdlet Get-AzBatchAccountKey, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d0cc0-117">Przykład 2: pobieranie wszystkich wykonanych zadań z określonego zadania</span><span class="sxs-lookup"><span data-stu-id="d0cc0-117">Example 2: Get all completed tasks from a specified job</span></span>
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

<span data-ttu-id="d0cc0-118">To polecenie pobiera wykonane zadania z zadania o IDENTYFIKATORze Job02.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="d0cc0-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0cc0-119">PARAMETERS</span></span>

### <span data-ttu-id="d0cc0-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d0cc0-120">-BatchContext</span></span>
<span data-ttu-id="d0cc0-121">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d0cc0-122">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d0cc0-123">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d0cc0-124">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d0cc0-125">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d0cc0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0cc0-126">-DefaultProfile</span></span>
<span data-ttu-id="d0cc0-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0cc0-128">-Expand</span><span class="sxs-lookup"><span data-stu-id="d0cc0-128">-Expand</span></span>
<span data-ttu-id="d0cc0-129">Określa klauzulę expandu OData.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="d0cc0-130">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównego encji.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="d0cc0-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="d0cc0-131">-Filter</span></span>
<span data-ttu-id="d0cc0-132">Określa klauzulę filtru OData dla zadań.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="d0cc0-133">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie zadania dla tego konta lub zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="d0cc0-134">-ID</span><span class="sxs-lookup"><span data-stu-id="d0cc0-134">-Id</span></span>
<span data-ttu-id="d0cc0-135">Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="d0cc0-136">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-136">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="d0cc0-137">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="d0cc0-137">-Job</span></span>
<span data-ttu-id="d0cc0-138">Określa zadanie zawierające zadania, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="d0cc0-139">Aby uzyskać obiekt **PSCloudJob** , użyj polecenia cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="d0cc0-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="d0cc0-140">-JobId</span></span>
<span data-ttu-id="d0cc0-141">Określa identyfikator zadania zawierającego zadania, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d0cc0-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d0cc0-142">-MaxCount</span></span>
<span data-ttu-id="d0cc0-143">Określa maksymalną liczbę zadań, które należy zwrócić.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="d0cc0-144">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="d0cc0-145">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-145">The default value is 1000.</span></span>

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

### <span data-ttu-id="d0cc0-146">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="d0cc0-146">-Select</span></span>
<span data-ttu-id="d0cc0-147">Określa klauzulę SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="d0cc0-148">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="d0cc0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0cc0-149">CommonParameters</span></span>
<span data-ttu-id="d0cc0-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0cc0-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0cc0-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0cc0-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0cc0-152">INPUTS</span></span>

### <span data-ttu-id="d0cc0-153">System. String</span><span class="sxs-lookup"><span data-stu-id="d0cc0-153">System.String</span></span>

### <span data-ttu-id="d0cc0-154">Microsoft.Azure.Commands.Batch. Modele. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="d0cc0-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="d0cc0-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d0cc0-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d0cc0-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0cc0-156">OUTPUTS</span></span>

### <span data-ttu-id="d0cc0-157">Microsoft.Azure.Commands.Batch. Modele. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="d0cc0-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="d0cc0-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0cc0-158">NOTES</span></span>

## <span data-ttu-id="d0cc0-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0cc0-159">RELATED LINKS</span></span>

[<span data-ttu-id="d0cc0-160">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d0cc0-160">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d0cc0-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d0cc0-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="d0cc0-162">Nowe — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d0cc0-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="d0cc0-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d0cc0-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="d0cc0-164">Zatrzymaj — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d0cc0-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="d0cc0-165">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="d0cc0-165">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


