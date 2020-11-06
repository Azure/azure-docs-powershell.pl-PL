---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 33ae727ea31d533652943240cd9cd25014635533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549427"
---
# <span data-ttu-id="98085-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98085-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="98085-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98085-102">SYNOPSIS</span></span>
<span data-ttu-id="98085-103">Zatrzymuje harmonogram zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="98085-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98085-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98085-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98085-105">Opis</span><span class="sxs-lookup"><span data-stu-id="98085-105">DESCRIPTION</span></span>
<span data-ttu-id="98085-106">Polecenie cmdlet **stop-AzureBatchJobSchedule** zatrzymuje harmonogram zadań usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="98085-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="98085-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98085-107">EXAMPLES</span></span>

### <span data-ttu-id="98085-108">Przykład 1: zatrzymywanie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="98085-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="98085-109">To polecenie zatrzymuje harmonogram zadań o IDENTYFIKATORze JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="98085-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="98085-110">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="98085-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="98085-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98085-111">PARAMETERS</span></span>

### <span data-ttu-id="98085-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="98085-112">-BatchContext</span></span>
<span data-ttu-id="98085-113">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="98085-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="98085-114">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="98085-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="98085-115">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="98085-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="98085-116">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="98085-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="98085-117">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="98085-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="98085-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98085-118">-DefaultProfile</span></span>
<span data-ttu-id="98085-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98085-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98085-120">-ID</span><span class="sxs-lookup"><span data-stu-id="98085-120">-Id</span></span>
<span data-ttu-id="98085-121">Określa identyfikator harmonogramu zadań, który zostanie zatrzymany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98085-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="98085-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98085-122">CommonParameters</span></span>
<span data-ttu-id="98085-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98085-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98085-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98085-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98085-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98085-125">INPUTS</span></span>

### <span data-ttu-id="98085-126">System. String</span><span class="sxs-lookup"><span data-stu-id="98085-126">System.String</span></span>

### <span data-ttu-id="98085-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="98085-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="98085-128">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="98085-128">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="98085-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98085-129">OUTPUTS</span></span>

### <span data-ttu-id="98085-130">System. void</span><span class="sxs-lookup"><span data-stu-id="98085-130">System.Void</span></span>

## <span data-ttu-id="98085-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98085-131">NOTES</span></span>

## <span data-ttu-id="98085-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98085-132">RELATED LINKS</span></span>

[<span data-ttu-id="98085-133">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98085-133">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="98085-134">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98085-134">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="98085-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="98085-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="98085-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98085-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="98085-137">Nowe — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98085-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="98085-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98085-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="98085-139">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="98085-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


