---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: a878002c509fd2a895f61a97af1bef2afebc3691
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552227"
---
# <span data-ttu-id="b382d-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b382d-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="b382d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b382d-102">SYNOPSIS</span></span>
<span data-ttu-id="b382d-103">Umożliwia zaktualizowanie zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="b382d-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b382d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b382d-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b382d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b382d-105">DESCRIPTION</span></span>
<span data-ttu-id="b382d-106">Polecenie cmdlet **Set-AzureBatchJob** aktualizuje zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="b382d-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="b382d-107">Użyj polecenia cmdlet Get-AzureBatchJob, aby uzyskać obiekt **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="b382d-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="b382d-108">Zmodyfikuj właściwości tego obiektu, a następnie użyj bieżącego polecenia cmdlet, aby zatwierdzić zmiany w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="b382d-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="b382d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b382d-109">EXAMPLES</span></span>

### <span data-ttu-id="b382d-110">Przykład 1: aktualizowanie zadania</span><span class="sxs-lookup"><span data-stu-id="b382d-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="b382d-111">Pierwsze polecenie uzyskuje pulę przy użyciu polecenia **Get-AzureBatchJob** , a następnie zapisuje ją w zmiennej $Job.</span><span class="sxs-lookup"><span data-stu-id="b382d-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="b382d-112">Drugie polecenie modyfikuje specyfikację priorytetu obiektu $Job.</span><span class="sxs-lookup"><span data-stu-id="b382d-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="b382d-113">Polecenie ostatnie aktualizuje usługę wsadu tak, aby odpowiadała obiektowi lokalnemu w $Job.</span><span class="sxs-lookup"><span data-stu-id="b382d-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="b382d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b382d-114">PARAMETERS</span></span>

### <span data-ttu-id="b382d-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b382d-115">-BatchContext</span></span>
<span data-ttu-id="b382d-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="b382d-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b382d-117">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="b382d-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b382d-118">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="b382d-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b382d-119">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="b382d-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b382d-120">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b382d-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b382d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b382d-121">-DefaultProfile</span></span>
<span data-ttu-id="b382d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b382d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b382d-123">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="b382d-123">-Job</span></span>
<span data-ttu-id="b382d-124">Określa **PSCloudJob** , do którego to polecenie cmdlet aktualizuje usługę wsadu.</span><span class="sxs-lookup"><span data-stu-id="b382d-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b382d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b382d-125">CommonParameters</span></span>
<span data-ttu-id="b382d-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b382d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b382d-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b382d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b382d-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b382d-128">INPUTS</span></span>

### <span data-ttu-id="b382d-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b382d-129">BatchAccountContext</span></span>
<span data-ttu-id="b382d-130">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="b382d-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b382d-131">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="b382d-131">PSCloudJob</span></span>
<span data-ttu-id="b382d-132">Parametr "zadanie" akceptuje wartość typu "PSCloudJob" z potoku.</span><span class="sxs-lookup"><span data-stu-id="b382d-132">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="b382d-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b382d-133">OUTPUTS</span></span>

## <span data-ttu-id="b382d-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b382d-134">NOTES</span></span>

## <span data-ttu-id="b382d-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b382d-135">RELATED LINKS</span></span>

[<span data-ttu-id="b382d-136">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b382d-136">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="b382d-137">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b382d-137">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="b382d-138">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b382d-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="b382d-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b382d-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b382d-140">Nowe — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b382d-140">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="b382d-141">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b382d-141">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="b382d-142">Zatrzymaj — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b382d-142">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="b382d-143">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="b382d-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


