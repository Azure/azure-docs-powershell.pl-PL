---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: eff141494c2b34622f35b687dd1803c449e8b727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550096"
---
# <span data-ttu-id="52b91-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="52b91-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="52b91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52b91-102">SYNOPSIS</span></span>
<span data-ttu-id="52b91-103">Ponowna rozruch określonego węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="52b91-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52b91-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52b91-104">SYNTAX</span></span>

### <span data-ttu-id="52b91-105">Identyfikator (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="52b91-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52b91-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="52b91-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52b91-107">Opis</span><span class="sxs-lookup"><span data-stu-id="52b91-107">DESCRIPTION</span></span>
<span data-ttu-id="52b91-108">Polecenie cmdlet **restart-AzureBatchComputeNode** powoduje ponowne uruchomienie określonego węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="52b91-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="52b91-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52b91-109">EXAMPLES</span></span>

### <span data-ttu-id="52b91-110">Przykład 1: ponowne uruchamianie węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="52b91-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="52b91-111">To polecenie powoduje ponowne uruchomienie węzła obliczeniowego z IDENTYFIKATORem "TVM-3257026573_2-20150813t200938z" w puli moja Pula.</span><span class="sxs-lookup"><span data-stu-id="52b91-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="52b91-112">Przykład 2: ponowne uruchamianie każdego węzła obliczeniowego w puli</span><span class="sxs-lookup"><span data-stu-id="52b91-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="52b91-113">To polecenie wykonuje ponownie rozruch każdego węzła obliczeniowego w puli moja Pula.</span><span class="sxs-lookup"><span data-stu-id="52b91-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="52b91-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52b91-114">PARAMETERS</span></span>

### <span data-ttu-id="52b91-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="52b91-115">-BatchContext</span></span>
<span data-ttu-id="52b91-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="52b91-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="52b91-117">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="52b91-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="52b91-118">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="52b91-118">-ComputeNode</span></span>
<span data-ttu-id="52b91-119">Określa obiekt **PSComputeNode** reprezentujący węzeł obliczeniowy, który ma zostać ponownie uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="52b91-119">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="52b91-120">-ID</span><span class="sxs-lookup"><span data-stu-id="52b91-120">-Id</span></span>
<span data-ttu-id="52b91-121">Określa identyfikator węzła obliczeniowego do ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="52b91-121">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="52b91-122">-PoolId</span><span class="sxs-lookup"><span data-stu-id="52b91-122">-PoolId</span></span>
<span data-ttu-id="52b91-123">Określa identyfikator puli zawierającej węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="52b91-123">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="52b91-124">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="52b91-124">-RebootOption</span></span>
<span data-ttu-id="52b91-125">Określa, kiedy należy ponownie uruchomić węzeł i co należy zrobić z uruchomionymi obecnie zadaniami.</span><span class="sxs-lookup"><span data-stu-id="52b91-125">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="52b91-126">Wartość domyślna to requeued.</span><span class="sxs-lookup"><span data-stu-id="52b91-126">The default is Requeue.</span></span>

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

### <span data-ttu-id="52b91-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b91-127">-DefaultProfile</span></span>
<span data-ttu-id="52b91-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="52b91-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52b91-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b91-129">CommonParameters</span></span>
<span data-ttu-id="52b91-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b91-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b91-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52b91-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b91-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52b91-132">INPUTS</span></span>

### <span data-ttu-id="52b91-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="52b91-133">BatchAccountContext</span></span>
<span data-ttu-id="52b91-134">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="52b91-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="52b91-135">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="52b91-135">PSComputeNode</span></span>
<span data-ttu-id="52b91-136">Parametr "ComputeNode" akceptuje wartość typu "PSComputeNode" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="52b91-136">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="52b91-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52b91-137">OUTPUTS</span></span>

## <span data-ttu-id="52b91-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52b91-138">NOTES</span></span>

## <span data-ttu-id="52b91-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52b91-139">RELATED LINKS</span></span>

[<span data-ttu-id="52b91-140">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="52b91-140">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="52b91-141">Resetowanie — AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="52b91-141">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="52b91-142">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="52b91-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


