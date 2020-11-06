---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: 3baaa7296ab0fdd2c1dcab606b2896b11e5773f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526285"
---
# <span data-ttu-id="2373d-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2373d-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="2373d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2373d-102">SYNOPSIS</span></span>
<span data-ttu-id="2373d-103">Umożliwia zaktualizowanie zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="2373d-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2373d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2373d-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2373d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2373d-105">DESCRIPTION</span></span>
<span data-ttu-id="2373d-106">Polecenie cmdlet **Set-AzureBatchJob** aktualizuje zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="2373d-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="2373d-107">Użyj polecenia cmdlet Get-AzureBatchJob, aby uzyskać obiekt **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="2373d-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="2373d-108">Zmodyfikuj właściwości tego obiektu, a następnie użyj bieżącego polecenia cmdlet, aby zatwierdzić zmiany w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="2373d-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="2373d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2373d-109">EXAMPLES</span></span>

### <span data-ttu-id="2373d-110">Przykład 1: aktualizowanie zadania</span><span class="sxs-lookup"><span data-stu-id="2373d-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="2373d-111">Pierwsze polecenie uzyskuje pulę przy użyciu polecenia **Get-AzureBatchJob** , a następnie zapisuje ją w zmiennej $Job.</span><span class="sxs-lookup"><span data-stu-id="2373d-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="2373d-112">Drugie polecenie modyfikuje specyfikację priorytetu obiektu $Job.</span><span class="sxs-lookup"><span data-stu-id="2373d-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="2373d-113">Polecenie ostatnie aktualizuje usługę wsadu tak, aby odpowiadała obiektowi lokalnemu w $Job.</span><span class="sxs-lookup"><span data-stu-id="2373d-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="2373d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2373d-114">PARAMETERS</span></span>

### <span data-ttu-id="2373d-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2373d-115">-BatchContext</span></span>
<span data-ttu-id="2373d-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="2373d-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2373d-117">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="2373d-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2373d-118">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="2373d-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2373d-119">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="2373d-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2373d-120">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2373d-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2373d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2373d-121">-DefaultProfile</span></span>
<span data-ttu-id="2373d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2373d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2373d-123">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="2373d-123">-Job</span></span>
<span data-ttu-id="2373d-124">Określa **PSCloudJob** , do którego to polecenie cmdlet aktualizuje usługę wsadu.</span><span class="sxs-lookup"><span data-stu-id="2373d-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="2373d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2373d-125">CommonParameters</span></span>
<span data-ttu-id="2373d-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2373d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2373d-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2373d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2373d-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2373d-128">INPUTS</span></span>

### <span data-ttu-id="2373d-129">Microsoft.Azure.Commands.Batch. Modele. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="2373d-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>
<span data-ttu-id="2373d-130">Parametry: zadanie (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2373d-130">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="2373d-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2373d-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="2373d-132">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2373d-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="2373d-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2373d-133">OUTPUTS</span></span>

### <span data-ttu-id="2373d-134">System. void</span><span class="sxs-lookup"><span data-stu-id="2373d-134">System.Void</span></span>

## <span data-ttu-id="2373d-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2373d-135">NOTES</span></span>

## <span data-ttu-id="2373d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2373d-136">RELATED LINKS</span></span>

[<span data-ttu-id="2373d-137">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2373d-137">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="2373d-138">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2373d-138">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="2373d-139">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2373d-139">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="2373d-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2373d-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2373d-141">Nowe — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2373d-141">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="2373d-142">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2373d-142">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="2373d-143">Zatrzymaj — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2373d-143">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="2373d-144">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="2373d-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


