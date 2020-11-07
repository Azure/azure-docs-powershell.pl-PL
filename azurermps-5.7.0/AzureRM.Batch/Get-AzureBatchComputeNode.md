---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
ms.openlocfilehash: d5cbd8c37f6d527a741f5bb92211d6b4f90b8113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551779"
---
# <span data-ttu-id="650f7-101">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="650f7-101">Get-AzureBatchComputeNode</span></span>

## <span data-ttu-id="650f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="650f7-102">SYNOPSIS</span></span>
<span data-ttu-id="650f7-103">Pobiera węzły obliczeniowe partii z puli.</span><span class="sxs-lookup"><span data-stu-id="650f7-103">Gets Batch compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="650f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="650f7-104">SYNTAX</span></span>

### <span data-ttu-id="650f7-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="650f7-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="650f7-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="650f7-106">Id</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="650f7-107">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="650f7-107">ParentObject</span></span>
```
Get-AzureBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="650f7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="650f7-108">DESCRIPTION</span></span>
<span data-ttu-id="650f7-109">Polecenie cmdlet **Get-AzureBatchComputeNode** pobiera węzły obliczeniowe usługi Azure Batch z puli.</span><span class="sxs-lookup"><span data-stu-id="650f7-109">The **Get-AzureBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="650f7-110">Określ parametr *PoolID* lub *Pool (Pula* ).</span><span class="sxs-lookup"><span data-stu-id="650f7-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="650f7-111">Określ parametr *ID* , aby uzyskać jeden węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="650f7-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="650f7-112">Określ parametr *Filter* , aby uzyskać węzły obliczeniowe, które pasują do filtru protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="650f7-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="650f7-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="650f7-113">EXAMPLES</span></span>

### <span data-ttu-id="650f7-114">Przykład 1: uzyskiwanie węzła obliczeniowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="650f7-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="650f7-115">To polecenie uzyskuje węzeł obliczeniowy mający identyfikator TVM-2316545714_1-20150725t213220z z puli zawierającej identyfikator Pool06.</span><span class="sxs-lookup"><span data-stu-id="650f7-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="650f7-116">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="650f7-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="650f7-117">Przykład 2: uzyskiwanie wszystkich węzłów obliczeń bezczynnych z puli</span><span class="sxs-lookup"><span data-stu-id="650f7-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                : 

Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM
IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="650f7-118">To polecenie pobiera wszystkie węzły obliczeniowe, które są zawarte w puli o IDENTYFIKATORze Pool06.</span><span class="sxs-lookup"><span data-stu-id="650f7-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="650f7-119">To polecenie określa stan bezczynności za pomocą parametru *Filter* .</span><span class="sxs-lookup"><span data-stu-id="650f7-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="650f7-120">Przykład 3: uzyskiwanie wszystkich węzłów obliczeniowych w określonej puli</span><span class="sxs-lookup"><span data-stu-id="650f7-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzureBatchPool -Id "Pool07" -BatchContext $Context | Get-AzureBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                : 


Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM

IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="650f7-121">To polecenie pobiera pulę o IDENTYFIKATORze Pool07 przy użyciu polecenia cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="650f7-121">This command gets the pool that has the ID Pool07 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="650f7-122">Polecenie przekazuje tę pulę do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="650f7-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="650f7-123">To polecenie cmdlet pobiera wszystkie węzły COMPUTE z tej puli.</span><span class="sxs-lookup"><span data-stu-id="650f7-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="650f7-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="650f7-124">PARAMETERS</span></span>

### <span data-ttu-id="650f7-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="650f7-125">-BatchContext</span></span>
<span data-ttu-id="650f7-126">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="650f7-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="650f7-127">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="650f7-127">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="650f7-128">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="650f7-128">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="650f7-129">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="650f7-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="650f7-130">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="650f7-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="650f7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="650f7-131">-DefaultProfile</span></span>
<span data-ttu-id="650f7-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="650f7-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="650f7-133">-Filter</span><span class="sxs-lookup"><span data-stu-id="650f7-133">-Filter</span></span>
<span data-ttu-id="650f7-134">Określa klauzulę filtru OData.</span><span class="sxs-lookup"><span data-stu-id="650f7-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="650f7-135">To polecenie cmdlet zwraca węzły obliczeniowe, które pasują do filtru, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="650f7-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="650f7-136">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie węzły COMPUTE dla puli.</span><span class="sxs-lookup"><span data-stu-id="650f7-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650f7-137">-ID</span><span class="sxs-lookup"><span data-stu-id="650f7-137">-Id</span></span>
<span data-ttu-id="650f7-138">Określa identyfikator węzła obliczeniowego, który ten polecenie cmdlet pobiera z puli.</span><span class="sxs-lookup"><span data-stu-id="650f7-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="650f7-139">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="650f7-139">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="650f7-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="650f7-140">-MaxCount</span></span>
<span data-ttu-id="650f7-141">Określa maksymalną liczbę węzłów obliczeniowych, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="650f7-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="650f7-142">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="650f7-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="650f7-143">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="650f7-143">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650f7-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="650f7-144">-Pool</span></span>
<span data-ttu-id="650f7-145">Określa pulę jako obiekt **PSCloudPool** , który zawiera węzły obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="650f7-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="650f7-146">Aby uzyskać obiekt **PSCloudPool** , użyj polecenia cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="650f7-146">To obtain a **PSCloudPool** object, use the Get-AzureBatchPool cmdlet.</span></span>

```yaml
Type: PSCloudPool
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="650f7-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="650f7-147">-PoolId</span></span>
<span data-ttu-id="650f7-148">Określa identyfikator puli zawierającej węzły obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="650f7-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="650f7-149">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="650f7-149">-Select</span></span>
<span data-ttu-id="650f7-150">Określa klauzulę SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="650f7-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="650f7-151">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="650f7-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650f7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="650f7-152">CommonParameters</span></span>
<span data-ttu-id="650f7-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="650f7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="650f7-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="650f7-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="650f7-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="650f7-155">INPUTS</span></span>

### <span data-ttu-id="650f7-156">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="650f7-156">BatchAccountContext</span></span>
<span data-ttu-id="650f7-157">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="650f7-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="650f7-158">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="650f7-158">PSCloudPool</span></span>
<span data-ttu-id="650f7-159">Parametr "Pool" przyjmuje wartość typu "PSCloudPool" z procesu</span><span class="sxs-lookup"><span data-stu-id="650f7-159">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="650f7-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="650f7-160">OUTPUTS</span></span>

### <span data-ttu-id="650f7-161">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="650f7-161">PSComputeNode</span></span>

## <span data-ttu-id="650f7-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="650f7-162">NOTES</span></span>

## <span data-ttu-id="650f7-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="650f7-163">RELATED LINKS</span></span>

[<span data-ttu-id="650f7-164">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="650f7-164">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="650f7-165">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="650f7-165">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="650f7-166">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="650f7-166">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="650f7-167">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="650f7-167">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="650f7-168">Resetowanie — AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="650f7-168">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="650f7-169">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="650f7-169">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="650f7-170">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="650f7-170">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

