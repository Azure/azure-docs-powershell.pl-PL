---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 58ac726d722959e3ee32bce84c0abe3c771fcbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549256"
---
# <span data-ttu-id="19788-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="19788-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="19788-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19788-102">SYNOPSIS</span></span>
<span data-ttu-id="19788-103">Zatrzymuje harmonogram zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="19788-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19788-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19788-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19788-105">Opis</span><span class="sxs-lookup"><span data-stu-id="19788-105">DESCRIPTION</span></span>
<span data-ttu-id="19788-106">Polecenie cmdlet **stop-AzureBatchJobSchedule** zatrzymuje harmonogram zadań usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="19788-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="19788-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19788-107">EXAMPLES</span></span>

### <span data-ttu-id="19788-108">Przykład 1: zatrzymywanie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="19788-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="19788-109">To polecenie zatrzymuje harmonogram zadań o IDENTYFIKATORze JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="19788-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="19788-110">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="19788-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="19788-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19788-111">PARAMETERS</span></span>

### <span data-ttu-id="19788-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="19788-112">-BatchContext</span></span>
<span data-ttu-id="19788-113">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="19788-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="19788-114">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="19788-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="19788-115">-ID</span><span class="sxs-lookup"><span data-stu-id="19788-115">-Id</span></span>
<span data-ttu-id="19788-116">Określa identyfikator harmonogramu zadań, który zostanie zatrzymany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19788-116">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="19788-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19788-117">-DefaultProfile</span></span>
<span data-ttu-id="19788-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19788-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19788-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19788-119">CommonParameters</span></span>
<span data-ttu-id="19788-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19788-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19788-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19788-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19788-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19788-122">INPUTS</span></span>

### <span data-ttu-id="19788-123">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="19788-123">BatchAccountContext</span></span>
<span data-ttu-id="19788-124">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="19788-124">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="19788-125">Ciąg</span><span class="sxs-lookup"><span data-stu-id="19788-125">String</span></span>
<span data-ttu-id="19788-126">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="19788-126">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="19788-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19788-127">OUTPUTS</span></span>

## <span data-ttu-id="19788-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19788-128">NOTES</span></span>

## <span data-ttu-id="19788-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19788-129">RELATED LINKS</span></span>

[<span data-ttu-id="19788-130">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="19788-130">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="19788-131">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="19788-131">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="19788-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="19788-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="19788-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="19788-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="19788-134">Nowe — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="19788-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="19788-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="19788-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="19788-136">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="19788-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


