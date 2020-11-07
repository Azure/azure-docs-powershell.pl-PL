---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: 530db3d911d0300e1bd587cd953fb357ca810c9c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710798"
---
# <span data-ttu-id="a69eb-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a69eb-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="a69eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a69eb-102">SYNOPSIS</span></span>
<span data-ttu-id="a69eb-103">Ponownie instaluje system operacyjny w określonym węźle COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="a69eb-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="a69eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a69eb-104">SYNTAX</span></span>

### <span data-ttu-id="a69eb-105">Identyfikator (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a69eb-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a69eb-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="a69eb-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a69eb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a69eb-107">DESCRIPTION</span></span>
<span data-ttu-id="a69eb-108">Polecenie cmdlet **Reset-AzBatchComputeNode** umożliwia ponowne zainstalowanie systemu operacyjnego w określonym węźle COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="a69eb-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="a69eb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a69eb-109">EXAMPLES</span></span>

### <span data-ttu-id="a69eb-110">Przykład 1: odobrazowanie węzła</span><span class="sxs-lookup"><span data-stu-id="a69eb-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="a69eb-111">To polecenie powoduje ponowne zdjęcie węzła obliczeniowego z IDENTYFIKATORem "TVM-3257026573_2-20150813t200938z" w puli o nazwie Moja Pula.</span><span class="sxs-lookup"><span data-stu-id="a69eb-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="a69eb-112">Użyj polecenia cmdlet Get-AzBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="a69eb-112">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a69eb-113">Przykład 2: odtworzenie obrazu na wszystkich węzłach w puli</span><span class="sxs-lookup"><span data-stu-id="a69eb-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="a69eb-114">To polecenie powoduje ponowne zdjęcie każdego węzła obliczeniowego w puli o nazwie Moja Pula.</span><span class="sxs-lookup"><span data-stu-id="a69eb-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="a69eb-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a69eb-115">PARAMETERS</span></span>

### <span data-ttu-id="a69eb-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a69eb-116">-BatchContext</span></span>
<span data-ttu-id="a69eb-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a69eb-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a69eb-118">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a69eb-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a69eb-119">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="a69eb-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a69eb-120">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="a69eb-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a69eb-121">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a69eb-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a69eb-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="a69eb-122">-ComputeNode</span></span>
<span data-ttu-id="a69eb-123">Określa obiekt **PSComputeNode** reprezentujący węzeł obliczeniowy, który ma zostać ponownie utworzony.</span><span class="sxs-lookup"><span data-stu-id="a69eb-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="a69eb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a69eb-124">-DefaultProfile</span></span>
<span data-ttu-id="a69eb-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a69eb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a69eb-126">-ID</span><span class="sxs-lookup"><span data-stu-id="a69eb-126">-Id</span></span>
<span data-ttu-id="a69eb-127">Określa identyfikator węzła obliczeniowego do odobrazowania.</span><span class="sxs-lookup"><span data-stu-id="a69eb-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="a69eb-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="a69eb-128">-PoolId</span></span>
<span data-ttu-id="a69eb-129">Określa identyfikator puli zawierającej węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="a69eb-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="a69eb-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="a69eb-130">-ReimageOption</span></span>
<span data-ttu-id="a69eb-131">Określa, kiedy należy przeobrazować węzeł i co zrobić z uruchomionymi obecnie zadaniami.</span><span class="sxs-lookup"><span data-stu-id="a69eb-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="a69eb-132">Wartość domyślna to requeued.</span><span class="sxs-lookup"><span data-stu-id="a69eb-132">The default is Requeue.</span></span>

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

### <span data-ttu-id="a69eb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a69eb-133">CommonParameters</span></span>
<span data-ttu-id="a69eb-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a69eb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a69eb-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a69eb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a69eb-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a69eb-136">INPUTS</span></span>

### <span data-ttu-id="a69eb-137">Microsoft.Azure.Commands.Batch. Modele. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="a69eb-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="a69eb-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a69eb-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a69eb-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a69eb-139">OUTPUTS</span></span>

### <span data-ttu-id="a69eb-140">System. void</span><span class="sxs-lookup"><span data-stu-id="a69eb-140">System.Void</span></span>

## <span data-ttu-id="a69eb-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a69eb-141">NOTES</span></span>

## <span data-ttu-id="a69eb-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a69eb-142">RELATED LINKS</span></span>

[<span data-ttu-id="a69eb-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a69eb-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="a69eb-144">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a69eb-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="a69eb-145">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="a69eb-145">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


