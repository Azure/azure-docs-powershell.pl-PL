---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: 2e19e6b1733ccc3dfe0a802756e2c0a517232803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719376"
---
# <span data-ttu-id="5bad4-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5bad4-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="5bad4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5bad4-102">SYNOPSIS</span></span>
<span data-ttu-id="5bad4-103">Wyłącza zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="5bad4-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bad4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5bad4-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bad4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5bad4-105">DESCRIPTION</span></span>
<span data-ttu-id="5bad4-106">Polecenie cmdlet **disable-AzureBatchJob** wyłącza zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="5bad4-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="5bad4-107">Po włączeniu zadania można uruchamiać nowe zadania.</span><span class="sxs-lookup"><span data-stu-id="5bad4-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="5bad4-108">Wyłączone zadania nie uruchamiają nowych zadań.</span><span class="sxs-lookup"><span data-stu-id="5bad4-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="5bad4-109">Możesz włączyć wyłączone zadanie później.</span><span class="sxs-lookup"><span data-stu-id="5bad4-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="5bad4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5bad4-110">EXAMPLES</span></span>

### <span data-ttu-id="5bad4-111">Przykład 1. wyłączenie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="5bad4-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="5bad4-112">To polecenie wyłącza zadanie o IDENTYFIKATORze zadania w 000001.</span><span class="sxs-lookup"><span data-stu-id="5bad4-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="5bad4-113">Polecenie przerywa zadania aktywne dla zadania.</span><span class="sxs-lookup"><span data-stu-id="5bad4-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="5bad4-114">Użyj polecenia cmdlet **Get-AzureRmBatchAccountKeys** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="5bad4-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5bad4-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5bad4-115">PARAMETERS</span></span>

### <span data-ttu-id="5bad4-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5bad4-116">-BatchContext</span></span>
<span data-ttu-id="5bad4-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5bad4-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5bad4-118">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="5bad4-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="5bad4-119">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="5bad4-119">-DisableJobOption</span></span>
<span data-ttu-id="5bad4-120">Określa, co należy zrobić z aktywnymi zadaniami skojarzonymi z zadaniem, które wyłączy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bad4-120">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="5bad4-121">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="5bad4-121">Valid values are:</span></span> 

- <span data-ttu-id="5bad4-122">Przekolejkowanie</span><span class="sxs-lookup"><span data-stu-id="5bad4-122">Requeue</span></span> 
- <span data-ttu-id="5bad4-123">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="5bad4-123">Terminate</span></span> 
- <span data-ttu-id="5bad4-124">Czekaj</span><span class="sxs-lookup"><span data-stu-id="5bad4-124">Wait</span></span>

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

### <span data-ttu-id="5bad4-125">-ID</span><span class="sxs-lookup"><span data-stu-id="5bad4-125">-Id</span></span>
<span data-ttu-id="5bad4-126">Określa identyfikator zadania wyłączającego to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bad4-126">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="5bad4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bad4-127">-DefaultProfile</span></span>
<span data-ttu-id="5bad4-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5bad4-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bad4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bad4-129">CommonParameters</span></span>
<span data-ttu-id="5bad4-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bad4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bad4-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bad4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bad4-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bad4-132">INPUTS</span></span>

### <span data-ttu-id="5bad4-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5bad4-133">BatchAccountContext</span></span>
<span data-ttu-id="5bad4-134">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="5bad4-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5bad4-135">Ciąg</span><span class="sxs-lookup"><span data-stu-id="5bad4-135">String</span></span>
<span data-ttu-id="5bad4-136">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="5bad4-136">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5bad4-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5bad4-137">OUTPUTS</span></span>

## <span data-ttu-id="5bad4-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5bad4-138">NOTES</span></span>

## <span data-ttu-id="5bad4-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5bad4-139">RELATED LINKS</span></span>

[<span data-ttu-id="5bad4-140">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5bad4-140">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="5bad4-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5bad4-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5bad4-142">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5bad4-142">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="5bad4-143">Nowe — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5bad4-143">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="5bad4-144">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5bad4-144">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="5bad4-145">Zatrzymaj — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5bad4-145">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="5bad4-146">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="5bad4-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


