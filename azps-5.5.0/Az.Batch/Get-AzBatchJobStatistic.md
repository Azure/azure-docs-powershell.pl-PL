---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: 11532648242438983ae1bc9222dbc3ac12fa05e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239360"
---
# <span data-ttu-id="36aff-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="36aff-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="36aff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36aff-102">SYNOPSIS</span></span>
<span data-ttu-id="36aff-103">Pobiera statystykę podsumowania zadań dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="36aff-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="36aff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="36aff-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36aff-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="36aff-105">DESCRIPTION</span></span>
<span data-ttu-id="36aff-106">Polecenie **cmdlet Get-AzBatchJobStatistic** otrzymuje odżywoną statystykę podsumowania dla wszystkich zadań na koncie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="36aff-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="36aff-107">Statystyki są agregowane we wszystkich zadaniach, które kiedykolwiek istniały na koncie, od tworzenia konta do ostatniej aktualizacji statystyki.</span><span class="sxs-lookup"><span data-stu-id="36aff-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="36aff-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="36aff-108">EXAMPLES</span></span>

### <span data-ttu-id="36aff-109">Przykład 1. Uzyskiwanie statystyk podsumowania dla wszystkich zadań</span><span class="sxs-lookup"><span data-stu-id="36aff-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzBatchJobStatistic -BatchContext $Context
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

<span data-ttu-id="36aff-110">Pierwsze polecenie tworzy odwołanie do obiektu do kluczy konta dla konta partii o nazwie ContosoBatchAccount przy użyciu polecenia **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="36aff-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="36aff-111">Polecenie przechowuje to odwołanie do obiektu w $Context zmienną.</span><span class="sxs-lookup"><span data-stu-id="36aff-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="36aff-112">Drugie polecenie pobiera statystykę podsumowania dla wszystkich zadań.</span><span class="sxs-lookup"><span data-stu-id="36aff-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="36aff-113">To polecenie używa $Context wartości pierwszego polecenia.</span><span class="sxs-lookup"><span data-stu-id="36aff-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="36aff-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36aff-114">PARAMETERS</span></span>

### <span data-ttu-id="36aff-115">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="36aff-115">-BatchContext</span></span>
<span data-ttu-id="36aff-116">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="36aff-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="36aff-117">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="36aff-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="36aff-118">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="36aff-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="36aff-119">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="36aff-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="36aff-120">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="36aff-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="36aff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36aff-121">-DefaultProfile</span></span>
<span data-ttu-id="36aff-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="36aff-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36aff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36aff-123">CommonParameters</span></span>
<span data-ttu-id="36aff-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36aff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36aff-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36aff-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36aff-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36aff-126">INPUTS</span></span>

### <span data-ttu-id="36aff-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="36aff-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="36aff-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36aff-128">OUTPUTS</span></span>

### <span data-ttu-id="36aff-129">Microsoft.Azure.Commands.Batch. Models.PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="36aff-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="36aff-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="36aff-130">NOTES</span></span>

## <span data-ttu-id="36aff-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36aff-131">RELATED LINKS</span></span>

[<span data-ttu-id="36aff-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="36aff-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="36aff-133">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="36aff-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="36aff-134">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="36aff-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)
