---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: c012fe266bc25752729b14192c4d9c0a42cd8961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554023"
---
# <span data-ttu-id="da856-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="da856-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="da856-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da856-102">SYNOPSIS</span></span>
<span data-ttu-id="da856-103">Umożliwia planowanie zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="da856-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da856-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da856-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da856-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da856-105">DESCRIPTION</span></span>
<span data-ttu-id="da856-106">Polecenie cmdlet **enable-AzureBatchJobSchedule** włącza harmonogram zadania usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="da856-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="da856-107">Po włączeniu harmonogramu zadań można utworzyć zadania według harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="da856-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="da856-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da856-108">EXAMPLES</span></span>

### <span data-ttu-id="da856-109">Przykład 1. Włączanie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="da856-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="da856-110">To polecenie włącza harmonogram zadań o IDENTYFIKATORze JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="da856-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="da856-111">Użyj polecenia cmdlet **Get-AzureRmBatchAccountKeys** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="da856-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="da856-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da856-112">PARAMETERS</span></span>

### <span data-ttu-id="da856-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="da856-113">-BatchContext</span></span>
<span data-ttu-id="da856-114">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="da856-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="da856-115">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="da856-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="da856-116">-ID</span><span class="sxs-lookup"><span data-stu-id="da856-116">-Id</span></span>
<span data-ttu-id="da856-117">Określa identyfikator harmonogramu zadań, który włącza to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da856-117">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="da856-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da856-118">-DefaultProfile</span></span>
<span data-ttu-id="da856-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da856-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da856-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da856-120">CommonParameters</span></span>
<span data-ttu-id="da856-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da856-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da856-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da856-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da856-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da856-123">INPUTS</span></span>

### <span data-ttu-id="da856-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="da856-124">BatchAccountContext</span></span>
<span data-ttu-id="da856-125">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="da856-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="da856-126">Ciąg</span><span class="sxs-lookup"><span data-stu-id="da856-126">String</span></span>
<span data-ttu-id="da856-127">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="da856-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="da856-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da856-128">OUTPUTS</span></span>

## <span data-ttu-id="da856-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da856-129">NOTES</span></span>

## <span data-ttu-id="da856-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da856-130">RELATED LINKS</span></span>

[<span data-ttu-id="da856-131">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="da856-131">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="da856-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="da856-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="da856-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="da856-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="da856-134">Nowe — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="da856-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="da856-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="da856-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="da856-136">Zatrzymaj — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="da856-136">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="da856-137">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="da856-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


