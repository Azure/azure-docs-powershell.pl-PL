---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: 79a758007c5a84e963432da60100c51fc217edc0
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "94061661"
---
# <span data-ttu-id="87ff8-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="87ff8-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="87ff8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="87ff8-103">Wyłącza zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="87ff8-103">Disables a Batch job.</span></span>

## <span data-ttu-id="87ff8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87ff8-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87ff8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87ff8-105">DESCRIPTION</span></span>
<span data-ttu-id="87ff8-106">Polecenie cmdlet **disable-AzBatchJob** wyłącza zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="87ff8-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="87ff8-107">Po włączeniu zadania można uruchamiać nowe zadania.</span><span class="sxs-lookup"><span data-stu-id="87ff8-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="87ff8-108">Wyłączone zadania nie uruchamiają nowych zadań.</span><span class="sxs-lookup"><span data-stu-id="87ff8-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="87ff8-109">Możesz włączyć wyłączone zadanie później.</span><span class="sxs-lookup"><span data-stu-id="87ff8-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="87ff8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87ff8-110">EXAMPLES</span></span>

### <span data-ttu-id="87ff8-111">Przykład 1. wyłączenie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="87ff8-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="87ff8-112">To polecenie wyłącza zadanie o IDENTYFIKATORze zadania w 000001.</span><span class="sxs-lookup"><span data-stu-id="87ff8-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="87ff8-113">Polecenie przerywa zadania aktywne dla zadania.</span><span class="sxs-lookup"><span data-stu-id="87ff8-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="87ff8-114">Użyj polecenia cmdlet **Get-AzBatchAccountKey** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="87ff8-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="87ff8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87ff8-115">PARAMETERS</span></span>

### <span data-ttu-id="87ff8-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="87ff8-116">-BatchContext</span></span>
<span data-ttu-id="87ff8-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="87ff8-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="87ff8-118">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="87ff8-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="87ff8-119">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="87ff8-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="87ff8-120">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="87ff8-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="87ff8-121">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="87ff8-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="87ff8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ff8-122">-DefaultProfile</span></span>
<span data-ttu-id="87ff8-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87ff8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87ff8-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="87ff8-124">-DisableJobOption</span></span>
<span data-ttu-id="87ff8-125">Określa, co należy zrobić z aktywnymi zadaniami skojarzonymi z zadaniem, które wyłączy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87ff8-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="87ff8-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="87ff8-126">Valid values are:</span></span> 
- <span data-ttu-id="87ff8-127">Przekolejkowanie</span><span class="sxs-lookup"><span data-stu-id="87ff8-127">Requeue</span></span> 
- <span data-ttu-id="87ff8-128">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="87ff8-128">Terminate</span></span> 
- <span data-ttu-id="87ff8-129">Czekaj</span><span class="sxs-lookup"><span data-stu-id="87ff8-129">Wait</span></span>

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

### <span data-ttu-id="87ff8-130">-ID</span><span class="sxs-lookup"><span data-stu-id="87ff8-130">-Id</span></span>
<span data-ttu-id="87ff8-131">Określa identyfikator zadania wyłączającego to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87ff8-131">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="87ff8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ff8-132">CommonParameters</span></span>
<span data-ttu-id="87ff8-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87ff8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ff8-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87ff8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ff8-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87ff8-135">INPUTS</span></span>

### <span data-ttu-id="87ff8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="87ff8-136">System.String</span></span>

### <span data-ttu-id="87ff8-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="87ff8-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="87ff8-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87ff8-138">OUTPUTS</span></span>

### <span data-ttu-id="87ff8-139">System. void</span><span class="sxs-lookup"><span data-stu-id="87ff8-139">System.Void</span></span>

## <span data-ttu-id="87ff8-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87ff8-140">NOTES</span></span>

## <span data-ttu-id="87ff8-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87ff8-141">RELATED LINKS</span></span>

[<span data-ttu-id="87ff8-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="87ff8-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="87ff8-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="87ff8-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="87ff8-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="87ff8-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="87ff8-145">Nowe — AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="87ff8-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="87ff8-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="87ff8-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="87ff8-147">Zatrzymaj — AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="87ff8-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="87ff8-148">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="87ff8-148">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


