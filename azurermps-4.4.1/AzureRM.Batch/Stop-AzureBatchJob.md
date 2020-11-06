---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: 8893ed4002e576e257cd9b885d5773c5851edde0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549259"
---
# <span data-ttu-id="a18e5-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a18e5-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="a18e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a18e5-102">SYNOPSIS</span></span>
<span data-ttu-id="a18e5-103">Zatrzymuje zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="a18e5-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a18e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a18e5-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a18e5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a18e5-105">DESCRIPTION</span></span>
<span data-ttu-id="a18e5-106">Polecenie cmdlet **stop-AzureBatchJob** zatrzymuje zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="a18e5-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="a18e5-107">To polecenie oznacza zadanie jako ukończone.</span><span class="sxs-lookup"><span data-stu-id="a18e5-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="a18e5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a18e5-108">EXAMPLES</span></span>

### <span data-ttu-id="a18e5-109">Przykład 1. zatrzymanie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="a18e5-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="a18e5-110">To polecenie zatrzymuje zadanie o identyfikatorze zadania ID-000001.</span><span class="sxs-lookup"><span data-stu-id="a18e5-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="a18e5-111">Polecenie określa powód, dla którego wybrano zatrzymanie zadania.</span><span class="sxs-lookup"><span data-stu-id="a18e5-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="a18e5-112">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="a18e5-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a18e5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a18e5-113">PARAMETERS</span></span>

### <span data-ttu-id="a18e5-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a18e5-114">-BatchContext</span></span>
<span data-ttu-id="a18e5-115">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a18e5-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a18e5-116">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="a18e5-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="a18e5-117">-ID</span><span class="sxs-lookup"><span data-stu-id="a18e5-117">-Id</span></span>
<span data-ttu-id="a18e5-118">Określa identyfikator zadania, które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a18e5-118">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="a18e5-119">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="a18e5-119">-TerminateReason</span></span>
<span data-ttu-id="a18e5-120">Umożliwia określenie przyczyny zadecydowania o zatrzymywaniu zadania.</span><span class="sxs-lookup"><span data-stu-id="a18e5-120">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="a18e5-121">To polecenie cmdlet zapisuje ten tekst jako właściwość **TerminateReason** zadania.</span><span class="sxs-lookup"><span data-stu-id="a18e5-121">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18e5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a18e5-122">-DefaultProfile</span></span>
<span data-ttu-id="a18e5-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a18e5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a18e5-124">CommonParameters</span></span>
<span data-ttu-id="a18e5-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a18e5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a18e5-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a18e5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a18e5-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a18e5-127">INPUTS</span></span>

### <span data-ttu-id="a18e5-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a18e5-128">BatchAccountContext</span></span>
<span data-ttu-id="a18e5-129">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="a18e5-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a18e5-130">Ciąg</span><span class="sxs-lookup"><span data-stu-id="a18e5-130">String</span></span>
<span data-ttu-id="a18e5-131">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="a18e5-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a18e5-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a18e5-132">OUTPUTS</span></span>

## <span data-ttu-id="a18e5-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a18e5-133">NOTES</span></span>

## <span data-ttu-id="a18e5-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a18e5-134">RELATED LINKS</span></span>

[<span data-ttu-id="a18e5-135">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a18e5-135">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="a18e5-136">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a18e5-136">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="a18e5-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a18e5-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a18e5-138">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a18e5-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="a18e5-139">Nowe — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a18e5-139">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="a18e5-140">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a18e5-140">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="a18e5-141">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="a18e5-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


