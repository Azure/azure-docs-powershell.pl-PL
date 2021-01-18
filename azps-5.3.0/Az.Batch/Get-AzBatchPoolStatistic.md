---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
ms.openlocfilehash: 49aa971dcc9d46f5a063042cbcdf8ca449c41e94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502174"
---
# <span data-ttu-id="78716-101">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="78716-101">Get-AzBatchPoolStatistic</span></span>

## <span data-ttu-id="78716-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78716-102">SYNOPSIS</span></span>
<span data-ttu-id="78716-103">Pobiera statystykę podsumowania puli dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="78716-103">Gets pool summary statistics for a Batch account.</span></span>

## <span data-ttu-id="78716-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78716-104">SYNTAX</span></span>

```
Get-AzBatchPoolStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78716-105">Opis</span><span class="sxs-lookup"><span data-stu-id="78716-105">DESCRIPTION</span></span>
<span data-ttu-id="78716-106">Polecenie cmdlet **Get-AzBatchPoolStatistic** pobiera statystykę okresu istnienia dla wszystkich pul na określonym koncie.</span><span class="sxs-lookup"><span data-stu-id="78716-106">The **Get-AzBatchPoolStatistic** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="78716-107">Statystyka jest agregowana we wszystkich pulach, które kiedykolwiek istniały na koncie, od utworzenia konta do ostatniej aktualizacji statystyk.</span><span class="sxs-lookup"><span data-stu-id="78716-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="78716-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78716-108">EXAMPLES</span></span>

### <span data-ttu-id="78716-109">Przykład 1: Pobieranie statystyk zasobów wszystkich pul na koncie</span><span class="sxs-lookup"><span data-stu-id="78716-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzBatchPoolStatistic -BatchContext $Context
PS C:\> $PoolStatistics.ResourceStatistics
AverageCpuPercentage : 0.351232518750755
AverageDiskGiB       : 55.2569014701165
AverageMemoryGiB     : 2.87273772318252
DiskReadGiB          : 45.1326256990433
DiskReadIOps         : 878278
DiskWriteGiB         : 1230.72120628133
DiskWriteIOps        : 176832212
LastUpdateTime       : 5/16/2016 4:30:00 PM
NetworkReadGiB       : 29.3502839952707
NetworkWriteGiB      : 25.5208827350289
PeakDiskGiB          : 21.9638671875
PeakMemoryGiB        : 1.11184692382813
StartTime            : 2/10/2016 7:07:24 PM
```

<span data-ttu-id="78716-110">Pierwsze polecenie tworzy odwołanie obiektu do kluczy konta dla konta wsadowego o nazwie ContosoBatchAccount przy użyciu polecenia **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="78716-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="78716-111">Polecenie zapisuje to odwołanie do obiektu w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="78716-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="78716-112">Drugie polecenie pobiera statystykę wszystkich pul z określonego konta, a następnie zapisuje je w $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="78716-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="78716-113">Polecenie ostatnie wyświetla Właściwość **ResourceStatistics** $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="78716-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="78716-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78716-114">PARAMETERS</span></span>

### <span data-ttu-id="78716-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="78716-115">-BatchContext</span></span>
<span data-ttu-id="78716-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="78716-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="78716-117">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="78716-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="78716-118">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="78716-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="78716-119">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="78716-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="78716-120">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="78716-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="78716-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78716-121">-DefaultProfile</span></span>
<span data-ttu-id="78716-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78716-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78716-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78716-123">CommonParameters</span></span>
<span data-ttu-id="78716-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78716-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78716-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78716-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78716-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78716-126">INPUTS</span></span>

### <span data-ttu-id="78716-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="78716-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="78716-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78716-128">OUTPUTS</span></span>

### <span data-ttu-id="78716-129">Microsoft.Azure.Commands.Batch. Modele. PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="78716-129">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="78716-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78716-130">NOTES</span></span>

## <span data-ttu-id="78716-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78716-131">RELATED LINKS</span></span>

[<span data-ttu-id="78716-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="78716-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="78716-133">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="78716-133">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)

[<span data-ttu-id="78716-134">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="78716-134">Get-AzBatchJobStatistic</span></span>](./Get-AzBatchJobStatistic.md)
