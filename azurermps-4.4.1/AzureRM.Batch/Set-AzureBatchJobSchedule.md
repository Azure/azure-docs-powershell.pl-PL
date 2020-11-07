---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 0f9d20cdd1d2acabbd644fda91f5f8d22ff1ccd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719370"
---
# <span data-ttu-id="d7a9d-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d7a9d-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="d7a9d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7a9d-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a9d-103">Ustawia harmonogram zadań.</span><span class="sxs-lookup"><span data-stu-id="d7a9d-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7a9d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7a9d-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7a9d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7a9d-105">DESCRIPTION</span></span>
<span data-ttu-id="d7a9d-106">Polecenie cmdlet **Set-AzureBatchJobSchedule** ustawia harmonogram zadań w usłudze Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="d7a9d-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="d7a9d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7a9d-107">EXAMPLES</span></span>

## <span data-ttu-id="d7a9d-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7a9d-108">PARAMETERS</span></span>

### <span data-ttu-id="d7a9d-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d7a9d-109">-BatchContext</span></span>
<span data-ttu-id="d7a9d-110">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="d7a9d-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d7a9d-111">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="d7a9d-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d7a9d-112">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="d7a9d-112">-JobSchedule</span></span>
<span data-ttu-id="d7a9d-113">Określa obiekt **PSCloudJobSchedule** , który reprezentuje harmonogram zadania.</span><span class="sxs-lookup"><span data-stu-id="d7a9d-113">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="d7a9d-114">Aby uzyskać obiekt **PSCloudJobSchedule** , użyj polecenia cmdlet Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="d7a9d-114">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="d7a9d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7a9d-115">-DefaultProfile</span></span>
<span data-ttu-id="d7a9d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7a9d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7a9d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a9d-117">CommonParameters</span></span>
<span data-ttu-id="d7a9d-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7a9d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a9d-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7a9d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a9d-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7a9d-120">INPUTS</span></span>

### <span data-ttu-id="d7a9d-121">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d7a9d-121">BatchAccountContext</span></span>
<span data-ttu-id="d7a9d-122">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="d7a9d-122">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d7a9d-123">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d7a9d-123">PSCloudJobSchedule</span></span>
<span data-ttu-id="d7a9d-124">Parametr "JobSchedule" akceptuje wartość typu "PSCloudJobSchedule" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="d7a9d-124">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="d7a9d-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7a9d-125">OUTPUTS</span></span>

## <span data-ttu-id="d7a9d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7a9d-126">NOTES</span></span>

## <span data-ttu-id="d7a9d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7a9d-127">RELATED LINKS</span></span>

[<span data-ttu-id="d7a9d-128">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d7a9d-128">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="d7a9d-129">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d7a9d-129">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="d7a9d-130">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d7a9d-130">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="d7a9d-131">Nowe — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d7a9d-131">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="d7a9d-132">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d7a9d-132">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="d7a9d-133">Zatrzymaj — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d7a9d-133">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


