---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: accba78cd05d6fcc18eb7f48c7cfb2839c0e9417
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710856"
---
# <span data-ttu-id="e6906-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="e6906-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="e6906-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6906-102">SYNOPSIS</span></span>
<span data-ttu-id="e6906-103">Pobiera zadanie wsadowe i zwalnia stan zadania.</span><span class="sxs-lookup"><span data-stu-id="e6906-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="e6906-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6906-104">SYNTAX</span></span>

### <span data-ttu-id="e6906-105">Identyfikator (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e6906-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6906-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="e6906-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6906-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e6906-107">DESCRIPTION</span></span>
<span data-ttu-id="e6906-108">Polecenie cmdlet **Get-AzBatchJobPreparationAndReleaseTaskStatus** pobiera zadanie usługi Azure Batch dotyczące przygotowania i zwolnienia zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="e6906-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="e6906-109">Do tego polecenia cmdlet należy podać parametr *identyfikatora* lub wystąpienie **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="e6906-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="e6906-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6906-110">EXAMPLES</span></span>

### <span data-ttu-id="e6906-111">Przykład 1: uzyskiwanie statusu przygotowywania i udostępniania zadania</span><span class="sxs-lookup"><span data-stu-id="e6906-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="e6906-112">To polecenie pobiera zadanie przygotowywania zadań i zwalnianie stanu zadań dla zadania "test".</span><span class="sxs-lookup"><span data-stu-id="e6906-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="e6906-113">Użyj polecenia cmdlet Get-AzBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="e6906-113">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="e6906-114">Przykład 2: Uzyskaj stan przygotowania i udostępniania zadania, korzystając z filtru i wybierz pozycję określony.</span><span class="sxs-lookup"><span data-stu-id="e6906-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="e6906-115">To polecenie pobiera zadania przygotowywania zadań i zwalniania stanu zadań dla zadania "test" w węźle "TVM-2316545714_1-20170613t201733z" i używa klauzuli SELECT w celu określenia, aby zwracała tylko informacje JobPreparationTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="e6906-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="e6906-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6906-116">PARAMETERS</span></span>

### <span data-ttu-id="e6906-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e6906-117">-BatchContext</span></span>
<span data-ttu-id="e6906-118">Wystąpienie BatchAccountContext, które ma być używane podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="e6906-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="e6906-119">Użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="e6906-119">Use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="e6906-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6906-120">-DefaultProfile</span></span>
<span data-ttu-id="e6906-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6906-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6906-122">-Expand</span><span class="sxs-lookup"><span data-stu-id="e6906-122">-Expand</span></span>
<span data-ttu-id="e6906-123">Określa klauzulę expanda Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="e6906-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="e6906-124">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej jednostki.</span><span class="sxs-lookup"><span data-stu-id="e6906-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="e6906-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="e6906-125">-Filter</span></span>
<span data-ttu-id="e6906-126">Określa klauzulę filtru OData.</span><span class="sxs-lookup"><span data-stu-id="e6906-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="e6906-127">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie zadania przygotowywania i zwalniania o stanie zadań dla tego zadania.</span><span class="sxs-lookup"><span data-stu-id="e6906-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="e6906-128">-ID</span><span class="sxs-lookup"><span data-stu-id="e6906-128">-Id</span></span>
<span data-ttu-id="e6906-129">Określa identyfikator zadania, dla którego mają zostać pobrane zadania przygotowania i wydania.</span><span class="sxs-lookup"><span data-stu-id="e6906-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="e6906-130">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="e6906-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="e6906-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e6906-131">-InputObject</span></span>
<span data-ttu-id="e6906-132">Określa obiekt **PSCloudJob** reprezentujący zadanie w celu uzyskania statusu zadania przygotowania i wydania.</span><span class="sxs-lookup"><span data-stu-id="e6906-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="e6906-133">Aby uzyskać obiekt **PSCloudJob** , użyj polecenia cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="e6906-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="e6906-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e6906-134">-MaxCount</span></span>
<span data-ttu-id="e6906-135">Określa maksymalną liczbę zadań przygotowywania i zwalniania statusu zadania, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="e6906-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="e6906-136">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="e6906-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="e6906-137">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="e6906-137">The default value is 1000.</span></span>

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

### <span data-ttu-id="e6906-138">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="e6906-138">-Select</span></span>
<span data-ttu-id="e6906-139">Określa klauzulę SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="e6906-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="e6906-140">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="e6906-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="e6906-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6906-141">CommonParameters</span></span>
<span data-ttu-id="e6906-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6906-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6906-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6906-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6906-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6906-144">INPUTS</span></span>

### <span data-ttu-id="e6906-145">Microsoft.Azure.Commands.Batch. Modele. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="e6906-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="e6906-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e6906-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e6906-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6906-147">OUTPUTS</span></span>

### <span data-ttu-id="e6906-148">Microsoft.Azure.Commands.Batch. Modele. PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="e6906-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="e6906-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6906-149">NOTES</span></span>

## <span data-ttu-id="e6906-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6906-150">RELATED LINKS</span></span>

[<span data-ttu-id="e6906-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e6906-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="e6906-152">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="e6906-152">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)