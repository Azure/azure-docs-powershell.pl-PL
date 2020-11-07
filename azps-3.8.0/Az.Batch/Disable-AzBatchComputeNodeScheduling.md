---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895461"
---
# <span data-ttu-id="021fe-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="021fe-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="021fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="021fe-102">SYNOPSIS</span></span>
<span data-ttu-id="021fe-103">Wyłącza planowanie zadań w określonym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="021fe-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="021fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="021fe-104">SYNTAX</span></span>

### <span data-ttu-id="021fe-105">Identyfikator (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="021fe-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="021fe-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="021fe-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="021fe-107">Opis</span><span class="sxs-lookup"><span data-stu-id="021fe-107">DESCRIPTION</span></span>
<span data-ttu-id="021fe-108">Polecenie cmdlet **disable-AzBatchComputeNodeScheduling** wyłącza planowanie zadań w określonym węźle COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="021fe-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="021fe-109">Węzeł obliczeniowy to maszyna wirtualna platformy Azure przeznaczona do konkretnego obciążenia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="021fe-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="021fe-110">Po wyłączeniu planowania zadań w węźle obliczeniowym dostępna jest również opcja określająca, co należy zrobić w kolejce zadań węzła.</span><span class="sxs-lookup"><span data-stu-id="021fe-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="021fe-111">**Disable-AzBatchComputeNodeScheduling** umożliwia wykonywanie następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="021fe-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="021fe-112">Zakończ zadania i umieść je z powrotem w kolejce zadań.</span><span class="sxs-lookup"><span data-stu-id="021fe-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="021fe-113">Dzięki temu zadania mogą być ponownie planowane w innym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="021fe-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="021fe-114">Kończenie zadań i usuwanie ich z kolejki zadań.</span><span class="sxs-lookup"><span data-stu-id="021fe-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="021fe-115">Zadania zatrzymane w ten sposób nie będą ponownie planowane.</span><span class="sxs-lookup"><span data-stu-id="021fe-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="021fe-116">Poczekaj na ukończenie wszystkich zadań, które są obecnie wykonywane, a następnie wyłącz planowanie zadań w węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="021fe-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="021fe-117">Poczekaj na ukończenie wszystkich uruchomionych zadań, a wszystkie okresy przechowywania danych wygasną, a następnie wyłącz planowanie zadań w węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="021fe-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="021fe-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="021fe-118">EXAMPLES</span></span>

### <span data-ttu-id="021fe-119">Przykład 1. wyłączenie planowania zadań w węźle obliczeniowym</span><span class="sxs-lookup"><span data-stu-id="021fe-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="021fe-120">Te polecenia wyłączają harmonogram zadań na węźle obliczeniowym TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="021fe-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="021fe-121">W tym celu pierwszym poleceniem w przykładzie jest tworzenie odwołania do obiektu dla kluczy konta dla konta wsadowego contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="021fe-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="021fe-122">Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $context.</span><span class="sxs-lookup"><span data-stu-id="021fe-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="021fe-123">Drugie polecenie korzysta z tego odwołania do obiektu i polecenia cmdlet **disable-AzBatchComputeNodeScheduling** , aby połączyć się z pulą moja Pula i wyłączyć planowanie zadań w węźle TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="021fe-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="021fe-124">Ponieważ parametr *DisableComputeNodeSchedulingOptions* nie został uwzględniony, żadne zadania obecnie uruchomione w węźle obliczeniowym zostaną ponownie przekolejkowane.</span><span class="sxs-lookup"><span data-stu-id="021fe-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="021fe-125">Przykład 2: wyłączenie planowania zadań we wszystkich węzłach obliczeniowych w puli</span><span class="sxs-lookup"><span data-stu-id="021fe-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="021fe-126">Te polecenia wyłączają planowanie zadań na wszystkich węzłach komputerów w Pool06 puli partii.</span><span class="sxs-lookup"><span data-stu-id="021fe-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="021fe-127">Aby wykonać to zadanie, pierwsze polecenie w przykładzie powoduje utworzenie odwołania do obiektu dla kluczy konta dla konta wsadowego contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="021fe-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="021fe-128">Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $context.</span><span class="sxs-lookup"><span data-stu-id="021fe-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="021fe-129">Drugie polecenie w przykładzie używa tego odwołania do obiektu i funkcji **Get-AzBatchComputeNode** , aby zwrócić kolekcję wszystkich węzłów obliczeniowych znalezionych w Pool06.</span><span class="sxs-lookup"><span data-stu-id="021fe-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="021fe-130">Ta kolekcja jest następnie **przełączana do polecenia cmdlet Disable-AzBatchComputeNodeScheduling** , aby wyłączyć planowanie zadań w każdym węźle obliczeniowym w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="021fe-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="021fe-131">Ponieważ parametr *DisableComputeNodeSchedulingOptions* nie został uwzględniony, żadne zadania obecnie uruchomione w węzłach obliczeniowych zostaną ponownie przekolejkowane.</span><span class="sxs-lookup"><span data-stu-id="021fe-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="021fe-132">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="021fe-132">PARAMETERS</span></span>

### <span data-ttu-id="021fe-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="021fe-133">-BatchContext</span></span>
<span data-ttu-id="021fe-134">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="021fe-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="021fe-135">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="021fe-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="021fe-136">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="021fe-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="021fe-137">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="021fe-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="021fe-138">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="021fe-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="021fe-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="021fe-139">-ComputeNode</span></span>
<span data-ttu-id="021fe-140">Określa odwołanie obiektu do węzła obliczeniowego, w którym jest wyłączone planowanie zadań.</span><span class="sxs-lookup"><span data-stu-id="021fe-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="021fe-141">Odwołanie do obiektu jest tworzone przy użyciu polecenia cmdlet Get-AzBatchComputeNode i przechowywania zwróconego obiektu węzła obliczeniowego w zmiennej.</span><span class="sxs-lookup"><span data-stu-id="021fe-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="021fe-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="021fe-142">-DefaultProfile</span></span>
<span data-ttu-id="021fe-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="021fe-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="021fe-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="021fe-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="021fe-145">Określa, jak to polecenie cmdlet dotyczy wszystkich zadań uruchomionych obecnie w węźle komputera, na którym jest wyłączone planowanie.</span><span class="sxs-lookup"><span data-stu-id="021fe-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="021fe-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="021fe-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="021fe-147">Przekolejkowanie.</span><span class="sxs-lookup"><span data-stu-id="021fe-147">Requeue.</span></span>
<span data-ttu-id="021fe-148">Zadania zostaną natychmiast zatrzymane i zwrócone do kolejki zadań.</span><span class="sxs-lookup"><span data-stu-id="021fe-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="021fe-149">Umożliwia to ponowne planowanie zadań w innym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="021fe-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="021fe-150">Jest to wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="021fe-150">This is the default value.</span></span> 
- <span data-ttu-id="021fe-151">Zakończyć.</span><span class="sxs-lookup"><span data-stu-id="021fe-151">Terminate.</span></span>
<span data-ttu-id="021fe-152">Zadania są natychmiast przetrzymywane i usuwane z kolejki zadań.</span><span class="sxs-lookup"><span data-stu-id="021fe-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="021fe-153">Te zadania nie zostaną zaplanowane ponownie.</span><span class="sxs-lookup"><span data-stu-id="021fe-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="021fe-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="021fe-154">TaskCompletion.</span></span>
<span data-ttu-id="021fe-155">Obecnie uruchomione zadania będą mogły zostać ukończone przed wyłączeniem planowania zadań w węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="021fe-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="021fe-156">Żadne nowe zadania nie będą planowane w tym węźle.</span><span class="sxs-lookup"><span data-stu-id="021fe-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="021fe-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="021fe-157">RetainedData.</span></span>
<span data-ttu-id="021fe-158">Obecnie uruchomione zadania będą mogły zostać ukończone, a okres przechowywania danych będzie mógł wygasnąć, zanim planowanie zadań zostanie wyłączone w węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="021fe-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="021fe-159">Żadne nowe zadania nie będą planowane w tym węźle.</span><span class="sxs-lookup"><span data-stu-id="021fe-159">No new tasks will be scheduled on this node.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="021fe-160">-ID</span><span class="sxs-lookup"><span data-stu-id="021fe-160">-Id</span></span>
<span data-ttu-id="021fe-161">Określa identyfikator węzła obliczeniowego, w którym jest wyłączone planowanie zadań.</span><span class="sxs-lookup"><span data-stu-id="021fe-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="021fe-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="021fe-162">-PoolId</span></span>
<span data-ttu-id="021fe-163">Określa identyfikator puli partii zawierającej węzeł obliczeniowy, w którym jest wyłączone planowanie zadań.</span><span class="sxs-lookup"><span data-stu-id="021fe-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="021fe-164">Jeśli używasz parametru *PoolId* , nie używaj parametru *ComputeNode* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="021fe-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="021fe-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="021fe-165">CommonParameters</span></span>
<span data-ttu-id="021fe-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="021fe-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="021fe-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="021fe-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="021fe-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="021fe-168">INPUTS</span></span>

### <span data-ttu-id="021fe-169">Microsoft.Azure.Commands.Batch. Modele. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="021fe-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="021fe-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="021fe-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="021fe-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="021fe-171">OUTPUTS</span></span>

### <span data-ttu-id="021fe-172">System. void</span><span class="sxs-lookup"><span data-stu-id="021fe-172">System.Void</span></span>

## <span data-ttu-id="021fe-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="021fe-173">NOTES</span></span>

## <span data-ttu-id="021fe-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="021fe-174">RELATED LINKS</span></span>

[<span data-ttu-id="021fe-175">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="021fe-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="021fe-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="021fe-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)


