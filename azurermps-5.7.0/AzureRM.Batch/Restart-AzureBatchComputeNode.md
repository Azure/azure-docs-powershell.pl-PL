---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/restart-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: 5f32963630769dc25ed62f47d93fe47e56abda91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544543"
---
# <span data-ttu-id="aac7b-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="aac7b-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="aac7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aac7b-102">SYNOPSIS</span></span>
<span data-ttu-id="aac7b-103">Ponowna rozruch określonego węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="aac7b-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aac7b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aac7b-104">SYNTAX</span></span>

### <span data-ttu-id="aac7b-105">Identyfikator (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="aac7b-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aac7b-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="aac7b-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aac7b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="aac7b-107">DESCRIPTION</span></span>
<span data-ttu-id="aac7b-108">Polecenie cmdlet **restart-AzureBatchComputeNode** powoduje ponowne uruchomienie określonego węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="aac7b-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="aac7b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aac7b-109">EXAMPLES</span></span>

### <span data-ttu-id="aac7b-110">Przykład 1: ponowne uruchamianie węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="aac7b-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="aac7b-111">To polecenie powoduje ponowne uruchomienie węzła obliczeniowego z IDENTYFIKATORem "TVM-3257026573_2-20150813t200938z" w puli moja Pula.</span><span class="sxs-lookup"><span data-stu-id="aac7b-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="aac7b-112">Przykład 2: ponowne uruchamianie każdego węzła obliczeniowego w puli</span><span class="sxs-lookup"><span data-stu-id="aac7b-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="aac7b-113">To polecenie wykonuje ponownie rozruch każdego węzła obliczeniowego w puli moja Pula.</span><span class="sxs-lookup"><span data-stu-id="aac7b-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="aac7b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aac7b-114">PARAMETERS</span></span>

### <span data-ttu-id="aac7b-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="aac7b-115">-BatchContext</span></span>
<span data-ttu-id="aac7b-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="aac7b-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="aac7b-117">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="aac7b-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="aac7b-118">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="aac7b-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="aac7b-119">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="aac7b-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="aac7b-120">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="aac7b-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aac7b-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="aac7b-121">-ComputeNode</span></span>
<span data-ttu-id="aac7b-122">Określa obiekt **PSComputeNode** reprezentujący węzeł obliczeniowy, który ma zostać ponownie uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="aac7b-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aac7b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac7b-123">-DefaultProfile</span></span>
<span data-ttu-id="aac7b-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aac7b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac7b-125">-ID</span><span class="sxs-lookup"><span data-stu-id="aac7b-125">-Id</span></span>
<span data-ttu-id="aac7b-126">Określa identyfikator węzła obliczeniowego do ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="aac7b-126">Specifies the ID of the compute node to reboot.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac7b-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="aac7b-127">-PoolId</span></span>
<span data-ttu-id="aac7b-128">Określa identyfikator puli zawierającej węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="aac7b-128">Specifies the ID of the pool that contains the compute node.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac7b-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="aac7b-129">-RebootOption</span></span>
<span data-ttu-id="aac7b-130">Określa, kiedy należy ponownie uruchomić węzeł i co należy zrobić z uruchomionymi obecnie zadaniami.</span><span class="sxs-lookup"><span data-stu-id="aac7b-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="aac7b-131">Wartość domyślna to requeued.</span><span class="sxs-lookup"><span data-stu-id="aac7b-131">The default is Requeue.</span></span>

```yaml
Type: ComputeNodeRebootOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac7b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac7b-132">CommonParameters</span></span>
<span data-ttu-id="aac7b-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aac7b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac7b-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aac7b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac7b-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aac7b-135">INPUTS</span></span>

### <span data-ttu-id="aac7b-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="aac7b-136">BatchAccountContext</span></span>
<span data-ttu-id="aac7b-137">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="aac7b-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="aac7b-138">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="aac7b-138">PSComputeNode</span></span>
<span data-ttu-id="aac7b-139">Parametr "ComputeNode" akceptuje wartość typu "PSComputeNode" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="aac7b-139">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="aac7b-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aac7b-140">OUTPUTS</span></span>

## <span data-ttu-id="aac7b-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aac7b-141">NOTES</span></span>

## <span data-ttu-id="aac7b-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aac7b-142">RELATED LINKS</span></span>

[<span data-ttu-id="aac7b-143">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="aac7b-143">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="aac7b-144">Resetowanie — AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="aac7b-144">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="aac7b-145">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="aac7b-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


