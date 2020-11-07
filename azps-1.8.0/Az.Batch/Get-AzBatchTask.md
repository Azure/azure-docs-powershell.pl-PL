---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: b16939cdce5a4be471e1ae8133271349884e63a7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710832"
---
# <span data-ttu-id="bd221-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="bd221-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="bd221-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd221-102">SYNOPSIS</span></span>
<span data-ttu-id="bd221-103">Pobiera zadania wsadowe dla zadania.</span><span class="sxs-lookup"><span data-stu-id="bd221-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="bd221-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd221-104">SYNTAX</span></span>

### <span data-ttu-id="bd221-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bd221-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd221-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="bd221-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd221-107">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="bd221-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd221-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bd221-108">DESCRIPTION</span></span>
<span data-ttu-id="bd221-109">Polecenie cmdlet **Get-AzBatchTask** pobiera zadania wsadowe Azure Batch dla zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="bd221-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="bd221-110">Zadanie należy określić za pomocą parametru *JobID* lub parametru *zadania* .</span><span class="sxs-lookup"><span data-stu-id="bd221-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="bd221-111">Aby uzyskać jedno zadanie, określ parametr *ID* .</span><span class="sxs-lookup"><span data-stu-id="bd221-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="bd221-112">Możesz określić parametr *Filter* , aby uzyskać zadania zgodne z filtrem Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="bd221-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="bd221-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd221-113">EXAMPLES</span></span>

### <span data-ttu-id="bd221-114">Przykład 1. Uzyskaj zadanie według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="bd221-114">Example 1: Get a task by ID</span></span>
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

<span data-ttu-id="bd221-115">To polecenie pobiera zadanie z IDENTYFIKATORem Task03 w obszarze zadanie Job01.</span><span class="sxs-lookup"><span data-stu-id="bd221-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="bd221-116">Użyj polecenia cmdlet Get-AzBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="bd221-116">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="bd221-117">Przykład 2: pobieranie wszystkich wykonanych zadań z określonego zadania</span><span class="sxs-lookup"><span data-stu-id="bd221-117">Example 2: Get all completed tasks from a specified job</span></span>
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

<span data-ttu-id="bd221-118">To polecenie pobiera wykonane zadania z zadania o IDENTYFIKATORze Job02.</span><span class="sxs-lookup"><span data-stu-id="bd221-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="bd221-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd221-119">PARAMETERS</span></span>

### <span data-ttu-id="bd221-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bd221-120">-BatchContext</span></span>
<span data-ttu-id="bd221-121">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="bd221-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bd221-122">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="bd221-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bd221-123">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="bd221-123">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bd221-124">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="bd221-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bd221-125">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bd221-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bd221-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd221-126">-DefaultProfile</span></span>
<span data-ttu-id="bd221-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd221-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd221-128">-Expand</span><span class="sxs-lookup"><span data-stu-id="bd221-128">-Expand</span></span>
<span data-ttu-id="bd221-129">Określa klauzulę expandu OData.</span><span class="sxs-lookup"><span data-stu-id="bd221-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="bd221-130">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównego encji.</span><span class="sxs-lookup"><span data-stu-id="bd221-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="bd221-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="bd221-131">-Filter</span></span>
<span data-ttu-id="bd221-132">Określa klauzulę filtru OData dla zadań.</span><span class="sxs-lookup"><span data-stu-id="bd221-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="bd221-133">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie zadania dla tego konta lub zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="bd221-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="bd221-134">-ID</span><span class="sxs-lookup"><span data-stu-id="bd221-134">-Id</span></span>
<span data-ttu-id="bd221-135">Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd221-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="bd221-136">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="bd221-136">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="bd221-137">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="bd221-137">-Job</span></span>
<span data-ttu-id="bd221-138">Określa zadanie zawierające zadania, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd221-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="bd221-139">Aby uzyskać obiekt **PSCloudJob** , użyj polecenia cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="bd221-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="bd221-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="bd221-140">-JobId</span></span>
<span data-ttu-id="bd221-141">Określa identyfikator zadania zawierającego zadania, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd221-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bd221-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bd221-142">-MaxCount</span></span>
<span data-ttu-id="bd221-143">Określa maksymalną liczbę zadań, które należy zwrócić.</span><span class="sxs-lookup"><span data-stu-id="bd221-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="bd221-144">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="bd221-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="bd221-145">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="bd221-145">The default value is 1000.</span></span>

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

### <span data-ttu-id="bd221-146">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="bd221-146">-Select</span></span>
<span data-ttu-id="bd221-147">Określa klauzulę SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="bd221-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="bd221-148">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="bd221-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="bd221-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd221-149">CommonParameters</span></span>
<span data-ttu-id="bd221-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd221-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd221-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd221-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd221-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd221-152">INPUTS</span></span>

### <span data-ttu-id="bd221-153">System. String</span><span class="sxs-lookup"><span data-stu-id="bd221-153">System.String</span></span>

### <span data-ttu-id="bd221-154">Microsoft.Azure.Commands.Batch. Modele. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="bd221-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="bd221-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bd221-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bd221-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd221-156">OUTPUTS</span></span>

### <span data-ttu-id="bd221-157">Microsoft.Azure.Commands.Batch. Modele. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="bd221-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="bd221-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd221-158">NOTES</span></span>

## <span data-ttu-id="bd221-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd221-159">RELATED LINKS</span></span>

[<span data-ttu-id="bd221-160">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bd221-160">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="bd221-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="bd221-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="bd221-162">Nowe — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="bd221-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="bd221-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="bd221-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="bd221-164">Zatrzymaj — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="bd221-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="bd221-165">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="bd221-165">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

