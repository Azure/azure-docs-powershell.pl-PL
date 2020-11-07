---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: b90a70bb6b4a8104597056715c75f5699db5a24e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717352"
---
# <span data-ttu-id="9f852-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="9f852-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="9f852-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9f852-102">SYNOPSIS</span></span>
<span data-ttu-id="9f852-103">Ponownie instaluje system operacyjny w określonym węźle COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="9f852-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f852-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9f852-104">SYNTAX</span></span>

### <span data-ttu-id="9f852-105">Identyfikator (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9f852-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f852-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="9f852-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f852-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9f852-107">DESCRIPTION</span></span>
<span data-ttu-id="9f852-108">Polecenie cmdlet **Reset-AzureBatchComputeNode** umożliwia ponowne zainstalowanie systemu operacyjnego w określonym węźle COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="9f852-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="9f852-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9f852-109">EXAMPLES</span></span>

### <span data-ttu-id="9f852-110">Przykład 1: odobrazowanie węzła</span><span class="sxs-lookup"><span data-stu-id="9f852-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="9f852-111">To polecenie powoduje ponowne zdjęcie węzła obliczeniowego z IDENTYFIKATORem "TVM-3257026573_2-20150813t200938z" w puli o nazwie Moja Pula.</span><span class="sxs-lookup"><span data-stu-id="9f852-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="9f852-112">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="9f852-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="9f852-113">Przykład 2: odtworzenie obrazu na wszystkich węzłach w puli</span><span class="sxs-lookup"><span data-stu-id="9f852-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="9f852-114">To polecenie powoduje ponowne zdjęcie każdego węzła obliczeniowego w puli o nazwie Moja Pula.</span><span class="sxs-lookup"><span data-stu-id="9f852-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="9f852-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f852-115">PARAMETERS</span></span>

### <span data-ttu-id="9f852-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9f852-116">-BatchContext</span></span>
<span data-ttu-id="9f852-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9f852-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9f852-118">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="9f852-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="9f852-119">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="9f852-119">-ComputeNode</span></span>
<span data-ttu-id="9f852-120">Określa obiekt **PSComputeNode** reprezentujący węzeł obliczeniowy, który ma zostać ponownie utworzony.</span><span class="sxs-lookup"><span data-stu-id="9f852-120">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="9f852-121">-ID</span><span class="sxs-lookup"><span data-stu-id="9f852-121">-Id</span></span>
<span data-ttu-id="9f852-122">Określa identyfikator węzła obliczeniowego do odobrazowania.</span><span class="sxs-lookup"><span data-stu-id="9f852-122">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="9f852-123">-PoolId</span><span class="sxs-lookup"><span data-stu-id="9f852-123">-PoolId</span></span>
<span data-ttu-id="9f852-124">Określa identyfikator puli zawierającej węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="9f852-124">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="9f852-125">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="9f852-125">-ReimageOption</span></span>
<span data-ttu-id="9f852-126">Określa, kiedy należy przeobrazować węzeł i co zrobić z uruchomionymi obecnie zadaniami.</span><span class="sxs-lookup"><span data-stu-id="9f852-126">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="9f852-127">Wartość domyślna to requeued.</span><span class="sxs-lookup"><span data-stu-id="9f852-127">The default is Requeue.</span></span>

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

### <span data-ttu-id="9f852-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f852-128">-DefaultProfile</span></span>
<span data-ttu-id="9f852-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9f852-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f852-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f852-130">CommonParameters</span></span>
<span data-ttu-id="9f852-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f852-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f852-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f852-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f852-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f852-133">INPUTS</span></span>

### <span data-ttu-id="9f852-134">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9f852-134">BatchAccountContext</span></span>
<span data-ttu-id="9f852-135">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="9f852-135">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="9f852-136">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="9f852-136">PSComputeNode</span></span>
<span data-ttu-id="9f852-137">Parametr "ComputeNode" akceptuje wartość typu "PSComputeNode" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="9f852-137">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="9f852-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9f852-138">OUTPUTS</span></span>

## <span data-ttu-id="9f852-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9f852-139">NOTES</span></span>

## <span data-ttu-id="9f852-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f852-140">RELATED LINKS</span></span>

[<span data-ttu-id="9f852-141">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="9f852-141">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="9f852-142">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="9f852-142">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="9f852-143">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="9f852-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


