---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222671"
---
# <span data-ttu-id="e91ab-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="e91ab-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="e91ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e91ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e91ab-103">Pobiera liczbę zadań dla określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="e91ab-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="e91ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e91ab-104">SYNTAX</span></span>

### <span data-ttu-id="e91ab-105">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="e91ab-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e91ab-106">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="e91ab-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e91ab-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e91ab-107">DESCRIPTION</span></span>
<span data-ttu-id="e91ab-108">Polecenie cmdlet **Get-AzBatchTaskCount** Pobiera liczbę zadań wsadowych platformy Azure dla zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="e91ab-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="e91ab-109">Zadanie należy określić za pomocą parametru *JobID* lub parametru *zadania* .</span><span class="sxs-lookup"><span data-stu-id="e91ab-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="e91ab-110">Zliczanie zadań zapewnia liczbę zadań według stanu aktywnego, uruchomionego lub wykonanego, a także liczbę zadań zakończonych powodzeniem lub zakończonych niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="e91ab-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="e91ab-111">Zadania w stanie przygotowania są liczone jako uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e91ab-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="e91ab-112">Jeśli validationStatus nie jest unieważniony, usługa przetwarzania wsadowego nie mogła sprawdzić liczby stanów w Stanach zadań, które zostały zgłoszone przez interfejs API zadania listy.</span><span class="sxs-lookup"><span data-stu-id="e91ab-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="e91ab-113">ValidationStatus może nie zostać unieważniony, jeśli zadanie zawiera więcej niż 200 000 zadań.</span><span class="sxs-lookup"><span data-stu-id="e91ab-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="e91ab-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e91ab-114">EXAMPLES</span></span>

### <span data-ttu-id="e91ab-115">Przykład 1: pobieranie liczby zadań według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="e91ab-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="e91ab-116">To polecenie pobiera liczniki zadań dla Job01 zadań.</span><span class="sxs-lookup"><span data-stu-id="e91ab-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="e91ab-117">Użyj polecenia cmdlet Get-AzBatchAccountKey, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="e91ab-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e91ab-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e91ab-118">PARAMETERS</span></span>

### <span data-ttu-id="e91ab-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e91ab-119">-BatchContext</span></span>
<span data-ttu-id="e91ab-120">Wystąpienie BatchAccountContext, które ma być używane podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="e91ab-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="e91ab-121">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="e91ab-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="e91ab-122">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="e91ab-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="e91ab-123">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="e91ab-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="e91ab-124">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e91ab-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e91ab-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e91ab-125">-DefaultProfile</span></span>
<span data-ttu-id="e91ab-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e91ab-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e91ab-127">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="e91ab-127">-Job</span></span>
<span data-ttu-id="e91ab-128">Określa zadanie zawierające zadania, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e91ab-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="e91ab-129">Aby uzyskać obiekt **PSCloudJob** , użyj polecenia cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="e91ab-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="e91ab-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="e91ab-130">-JobId</span></span>
<span data-ttu-id="e91ab-131">Identyfikator zadania, dla którego mają zostać wyświetlone Zliczanie zadań.</span><span class="sxs-lookup"><span data-stu-id="e91ab-131">The id of the job for which to get task counts.</span></span>

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

### <span data-ttu-id="e91ab-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e91ab-132">CommonParameters</span></span>
<span data-ttu-id="e91ab-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e91ab-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e91ab-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e91ab-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e91ab-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e91ab-135">INPUTS</span></span>

### <span data-ttu-id="e91ab-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e91ab-136">System.String</span></span>

### <span data-ttu-id="e91ab-137">Microsoft.Azure.Commands.Batch. Modele. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="e91ab-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="e91ab-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e91ab-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e91ab-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e91ab-139">OUTPUTS</span></span>

### <span data-ttu-id="e91ab-140">Microsoft.Azure.Commands.Batch. Modele. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="e91ab-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="e91ab-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e91ab-141">NOTES</span></span>

## <span data-ttu-id="e91ab-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e91ab-142">RELATED LINKS</span></span>

[<span data-ttu-id="e91ab-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e91ab-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e91ab-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e91ab-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="e91ab-145">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="e91ab-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
