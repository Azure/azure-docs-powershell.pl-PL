---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 5e26bd47c9c53b88442505aeb66d81a96c137b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524578"
---
# <span data-ttu-id="e4528-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e4528-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="e4528-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4528-102">SYNOPSIS</span></span>
<span data-ttu-id="e4528-103">Ustawia harmonogram zadań.</span><span class="sxs-lookup"><span data-stu-id="e4528-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4528-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4528-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4528-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4528-105">DESCRIPTION</span></span>
<span data-ttu-id="e4528-106">Polecenie cmdlet **Set-AzureBatchJobSchedule** ustawia harmonogram zadań w usłudze Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="e4528-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="e4528-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4528-107">EXAMPLES</span></span>

## <span data-ttu-id="e4528-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4528-108">PARAMETERS</span></span>

### <span data-ttu-id="e4528-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e4528-109">-BatchContext</span></span>
<span data-ttu-id="e4528-110">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="e4528-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e4528-111">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="e4528-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e4528-112">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="e4528-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e4528-113">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="e4528-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e4528-114">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e4528-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e4528-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4528-115">-DefaultProfile</span></span>
<span data-ttu-id="e4528-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4528-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4528-117">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="e4528-117">-JobSchedule</span></span>
<span data-ttu-id="e4528-118">Określa obiekt **PSCloudJobSchedule** , który reprezentuje harmonogram zadania.</span><span class="sxs-lookup"><span data-stu-id="e4528-118">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="e4528-119">Aby uzyskać obiekt **PSCloudJobSchedule** , użyj polecenia cmdlet Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="e4528-119">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4528-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4528-120">CommonParameters</span></span>
<span data-ttu-id="e4528-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4528-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4528-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4528-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4528-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4528-123">INPUTS</span></span>

### <span data-ttu-id="e4528-124">Microsoft.Azure.Commands.Batch. Modele. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e4528-124">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>
<span data-ttu-id="e4528-125">Parametry: JobSchedule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e4528-125">Parameters: JobSchedule (ByValue)</span></span>

### <span data-ttu-id="e4528-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e4528-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="e4528-127">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e4528-127">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="e4528-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4528-128">OUTPUTS</span></span>

### <span data-ttu-id="e4528-129">System. void</span><span class="sxs-lookup"><span data-stu-id="e4528-129">System.Void</span></span>

## <span data-ttu-id="e4528-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4528-130">NOTES</span></span>

## <span data-ttu-id="e4528-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4528-131">RELATED LINKS</span></span>

[<span data-ttu-id="e4528-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e4528-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="e4528-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e4528-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="e4528-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e4528-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="e4528-135">Nowe — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e4528-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="e4528-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e4528-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="e4528-137">Zatrzymaj — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e4528-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


