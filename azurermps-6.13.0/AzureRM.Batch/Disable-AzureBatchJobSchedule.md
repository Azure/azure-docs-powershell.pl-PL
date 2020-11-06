---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: e1eb586ff23f5f56cd9fc117f5039d3ccc841367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547619"
---
# <span data-ttu-id="81a17-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="81a17-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="81a17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81a17-102">SYNOPSIS</span></span>
<span data-ttu-id="81a17-103">Wyłącza harmonogram zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="81a17-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81a17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81a17-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81a17-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81a17-105">DESCRIPTION</span></span>
<span data-ttu-id="81a17-106">Polecenie cmdlet **disable-AzureBatchJobSchedule** wyłącza harmonogram zadań usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="81a17-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="81a17-107">W przypadku wyłączenia harmonogramu zadania nie są tworzone zgodnie z tym harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="81a17-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="81a17-108">Możesz włączyć wyłączony harmonogram później.</span><span class="sxs-lookup"><span data-stu-id="81a17-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="81a17-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81a17-109">EXAMPLES</span></span>

### <span data-ttu-id="81a17-110">Przykład 1: wyłączanie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="81a17-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="81a17-111">To polecenie wyłącza harmonogram zadań o IDENTYFIKATORze JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="81a17-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="81a17-112">Użyj polecenia cmdlet **Get-AzureRmBatchAccountKeys** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="81a17-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="81a17-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81a17-113">PARAMETERS</span></span>

### <span data-ttu-id="81a17-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="81a17-114">-BatchContext</span></span>
<span data-ttu-id="81a17-115">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="81a17-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="81a17-116">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="81a17-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="81a17-117">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="81a17-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="81a17-118">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="81a17-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="81a17-119">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="81a17-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="81a17-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a17-120">-DefaultProfile</span></span>
<span data-ttu-id="81a17-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81a17-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81a17-122">-ID</span><span class="sxs-lookup"><span data-stu-id="81a17-122">-Id</span></span>
<span data-ttu-id="81a17-123">Określa identyfikator harmonogramu zadań, który ma zostać wyłączony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81a17-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="81a17-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a17-124">CommonParameters</span></span>
<span data-ttu-id="81a17-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a17-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a17-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a17-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a17-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81a17-127">INPUTS</span></span>

### <span data-ttu-id="81a17-128">System. String</span><span class="sxs-lookup"><span data-stu-id="81a17-128">System.String</span></span>

### <span data-ttu-id="81a17-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="81a17-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="81a17-130">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="81a17-130">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="81a17-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81a17-131">OUTPUTS</span></span>

### <span data-ttu-id="81a17-132">System. void</span><span class="sxs-lookup"><span data-stu-id="81a17-132">System.Void</span></span>

## <span data-ttu-id="81a17-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81a17-133">NOTES</span></span>

## <span data-ttu-id="81a17-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81a17-134">RELATED LINKS</span></span>

[<span data-ttu-id="81a17-135">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="81a17-135">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="81a17-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="81a17-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="81a17-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="81a17-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="81a17-138">Nowe — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="81a17-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="81a17-139">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="81a17-139">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="81a17-140">Zatrzymaj — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="81a17-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="81a17-141">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="81a17-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


