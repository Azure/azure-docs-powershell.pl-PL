---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: eb15991e0bf7aefd60b53dbb02785a1b2004cb22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554014"
---
# <span data-ttu-id="0ed84-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ed84-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="0ed84-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ed84-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed84-103">Umożliwia zaktualizowanie zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="0ed84-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ed84-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ed84-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ed84-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0ed84-105">DESCRIPTION</span></span>
<span data-ttu-id="0ed84-106">Polecenie cmdlet **Set-AzureBatchJob** aktualizuje zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="0ed84-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="0ed84-107">Użyj polecenia cmdlet Get-AzureBatchJob, aby uzyskać obiekt **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="0ed84-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="0ed84-108">Zmodyfikuj właściwości tego obiektu, a następnie użyj bieżącego polecenia cmdlet, aby zatwierdzić zmiany w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="0ed84-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="0ed84-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ed84-109">EXAMPLES</span></span>

### <span data-ttu-id="0ed84-110">Przykład 1: aktualizowanie zadania</span><span class="sxs-lookup"><span data-stu-id="0ed84-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="0ed84-111">Pierwsze polecenie uzyskuje pulę przy użyciu polecenia **Get-AzureBatchJob** , a następnie zapisuje ją w zmiennej $Job.</span><span class="sxs-lookup"><span data-stu-id="0ed84-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="0ed84-112">Drugie polecenie modyfikuje specyfikację priorytetu obiektu $Job.</span><span class="sxs-lookup"><span data-stu-id="0ed84-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="0ed84-113">Polecenie ostatnie aktualizuje usługę wsadu tak, aby odpowiadała obiektowi lokalnemu w $Job.</span><span class="sxs-lookup"><span data-stu-id="0ed84-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="0ed84-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ed84-114">PARAMETERS</span></span>

### <span data-ttu-id="0ed84-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0ed84-115">-BatchContext</span></span>
<span data-ttu-id="0ed84-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="0ed84-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0ed84-117">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="0ed84-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="0ed84-118">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="0ed84-118">-Job</span></span>
<span data-ttu-id="0ed84-119">Określa **PSCloudJob** , do którego to polecenie cmdlet aktualizuje usługę wsadu.</span><span class="sxs-lookup"><span data-stu-id="0ed84-119">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed84-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed84-120">-DefaultProfile</span></span>
<span data-ttu-id="0ed84-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ed84-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ed84-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed84-122">CommonParameters</span></span>
<span data-ttu-id="0ed84-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ed84-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed84-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ed84-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed84-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ed84-125">INPUTS</span></span>

### <span data-ttu-id="0ed84-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0ed84-126">BatchAccountContext</span></span>
<span data-ttu-id="0ed84-127">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="0ed84-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="0ed84-128">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="0ed84-128">PSCloudJob</span></span>
<span data-ttu-id="0ed84-129">Parametr "zadanie" akceptuje wartość typu "PSCloudJob" z potoku.</span><span class="sxs-lookup"><span data-stu-id="0ed84-129">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="0ed84-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ed84-130">OUTPUTS</span></span>

## <span data-ttu-id="0ed84-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ed84-131">NOTES</span></span>

## <span data-ttu-id="0ed84-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ed84-132">RELATED LINKS</span></span>

[<span data-ttu-id="0ed84-133">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ed84-133">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="0ed84-134">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ed84-134">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="0ed84-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ed84-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="0ed84-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0ed84-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0ed84-137">Nowe — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ed84-137">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="0ed84-138">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ed84-138">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="0ed84-139">Zatrzymaj — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ed84-139">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="0ed84-140">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="0ed84-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


