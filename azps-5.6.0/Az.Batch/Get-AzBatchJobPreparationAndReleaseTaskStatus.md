---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: e85976b4d4b5de508e1a4f25338b21abdb0c097f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983466"
---
# <span data-ttu-id="741b2-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="741b2-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="741b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="741b2-102">SYNOPSIS</span></span>
<span data-ttu-id="741b2-103">Pobiera stan zadań wsadowych i zwalniania zadań.</span><span class="sxs-lookup"><span data-stu-id="741b2-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="741b2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="741b2-104">SYNTAX</span></span>

### <span data-ttu-id="741b2-105">Identyfikator (domyślne)</span><span class="sxs-lookup"><span data-stu-id="741b2-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="741b2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="741b2-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="741b2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="741b2-107">DESCRIPTION</span></span>
<span data-ttu-id="741b2-108">Polecenie **cmdlet Get-AzBatchJobPreparationAndReleaseTaskStatus** pobiera zadanie wsadowe platformy Azure i stan zadania wsadowego dla zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="741b2-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="741b2-109">Do tego  polecenia cmdlet należy podać parametr Id lub wystąpienie usługi **PSCloudJob.**</span><span class="sxs-lookup"><span data-stu-id="741b2-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="741b2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="741b2-110">EXAMPLES</span></span>

### <span data-ttu-id="741b2-111">Przykład 1. Uzyskiwanie informacji o przygotowaniu stanowiska i zwolnieniu jego stanowiska</span><span class="sxs-lookup"><span data-stu-id="741b2-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="741b2-112">To polecenie pobiera informacje o przygotowaniu zadania i zwolnieniu stanu zadania dla zadania "Test".</span><span class="sxs-lookup"><span data-stu-id="741b2-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="741b2-113">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="741b2-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="741b2-114">Przykład 2. Uzyskiwanie informacji o przygotowaniu stanowiska i stanie zwolnienia zadania za pomocą opcji Filtruj i Wybierz</span><span class="sxs-lookup"><span data-stu-id="741b2-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="741b2-115">To polecenie pobiera informacje o przygotowaniu zadania i zwolnieniu stanu zadania "Test" w węźle "tvm-2316545714_1-20170613t201733z" i używa klauzuli Select w celu zwrócenia tylko informacji JobPreparationTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="741b2-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="741b2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="741b2-116">PARAMETERS</span></span>

### <span data-ttu-id="741b2-117">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="741b2-117">-BatchContext</span></span>
<span data-ttu-id="741b2-118">Wystąpienie BatchAccountContext do użycia podczas interakcji z usługą batch.</span><span class="sxs-lookup"><span data-stu-id="741b2-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="741b2-119">Użyj Get-AzBatchAccountKey cmdlet, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="741b2-119">Use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="741b2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="741b2-120">-DefaultProfile</span></span>
<span data-ttu-id="741b2-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="741b2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="741b2-122">— Rozwiń</span><span class="sxs-lookup"><span data-stu-id="741b2-122">-Expand</span></span>
<span data-ttu-id="741b2-123">Określa klauzulę rozwijania protokołu Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="741b2-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="741b2-124">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej o otrzymuję.</span><span class="sxs-lookup"><span data-stu-id="741b2-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="741b2-125">— Filtr</span><span class="sxs-lookup"><span data-stu-id="741b2-125">-Filter</span></span>
<span data-ttu-id="741b2-126">Określa klauzulę filtru OData.</span><span class="sxs-lookup"><span data-stu-id="741b2-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="741b2-127">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie informacje o przygotowaniu zadania i zwolnieniu stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="741b2-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="741b2-128">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="741b2-128">-Id</span></span>
<span data-ttu-id="741b2-129">Określa identyfikator zadania, którego zadania związane z przygotowaniem i wydaniem powinny zostać pobrane.</span><span class="sxs-lookup"><span data-stu-id="741b2-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="741b2-130">Nie można określić symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="741b2-130">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="741b2-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="741b2-131">-InputObject</span></span>
<span data-ttu-id="741b2-132">Określa obiekt **PSCloudJob** reprezentujący zadanie w celu uzyskania przygotowania i zwolnienia stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="741b2-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="741b2-133">Aby uzyskać obiekt **PSCloudJob,** użyj Get-AzBatchJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="741b2-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="741b2-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="741b2-134">-MaxCount</span></span>
<span data-ttu-id="741b2-135">Określa maksymalną liczbę zadań do zwrócenia w związku z przygotowaniem i wydaniem stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="741b2-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="741b2-136">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie użyje górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="741b2-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="741b2-137">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="741b2-137">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="741b2-138">— Wybierz</span><span class="sxs-lookup"><span data-stu-id="741b2-138">-Select</span></span>
<span data-ttu-id="741b2-139">Określa klauzulę wybierania danych OData.</span><span class="sxs-lookup"><span data-stu-id="741b2-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="741b2-140">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="741b2-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="741b2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="741b2-141">CommonParameters</span></span>
<span data-ttu-id="741b2-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="741b2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="741b2-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="741b2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="741b2-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="741b2-144">INPUTS</span></span>

### <span data-ttu-id="741b2-145">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="741b2-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="741b2-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="741b2-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="741b2-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="741b2-147">OUTPUTS</span></span>

### <span data-ttu-id="741b2-148">Microsoft.Azure.Commands.Batch. Models.PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="741b2-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="741b2-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="741b2-149">NOTES</span></span>

## <span data-ttu-id="741b2-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="741b2-150">RELATED LINKS</span></span>

[<span data-ttu-id="741b2-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="741b2-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="741b2-152">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="741b2-152">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
