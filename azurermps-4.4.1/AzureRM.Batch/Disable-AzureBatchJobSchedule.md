---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: 73d80d3547ea895e5cbd35b2d514d9a757164bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554027"
---
# <span data-ttu-id="86717-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="86717-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="86717-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86717-102">SYNOPSIS</span></span>
<span data-ttu-id="86717-103">Wyłącza harmonogram zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="86717-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86717-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86717-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86717-105">Opis</span><span class="sxs-lookup"><span data-stu-id="86717-105">DESCRIPTION</span></span>
<span data-ttu-id="86717-106">Polecenie cmdlet **disable-AzureBatchJobSchedule** wyłącza harmonogram zadań usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="86717-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="86717-107">W przypadku wyłączenia harmonogramu zadania nie są tworzone zgodnie z tym harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="86717-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="86717-108">Możesz włączyć wyłączony harmonogram później.</span><span class="sxs-lookup"><span data-stu-id="86717-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="86717-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86717-109">EXAMPLES</span></span>

### <span data-ttu-id="86717-110">Przykład 1: wyłączanie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="86717-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="86717-111">To polecenie wyłącza harmonogram zadań o IDENTYFIKATORze JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="86717-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="86717-112">Użyj polecenia cmdlet **Get-AzureRmBatchAccountKeys** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="86717-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="86717-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86717-113">PARAMETERS</span></span>

### <span data-ttu-id="86717-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="86717-114">-BatchContext</span></span>
<span data-ttu-id="86717-115">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="86717-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="86717-116">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="86717-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="86717-117">-ID</span><span class="sxs-lookup"><span data-stu-id="86717-117">-Id</span></span>
<span data-ttu-id="86717-118">Określa identyfikator harmonogramu zadań, który ma zostać wyłączony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86717-118">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="86717-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86717-119">-DefaultProfile</span></span>
<span data-ttu-id="86717-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86717-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86717-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86717-121">CommonParameters</span></span>
<span data-ttu-id="86717-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86717-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86717-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86717-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86717-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86717-124">INPUTS</span></span>

### <span data-ttu-id="86717-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="86717-125">BatchAccountContext</span></span>
<span data-ttu-id="86717-126">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="86717-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="86717-127">Ciąg</span><span class="sxs-lookup"><span data-stu-id="86717-127">String</span></span>
<span data-ttu-id="86717-128">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="86717-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="86717-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86717-129">OUTPUTS</span></span>

## <span data-ttu-id="86717-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86717-130">NOTES</span></span>

## <span data-ttu-id="86717-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86717-131">RELATED LINKS</span></span>

[<span data-ttu-id="86717-132">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="86717-132">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="86717-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="86717-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="86717-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="86717-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="86717-135">Nowe — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="86717-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="86717-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="86717-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="86717-137">Zatrzymaj — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="86717-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="86717-138">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="86717-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


