---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: ff8c758b5e384fbab8f690030eb8a7fbe35c79f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200986"
---
# <span data-ttu-id="a0540-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a0540-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="a0540-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0540-102">SYNOPSIS</span></span>
<span data-ttu-id="a0540-103">Ponowne instalowanie systemu operacyjnego w określonym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="a0540-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="a0540-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a0540-104">SYNTAX</span></span>

### <span data-ttu-id="a0540-105">Identyfikator (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a0540-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0540-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a0540-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0540-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a0540-107">DESCRIPTION</span></span>
<span data-ttu-id="a0540-108">Polecenie cmdlet **Reset-AzBatchComputeNode** ponownie instaluje system operacyjny w określonym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="a0540-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="a0540-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a0540-109">EXAMPLES</span></span>

### <span data-ttu-id="a0540-110">Przykład 1. Ponowne zaimportowanie węzła</span><span class="sxs-lookup"><span data-stu-id="a0540-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="a0540-111">To polecenie ponownie oblicza węzeł obliczeniowy o identyfikatorze "tvm-3257026573_2-20150813t200938z" w puli o nazwie MyPool.</span><span class="sxs-lookup"><span data-stu-id="a0540-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="a0540-112">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="a0540-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a0540-113">Przykład 2. Ponowne zaimportowanie wszystkich węzłów w puli</span><span class="sxs-lookup"><span data-stu-id="a0540-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="a0540-114">To polecenie ponownie oblicza każdy węzeł obliczeniowy w puli o nazwie MyPool.</span><span class="sxs-lookup"><span data-stu-id="a0540-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="a0540-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0540-115">PARAMETERS</span></span>

### <span data-ttu-id="a0540-116">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="a0540-116">-BatchContext</span></span>
<span data-ttu-id="a0540-117">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="a0540-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a0540-118">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a0540-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a0540-119">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="a0540-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a0540-120">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="a0540-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a0540-121">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a0540-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a0540-122">- ComputeNode</span><span class="sxs-lookup"><span data-stu-id="a0540-122">-ComputeNode</span></span>
<span data-ttu-id="a0540-123">Określa obiekt **PSComputeNode** reprezentujący węzeł obliczeniowy do ponownego zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="a0540-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="a0540-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0540-124">-DefaultProfile</span></span>
<span data-ttu-id="a0540-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0540-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0540-126">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="a0540-126">-Id</span></span>
<span data-ttu-id="a0540-127">Określa identyfikator węzła obliczeniowego do ponownego zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="a0540-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="a0540-128">- PoolId</span><span class="sxs-lookup"><span data-stu-id="a0540-128">-PoolId</span></span>
<span data-ttu-id="a0540-129">Określa identyfikator puli zawierającej węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="a0540-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="a0540-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="a0540-130">-ReimageOption</span></span>
<span data-ttu-id="a0540-131">Określa, kiedy ponownie zaimportować węzeł i co zrobić z obecnie uruchomionymi zadaniami.</span><span class="sxs-lookup"><span data-stu-id="a0540-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="a0540-132">Ustawieniem domyślnym jest kolejkowanie ponowne.</span><span class="sxs-lookup"><span data-stu-id="a0540-132">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeReimageOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0540-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0540-133">CommonParameters</span></span>
<span data-ttu-id="a0540-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0540-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0540-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0540-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0540-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0540-136">INPUTS</span></span>

### <span data-ttu-id="a0540-137">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="a0540-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="a0540-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a0540-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a0540-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a0540-139">OUTPUTS</span></span>

### <span data-ttu-id="a0540-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="a0540-140">System.Void</span></span>

## <span data-ttu-id="a0540-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a0540-141">NOTES</span></span>

## <span data-ttu-id="a0540-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0540-142">RELATED LINKS</span></span>

[<span data-ttu-id="a0540-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a0540-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="a0540-144">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a0540-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="a0540-145">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a0540-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
