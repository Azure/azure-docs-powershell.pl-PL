---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: 4b570f78ddb73c7f0ab6dedcd4eca3ac26ff12df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986238"
---
# <span data-ttu-id="ec75a-101">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="ec75a-101">Get-AzBatchJob</span></span>

## <span data-ttu-id="ec75a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec75a-102">SYNOPSIS</span></span>
<span data-ttu-id="ec75a-103">Pobiera zadania partii dla konta wsadowego lub harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="ec75a-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

## <span data-ttu-id="ec75a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ec75a-104">SYNTAX</span></span>

### <span data-ttu-id="ec75a-105">FiltrDanych OData (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ec75a-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec75a-106">Identyfikator</span><span class="sxs-lookup"><span data-stu-id="ec75a-106">Id</span></span>
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec75a-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="ec75a-107">ParentObject</span></span>
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec75a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ec75a-108">DESCRIPTION</span></span>
<span data-ttu-id="ec75a-109">Polecenie **cmdlet Get-AzBatchJob** pobiera zadania usługi Azure Batch dla konta batch określonego przez *parametr BatchAccountContext.*</span><span class="sxs-lookup"><span data-stu-id="ec75a-109">The **Get-AzBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="ec75a-110">Możesz użyć *parametru Id,* aby uzyskać jedno zadanie.</span><span class="sxs-lookup"><span data-stu-id="ec75a-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="ec75a-111">Za pomocą *parametru Filter* można uzyskać zadania zgodne z filtrem protokołu Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="ec75a-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="ec75a-112">Jeśli zostanie nadany identyfikator harmonogramu zadań lub wystąpienie **psCloudJobSchedule,** to polecenie cmdlet zwróci tylko zadania dla tego harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="ec75a-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="ec75a-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ec75a-113">EXAMPLES</span></span>

### <span data-ttu-id="ec75a-114">Przykład 1. Uzyskiwanie zadania wsadowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="ec75a-114">Example 1: Get a Batch job by ID</span></span>
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

<span data-ttu-id="ec75a-115">To polecenie otrzymuje zadanie o identyfikatorze Zadanie01.</span><span class="sxs-lookup"><span data-stu-id="ec75a-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="ec75a-116">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="ec75a-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ec75a-117">Przykład 2. Uzyskiwanie wszystkich aktywnych zadań w harmonogramie zadań</span><span class="sxs-lookup"><span data-stu-id="ec75a-117">Example 2: Get all active jobs for a job schedule</span></span>
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

<span data-ttu-id="ec75a-118">To polecenie pobiera aktywne zadania dla harmonogramu zadań z harmonogramem zadań o identyfikatorze Harmonogram zadań27.</span><span class="sxs-lookup"><span data-stu-id="ec75a-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="ec75a-119">Przykład 3. Pobiera wszystkie zadania w ramach harmonogramu zadań przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="ec75a-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
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

<span data-ttu-id="ec75a-120">To polecenie pobiera harmonogram zadań, który ma identyfikator JobSchedule27, za pomocą Get-AzBatchJobSchedule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec75a-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="ec75a-121">Polecenie przekazuje ten harmonogram zadań do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="ec75a-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ec75a-122">To polecenie otrzymuje wszystkie zadania dla tego harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="ec75a-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="ec75a-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec75a-123">PARAMETERS</span></span>

### <span data-ttu-id="ec75a-124">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="ec75a-124">-BatchContext</span></span>
<span data-ttu-id="ec75a-125">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="ec75a-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ec75a-126">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ec75a-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ec75a-127">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="ec75a-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ec75a-128">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="ec75a-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ec75a-129">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ec75a-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ec75a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec75a-130">-DefaultProfile</span></span>
<span data-ttu-id="ec75a-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec75a-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec75a-132">— Rozwiń</span><span class="sxs-lookup"><span data-stu-id="ec75a-132">-Expand</span></span>
<span data-ttu-id="ec75a-133">Określa klauzulę rozwijania protokołu Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="ec75a-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="ec75a-134">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej o otrzymuję.</span><span class="sxs-lookup"><span data-stu-id="ec75a-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="ec75a-135">— Filtr</span><span class="sxs-lookup"><span data-stu-id="ec75a-135">-Filter</span></span>
<span data-ttu-id="ec75a-136">Określa klauzulę filtru OData dla zadań.</span><span class="sxs-lookup"><span data-stu-id="ec75a-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="ec75a-137">Jeśli filtr nie zostanie określony, to polecenie cmdlet zwróci wszystkie zadania dla konta wsadowego lub harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="ec75a-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="ec75a-138">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="ec75a-138">-Id</span></span>
<span data-ttu-id="ec75a-139">Określa identyfikator zadania, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec75a-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="ec75a-140">Nie można określić symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="ec75a-140">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="ec75a-141">— Harmonogram zadań</span><span class="sxs-lookup"><span data-stu-id="ec75a-141">-JobSchedule</span></span>
<span data-ttu-id="ec75a-142">Określa obiekt **PSCloudJobSchedule** reprezentujący harmonogram zadań zawierający te zadania.</span><span class="sxs-lookup"><span data-stu-id="ec75a-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="ec75a-143">Aby uzyskać **obiekt PSCloudJobSchedule,** użyj Get-AzBatchJobSchedule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec75a-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="ec75a-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="ec75a-144">-JobScheduleId</span></span>
<span data-ttu-id="ec75a-145">Określa identyfikator harmonogramu zadań, który zawiera zadania.</span><span class="sxs-lookup"><span data-stu-id="ec75a-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="ec75a-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ec75a-146">-MaxCount</span></span>
<span data-ttu-id="ec75a-147">Określa maksymalną liczbę zadań do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="ec75a-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="ec75a-148">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie użyje górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="ec75a-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="ec75a-149">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="ec75a-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="ec75a-150">— Wybierz</span><span class="sxs-lookup"><span data-stu-id="ec75a-150">-Select</span></span>
<span data-ttu-id="ec75a-151">Określa klauzulę wybierania danych OData.</span><span class="sxs-lookup"><span data-stu-id="ec75a-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="ec75a-152">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="ec75a-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="ec75a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec75a-153">CommonParameters</span></span>
<span data-ttu-id="ec75a-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec75a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec75a-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec75a-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec75a-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec75a-156">INPUTS</span></span>

### <span data-ttu-id="ec75a-157">System.String</span><span class="sxs-lookup"><span data-stu-id="ec75a-157">System.String</span></span>

### <span data-ttu-id="ec75a-158">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ec75a-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="ec75a-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ec75a-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ec75a-160">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec75a-160">OUTPUTS</span></span>

### <span data-ttu-id="ec75a-161">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="ec75a-161">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="ec75a-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ec75a-162">NOTES</span></span>

## <span data-ttu-id="ec75a-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec75a-163">RELATED LINKS</span></span>

[<span data-ttu-id="ec75a-164">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="ec75a-164">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="ec75a-165">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="ec75a-165">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="ec75a-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ec75a-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ec75a-167">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ec75a-167">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="ec75a-168">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="ec75a-168">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="ec75a-169">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="ec75a-169">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="ec75a-170">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="ec75a-170">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="ec75a-171">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ec75a-171">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
