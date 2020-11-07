---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 665d7b64f3e8d83dd45ebc8de0cc36da960f8c35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719375"
---
# <span data-ttu-id="4a47c-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4a47c-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="4a47c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a47c-102">SYNOPSIS</span></span>
<span data-ttu-id="4a47c-103">Umożliwia wykonywanie zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="4a47c-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a47c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a47c-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a47c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4a47c-105">DESCRIPTION</span></span>
<span data-ttu-id="4a47c-106">Polecenie cmdlet **enable-AzureBatchJob** włącza zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="4a47c-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="4a47c-107">Po włączeniu zadania można uruchamiać nowe zadania.</span><span class="sxs-lookup"><span data-stu-id="4a47c-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="4a47c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a47c-108">EXAMPLES</span></span>

### <span data-ttu-id="4a47c-109">Przykład 1. Włączanie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="4a47c-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="4a47c-110">To polecenie umożliwia włączenie zadania o identyfikatorze ID-000001.</span><span class="sxs-lookup"><span data-stu-id="4a47c-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="4a47c-111">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="4a47c-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="4a47c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a47c-112">PARAMETERS</span></span>

### <span data-ttu-id="4a47c-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4a47c-113">-BatchContext</span></span>
<span data-ttu-id="4a47c-114">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="4a47c-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4a47c-115">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="4a47c-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="4a47c-116">-ID</span><span class="sxs-lookup"><span data-stu-id="4a47c-116">-Id</span></span>
<span data-ttu-id="4a47c-117">Określa identyfikator zadania, które włącza to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a47c-117">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="4a47c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a47c-118">-DefaultProfile</span></span>
<span data-ttu-id="4a47c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a47c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a47c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a47c-120">CommonParameters</span></span>
<span data-ttu-id="4a47c-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a47c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a47c-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a47c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a47c-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a47c-123">INPUTS</span></span>

### <span data-ttu-id="4a47c-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4a47c-124">BatchAccountContext</span></span>
<span data-ttu-id="4a47c-125">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="4a47c-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="4a47c-126">Ciąg</span><span class="sxs-lookup"><span data-stu-id="4a47c-126">String</span></span>
<span data-ttu-id="4a47c-127">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="4a47c-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="4a47c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a47c-128">OUTPUTS</span></span>

## <span data-ttu-id="4a47c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a47c-129">NOTES</span></span>

## <span data-ttu-id="4a47c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a47c-130">RELATED LINKS</span></span>

[<span data-ttu-id="4a47c-131">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4a47c-131">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="4a47c-132">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4a47c-132">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="4a47c-133">Nowe — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4a47c-133">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="4a47c-134">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4a47c-134">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="4a47c-135">Zatrzymaj — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4a47c-135">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="4a47c-136">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="4a47c-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


