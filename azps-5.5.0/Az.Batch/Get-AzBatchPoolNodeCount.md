---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: b3b1adfe9549a7b04a1e7c6d57542cef8a40cfd7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239319"
---
# <span data-ttu-id="e26c3-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="e26c3-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="e26c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e26c3-102">SYNOPSIS</span></span>
<span data-ttu-id="e26c3-103">Pobiera liczbę węzła wsadowego na stan węzła pogrupowane według identyfikatora puli.</span><span class="sxs-lookup"><span data-stu-id="e26c3-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="e26c3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e26c3-104">SYNTAX</span></span>

### <span data-ttu-id="e26c3-105">AzureBatchPoolNodeCounts (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e26c3-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e26c3-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="e26c3-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e26c3-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="e26c3-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e26c3-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="e26c3-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e26c3-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="e26c3-109">DESCRIPTION</span></span>
<span data-ttu-id="e26c3-110">Polecenie Get-AzBatchPoolNodeCount cmdlet umożliwia klientom powrót do liczby węzłów na stan węzła pogrupowany według puli.</span><span class="sxs-lookup"><span data-stu-id="e26c3-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="e26c3-111">Możliwe stany węzła to tworzenie, bezczynny, opuszczaniePool, offline, wyewolone, ponowne uruchomienie, ponowne uruchomienie, uruchamianie, uruchamianie, startTaskFailed, nieznane, niezdatne do użytku i czekanieForStartTask.</span><span class="sxs-lookup"><span data-stu-id="e26c3-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="e26c3-112">Polecenie cmdlet pobiera parametr PoolId lub Pool w celu filtrowania tylko puli o określonym identyfikatorze puli.</span><span class="sxs-lookup"><span data-stu-id="e26c3-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="e26c3-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e26c3-113">EXAMPLES</span></span>

### <span data-ttu-id="e26c3-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e26c3-114">Example 1</span></span>
```
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="e26c3-115">Węzeł listy zlicza pule w stanie węzła w kontekście bieżącego konta partii.</span><span class="sxs-lookup"><span data-stu-id="e26c3-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="e26c3-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e26c3-116">Example 2</span></span>

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

<span data-ttu-id="e26c3-117">Pokaż liczbę węzłów na stan węzła dla puli o identyfikatorze puli.</span><span class="sxs-lookup"><span data-stu-id="e26c3-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="e26c3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e26c3-118">PARAMETERS</span></span>

### <span data-ttu-id="e26c3-119">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="e26c3-119">-BatchContext</span></span>
<span data-ttu-id="e26c3-120">Wystąpienie BatchAccountContext do użycia podczas interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="e26c3-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="e26c3-121">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e26c3-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="e26c3-122">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="e26c3-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="e26c3-123">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="e26c3-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="e26c3-124">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e26c3-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e26c3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e26c3-125">-DefaultProfile</span></span>
<span data-ttu-id="e26c3-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e26c3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e26c3-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e26c3-127">-MaxCount</span></span>
<span data-ttu-id="e26c3-128">Określa maksymalną liczbę pul do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="e26c3-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="e26c3-129">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="e26c3-129">The default value is 10.</span></span>

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

### <span data-ttu-id="e26c3-130">— Pula</span><span class="sxs-lookup"><span data-stu-id="e26c3-130">-Pool</span></span>
<span data-ttu-id="e26c3-131">Określa wartość **PSCloudPool,** dla której zostanie wyliszczony węzeł.</span><span class="sxs-lookup"><span data-stu-id="e26c3-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

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

### <span data-ttu-id="e26c3-132">- PoolId</span><span class="sxs-lookup"><span data-stu-id="e26c3-132">-PoolId</span></span>
<span data-ttu-id="e26c3-133">Identyfikator puli, dla której zostanie zliczy się węzeł.</span><span class="sxs-lookup"><span data-stu-id="e26c3-133">The id of the pool for which to get node counts.</span></span>

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

### <span data-ttu-id="e26c3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e26c3-134">CommonParameters</span></span>
<span data-ttu-id="e26c3-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e26c3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e26c3-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e26c3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e26c3-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e26c3-137">INPUTS</span></span>

### <span data-ttu-id="e26c3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e26c3-138">System.String</span></span>

### <span data-ttu-id="e26c3-139">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="e26c3-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="e26c3-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e26c3-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e26c3-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e26c3-141">OUTPUTS</span></span>

### <span data-ttu-id="e26c3-142">Microsoft.Azure.Commands.Batch. Models.PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="e26c3-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="e26c3-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e26c3-143">NOTES</span></span>

## <span data-ttu-id="e26c3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e26c3-144">RELATED LINKS</span></span>

[<span data-ttu-id="e26c3-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e26c3-145">Get-AzBatchAccountKey</span></span>]()

[<span data-ttu-id="e26c3-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e26c3-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="e26c3-147">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e26c3-147">Azure Batch Cmdlets</span></span>]()

