---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199571"
---
# <span data-ttu-id="fa20c-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="fa20c-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="fa20c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa20c-102">SYNOPSIS</span></span>
<span data-ttu-id="fa20c-103">Wyłącza planowanie zadań w określonym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="fa20c-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="fa20c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fa20c-104">SYNTAX</span></span>

### <span data-ttu-id="fa20c-105">Identyfikator (domyślne)</span><span class="sxs-lookup"><span data-stu-id="fa20c-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa20c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fa20c-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa20c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fa20c-107">DESCRIPTION</span></span>
<span data-ttu-id="fa20c-108">Polecenie cmdlet **Disable-AzBatchComputeNodeScheduling** wyłącza planowanie zadań w określonym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="fa20c-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="fa20c-109">Węzeł obliczeniowy jest maszyną wirtualną platformy Azure dedykowaną konkretnym obciążeniem aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fa20c-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="fa20c-110">Wyłączenie planowania zadań w węźle obliczeniowym umożliwia również określenie, co należy zrobić w przypadku zadań obecnie w kolejce zadań węzła.</span><span class="sxs-lookup"><span data-stu-id="fa20c-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="fa20c-111">**Disable-AzBatchComputeNodeScheduling** umożliwia:</span><span class="sxs-lookup"><span data-stu-id="fa20c-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="fa20c-112">Zakończ zadania i umieść je z powrotem w kolejce zadań.</span><span class="sxs-lookup"><span data-stu-id="fa20c-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="fa20c-113">Dzięki temu te zadania będą ponownieplanowane w innym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="fa20c-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="fa20c-114">Zakończ zadania i usuń je z kolejki zadań.</span><span class="sxs-lookup"><span data-stu-id="fa20c-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="fa20c-115">Zadania zatrzymane w ten sposób nie będą ponownieplanowane.</span><span class="sxs-lookup"><span data-stu-id="fa20c-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="fa20c-116">Poczekaj na ukończenie wszystkich obecnie wykonywanych zadań, a następnie wyłącz planowanie zadań w węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="fa20c-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="fa20c-117">Zaczekaj na ukończenie wszystkich uruchomionych zadań i wygaśnie wszystkie okresy przechowywania danych, a następnie wyłącz planowanie zadań w węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="fa20c-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="fa20c-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fa20c-118">EXAMPLES</span></span>

### <span data-ttu-id="fa20c-119">Przykład 1. Wyłączanie planowania zadań w węźle obliczeniowym</span><span class="sxs-lookup"><span data-stu-id="fa20c-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="fa20c-120">Te polecenia wyłączyły harmonogram zadań w węźle obliczeniowym tvm-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="fa20c-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="fa20c-121">W tym celu pierwsze polecenie w tym przykładzie tworzy odwołanie obiektu do kluczy konta dla konta wsadowego contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="fa20c-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="fa20c-122">To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $context.</span><span class="sxs-lookup"><span data-stu-id="fa20c-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="fa20c-123">Drugie polecenie używa następnie tego odwołania do obiektu i polecenia cmdlet **Disable-AzBatchComputeNodeScheduling** w celu nawiązania połączenia z pulą myPool i wyłączenia planowania zadań w węźle tvm-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="fa20c-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="fa20c-124">Ponieważ parametr *DisableComputeNodeSchedulingOptions* nie został uwzględniony, żadne zadania obecnie uruchomione w węźle obliczeniowym będą przekierowywane w kolejkę.</span><span class="sxs-lookup"><span data-stu-id="fa20c-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="fa20c-125">Przykład 2. Wyłączanie planowania zadań we wszystkich węzłach obliczeniowych w puli</span><span class="sxs-lookup"><span data-stu-id="fa20c-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="fa20c-126">Te polecenia wyłączą planowanie zadań we wszystkich węzłach komputerów w puli partii (Pool06).</span><span class="sxs-lookup"><span data-stu-id="fa20c-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="fa20c-127">Aby wykonać to zadanie, pierwsze polecenie w tym przykładzie tworzy odwołanie do obiektu do kluczy konta dla konta wsadowego contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="fa20c-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="fa20c-128">To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $context.</span><span class="sxs-lookup"><span data-stu-id="fa20c-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="fa20c-129">Drugie polecenie w tym przykładzie używa następnie tego odwołania do obiektu i polecenia **Get-AzBatchComputeNode** w celu zwrócenia kolekcji wszystkich węzłów obliczeniowych znalezionych w pool06.</span><span class="sxs-lookup"><span data-stu-id="fa20c-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="fa20c-130">Ta kolekcja jest następnie przekierowyowana potokowo do polecenia cmdlet **Disable-AzBatchComputeNodeScheduling,** aby wyłączyć planowanie zadań na każdym węźle obliczeniowym w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="fa20c-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="fa20c-131">Parametr *DisableComputeNodeSchedulingOptions* nie został uwzględniony, ponieważ żadne zadania obecnie uruchomione w węzłach obliczeniowych nie będą kolejkowane.</span><span class="sxs-lookup"><span data-stu-id="fa20c-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="fa20c-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa20c-132">PARAMETERS</span></span>

### <span data-ttu-id="fa20c-133">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="fa20c-133">-BatchContext</span></span>
<span data-ttu-id="fa20c-134">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="fa20c-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fa20c-135">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fa20c-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fa20c-136">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="fa20c-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fa20c-137">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="fa20c-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fa20c-138">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="fa20c-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fa20c-139">- ComputeNode</span><span class="sxs-lookup"><span data-stu-id="fa20c-139">-ComputeNode</span></span>
<span data-ttu-id="fa20c-140">Określa odwołanie do obiektu do węzła obliczeniowego, w którym planowanie zadań jest wyłączone.</span><span class="sxs-lookup"><span data-stu-id="fa20c-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="fa20c-141">To odwołanie do obiektu jest tworzone przy użyciu Get-AzBatchComputeNode cmdlet i przechowywania zwróconego obiektu węzła obliczeniowego w zmiennej.</span><span class="sxs-lookup"><span data-stu-id="fa20c-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="fa20c-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa20c-142">-DefaultProfile</span></span>
<span data-ttu-id="fa20c-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa20c-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa20c-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="fa20c-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="fa20c-145">Określa sposób, w jaki to polecenie cmdlet obsługuje wszystkie zadania obecnie uruchomione w węźle komputera, w którym planowanie jest wyłączone.</span><span class="sxs-lookup"><span data-stu-id="fa20c-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="fa20c-146">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fa20c-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fa20c-147">Kolejkowanie ponownie.</span><span class="sxs-lookup"><span data-stu-id="fa20c-147">Requeue.</span></span>
<span data-ttu-id="fa20c-148">Zadania są natychmiast zatrzymywane i zwracane do kolejki zadań.</span><span class="sxs-lookup"><span data-stu-id="fa20c-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="fa20c-149">Dzięki temu zadania będą ponownieplanowane w innym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="fa20c-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="fa20c-150">Jest to wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="fa20c-150">This is the default value.</span></span> 
- <span data-ttu-id="fa20c-151">Zakończ.</span><span class="sxs-lookup"><span data-stu-id="fa20c-151">Terminate.</span></span>
<span data-ttu-id="fa20c-152">Zadania są natychmiast zatrzymywane i usuwane z kolejki zadań.</span><span class="sxs-lookup"><span data-stu-id="fa20c-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="fa20c-153">Te zadania nie zostaną ponownieplanowane.</span><span class="sxs-lookup"><span data-stu-id="fa20c-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="fa20c-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="fa20c-154">TaskCompletion.</span></span>
<span data-ttu-id="fa20c-155">Obecnie uruchomione zadania będą mogły zostać ukończone przed wyłączeniem planowania zadań w węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="fa20c-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="fa20c-156">W tym węźle nie będą planowane żadne nowe zadania.</span><span class="sxs-lookup"><span data-stu-id="fa20c-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="fa20c-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="fa20c-157">RetainedData.</span></span>
<span data-ttu-id="fa20c-158">Obecnie uruchomione zadania będą mogły wykonywać, a okresy przechowywania danych będą mogły wygasać przed wyłączeniem planowania zadań w węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="fa20c-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="fa20c-159">W tym węźle nie będą planowane żadne nowe zadania.</span><span class="sxs-lookup"><span data-stu-id="fa20c-159">No new tasks will be scheduled on this node.</span></span>

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

### <span data-ttu-id="fa20c-160">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="fa20c-160">-Id</span></span>
<span data-ttu-id="fa20c-161">Określa identyfikator węzła obliczeniowego, w którym planowanie zadań jest wyłączone.</span><span class="sxs-lookup"><span data-stu-id="fa20c-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="fa20c-162">- PoolId</span><span class="sxs-lookup"><span data-stu-id="fa20c-162">-PoolId</span></span>
<span data-ttu-id="fa20c-163">Określa identyfikator puli partii zawierającej węzeł obliczeniowy, w którym planowanie zadań jest wyłączone.</span><span class="sxs-lookup"><span data-stu-id="fa20c-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="fa20c-164">W przypadku użycia *parametru PoolId* nie należy używać *parametru ComputeNode* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="fa20c-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="fa20c-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa20c-165">CommonParameters</span></span>
<span data-ttu-id="fa20c-166">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa20c-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa20c-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa20c-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa20c-168">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa20c-168">INPUTS</span></span>

### <span data-ttu-id="fa20c-169">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="fa20c-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="fa20c-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fa20c-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fa20c-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fa20c-171">OUTPUTS</span></span>

### <span data-ttu-id="fa20c-172">System.Void</span><span class="sxs-lookup"><span data-stu-id="fa20c-172">System.Void</span></span>

## <span data-ttu-id="fa20c-173">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fa20c-173">NOTES</span></span>

## <span data-ttu-id="fa20c-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa20c-174">RELATED LINKS</span></span>

[<span data-ttu-id="fa20c-175">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="fa20c-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="fa20c-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="fa20c-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)


