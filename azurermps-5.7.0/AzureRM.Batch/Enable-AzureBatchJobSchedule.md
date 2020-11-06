---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: 3081721db5cb113d48417ddf28d8a96512d27f99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551780"
---
# <span data-ttu-id="76c5e-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="76c5e-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="76c5e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="76c5e-103">Umożliwia planowanie zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="76c5e-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76c5e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76c5e-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76c5e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="76c5e-105">DESCRIPTION</span></span>
<span data-ttu-id="76c5e-106">Polecenie cmdlet **enable-AzureBatchJobSchedule** włącza harmonogram zadania usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="76c5e-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="76c5e-107">Po włączeniu harmonogramu zadań można utworzyć zadania według harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="76c5e-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="76c5e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76c5e-108">EXAMPLES</span></span>

### <span data-ttu-id="76c5e-109">Przykład 1. Włączanie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="76c5e-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="76c5e-110">To polecenie włącza harmonogram zadań o IDENTYFIKATORze JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="76c5e-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="76c5e-111">Użyj polecenia cmdlet **Get-AzureRmBatchAccountKeys** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="76c5e-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="76c5e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76c5e-112">PARAMETERS</span></span>

### <span data-ttu-id="76c5e-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="76c5e-113">-BatchContext</span></span>
<span data-ttu-id="76c5e-114">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="76c5e-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="76c5e-115">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="76c5e-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="76c5e-116">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="76c5e-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="76c5e-117">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="76c5e-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="76c5e-118">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="76c5e-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="76c5e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c5e-119">-DefaultProfile</span></span>
<span data-ttu-id="76c5e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76c5e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76c5e-121">-ID</span><span class="sxs-lookup"><span data-stu-id="76c5e-121">-Id</span></span>
<span data-ttu-id="76c5e-122">Określa identyfikator harmonogramu zadań, który włącza to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76c5e-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="76c5e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c5e-123">CommonParameters</span></span>
<span data-ttu-id="76c5e-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c5e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c5e-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c5e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c5e-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76c5e-126">INPUTS</span></span>

### <span data-ttu-id="76c5e-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="76c5e-127">BatchAccountContext</span></span>
<span data-ttu-id="76c5e-128">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="76c5e-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="76c5e-129">Ciąg</span><span class="sxs-lookup"><span data-stu-id="76c5e-129">String</span></span>
<span data-ttu-id="76c5e-130">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="76c5e-130">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="76c5e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76c5e-131">OUTPUTS</span></span>

## <span data-ttu-id="76c5e-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76c5e-132">NOTES</span></span>

## <span data-ttu-id="76c5e-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76c5e-133">RELATED LINKS</span></span>

[<span data-ttu-id="76c5e-134">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="76c5e-134">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="76c5e-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="76c5e-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="76c5e-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="76c5e-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="76c5e-137">Nowe — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="76c5e-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="76c5e-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="76c5e-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="76c5e-139">Zatrzymaj — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="76c5e-139">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="76c5e-140">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="76c5e-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


