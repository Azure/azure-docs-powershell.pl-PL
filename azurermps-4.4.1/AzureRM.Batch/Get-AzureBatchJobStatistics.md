---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
ms.openlocfilehash: 03b7e3999fbc482223365b59867c02c75e9d5ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546287"
---
# <span data-ttu-id="db646-101">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="db646-101">Get-AzureBatchJobStatistics</span></span>

## <span data-ttu-id="db646-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db646-102">SYNOPSIS</span></span>
<span data-ttu-id="db646-103">Pobiera statystykę podsumowania zadania dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="db646-103">Gets job summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db646-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db646-104">SYNTAX</span></span>

```
Get-AzureBatchJobStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db646-105">Opis</span><span class="sxs-lookup"><span data-stu-id="db646-105">DESCRIPTION</span></span>
<span data-ttu-id="db646-106">Polecenie cmdlet **Get-AzureBatchJobStatistics** pobiera statystykę podsumowania okresu ważności dla wszystkich zadań na koncie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="db646-106">The **Get-AzureBatchJobStatistics** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="db646-107">Statystyki są agregowane we wszystkich zadaniach, które kiedykolwiek istniały na koncie, od utworzenia konta do ostatniej aktualizacji statystyk.</span><span class="sxs-lookup"><span data-stu-id="db646-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="db646-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db646-108">EXAMPLES</span></span>

### <span data-ttu-id="db646-109">Przykład 1: Pobieranie statystyk podsumowań dla wszystkich zadań</span><span class="sxs-lookup"><span data-stu-id="db646-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzureBatchJobStatistics -BatchContext $Context
FailedTaskCount    : 330
KernelCpuTime      : 00:24:31.8440000
LastUpdateTime     : 5/16/2016 6:00:00 PM
ReadIOGiB          : 38.1271341182292
ReadIOps           : 26546054
StartTime          : 11/3/2015 9:47:14 PM
SucceededTaskCount : 766
TaskRetryCount     : 0
Url                : https://accountname.westus.batch.azure.com/lifetimejobstats
UserCpuTime        : 20:55:50.3200000
WaitTime           : 03:54:49.8530000
WallClockTime      : 20:55:50.3200000
WriteIOGiB         : 0.159623090177774
WriteIOps          : 146946
```

<span data-ttu-id="db646-110">Pierwsze polecenie tworzy odwołanie obiektu do kluczy konta dla konta wsadowego o nazwie ContosoBatchAccount przy użyciu polecenia **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="db646-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="db646-111">Polecenie zapisuje to odwołanie do obiektu w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="db646-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="db646-112">Drugie polecenie pobiera statystykę podsumowania dla wszystkich zadań.</span><span class="sxs-lookup"><span data-stu-id="db646-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="db646-113">W poleceniu użyto wartości $Context z pierwszego polecenia.</span><span class="sxs-lookup"><span data-stu-id="db646-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="db646-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db646-114">PARAMETERS</span></span>

### <span data-ttu-id="db646-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="db646-115">-BatchContext</span></span>
<span data-ttu-id="db646-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="db646-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="db646-117">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="db646-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="db646-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db646-118">-DefaultProfile</span></span>
<span data-ttu-id="db646-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="db646-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db646-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db646-120">CommonParameters</span></span>
<span data-ttu-id="db646-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db646-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db646-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db646-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db646-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db646-123">INPUTS</span></span>

### <span data-ttu-id="db646-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="db646-124">BatchAccountContext</span></span>
<span data-ttu-id="db646-125">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="db646-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="db646-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db646-126">OUTPUTS</span></span>

### <span data-ttu-id="db646-127">PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="db646-127">PSJobStatistics</span></span>

## <span data-ttu-id="db646-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db646-128">NOTES</span></span>

## <span data-ttu-id="db646-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db646-129">RELATED LINKS</span></span>

[<span data-ttu-id="db646-130">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="db646-130">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="db646-131">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="db646-131">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="db646-132">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="db646-132">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)


