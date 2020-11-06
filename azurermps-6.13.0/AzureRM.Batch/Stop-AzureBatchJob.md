---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: f67660cdc64c814d04ec4a987b711c802ca222d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547551"
---
# <span data-ttu-id="82ed5-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="82ed5-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="82ed5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="82ed5-103">Zatrzymuje zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="82ed5-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82ed5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82ed5-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82ed5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="82ed5-105">DESCRIPTION</span></span>
<span data-ttu-id="82ed5-106">Polecenie cmdlet **stop-AzureBatchJob** zatrzymuje zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="82ed5-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="82ed5-107">To polecenie oznacza zadanie jako ukończone.</span><span class="sxs-lookup"><span data-stu-id="82ed5-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="82ed5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82ed5-108">EXAMPLES</span></span>

### <span data-ttu-id="82ed5-109">Przykład 1. zatrzymanie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="82ed5-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="82ed5-110">To polecenie zatrzymuje zadanie o identyfikatorze zadania ID-000001.</span><span class="sxs-lookup"><span data-stu-id="82ed5-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="82ed5-111">Polecenie określa powód, dla którego wybrano zatrzymanie zadania.</span><span class="sxs-lookup"><span data-stu-id="82ed5-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="82ed5-112">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="82ed5-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="82ed5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82ed5-113">PARAMETERS</span></span>

### <span data-ttu-id="82ed5-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="82ed5-114">-BatchContext</span></span>
<span data-ttu-id="82ed5-115">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="82ed5-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="82ed5-116">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="82ed5-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="82ed5-117">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="82ed5-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="82ed5-118">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="82ed5-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="82ed5-119">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="82ed5-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="82ed5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ed5-120">-DefaultProfile</span></span>
<span data-ttu-id="82ed5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="82ed5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82ed5-122">-ID</span><span class="sxs-lookup"><span data-stu-id="82ed5-122">-Id</span></span>
<span data-ttu-id="82ed5-123">Określa identyfikator zadania, które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82ed5-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="82ed5-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="82ed5-124">-TerminateReason</span></span>
<span data-ttu-id="82ed5-125">Umożliwia określenie przyczyny zadecydowania o zatrzymywaniu zadania.</span><span class="sxs-lookup"><span data-stu-id="82ed5-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="82ed5-126">To polecenie cmdlet zapisuje ten tekst jako właściwość **TerminateReason** zadania.</span><span class="sxs-lookup"><span data-stu-id="82ed5-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="82ed5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ed5-127">CommonParameters</span></span>
<span data-ttu-id="82ed5-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82ed5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ed5-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ed5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ed5-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82ed5-130">INPUTS</span></span>

### <span data-ttu-id="82ed5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="82ed5-131">System.String</span></span>

### <span data-ttu-id="82ed5-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="82ed5-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="82ed5-133">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="82ed5-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="82ed5-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82ed5-134">OUTPUTS</span></span>

### <span data-ttu-id="82ed5-135">System. void</span><span class="sxs-lookup"><span data-stu-id="82ed5-135">System.Void</span></span>

## <span data-ttu-id="82ed5-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82ed5-136">NOTES</span></span>

## <span data-ttu-id="82ed5-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82ed5-137">RELATED LINKS</span></span>

[<span data-ttu-id="82ed5-138">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="82ed5-138">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="82ed5-139">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="82ed5-139">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="82ed5-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="82ed5-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="82ed5-141">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="82ed5-141">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="82ed5-142">Nowe — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="82ed5-142">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="82ed5-143">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="82ed5-143">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="82ed5-144">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="82ed5-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


