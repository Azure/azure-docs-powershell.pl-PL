---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 81ace9fd18b916f8f4788cf5878af1a620a61882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718508"
---
# <span data-ttu-id="4d634-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4d634-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="4d634-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d634-102">SYNOPSIS</span></span>
<span data-ttu-id="4d634-103">Umożliwia wykonywanie zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="4d634-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d634-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d634-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d634-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d634-105">DESCRIPTION</span></span>
<span data-ttu-id="4d634-106">Polecenie cmdlet **enable-AzureBatchJob** włącza zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="4d634-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="4d634-107">Po włączeniu zadania można uruchamiać nowe zadania.</span><span class="sxs-lookup"><span data-stu-id="4d634-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="4d634-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d634-108">EXAMPLES</span></span>

### <span data-ttu-id="4d634-109">Przykład 1. Włączanie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="4d634-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="4d634-110">To polecenie umożliwia włączenie zadania o identyfikatorze ID-000001.</span><span class="sxs-lookup"><span data-stu-id="4d634-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="4d634-111">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="4d634-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="4d634-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d634-112">PARAMETERS</span></span>

### <span data-ttu-id="4d634-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4d634-113">-BatchContext</span></span>
<span data-ttu-id="4d634-114">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="4d634-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4d634-115">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="4d634-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4d634-116">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="4d634-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4d634-117">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="4d634-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4d634-118">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4d634-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4d634-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d634-119">-DefaultProfile</span></span>
<span data-ttu-id="4d634-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d634-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d634-121">-ID</span><span class="sxs-lookup"><span data-stu-id="4d634-121">-Id</span></span>
<span data-ttu-id="4d634-122">Określa identyfikator zadania, które włącza to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d634-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="4d634-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d634-123">CommonParameters</span></span>
<span data-ttu-id="4d634-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d634-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d634-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d634-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d634-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d634-126">INPUTS</span></span>

### <span data-ttu-id="4d634-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4d634-127">BatchAccountContext</span></span>
<span data-ttu-id="4d634-128">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="4d634-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="4d634-129">Ciąg</span><span class="sxs-lookup"><span data-stu-id="4d634-129">String</span></span>
<span data-ttu-id="4d634-130">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="4d634-130">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="4d634-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d634-131">OUTPUTS</span></span>

## <span data-ttu-id="4d634-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d634-132">NOTES</span></span>

## <span data-ttu-id="4d634-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d634-133">RELATED LINKS</span></span>

[<span data-ttu-id="4d634-134">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4d634-134">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="4d634-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4d634-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="4d634-136">Nowe — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4d634-136">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="4d634-137">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4d634-137">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="4d634-138">Zatrzymaj — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4d634-138">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="4d634-139">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="4d634-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


