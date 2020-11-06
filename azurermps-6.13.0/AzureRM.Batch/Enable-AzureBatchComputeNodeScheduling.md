---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: e00a1a923afdd8a851416e872028a30ce1e04a55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547603"
---
# <span data-ttu-id="25fba-101">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="25fba-101">Enable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="25fba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25fba-102">SYNOPSIS</span></span>
<span data-ttu-id="25fba-103">Umożliwia planowanie zadań w określonym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="25fba-103">Enables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25fba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25fba-104">SYNTAX</span></span>

### <span data-ttu-id="25fba-105">Identyfikator (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="25fba-105">Id (Default)</span></span>
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25fba-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="25fba-106">InputObject</span></span>
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25fba-107">Opis</span><span class="sxs-lookup"><span data-stu-id="25fba-107">DESCRIPTION</span></span>
<span data-ttu-id="25fba-108">Polecenie cmdlet **enable-AzureBatchComputeNodeScheduling** umożliwia planowanie zadań w określonym węźle COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="25fba-108">The **Enable-AzureBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="25fba-109">Węzeł obliczeniowy to maszyna wirtualna platformy Azure przeznaczona do konkretnego obciążenia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="25fba-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="25fba-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25fba-110">EXAMPLES</span></span>

### <span data-ttu-id="25fba-111">Przykład 1: Włączanie planowania zadań w węźle obliczeniowym</span><span class="sxs-lookup"><span data-stu-id="25fba-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="25fba-112">Te polecenia umożliwiają planowanie zadań na węźle obliczeniowym TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="25fba-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="25fba-113">W tym celu pierwszym poleceniem w przykładzie jest tworzenie odwołania do obiektu zawierającego klucze konta dla konta wsadowego contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="25fba-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="25fba-114">Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $context.</span><span class="sxs-lookup"><span data-stu-id="25fba-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="25fba-115">Drugie polecenie korzysta z tego odwołania do obiektu i polecenia cmdlet **enable-AzureBatchComputeNodeScheduling** w celu nawiązania połączenia z pulą moja Pula i włączenia planowania zadań w witrynie TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="25fba-115">The second command then uses this object reference and the **Enable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="25fba-116">Przykład 2: Włączanie planowania zadań w węzłach obliczeniowych w puli</span><span class="sxs-lookup"><span data-stu-id="25fba-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="25fba-117">Te polecenia umożliwiają planowanie zadań na wszystkich węzłach obliczeniowych znajdujących się w puli Pool06.</span><span class="sxs-lookup"><span data-stu-id="25fba-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="25fba-118">Aby wykonać to zadanie, pierwsze polecenie w przykładzie powoduje utworzenie odwołania do obiektu zawierającego klucze konta dla konta wsadowego contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="25fba-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="25fba-119">Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $context.</span><span class="sxs-lookup"><span data-stu-id="25fba-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="25fba-120">Drugie polecenie w przykładzie używa tego odwołania do obiektu i funkcji **Get-AzureBatchComputeNode** , aby zwrócić kolekcję wszystkich węzłów obliczeniowych znalezionych w Pool06.</span><span class="sxs-lookup"><span data-stu-id="25fba-120">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="25fba-121">Ta kolekcja jest następnie **przestawna do polecenia cmdlet Enable-AzureBatchComputeNodeScheduling** , które umożliwia planowanie zadań w poszczególnych węzłach obliczeniowych w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="25fba-121">That collection is then piped to the **Enable-AzureBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="25fba-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25fba-122">PARAMETERS</span></span>

### <span data-ttu-id="25fba-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="25fba-123">-BatchContext</span></span>
<span data-ttu-id="25fba-124">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="25fba-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="25fba-125">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="25fba-125">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="25fba-126">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="25fba-126">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="25fba-127">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="25fba-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="25fba-128">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="25fba-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="25fba-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="25fba-129">-ComputeNode</span></span>
<span data-ttu-id="25fba-130">Określa odwołanie obiektu do węzła obliczeniowego, w którym jest włączone planowanie zadań.</span><span class="sxs-lookup"><span data-stu-id="25fba-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="25fba-131">Odwołanie do obiektu jest tworzone przy użyciu polecenia cmdlet Get-AzureBatchComputeNode i przechowywania zwróconego obiektu węzła obliczeniowego w zmiennej.</span><span class="sxs-lookup"><span data-stu-id="25fba-131">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="25fba-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25fba-132">-DefaultProfile</span></span>
<span data-ttu-id="25fba-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="25fba-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25fba-134">-ID</span><span class="sxs-lookup"><span data-stu-id="25fba-134">-Id</span></span>
<span data-ttu-id="25fba-135">Określa identyfikator węzła obliczeniowego, w którym jest włączone planowanie zadań.</span><span class="sxs-lookup"><span data-stu-id="25fba-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="25fba-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="25fba-136">-PoolId</span></span>
<span data-ttu-id="25fba-137">Określa identyfikator puli partii zawierającej węzeł obliczeniowy, w którym jest włączone planowanie zadań.</span><span class="sxs-lookup"><span data-stu-id="25fba-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="25fba-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25fba-138">CommonParameters</span></span>
<span data-ttu-id="25fba-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25fba-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25fba-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25fba-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25fba-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25fba-141">INPUTS</span></span>

### <span data-ttu-id="25fba-142">Microsoft.Azure.Commands.Batch. Modele. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="25fba-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="25fba-143">Parametry: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="25fba-143">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="25fba-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="25fba-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="25fba-145">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="25fba-145">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="25fba-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25fba-146">OUTPUTS</span></span>

### <span data-ttu-id="25fba-147">System. void</span><span class="sxs-lookup"><span data-stu-id="25fba-147">System.Void</span></span>

## <span data-ttu-id="25fba-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25fba-148">NOTES</span></span>

## <span data-ttu-id="25fba-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25fba-149">RELATED LINKS</span></span>

[<span data-ttu-id="25fba-150">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="25fba-150">Disable-AzureBatchComputeNodeScheduling</span></span>](./Disable-AzureBatchComputeNodeScheduling.md)


