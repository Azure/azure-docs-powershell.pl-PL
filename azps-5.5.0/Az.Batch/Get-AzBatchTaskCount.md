---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239270"
---
# <span data-ttu-id="666e2-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="666e2-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="666e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="666e2-102">SYNOPSIS</span></span>
<span data-ttu-id="666e2-103">Pobiera liczbę zadań dla określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="666e2-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="666e2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="666e2-104">SYNTAX</span></span>

### <span data-ttu-id="666e2-105">Identyfikator</span><span class="sxs-lookup"><span data-stu-id="666e2-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="666e2-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="666e2-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="666e2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="666e2-107">DESCRIPTION</span></span>
<span data-ttu-id="666e2-108">Polecenie **cmdlet Get-AzBatchTaskCount** pobiera liczbę zadań partii platformy Azure dla zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="666e2-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="666e2-109">Określ zadanie za pomocą parametru *JobId* lub *parametru Job.*</span><span class="sxs-lookup"><span data-stu-id="666e2-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="666e2-110">Zliczane zadania zapewniają liczbę zadań według stanu aktywnego, bieżącego lub ukończonego oraz liczbę zadań, które zakończyły się powodzeniem lub niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="666e2-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="666e2-111">Zadania w stanie przygotowywania są liczone jako uruchomione.</span><span class="sxs-lookup"><span data-stu-id="666e2-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="666e2-112">Jeśli stan sprawdzania poprawności jest nieuprawniony, usługa wsadowa nie mogła sprawdzić stanu w stosunku do stanów zadań zgłoszonych w interfejsie API zadań listy.</span><span class="sxs-lookup"><span data-stu-id="666e2-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="666e2-113">Jeśli zadanie zawiera więcej niż 200 000 zadań, statystyki sprawdzania poprawności mogą być nieuprawnione.</span><span class="sxs-lookup"><span data-stu-id="666e2-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="666e2-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="666e2-114">EXAMPLES</span></span>

### <span data-ttu-id="666e2-115">Przykład 1. Uzyskiwanie liczników zadań według identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="666e2-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="666e2-116">To polecenie pobiera liczbę zadań dla zadania Job01.</span><span class="sxs-lookup"><span data-stu-id="666e2-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="666e2-117">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="666e2-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="666e2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="666e2-118">PARAMETERS</span></span>

### <span data-ttu-id="666e2-119">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="666e2-119">-BatchContext</span></span>
<span data-ttu-id="666e2-120">Wystąpienie BatchAccountContext do użycia podczas interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="666e2-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="666e2-121">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="666e2-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="666e2-122">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="666e2-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="666e2-123">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="666e2-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="666e2-124">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="666e2-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="666e2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="666e2-125">-DefaultProfile</span></span>
<span data-ttu-id="666e2-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="666e2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="666e2-127">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="666e2-127">-Job</span></span>
<span data-ttu-id="666e2-128">Określa zadanie zawierające zadania, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="666e2-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="666e2-129">Aby uzyskać obiekt **PSCloudJob,** użyj Get-AzBatchJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="666e2-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="666e2-130">- JobId</span><span class="sxs-lookup"><span data-stu-id="666e2-130">-JobId</span></span>
<span data-ttu-id="666e2-131">Identyfikator zadania, dla którego ma być zliczane zadanie.</span><span class="sxs-lookup"><span data-stu-id="666e2-131">The id of the job for which to get task counts.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="666e2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="666e2-132">CommonParameters</span></span>
<span data-ttu-id="666e2-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="666e2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="666e2-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="666e2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="666e2-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="666e2-135">INPUTS</span></span>

### <span data-ttu-id="666e2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="666e2-136">System.String</span></span>

### <span data-ttu-id="666e2-137">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="666e2-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="666e2-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="666e2-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="666e2-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="666e2-139">OUTPUTS</span></span>

### <span data-ttu-id="666e2-140">Microsoft.Azure.Commands.Batch. Models.PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="666e2-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="666e2-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="666e2-141">NOTES</span></span>

## <span data-ttu-id="666e2-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="666e2-142">RELATED LINKS</span></span>

[<span data-ttu-id="666e2-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="666e2-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="666e2-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="666e2-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="666e2-145">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="666e2-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
