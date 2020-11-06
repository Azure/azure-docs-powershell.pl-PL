---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: fcb3586d1c27fd95c6bf386943830b92635162e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554290"
---
# <span data-ttu-id="a9b3d-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a9b3d-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="a9b3d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b3d-103">Wyłącza zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9b3d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9b3d-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9b3d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a9b3d-105">DESCRIPTION</span></span>
<span data-ttu-id="a9b3d-106">Polecenie cmdlet **disable-AzureBatchJob** wyłącza zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="a9b3d-107">Po włączeniu zadania można uruchamiać nowe zadania.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="a9b3d-108">Wyłączone zadania nie uruchamiają nowych zadań.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="a9b3d-109">Możesz włączyć wyłączone zadanie później.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="a9b3d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9b3d-110">EXAMPLES</span></span>

### <span data-ttu-id="a9b3d-111">Przykład 1. wyłączenie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="a9b3d-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="a9b3d-112">To polecenie wyłącza zadanie o IDENTYFIKATORze zadania w 000001.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="a9b3d-113">Polecenie przerywa zadania aktywne dla zadania.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="a9b3d-114">Użyj polecenia cmdlet **Get-AzureRmBatchAccountKeys** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a9b3d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9b3d-115">PARAMETERS</span></span>

### <span data-ttu-id="a9b3d-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a9b3d-116">-BatchContext</span></span>
<span data-ttu-id="a9b3d-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a9b3d-118">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a9b3d-119">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a9b3d-120">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a9b3d-121">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a9b3d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b3d-122">-DefaultProfile</span></span>
<span data-ttu-id="a9b3d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9b3d-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="a9b3d-124">-DisableJobOption</span></span>
<span data-ttu-id="a9b3d-125">Określa, co należy zrobić z aktywnymi zadaniami skojarzonymi z zadaniem, które wyłączy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="a9b3d-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="a9b3d-126">Valid values are:</span></span> 

- <span data-ttu-id="a9b3d-127">Przekolejkowanie</span><span class="sxs-lookup"><span data-stu-id="a9b3d-127">Requeue</span></span> 
- <span data-ttu-id="a9b3d-128">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="a9b3d-128">Terminate</span></span> 
- <span data-ttu-id="a9b3d-129">Czekaj</span><span class="sxs-lookup"><span data-stu-id="a9b3d-129">Wait</span></span>

```yaml
Type: DisableJobOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b3d-130">-ID</span><span class="sxs-lookup"><span data-stu-id="a9b3d-130">-Id</span></span>
<span data-ttu-id="a9b3d-131">Określa identyfikator zadania wyłączającego to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-131">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b3d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b3d-132">CommonParameters</span></span>
<span data-ttu-id="a9b3d-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9b3d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b3d-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9b3d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b3d-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9b3d-135">INPUTS</span></span>

### <span data-ttu-id="a9b3d-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a9b3d-136">BatchAccountContext</span></span>
<span data-ttu-id="a9b3d-137">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="a9b3d-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a9b3d-138">Ciąg</span><span class="sxs-lookup"><span data-stu-id="a9b3d-138">String</span></span>
<span data-ttu-id="a9b3d-139">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="a9b3d-139">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a9b3d-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9b3d-140">OUTPUTS</span></span>

## <span data-ttu-id="a9b3d-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9b3d-141">NOTES</span></span>

## <span data-ttu-id="a9b3d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9b3d-142">RELATED LINKS</span></span>

[<span data-ttu-id="a9b3d-143">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a9b3d-143">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="a9b3d-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a9b3d-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a9b3d-145">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a9b3d-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="a9b3d-146">Nowe — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a9b3d-146">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="a9b3d-147">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a9b3d-147">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="a9b3d-148">Zatrzymaj — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a9b3d-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="a9b3d-149">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="a9b3d-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


