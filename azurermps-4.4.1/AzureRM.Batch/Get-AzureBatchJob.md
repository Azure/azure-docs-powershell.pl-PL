---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: c2aa673b9cd0f8cccc3f1a8721313f5a3236270d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546295"
---
# <span data-ttu-id="90482-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="90482-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="90482-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90482-102">SYNOPSIS</span></span>
<span data-ttu-id="90482-103">Pobiera zadania wsadowe dla konta partii lub harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="90482-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90482-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90482-104">SYNTAX</span></span>

### <span data-ttu-id="90482-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="90482-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90482-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="90482-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90482-107">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="90482-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90482-108">Opis</span><span class="sxs-lookup"><span data-stu-id="90482-108">DESCRIPTION</span></span>
<span data-ttu-id="90482-109">Polecenie cmdlet **Get-AzureBatchJob** pobiera zadania wsadowe platformy Azure dla konta wsadowego określonego przez parametr *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="90482-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="90482-110">Za pomocą parametru *ID* można uzyskać jedno zadanie.</span><span class="sxs-lookup"><span data-stu-id="90482-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="90482-111">Za pomocą parametru *Filter* można uzyskać zadania zgodne z filtrem Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="90482-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="90482-112">Jeśli zostanie podany identyfikator harmonogramu zadań lub wystąpienie **PSCloudJobSchedule** , to polecenie cmdlet zwróci tylko zadania dla tego harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="90482-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="90482-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90482-113">EXAMPLES</span></span>

### <span data-ttu-id="90482-114">Przykład 1: uzyskiwanie zadania wsadowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="90482-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job01" -BatchContext $Context
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

<span data-ttu-id="90482-115">To polecenie uzyskuje zadanie o IDENTYFIKATORze Job01.</span><span class="sxs-lookup"><span data-stu-id="90482-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="90482-116">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="90482-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="90482-117">Przykład 2: pobieranie wszystkich aktywnych zadań dla harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="90482-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzureBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
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

<span data-ttu-id="90482-118">To polecenie pobiera aktywne zadania harmonogramu zadań o IDENTYFIKATORze JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="90482-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="90482-119">Przykład 3: Pobiera wszystkie zadania w harmonogramie zadań przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="90482-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzureBatchJob -BatchContext $Context
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

<span data-ttu-id="90482-120">To polecenie pobiera harmonogram zadań o IDENTYFIKATORze JobSchedule27 przy użyciu polecenia cmdlet Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="90482-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="90482-121">Polecenie przekazuje ten harmonogram zadań do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="90482-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="90482-122">Polecenie pobiera wszystkie zadania dla tego harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="90482-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="90482-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90482-123">PARAMETERS</span></span>

### <span data-ttu-id="90482-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="90482-124">-BatchContext</span></span>
<span data-ttu-id="90482-125">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="90482-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="90482-126">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="90482-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="90482-127">-Expand</span><span class="sxs-lookup"><span data-stu-id="90482-127">-Expand</span></span>
<span data-ttu-id="90482-128">Określa klauzulę expanda Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="90482-128">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="90482-129">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej jednostki.</span><span class="sxs-lookup"><span data-stu-id="90482-129">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="90482-130">-Filter</span><span class="sxs-lookup"><span data-stu-id="90482-130">-Filter</span></span>
<span data-ttu-id="90482-131">Określa klauzulę filtru OData dla zadań.</span><span class="sxs-lookup"><span data-stu-id="90482-131">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="90482-132">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie zadania dla konta partii lub harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="90482-132">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="90482-133">-ID</span><span class="sxs-lookup"><span data-stu-id="90482-133">-Id</span></span>
<span data-ttu-id="90482-134">Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90482-134">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="90482-135">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="90482-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="90482-136">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="90482-136">-JobSchedule</span></span>
<span data-ttu-id="90482-137">Określa obiekt **PSCloudJobSchedule** , który reprezentuje harmonogram zadań zawierający zadania.</span><span class="sxs-lookup"><span data-stu-id="90482-137">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="90482-138">Aby uzyskać obiekt **PSCloudJobSchedule** , użyj polecenia cmdlet Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="90482-138">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="90482-139">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="90482-139">-JobScheduleId</span></span>
<span data-ttu-id="90482-140">Określa identyfikator harmonogramu zadań zawierającego zadania.</span><span class="sxs-lookup"><span data-stu-id="90482-140">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="90482-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="90482-141">-MaxCount</span></span>
<span data-ttu-id="90482-142">Określa maksymalną liczbę zadań do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="90482-142">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="90482-143">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="90482-143">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="90482-144">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="90482-144">The default value is 1000.</span></span>

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

### <span data-ttu-id="90482-145">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="90482-145">-Select</span></span>
<span data-ttu-id="90482-146">Określa klauzulę SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="90482-146">Specifies an OData select clause.</span></span>
<span data-ttu-id="90482-147">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="90482-147">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="90482-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90482-148">-DefaultProfile</span></span>
<span data-ttu-id="90482-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90482-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90482-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90482-150">CommonParameters</span></span>
<span data-ttu-id="90482-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90482-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90482-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90482-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90482-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90482-153">INPUTS</span></span>

### <span data-ttu-id="90482-154">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="90482-154">BatchAccountContext</span></span>
<span data-ttu-id="90482-155">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="90482-155">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="90482-156">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="90482-156">PSCloudJobSchedule</span></span>
<span data-ttu-id="90482-157">Parametr "JobSchedule" akceptuje wartość typu "PSCloudJobSchedule" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="90482-157">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="90482-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90482-158">OUTPUTS</span></span>

### <span data-ttu-id="90482-159">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="90482-159">PSCloudJob</span></span>

## <span data-ttu-id="90482-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90482-160">NOTES</span></span>

## <span data-ttu-id="90482-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90482-161">RELATED LINKS</span></span>

[<span data-ttu-id="90482-162">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="90482-162">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="90482-163">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="90482-163">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="90482-164">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="90482-164">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="90482-165">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="90482-165">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="90482-166">Nowe — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="90482-166">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="90482-167">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="90482-167">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="90482-168">Zatrzymaj — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="90482-168">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="90482-169">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="90482-169">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


