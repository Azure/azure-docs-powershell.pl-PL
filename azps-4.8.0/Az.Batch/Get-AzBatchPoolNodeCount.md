---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: b3b1adfe9549a7b04a1e7c6d57542cef8a40cfd7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221582"
---
# <span data-ttu-id="fe420-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="fe420-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="fe420-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe420-102">SYNOPSIS</span></span>
<span data-ttu-id="fe420-103">Pobiera liczbę węzłów partii według stanu węzła pogrupowanych według identyfikatora puli.</span><span class="sxs-lookup"><span data-stu-id="fe420-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="fe420-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe420-104">SYNTAX</span></span>

### <span data-ttu-id="fe420-105">AzureBatchPoolNodeCounts (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fe420-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe420-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="fe420-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe420-107">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="fe420-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe420-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="fe420-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe420-109">Opis</span><span class="sxs-lookup"><span data-stu-id="fe420-109">DESCRIPTION</span></span>
<span data-ttu-id="fe420-110">Polecenie cmdlet Get-AzBatchPoolNodeCount umożliwia klientom otrzymywanie liczby węzłów na stan węzła pogrupowanych według puli.</span><span class="sxs-lookup"><span data-stu-id="fe420-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="fe420-111">Możliwe stany węzła to tworzenie, bezczynne, leavingPool, w trybie offline, przetworzone, ponowne uruchamianie, przetwarzanie obrazów, uruchamianie, uruchamianie, startTaskFailed, nieznany, bezużyteczny i waitingForStartTask.</span><span class="sxs-lookup"><span data-stu-id="fe420-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="fe420-112">Polecenie cmdlet pobiera parametr PoolId lub Pool, aby filtrować tylko pulę z określonym identyfikatorem puli.</span><span class="sxs-lookup"><span data-stu-id="fe420-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="fe420-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe420-113">EXAMPLES</span></span>

### <span data-ttu-id="fe420-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fe420-114">Example 1</span></span>
```
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="fe420-115">Liczba węzłów listy na stan węzła dla pul w obszarze bieżący kontekst konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="fe420-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="fe420-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fe420-116">Example 2</span></span>

```powershell
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"
PS C:\> $poolnodecounts.Dedicated

Creating            : 1
Idle                : 1
LeavingPool         : 0
Offline             : 0
Preempted           : 0
Rebooting           : 1
Reimaging           : 0
Running             : 5
Starting            : 0
StartTaskFailed     : 0
Total               : 8
Unknown             : 0
Unusable            : 0
WaitingForStartTask : 0

PS C:\> Get-AzBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="fe420-117">Pokazywanie liczby węzłów na stan węzła dla puli o danym identyfikatorze puli.</span><span class="sxs-lookup"><span data-stu-id="fe420-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="fe420-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe420-118">PARAMETERS</span></span>

### <span data-ttu-id="fe420-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fe420-119">-BatchContext</span></span>
<span data-ttu-id="fe420-120">Wystąpienie BatchAccountContext, które ma być używane podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="fe420-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="fe420-121">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="fe420-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="fe420-122">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="fe420-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="fe420-123">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="fe420-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="fe420-124">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="fe420-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fe420-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe420-125">-DefaultProfile</span></span>
<span data-ttu-id="fe420-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe420-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe420-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fe420-127">-MaxCount</span></span>
<span data-ttu-id="fe420-128">Określa maksymalną liczbę zestawów, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="fe420-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="fe420-129">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="fe420-129">The default value is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe420-130">-Pool</span><span class="sxs-lookup"><span data-stu-id="fe420-130">-Pool</span></span>
<span data-ttu-id="fe420-131">Określa **PSCloudPool** , dla którego mają zostać wyświetlone liczby węzłów.</span><span class="sxs-lookup"><span data-stu-id="fe420-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe420-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="fe420-132">-PoolId</span></span>
<span data-ttu-id="fe420-133">Identyfikator puli, dla której mają zostać wyświetlone liczby węzłów.</span><span class="sxs-lookup"><span data-stu-id="fe420-133">The id of the pool for which to get node counts.</span></span>

```yaml
Type: System.String
Parameter Sets: PoolId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe420-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe420-134">CommonParameters</span></span>
<span data-ttu-id="fe420-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe420-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe420-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe420-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe420-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe420-137">INPUTS</span></span>

### <span data-ttu-id="fe420-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fe420-138">System.String</span></span>

### <span data-ttu-id="fe420-139">Microsoft.Azure.Commands.Batch. Modele. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="fe420-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="fe420-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fe420-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fe420-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe420-141">OUTPUTS</span></span>

### <span data-ttu-id="fe420-142">Microsoft.Azure.Commands.Batch. Modele. PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="fe420-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="fe420-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe420-143">NOTES</span></span>

## <span data-ttu-id="fe420-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe420-144">RELATED LINKS</span></span>

[<span data-ttu-id="fe420-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="fe420-145">Get-AzBatchAccountKey</span></span>]()

[<span data-ttu-id="fe420-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="fe420-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="fe420-147">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="fe420-147">Azure Batch Cmdlets</span></span>]()

