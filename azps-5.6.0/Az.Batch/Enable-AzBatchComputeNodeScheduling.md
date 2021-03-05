---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2897a21f25ac0a91fec11d83b77c8219d12f88ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995723"
---
# <span data-ttu-id="8c6b3-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="8c6b3-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="8c6b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="8c6b3-103">Umożliwia planowanie zadań w określonym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="8c6b3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8c6b3-104">SYNTAX</span></span>

### <span data-ttu-id="8c6b3-105">Identyfikator (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8c6b3-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c6b3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8c6b3-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c6b3-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8c6b3-107">DESCRIPTION</span></span>
<span data-ttu-id="8c6b3-108">Polecenie cmdlet **Enable-AzBatchComputeNodeScheduling** umożliwia planowanie zadań w określonym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="8c6b3-109">Węzeł obliczeniowy jest maszyną wirtualną platformy Azure dedykowaną konkretnym obciążeniem aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="8c6b3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8c6b3-110">EXAMPLES</span></span>

### <span data-ttu-id="8c6b3-111">Przykład 1. Włączanie planowania zadań w węźle obliczeniowym</span><span class="sxs-lookup"><span data-stu-id="8c6b3-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="8c6b3-112">Te polecenia umożliwiają planowanie zadań w węźle obliczeniowym tvm-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="8c6b3-113">W tym celu pierwsze polecenie w tym przykładzie tworzy odwołanie do obiektu zawierające klucze konta dla konta wsadowego contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="8c6b3-114">To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $context.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="8c6b3-115">Drugie polecenie używa następnie tego odwołania do obiektu i polecenia cmdlet **Enable-AzBatchComputeNodeScheduling** w celu nawiązania połączenia z pulą myPool i włączenia planowania zadań w programie tvm-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="8c6b3-116">Przykład 2. Włączanie planowania zadań w węzłach obliczeniowych w puli</span><span class="sxs-lookup"><span data-stu-id="8c6b3-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="8c6b3-117">Te polecenia umożliwiają planowanie zadań we wszystkich węzłach obliczeniowych w puli Pula06.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="8c6b3-118">Aby wykonać to zadanie, pierwsze polecenie w tym przykładzie tworzy odwołanie do obiektu zawierające klucze konta dla konta wsadowego contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="8c6b3-119">To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $context.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="8c6b3-120">Drugie polecenie w tym przykładzie używa następnie tego odwołania do obiektu i polecenia **Get-AzBatchComputeNode** w celu zwrócenia kolekcji wszystkich węzłów obliczeniowych znalezionych w pool06.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="8c6b3-121">Ta kolekcja jest następnie przekierowyowana potokowo do polecenia cmdlet **Enable-AzBatchComputeNodeScheduling,** które umożliwia planowanie zadań w każdym węźle obliczeniowym w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="8c6b3-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c6b3-122">PARAMETERS</span></span>

### <span data-ttu-id="8c6b3-123">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="8c6b3-123">-BatchContext</span></span>
<span data-ttu-id="8c6b3-124">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8c6b3-125">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8c6b3-126">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-126">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8c6b3-127">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8c6b3-128">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8c6b3-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="8c6b3-129">-ComputeNode</span></span>
<span data-ttu-id="8c6b3-130">Określa odwołanie do obiektu do węzła obliczeniowego, w którym jest włączone planowanie zadań.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="8c6b3-131">To odwołanie do obiektu jest tworzone przy użyciu Get-AzBatchComputeNode cmdlet i przechowywania zwróconego obiektu węzła obliczeniowego w zmiennej.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="8c6b3-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c6b3-132">-DefaultProfile</span></span>
<span data-ttu-id="8c6b3-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c6b3-134">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="8c6b3-134">-Id</span></span>
<span data-ttu-id="8c6b3-135">Określa identyfikator węzła obliczeniowego, w którym jest włączone planowanie zadań.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="8c6b3-136">- PoolId</span><span class="sxs-lookup"><span data-stu-id="8c6b3-136">-PoolId</span></span>
<span data-ttu-id="8c6b3-137">Określa identyfikator puli partii zawierającej węzeł obliczeniowy, w którym jest włączone planowanie zadań.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="8c6b3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c6b3-138">CommonParameters</span></span>
<span data-ttu-id="8c6b3-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c6b3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c6b3-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c6b3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c6b3-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c6b3-141">INPUTS</span></span>

### <span data-ttu-id="8c6b3-142">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="8c6b3-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="8c6b3-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8c6b3-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8c6b3-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c6b3-144">OUTPUTS</span></span>

### <span data-ttu-id="8c6b3-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="8c6b3-145">System.Void</span></span>

## <span data-ttu-id="8c6b3-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8c6b3-146">NOTES</span></span>

## <span data-ttu-id="8c6b3-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c6b3-147">RELATED LINKS</span></span>

[<span data-ttu-id="8c6b3-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="8c6b3-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)


