---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtaskcounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
ms.openlocfilehash: d0b98081675cd11d8d3eb60a6495ac87a1111034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527090"
---
# <span data-ttu-id="d9ba0-101">Get-AzureBatchTaskCounts</span><span class="sxs-lookup"><span data-stu-id="d9ba0-101">Get-AzureBatchTaskCounts</span></span>

## <span data-ttu-id="d9ba0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ba0-103">Pobiera liczbę zadań dla określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-103">Gets the task counts for the specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9ba0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9ba0-104">SYNTAX</span></span>

### <span data-ttu-id="d9ba0-105">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="d9ba0-105">Id</span></span>
```
Get-AzureBatchTaskCounts [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="d9ba0-106">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="d9ba0-106">ParentObject</span></span>
```
Get-AzureBatchTaskCounts [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="d9ba0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d9ba0-107">DESCRIPTION</span></span>
<span data-ttu-id="d9ba0-108">Polecenie cmdlet **Get-AzureBatchTaskCounts** Pobiera liczbę zadań wsadowych platformy Azure dla zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-108">The **Get-AzureBatchTaskCounts** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="d9ba0-109">Zadanie należy określić za pomocą parametru *JobID* lub parametru *zadania* .</span><span class="sxs-lookup"><span data-stu-id="d9ba0-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="d9ba0-110">Zliczanie zadań zapewnia liczbę zadań według stanu aktywnego, uruchomionego lub wykonanego, a także liczbę zadań zakończonych powodzeniem lub zakończonych niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="d9ba0-111">Zadania w stanie przygotowania są liczone jako uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="d9ba0-112">Jeśli validationStatus nie jest unieważniony, usługa przetwarzania wsadowego nie mogła sprawdzić liczby stanów w Stanach zadań, które zostały zgłoszone przez interfejs API zadania listy.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="d9ba0-113">ValidationStatus może nie zostać unieważniony, jeśli zadanie zawiera więcej niż 200 000 zadań.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="d9ba0-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9ba0-114">EXAMPLES</span></span>

### <span data-ttu-id="d9ba0-115">Przykład 1: pobieranie liczby zadań według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="d9ba0-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzureBatchTaskCounts -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="d9ba0-116">To polecenie pobiera liczniki zadań dla Job01 zadań.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="d9ba0-117">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="d9ba0-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9ba0-118">PARAMETERS</span></span>

### <span data-ttu-id="d9ba0-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d9ba0-119">-BatchContext</span></span>
<span data-ttu-id="d9ba0-120">Wystąpienie BatchAccountContext, które ma być używane podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="d9ba0-121">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="d9ba0-122">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="d9ba0-123">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="d9ba0-124">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ba0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ba0-125">-DefaultProfile</span></span>
<span data-ttu-id="d9ba0-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ba0-127">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="d9ba0-127">-Job</span></span>
<span data-ttu-id="d9ba0-128">Określa zadanie zawierające zadania, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="d9ba0-129">Aby uzyskać obiekt **PSCloudJob** , użyj polecenia cmdlet Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-129">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ba0-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="d9ba0-130">-JobId</span></span>
<span data-ttu-id="d9ba0-131">Identyfikator zadania, dla którego mają zostać wyświetlone Zliczanie zadań.</span><span class="sxs-lookup"><span data-stu-id="d9ba0-131">The id of the job for which to get task counts.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="d9ba0-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9ba0-132">INPUTS</span></span>

### <span data-ttu-id="d9ba0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d9ba0-133">System.String</span></span>
<span data-ttu-id="d9ba0-134">Microsoft.Azure.Commands.Batch. Modele. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d9ba0-134">Microsoft.Azure.Commands.Batch.Models.PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>


## <span data-ttu-id="d9ba0-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9ba0-135">OUTPUTS</span></span>

### <span data-ttu-id="d9ba0-136">Microsoft.Azure.Commands.Batch. Modele. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="d9ba0-136">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>


## <span data-ttu-id="d9ba0-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9ba0-137">NOTES</span></span>

## <span data-ttu-id="d9ba0-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9ba0-138">RELATED LINKS</span></span>

[<span data-ttu-id="d9ba0-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d9ba0-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d9ba0-140">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d9ba0-140">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="d9ba0-141">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="d9ba0-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
