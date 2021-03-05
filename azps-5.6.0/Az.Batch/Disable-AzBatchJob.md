---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: fabc983e8c7b70685477a640d408beb65251b253
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999013"
---
# <span data-ttu-id="e4887-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4887-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="e4887-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4887-102">SYNOPSIS</span></span>
<span data-ttu-id="e4887-103">Wyłącza zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="e4887-103">Disables a Batch job.</span></span>

## <span data-ttu-id="e4887-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e4887-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4887-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e4887-105">DESCRIPTION</span></span>
<span data-ttu-id="e4887-106">Polecenie **cmdlet Disable-AzBatchJob** wyłącza zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="e4887-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="e4887-107">Po włączeniu zadania można uruchamiać nowe zadania.</span><span class="sxs-lookup"><span data-stu-id="e4887-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="e4887-108">Zadania wyłączone nie uruchamiają nowych zadań.</span><span class="sxs-lookup"><span data-stu-id="e4887-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="e4887-109">Zadanie wyłączone można włączyć później.</span><span class="sxs-lookup"><span data-stu-id="e4887-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="e4887-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e4887-110">EXAMPLES</span></span>

### <span data-ttu-id="e4887-111">Przykład 1. Wyłączanie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="e4887-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="e4887-112">To polecenie wyłącza zadanie o identyfikatorze Zadanie 0000001.</span><span class="sxs-lookup"><span data-stu-id="e4887-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="e4887-113">To polecenie kończy aktywne zadania związane z tym zadaniem.</span><span class="sxs-lookup"><span data-stu-id="e4887-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="e4887-114">Użyj polecenia **cmdlet Get-AzBatchAccountKey,** aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="e4887-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e4887-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4887-115">PARAMETERS</span></span>

### <span data-ttu-id="e4887-116">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="e4887-116">-BatchContext</span></span>
<span data-ttu-id="e4887-117">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="e4887-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e4887-118">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e4887-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e4887-119">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="e4887-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e4887-120">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="e4887-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e4887-121">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e4887-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e4887-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4887-122">-DefaultProfile</span></span>
<span data-ttu-id="e4887-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4887-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4887-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="e4887-124">-DisableJobOption</span></span>
<span data-ttu-id="e4887-125">Określa, co należy zrobić z aktywnymi zadaniami skojarzonymi z zadaniem, które to polecenie cmdlet wyłącza.</span><span class="sxs-lookup"><span data-stu-id="e4887-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="e4887-126">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="e4887-126">Valid values are:</span></span>
- <span data-ttu-id="e4887-127">Kolejkowanie ponownie</span><span class="sxs-lookup"><span data-stu-id="e4887-127">Requeue</span></span>
- <span data-ttu-id="e4887-128">Zakończ</span><span class="sxs-lookup"><span data-stu-id="e4887-128">Terminate</span></span>
- <span data-ttu-id="e4887-129">Czekaj</span><span class="sxs-lookup"><span data-stu-id="e4887-129">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4887-130">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="e4887-130">-Id</span></span>
<span data-ttu-id="e4887-131">Określa identyfikator zadania, które to polecenie cmdlet wyłącza.</span><span class="sxs-lookup"><span data-stu-id="e4887-131">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4887-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4887-132">CommonParameters</span></span>
<span data-ttu-id="e4887-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4887-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4887-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4887-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4887-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4887-135">INPUTS</span></span>

### <span data-ttu-id="e4887-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e4887-136">System.String</span></span>

### <span data-ttu-id="e4887-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e4887-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e4887-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4887-138">OUTPUTS</span></span>

### <span data-ttu-id="e4887-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="e4887-139">System.Void</span></span>

## <span data-ttu-id="e4887-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e4887-140">NOTES</span></span>

## <span data-ttu-id="e4887-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4887-141">RELATED LINKS</span></span>

[<span data-ttu-id="e4887-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4887-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="e4887-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e4887-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e4887-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4887-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="e4887-145">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4887-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="e4887-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4887-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="e4887-147">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4887-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="e4887-148">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e4887-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
