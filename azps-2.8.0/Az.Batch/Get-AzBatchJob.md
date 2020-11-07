---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: 332bdb8d32b42d391518d50aef82436675cf3f9e
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93896874"
---
# <span data-ttu-id="4e150-101">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4e150-101">Get-AzBatchJob</span></span>

## <span data-ttu-id="4e150-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e150-102">SYNOPSIS</span></span>
<span data-ttu-id="4e150-103">Pobiera zadania wsadowe dla konta partii lub harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="4e150-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

## <span data-ttu-id="4e150-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e150-104">SYNTAX</span></span>

### <span data-ttu-id="4e150-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4e150-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e150-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="4e150-106">Id</span></span>
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e150-107">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="4e150-107">ParentObject</span></span>
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e150-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4e150-108">DESCRIPTION</span></span>
<span data-ttu-id="4e150-109">Polecenie cmdlet **Get-AzBatchJob** pobiera zadania wsadowe platformy Azure dla konta wsadowego określonego przez parametr *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="4e150-109">The **Get-AzBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="4e150-110">Za pomocą parametru *ID* można uzyskać jedno zadanie.</span><span class="sxs-lookup"><span data-stu-id="4e150-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="4e150-111">Za pomocą parametru *Filter* można uzyskać zadania zgodne z filtrem Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="4e150-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="4e150-112">Jeśli zostanie podany identyfikator harmonogramu zadań lub wystąpienie **PSCloudJobSchedule** , to polecenie cmdlet zwróci tylko zadania dla tego harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="4e150-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="4e150-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e150-113">EXAMPLES</span></span>

### <span data-ttu-id="4e150-114">Przykład 1: uzyskiwanie zadania wsadowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="4e150-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job01" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:12:07 PM
DisplayName                 : 
ETag                        : 0x8D29535B2941439
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : Job01
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:12:07 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:12:07 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01
```

<span data-ttu-id="4e150-115">To polecenie uzyskuje zadanie o IDENTYFIKATORze Job01.</span><span class="sxs-lookup"><span data-stu-id="4e150-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="4e150-116">Użyj polecenia cmdlet Get-AzBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="4e150-116">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="4e150-117">Przykład 2: pobieranie wszystkich aktywnych zadań dla harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="4e150-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="4e150-118">To polecenie pobiera aktywne zadania harmonogramu zadań o IDENTYFIKATORze JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="4e150-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="4e150-119">Przykład 3: Pobiera wszystkie zadania w harmonogramie zadań przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="4e150-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzBatchJob -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="4e150-120">To polecenie pobiera harmonogram zadań o IDENTYFIKATORze JobSchedule27 przy użyciu polecenia cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="4e150-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="4e150-121">Polecenie przekazuje ten harmonogram zadań do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="4e150-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4e150-122">Polecenie pobiera wszystkie zadania dla tego harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="4e150-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="4e150-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e150-123">PARAMETERS</span></span>

### <span data-ttu-id="4e150-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4e150-124">-BatchContext</span></span>
<span data-ttu-id="4e150-125">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="4e150-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4e150-126">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="4e150-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4e150-127">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="4e150-127">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4e150-128">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="4e150-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4e150-129">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4e150-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4e150-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e150-130">-DefaultProfile</span></span>
<span data-ttu-id="4e150-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e150-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e150-132">-Expand</span><span class="sxs-lookup"><span data-stu-id="4e150-132">-Expand</span></span>
<span data-ttu-id="4e150-133">Określa klauzulę expanda Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="4e150-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="4e150-134">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej jednostki.</span><span class="sxs-lookup"><span data-stu-id="4e150-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="4e150-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="4e150-135">-Filter</span></span>
<span data-ttu-id="4e150-136">Określa klauzulę filtru OData dla zadań.</span><span class="sxs-lookup"><span data-stu-id="4e150-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="4e150-137">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie zadania dla konta partii lub harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="4e150-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="4e150-138">-ID</span><span class="sxs-lookup"><span data-stu-id="4e150-138">-Id</span></span>
<span data-ttu-id="4e150-139">Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e150-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="4e150-140">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="4e150-140">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e150-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="4e150-141">-JobSchedule</span></span>
<span data-ttu-id="4e150-142">Określa obiekt **PSCloudJobSchedule** , który reprezentuje harmonogram zadań zawierający zadania.</span><span class="sxs-lookup"><span data-stu-id="4e150-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="4e150-143">Aby uzyskać obiekt **PSCloudJobSchedule** , użyj polecenia cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="4e150-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e150-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="4e150-144">-JobScheduleId</span></span>
<span data-ttu-id="4e150-145">Określa identyfikator harmonogramu zadań zawierającego zadania.</span><span class="sxs-lookup"><span data-stu-id="4e150-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e150-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4e150-146">-MaxCount</span></span>
<span data-ttu-id="4e150-147">Określa maksymalną liczbę zadań do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="4e150-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="4e150-148">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="4e150-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="4e150-149">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="4e150-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="4e150-150">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="4e150-150">-Select</span></span>
<span data-ttu-id="4e150-151">Określa klauzulę SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="4e150-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="4e150-152">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="4e150-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="4e150-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e150-153">CommonParameters</span></span>
<span data-ttu-id="4e150-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e150-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e150-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e150-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e150-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e150-156">INPUTS</span></span>

### <span data-ttu-id="4e150-157">System. String</span><span class="sxs-lookup"><span data-stu-id="4e150-157">System.String</span></span>

### <span data-ttu-id="4e150-158">Microsoft.Azure.Commands.Batch. Modele. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4e150-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="4e150-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4e150-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4e150-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e150-160">OUTPUTS</span></span>

### <span data-ttu-id="4e150-161">Microsoft.Azure.Commands.Batch. Modele. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="4e150-161">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="4e150-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e150-162">NOTES</span></span>

## <span data-ttu-id="4e150-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e150-163">RELATED LINKS</span></span>

[<span data-ttu-id="4e150-164">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4e150-164">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="4e150-165">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4e150-165">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="4e150-166">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4e150-166">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4e150-167">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4e150-167">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="4e150-168">Nowe — AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4e150-168">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="4e150-169">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4e150-169">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="4e150-170">Zatrzymaj — AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4e150-170">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="4e150-171">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="4e150-171">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


