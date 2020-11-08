---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: 41c6ea8e069e03a759c04f39018e2fa3a4d16834
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225386"
---
# <span data-ttu-id="eba3d-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="eba3d-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="eba3d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eba3d-102">SYNOPSIS</span></span>
<span data-ttu-id="eba3d-103">Ponowna rozruch określonego węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="eba3d-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="eba3d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eba3d-104">SYNTAX</span></span>

### <span data-ttu-id="eba3d-105">Identyfikator (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="eba3d-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eba3d-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="eba3d-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eba3d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="eba3d-107">DESCRIPTION</span></span>
<span data-ttu-id="eba3d-108">Polecenie cmdlet **restart-AzBatchComputeNode** powoduje ponowne uruchomienie określonego węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="eba3d-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="eba3d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eba3d-109">EXAMPLES</span></span>

### <span data-ttu-id="eba3d-110">Przykład 1: ponowne uruchamianie węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="eba3d-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="eba3d-111">To polecenie powoduje ponowne uruchomienie węzła obliczeniowego z IDENTYFIKATORem "TVM-3257026573_2-20150813t200938z" w puli moja Pula.</span><span class="sxs-lookup"><span data-stu-id="eba3d-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="eba3d-112">Przykład 2: ponowne uruchamianie każdego węzła obliczeniowego w puli</span><span class="sxs-lookup"><span data-stu-id="eba3d-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="eba3d-113">To polecenie wykonuje ponownie rozruch każdego węzła obliczeniowego w puli moja Pula.</span><span class="sxs-lookup"><span data-stu-id="eba3d-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="eba3d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eba3d-114">PARAMETERS</span></span>

### <span data-ttu-id="eba3d-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="eba3d-115">-BatchContext</span></span>
<span data-ttu-id="eba3d-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="eba3d-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="eba3d-117">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="eba3d-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="eba3d-118">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="eba3d-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="eba3d-119">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="eba3d-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="eba3d-120">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="eba3d-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="eba3d-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="eba3d-121">-ComputeNode</span></span>
<span data-ttu-id="eba3d-122">Określa obiekt **PSComputeNode** reprezentujący węzeł obliczeniowy, który ma zostać ponownie uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="eba3d-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="eba3d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba3d-123">-DefaultProfile</span></span>
<span data-ttu-id="eba3d-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eba3d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eba3d-125">-ID</span><span class="sxs-lookup"><span data-stu-id="eba3d-125">-Id</span></span>
<span data-ttu-id="eba3d-126">Określa identyfikator węzła obliczeniowego do ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="eba3d-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="eba3d-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="eba3d-127">-PoolId</span></span>
<span data-ttu-id="eba3d-128">Określa identyfikator puli zawierającej węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="eba3d-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="eba3d-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="eba3d-129">-RebootOption</span></span>
<span data-ttu-id="eba3d-130">Określa, kiedy należy ponownie uruchomić węzeł i co należy zrobić z uruchomionymi obecnie zadaniami.</span><span class="sxs-lookup"><span data-stu-id="eba3d-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="eba3d-131">Wartość domyślna to requeued.</span><span class="sxs-lookup"><span data-stu-id="eba3d-131">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeRebootOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba3d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba3d-132">CommonParameters</span></span>
<span data-ttu-id="eba3d-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba3d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba3d-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eba3d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba3d-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eba3d-135">INPUTS</span></span>

### <span data-ttu-id="eba3d-136">Microsoft.Azure.Commands.Batch. Modele. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="eba3d-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="eba3d-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="eba3d-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="eba3d-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eba3d-138">OUTPUTS</span></span>

### <span data-ttu-id="eba3d-139">System. void</span><span class="sxs-lookup"><span data-stu-id="eba3d-139">System.Void</span></span>

## <span data-ttu-id="eba3d-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eba3d-140">NOTES</span></span>

## <span data-ttu-id="eba3d-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eba3d-141">RELATED LINKS</span></span>

[<span data-ttu-id="eba3d-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="eba3d-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="eba3d-143">Resetowanie — AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="eba3d-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="eba3d-144">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="eba3d-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
