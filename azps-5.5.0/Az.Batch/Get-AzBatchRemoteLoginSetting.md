---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239300"
---
# <span data-ttu-id="df03c-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="df03c-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="df03c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df03c-102">SYNOPSIS</span></span>
<span data-ttu-id="df03c-103">Pobiera ustawienia logowania zdalnego dla węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="df03c-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="df03c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="df03c-104">SYNTAX</span></span>

### <span data-ttu-id="df03c-105">Identyfikator (domyślne)</span><span class="sxs-lookup"><span data-stu-id="df03c-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df03c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="df03c-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df03c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="df03c-107">DESCRIPTION</span></span>
<span data-ttu-id="df03c-108">Polecenie **cmdlet Get-AzBatchRemoteLoginSetting** pobiera ustawienia logowania zdalnego dla węzła obliczeniowego w puli opartej na infrastrukturze maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="df03c-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="df03c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="df03c-109">EXAMPLES</span></span>

### <span data-ttu-id="df03c-110">Przykład 1. Uzyskiwanie ustawień logowania zdalnego dla wszystkich węzłów w puli</span><span class="sxs-lookup"><span data-stu-id="df03c-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="df03c-111">Pierwsze polecenie uzyskuje kontekst konta wsadowego zawierającego klucze dostępu dla Twojej subskrypcji przy użyciu klucza **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="df03c-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="df03c-112">Polecenie przechowuje kontekst w zmiennej $Context do użycia w następnym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="df03c-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="df03c-113">Drugie polecenie pobiera każdy węzeł obliczeniowy w puli o identyfikatorze ContosoPool przy użyciu polecenia **Get-AzBatchComputeNode.**</span><span class="sxs-lookup"><span data-stu-id="df03c-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="df03c-114">Polecenie przekazuje każdy węzeł komputera do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="df03c-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="df03c-115">Polecenie pobiera ustawienia logowania zdalnego dla każdego węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="df03c-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="df03c-116">Przykład 2. Uzyskiwanie ustawień logowania zdalnego dla węzła</span><span class="sxs-lookup"><span data-stu-id="df03c-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="df03c-117">Pierwsze polecenie pobiera kontekst konta wsadowego zawierającego klucze dostępu dla twojej subskrypcji, a następnie przechowuje je w $Context danych.</span><span class="sxs-lookup"><span data-stu-id="df03c-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="df03c-118">Drugie polecenie pobiera ustawienia logowania zdalnego dla węzła obliczeniowego, który ma określony identyfikator w puli, która ma identyfikator ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="df03c-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="df03c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df03c-119">PARAMETERS</span></span>

### <span data-ttu-id="df03c-120">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="df03c-120">-BatchContext</span></span>
<span data-ttu-id="df03c-121">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="df03c-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="df03c-122">Aby uzyskać **batchAccountContext** zawierający klucze dostępu dla subskrypcji, użyj Get-AzBatchAccountKey cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df03c-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKey cmdlet.</span></span>

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

### <span data-ttu-id="df03c-123">- ComputeNode</span><span class="sxs-lookup"><span data-stu-id="df03c-123">-ComputeNode</span></span>
<span data-ttu-id="df03c-124">Określa węzeł obliczeniowy jako **obiekt PSComputeNode,** dla którego to polecenie cmdlet pobiera ustawienia logowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="df03c-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="df03c-125">Aby uzyskać obiekt węzła obliczeniowego, użyj Get-AzBatchComputeNode cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df03c-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df03c-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="df03c-126">-ComputeNodeId</span></span>
<span data-ttu-id="df03c-127">Określa identyfikator węzła obliczeniowego, dla którego mają być obliczane ustawienia logowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="df03c-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="df03c-128">dla którego to polecenie cmdlet uzyskuje dostęp do ustawień logowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="df03c-128">for which this cmdlet gets remote logon settings.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df03c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df03c-129">-DefaultProfile</span></span>
<span data-ttu-id="df03c-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="df03c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df03c-131">- PoolId</span><span class="sxs-lookup"><span data-stu-id="df03c-131">-PoolId</span></span>
<span data-ttu-id="df03c-132">Określa identyfikator puli zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="df03c-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df03c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df03c-133">CommonParameters</span></span>
<span data-ttu-id="df03c-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df03c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df03c-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df03c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df03c-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df03c-136">INPUTS</span></span>

### <span data-ttu-id="df03c-137">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="df03c-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="df03c-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="df03c-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="df03c-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="df03c-139">OUTPUTS</span></span>

### <span data-ttu-id="df03c-140">Microsoft.Azure.Commands.Batch. Models.PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="df03c-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="df03c-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="df03c-141">NOTES</span></span>

## <span data-ttu-id="df03c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df03c-142">RELATED LINKS</span></span>

[<span data-ttu-id="df03c-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="df03c-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="df03c-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="df03c-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="df03c-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="df03c-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="df03c-146">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="df03c-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
