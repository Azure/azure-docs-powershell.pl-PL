---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: daf89fec73ed18cf5b67c4100556d490795708d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985342"
---
# <span data-ttu-id="454fd-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="454fd-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="454fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="454fd-102">SYNOPSIS</span></span>
<span data-ttu-id="454fd-103">Ponowne uruchomienie określonego węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="454fd-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="454fd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="454fd-104">SYNTAX</span></span>

### <span data-ttu-id="454fd-105">Identyfikator (domyślne)</span><span class="sxs-lookup"><span data-stu-id="454fd-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="454fd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="454fd-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="454fd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="454fd-107">DESCRIPTION</span></span>
<span data-ttu-id="454fd-108">Polecenie **cmdlet Restart-AzBatchComputeNode** powoduje ponowne uruchomienie określonego węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="454fd-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="454fd-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="454fd-109">EXAMPLES</span></span>

### <span data-ttu-id="454fd-110">Przykład 1. Ponowne uruchamianie węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="454fd-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="454fd-111">To polecenie uruchamia ponownie węzeł obliczeniowy o identyfikatorze "tvm-3257026573_2-20150813t200938z" w puli MyPool.</span><span class="sxs-lookup"><span data-stu-id="454fd-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="454fd-112">Przykład 2. Ponowne uruchamianie każdego węzła obliczeniowego w puli</span><span class="sxs-lookup"><span data-stu-id="454fd-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="454fd-113">To polecenie uruchamia ponownie każdy węzeł obliczeniowy w puli mypool.</span><span class="sxs-lookup"><span data-stu-id="454fd-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="454fd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="454fd-114">PARAMETERS</span></span>

### <span data-ttu-id="454fd-115">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="454fd-115">-BatchContext</span></span>
<span data-ttu-id="454fd-116">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="454fd-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="454fd-117">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="454fd-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="454fd-118">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="454fd-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="454fd-119">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="454fd-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="454fd-120">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="454fd-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="454fd-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="454fd-121">-ComputeNode</span></span>
<span data-ttu-id="454fd-122">Określa obiekt **PSComputeNode** reprezentujący węzeł obliczeniowy do ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="454fd-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="454fd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="454fd-123">-DefaultProfile</span></span>
<span data-ttu-id="454fd-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="454fd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="454fd-125">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="454fd-125">-Id</span></span>
<span data-ttu-id="454fd-126">Określa identyfikator węzła obliczeniowego, który ma być uruchamiany ponownie.</span><span class="sxs-lookup"><span data-stu-id="454fd-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="454fd-127">- PoolId</span><span class="sxs-lookup"><span data-stu-id="454fd-127">-PoolId</span></span>
<span data-ttu-id="454fd-128">Określa identyfikator puli zawierającej węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="454fd-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="454fd-129">- RebootOption</span><span class="sxs-lookup"><span data-stu-id="454fd-129">-RebootOption</span></span>
<span data-ttu-id="454fd-130">Określa, kiedy ponownie uruchomić węzeł i co należy zrobić z obecnie uruchomionymi zadaniami.</span><span class="sxs-lookup"><span data-stu-id="454fd-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="454fd-131">Ustawieniem domyślnym jest kolejkowanie ponowne.</span><span class="sxs-lookup"><span data-stu-id="454fd-131">The default is Requeue.</span></span>

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

### <span data-ttu-id="454fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="454fd-132">CommonParameters</span></span>
<span data-ttu-id="454fd-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="454fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="454fd-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="454fd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="454fd-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="454fd-135">INPUTS</span></span>

### <span data-ttu-id="454fd-136">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="454fd-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="454fd-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="454fd-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="454fd-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="454fd-138">OUTPUTS</span></span>

### <span data-ttu-id="454fd-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="454fd-139">System.Void</span></span>

## <span data-ttu-id="454fd-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="454fd-140">NOTES</span></span>

## <span data-ttu-id="454fd-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="454fd-141">RELATED LINKS</span></span>

[<span data-ttu-id="454fd-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="454fd-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="454fd-143">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="454fd-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="454fd-144">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="454fd-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
