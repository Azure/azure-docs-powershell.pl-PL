---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/reset-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: 998d559265aaa590cb62f72c9e6b9ec9dc5914df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526289"
---
# <span data-ttu-id="1eadb-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="1eadb-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="1eadb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1eadb-102">SYNOPSIS</span></span>
<span data-ttu-id="1eadb-103">Ponownie instaluje system operacyjny w określonym węźle COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="1eadb-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eadb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1eadb-104">SYNTAX</span></span>

### <span data-ttu-id="1eadb-105">Identyfikator (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1eadb-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eadb-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="1eadb-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1eadb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1eadb-107">DESCRIPTION</span></span>
<span data-ttu-id="1eadb-108">Polecenie cmdlet **Reset-AzureBatchComputeNode** umożliwia ponowne zainstalowanie systemu operacyjnego w określonym węźle COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="1eadb-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="1eadb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1eadb-109">EXAMPLES</span></span>

### <span data-ttu-id="1eadb-110">Przykład 1: odobrazowanie węzła</span><span class="sxs-lookup"><span data-stu-id="1eadb-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="1eadb-111">To polecenie powoduje ponowne zdjęcie węzła obliczeniowego z IDENTYFIKATORem "TVM-3257026573_2-20150813t200938z" w puli o nazwie Moja Pula.</span><span class="sxs-lookup"><span data-stu-id="1eadb-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="1eadb-112">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="1eadb-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="1eadb-113">Przykład 2: odtworzenie obrazu na wszystkich węzłach w puli</span><span class="sxs-lookup"><span data-stu-id="1eadb-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="1eadb-114">To polecenie powoduje ponowne zdjęcie każdego węzła obliczeniowego w puli o nazwie Moja Pula.</span><span class="sxs-lookup"><span data-stu-id="1eadb-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="1eadb-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1eadb-115">PARAMETERS</span></span>

### <span data-ttu-id="1eadb-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1eadb-116">-BatchContext</span></span>
<span data-ttu-id="1eadb-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="1eadb-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1eadb-118">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="1eadb-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1eadb-119">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="1eadb-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1eadb-120">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="1eadb-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1eadb-121">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="1eadb-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1eadb-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="1eadb-122">-ComputeNode</span></span>
<span data-ttu-id="1eadb-123">Określa obiekt **PSComputeNode** reprezentujący węzeł obliczeniowy, który ma zostać ponownie utworzony.</span><span class="sxs-lookup"><span data-stu-id="1eadb-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="1eadb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eadb-124">-DefaultProfile</span></span>
<span data-ttu-id="1eadb-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1eadb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1eadb-126">-ID</span><span class="sxs-lookup"><span data-stu-id="1eadb-126">-Id</span></span>
<span data-ttu-id="1eadb-127">Określa identyfikator węzła obliczeniowego do odobrazowania.</span><span class="sxs-lookup"><span data-stu-id="1eadb-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="1eadb-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="1eadb-128">-PoolId</span></span>
<span data-ttu-id="1eadb-129">Określa identyfikator puli zawierającej węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="1eadb-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="1eadb-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="1eadb-130">-ReimageOption</span></span>
<span data-ttu-id="1eadb-131">Określa, kiedy należy przeobrazować węzeł i co zrobić z uruchomionymi obecnie zadaniami.</span><span class="sxs-lookup"><span data-stu-id="1eadb-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="1eadb-132">Wartość domyślna to requeued.</span><span class="sxs-lookup"><span data-stu-id="1eadb-132">The default is Requeue.</span></span>

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

### <span data-ttu-id="1eadb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eadb-133">CommonParameters</span></span>
<span data-ttu-id="1eadb-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eadb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eadb-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eadb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eadb-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1eadb-136">INPUTS</span></span>

### <span data-ttu-id="1eadb-137">Microsoft.Azure.Commands.Batch. Modele. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="1eadb-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="1eadb-138">Parametry: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1eadb-138">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="1eadb-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1eadb-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="1eadb-140">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1eadb-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="1eadb-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1eadb-141">OUTPUTS</span></span>

### <span data-ttu-id="1eadb-142">System. void</span><span class="sxs-lookup"><span data-stu-id="1eadb-142">System.Void</span></span>

## <span data-ttu-id="1eadb-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1eadb-143">NOTES</span></span>

## <span data-ttu-id="1eadb-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1eadb-144">RELATED LINKS</span></span>

[<span data-ttu-id="1eadb-145">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="1eadb-145">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="1eadb-146">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="1eadb-146">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="1eadb-147">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="1eadb-147">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


