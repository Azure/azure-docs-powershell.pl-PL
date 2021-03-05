---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: c6ad25e5c6ba327ddcd5b4877cbac39937ec4feb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985356"
---
# <span data-ttu-id="901e1-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="901e1-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="901e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="901e1-102">SYNOPSIS</span></span>
<span data-ttu-id="901e1-103">Ponowne instalowanie systemu operacyjnego w określonym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="901e1-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="901e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="901e1-104">SYNTAX</span></span>

### <span data-ttu-id="901e1-105">Identyfikator (domyślne)</span><span class="sxs-lookup"><span data-stu-id="901e1-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="901e1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="901e1-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="901e1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="901e1-107">DESCRIPTION</span></span>
<span data-ttu-id="901e1-108">Polecenie cmdlet **Reset-AzBatchComputeNode** ponownie instaluje system operacyjny w określonym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="901e1-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="901e1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="901e1-109">EXAMPLES</span></span>

### <span data-ttu-id="901e1-110">Przykład 1. Ponowne zaimportowanie węzła</span><span class="sxs-lookup"><span data-stu-id="901e1-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="901e1-111">To polecenie ponownie oblicza węzeł obliczeniowy o identyfikatorze "tvm-3257026573_2-20150813t200938z" w puli o nazwie MyPool.</span><span class="sxs-lookup"><span data-stu-id="901e1-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="901e1-112">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="901e1-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="901e1-113">Przykład 2. Ponowne zaimportowanie wszystkich węzłów w puli</span><span class="sxs-lookup"><span data-stu-id="901e1-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="901e1-114">To polecenie ponownie oblicza każdy węzeł obliczeniowy w puli o nazwie MyPool.</span><span class="sxs-lookup"><span data-stu-id="901e1-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="901e1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="901e1-115">PARAMETERS</span></span>

### <span data-ttu-id="901e1-116">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="901e1-116">-BatchContext</span></span>
<span data-ttu-id="901e1-117">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="901e1-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="901e1-118">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="901e1-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="901e1-119">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="901e1-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="901e1-120">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="901e1-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="901e1-121">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="901e1-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="901e1-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="901e1-122">-ComputeNode</span></span>
<span data-ttu-id="901e1-123">Określa obiekt **PSComputeNode** reprezentujący węzeł obliczeniowy do ponownego zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="901e1-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="901e1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="901e1-124">-DefaultProfile</span></span>
<span data-ttu-id="901e1-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="901e1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="901e1-126">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="901e1-126">-Id</span></span>
<span data-ttu-id="901e1-127">Określa identyfikator węzła obliczeniowego do ponownego zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="901e1-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="901e1-128">- PoolId</span><span class="sxs-lookup"><span data-stu-id="901e1-128">-PoolId</span></span>
<span data-ttu-id="901e1-129">Określa identyfikator puli zawierającej węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="901e1-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="901e1-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="901e1-130">-ReimageOption</span></span>
<span data-ttu-id="901e1-131">Określa, kiedy ponownie zaimportować węzeł i co zrobić z obecnie uruchomionymi zadaniami.</span><span class="sxs-lookup"><span data-stu-id="901e1-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="901e1-132">Ustawieniem domyślnym jest kolejkowanie ponowne.</span><span class="sxs-lookup"><span data-stu-id="901e1-132">The default is Requeue.</span></span>

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

### <span data-ttu-id="901e1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="901e1-133">CommonParameters</span></span>
<span data-ttu-id="901e1-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="901e1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="901e1-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="901e1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="901e1-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="901e1-136">INPUTS</span></span>

### <span data-ttu-id="901e1-137">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="901e1-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="901e1-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="901e1-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="901e1-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="901e1-139">OUTPUTS</span></span>

### <span data-ttu-id="901e1-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="901e1-140">System.Void</span></span>

## <span data-ttu-id="901e1-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="901e1-141">NOTES</span></span>

## <span data-ttu-id="901e1-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="901e1-142">RELATED LINKS</span></span>

[<span data-ttu-id="901e1-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="901e1-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="901e1-144">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="901e1-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="901e1-145">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="901e1-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
