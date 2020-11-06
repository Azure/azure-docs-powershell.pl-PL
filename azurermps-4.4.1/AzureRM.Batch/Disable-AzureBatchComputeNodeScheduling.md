---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 778347394e9793b95434e1b308bbdb4e28fc0915
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551943"
---
# <span data-ttu-id="b8d15-101">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="b8d15-101">Disable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="b8d15-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8d15-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d15-103">Wyłącza planowanie zadań w określonym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="b8d15-103">Disables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8d15-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8d15-104">SYNTAX</span></span>

### <span data-ttu-id="b8d15-105">Identyfikator (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b8d15-105">Id (Default)</span></span>
```
Disable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8d15-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="b8d15-106">InputObject</span></span>
```
Disable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8d15-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b8d15-107">DESCRIPTION</span></span>
<span data-ttu-id="b8d15-108">Polecenie cmdlet **disable-AzureBatchComputeNodeScheduling** wyłącza planowanie zadań w określonym węźle COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="b8d15-108">The **Disable-AzureBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="b8d15-109">Węzeł obliczeniowy to maszyna wirtualna platformy Azure przeznaczona do konkretnego obciążenia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b8d15-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="b8d15-110">Po wyłączeniu planowania zadań w węźle obliczeniowym dostępna jest również opcja określająca, co należy zrobić w kolejce zadań węzła.</span><span class="sxs-lookup"><span data-stu-id="b8d15-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="b8d15-111">**Disable-AzureBatchComputeNodeScheduling** umożliwia wykonywanie następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="b8d15-111">**Disable-AzureBatchComputeNodeScheduling** lets you do the following:</span></span> 

- <span data-ttu-id="b8d15-112">Zakończ zadania i umieść je z powrotem w kolejce zadań.</span><span class="sxs-lookup"><span data-stu-id="b8d15-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="b8d15-113">Dzięki temu zadania mogą być ponownie planowane w innym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="b8d15-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="b8d15-114">Kończenie zadań i usuwanie ich z kolejki zadań.</span><span class="sxs-lookup"><span data-stu-id="b8d15-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="b8d15-115">Zadania zatrzymane w ten sposób nie będą ponownie planowane.</span><span class="sxs-lookup"><span data-stu-id="b8d15-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="b8d15-116">Poczekaj na ukończenie wszystkich zadań, które są obecnie wykonywane, a następnie wyłącz planowanie zadań w węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="b8d15-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="b8d15-117">Poczekaj na ukończenie wszystkich uruchomionych zadań, a wszystkie okresy przechowywania danych wygasną, a następnie wyłącz planowanie zadań w węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="b8d15-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="b8d15-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8d15-118">EXAMPLES</span></span>

### <span data-ttu-id="b8d15-119">Przykład 1. wyłączenie planowania zadań w węźle obliczeniowym</span><span class="sxs-lookup"><span data-stu-id="b8d15-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Disable-AzureBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="b8d15-120">Te polecenia wyłączają harmonogram zadań na węźle obliczeniowym TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="b8d15-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="b8d15-121">W tym celu pierwszym poleceniem w przykładzie jest tworzenie odwołania do obiektu dla kluczy konta dla konta wsadowego contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="b8d15-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="b8d15-122">Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $context.</span><span class="sxs-lookup"><span data-stu-id="b8d15-122">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="b8d15-123">Drugie polecenie korzysta z tego odwołania do obiektu i polecenia cmdlet **disable-AzureBatchComputeNodeScheduling** , aby połączyć się z pulą moja Pula i wyłączyć planowanie zadań w węźle TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="b8d15-123">The second command then uses this object reference and the **Disable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>

<span data-ttu-id="b8d15-124">Ponieważ parametr *DisableComputeNodeSchedulingOptions* nie został uwzględniony, żadne zadania obecnie uruchomione w węźle obliczeniowym zostaną ponownie przekolejkowane.</span><span class="sxs-lookup"><span data-stu-id="b8d15-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="b8d15-125">Przykład 2: wyłączenie planowania zadań we wszystkich węzłach obliczeniowych w puli</span><span class="sxs-lookup"><span data-stu-id="b8d15-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzureBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="b8d15-126">Te polecenia wyłączają planowanie zadań na wszystkich węzłach komputerów w Pool06 puli partii.</span><span class="sxs-lookup"><span data-stu-id="b8d15-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="b8d15-127">Aby wykonać to zadanie, pierwsze polecenie w przykładzie powoduje utworzenie odwołania do obiektu dla kluczy konta dla konta wsadowego contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="b8d15-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="b8d15-128">Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $context.</span><span class="sxs-lookup"><span data-stu-id="b8d15-128">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="b8d15-129">Drugie polecenie w przykładzie używa tego odwołania do obiektu i funkcji **Get-AzureBatchComputeNode** , aby zwrócić kolekcję wszystkich węzłów obliczeniowych znalezionych w Pool06.</span><span class="sxs-lookup"><span data-stu-id="b8d15-129">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="b8d15-130">Ta kolekcja jest następnie **przełączana do polecenia cmdlet Disable-AzureBatchComputeNodeScheduling** , aby wyłączyć planowanie zadań w każdym węźle obliczeniowym w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="b8d15-130">That collection is then piped to then **Disable-AzureBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>

<span data-ttu-id="b8d15-131">Ponieważ parametr *DisableComputeNodeSchedulingOptions* nie został uwzględniony, żadne zadania obecnie uruchomione w węzłach obliczeniowych zostaną ponownie przekolejkowane.</span><span class="sxs-lookup"><span data-stu-id="b8d15-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="b8d15-132">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8d15-132">PARAMETERS</span></span>

### <span data-ttu-id="b8d15-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b8d15-133">-BatchContext</span></span>
<span data-ttu-id="b8d15-134">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="b8d15-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b8d15-135">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="b8d15-135">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b8d15-136">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="b8d15-136">-ComputeNode</span></span>
<span data-ttu-id="b8d15-137">Określa odwołanie obiektu do węzła obliczeniowego, w którym jest wyłączone planowanie zadań.</span><span class="sxs-lookup"><span data-stu-id="b8d15-137">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="b8d15-138">Odwołanie do obiektu jest tworzone przy użyciu polecenia cmdlet Get-AzureBatchComputeNode i przechowywania zwróconego obiektu węzła obliczeniowego w zmiennej.</span><span class="sxs-lookup"><span data-stu-id="b8d15-138">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="b8d15-139">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="b8d15-139">-DisableSchedulingOption</span></span>
<span data-ttu-id="b8d15-140">Określa, jak to polecenie cmdlet dotyczy wszystkich zadań uruchomionych obecnie w węźle komputera, na którym jest wyłączone planowanie.</span><span class="sxs-lookup"><span data-stu-id="b8d15-140">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="b8d15-141">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b8d15-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8d15-142">Przekolejkowanie.</span><span class="sxs-lookup"><span data-stu-id="b8d15-142">Requeue.</span></span>
<span data-ttu-id="b8d15-143">Zadania zostaną natychmiast zatrzymane i zwrócone do kolejki zadań.</span><span class="sxs-lookup"><span data-stu-id="b8d15-143">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="b8d15-144">Umożliwia to ponowne planowanie zadań w innym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="b8d15-144">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="b8d15-145">Jest to wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="b8d15-145">This is the default value.</span></span> 
- <span data-ttu-id="b8d15-146">Zakończyć.</span><span class="sxs-lookup"><span data-stu-id="b8d15-146">Terminate.</span></span>
<span data-ttu-id="b8d15-147">Zadania są natychmiast przetrzymywane i usuwane z kolejki zadań.</span><span class="sxs-lookup"><span data-stu-id="b8d15-147">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="b8d15-148">Te zadania nie zostaną zaplanowane ponownie.</span><span class="sxs-lookup"><span data-stu-id="b8d15-148">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="b8d15-149">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="b8d15-149">TaskCompletion.</span></span>
<span data-ttu-id="b8d15-150">Obecnie uruchomione zadania będą mogły zostać ukończone przed wyłączeniem planowania zadań w węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="b8d15-150">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="b8d15-151">Żadne nowe zadania nie będą planowane w tym węźle.</span><span class="sxs-lookup"><span data-stu-id="b8d15-151">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="b8d15-152">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="b8d15-152">RetainedData.</span></span>
<span data-ttu-id="b8d15-153">Obecnie uruchomione zadania będą mogły zostać ukończone, a okres przechowywania danych będzie mógł wygasnąć, zanim planowanie zadań zostanie wyłączone w węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="b8d15-153">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="b8d15-154">Żadne nowe zadania nie będą planowane w tym węźle.</span><span class="sxs-lookup"><span data-stu-id="b8d15-154">No new tasks will be scheduled on this node.</span></span>

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

### <span data-ttu-id="b8d15-155">-ID</span><span class="sxs-lookup"><span data-stu-id="b8d15-155">-Id</span></span>
<span data-ttu-id="b8d15-156">Określa identyfikator węzła obliczeniowego, w którym jest wyłączone planowanie zadań.</span><span class="sxs-lookup"><span data-stu-id="b8d15-156">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="b8d15-157">-PoolId</span><span class="sxs-lookup"><span data-stu-id="b8d15-157">-PoolId</span></span>
<span data-ttu-id="b8d15-158">Określa identyfikator puli partii zawierającej węzeł obliczeniowy, w którym jest wyłączone planowanie zadań.</span><span class="sxs-lookup"><span data-stu-id="b8d15-158">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>

<span data-ttu-id="b8d15-159">Jeśli używasz parametru *PoolId* , nie używaj parametru *ComputeNode* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="b8d15-159">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="b8d15-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d15-160">-DefaultProfile</span></span>
<span data-ttu-id="b8d15-161">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d15-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8d15-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d15-162">CommonParameters</span></span>
<span data-ttu-id="b8d15-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8d15-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d15-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8d15-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d15-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8d15-165">INPUTS</span></span>

### <span data-ttu-id="b8d15-166">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b8d15-166">BatchAccountContext</span></span>
<span data-ttu-id="b8d15-167">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="b8d15-167">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b8d15-168">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="b8d15-168">PSComputeNode</span></span>
<span data-ttu-id="b8d15-169">Parametr "ComputeNode" akceptuje wartość typu "PSComputeNode" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="b8d15-169">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="b8d15-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8d15-170">OUTPUTS</span></span>

## <span data-ttu-id="b8d15-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8d15-171">NOTES</span></span>

## <span data-ttu-id="b8d15-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8d15-172">RELATED LINKS</span></span>

[<span data-ttu-id="b8d15-173">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b8d15-173">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b8d15-174">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="b8d15-174">Enable-AzureBatchComputeNodeScheduling</span></span>](./Enable-AzureBatchComputeNodeScheduling.md)


