---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
ms.openlocfilehash: f503352352c31369e594325c060cf0ab68490095
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554018"
---
# <span data-ttu-id="b3426-101">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b3426-101">Get-AzureBatchComputeNode</span></span>

## <span data-ttu-id="b3426-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3426-102">SYNOPSIS</span></span>
<span data-ttu-id="b3426-103">Pobiera węzły obliczeniowe partii z puli.</span><span class="sxs-lookup"><span data-stu-id="b3426-103">Gets Batch compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3426-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3426-104">SYNTAX</span></span>

### <span data-ttu-id="b3426-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b3426-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3426-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="b3426-106">Id</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3426-107">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="b3426-107">ParentObject</span></span>
```
Get-AzureBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3426-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b3426-108">DESCRIPTION</span></span>
<span data-ttu-id="b3426-109">Polecenie cmdlet **Get-AzureBatchComputeNode** pobiera węzły obliczeniowe usługi Azure Batch z puli.</span><span class="sxs-lookup"><span data-stu-id="b3426-109">The **Get-AzureBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="b3426-110">Określ parametr *PoolID* lub *Pool (Pula* ).</span><span class="sxs-lookup"><span data-stu-id="b3426-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="b3426-111">Określ parametr *ID* , aby uzyskać jeden węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="b3426-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="b3426-112">Określ parametr *Filter* , aby uzyskać węzły obliczeniowe, które pasują do filtru protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="b3426-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="b3426-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3426-113">EXAMPLES</span></span>

### <span data-ttu-id="b3426-114">Przykład 1: uzyskiwanie węzła obliczeniowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="b3426-114">Example 1: Get a compute node by ID</span></span>
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

<span data-ttu-id="b3426-115">To polecenie uzyskuje węzeł obliczeniowy mający identyfikator TVM-2316545714_1-20150725t213220z z puli zawierającej identyfikator Pool06.</span><span class="sxs-lookup"><span data-stu-id="b3426-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="b3426-116">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="b3426-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b3426-117">Przykład 2: uzyskiwanie wszystkich węzłów obliczeń bezczynnych z puli</span><span class="sxs-lookup"><span data-stu-id="b3426-117">Example 2: Get all idle compute nodes from a pool</span></span>
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

<span data-ttu-id="b3426-118">To polecenie pobiera wszystkie węzły obliczeniowe, które są zawarte w puli o IDENTYFIKATORze Pool06.</span><span class="sxs-lookup"><span data-stu-id="b3426-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="b3426-119">To polecenie określa stan bezczynności za pomocą parametru *Filter* .</span><span class="sxs-lookup"><span data-stu-id="b3426-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="b3426-120">Przykład 3: uzyskiwanie wszystkich węzłów obliczeniowych w określonej puli</span><span class="sxs-lookup"><span data-stu-id="b3426-120">Example 3: Get all compute nodes in a specified pool</span></span>
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

<span data-ttu-id="b3426-121">To polecenie pobiera pulę o IDENTYFIKATORze Pool07 przy użyciu polecenia cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="b3426-121">This command gets the pool that has the ID Pool07 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="b3426-122">Polecenie przekazuje tę pulę do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="b3426-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b3426-123">To polecenie cmdlet pobiera wszystkie węzły COMPUTE z tej puli.</span><span class="sxs-lookup"><span data-stu-id="b3426-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="b3426-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3426-124">PARAMETERS</span></span>

### <span data-ttu-id="b3426-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b3426-125">-BatchContext</span></span>
<span data-ttu-id="b3426-126">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="b3426-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b3426-127">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="b3426-127">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b3426-128">-Filter</span><span class="sxs-lookup"><span data-stu-id="b3426-128">-Filter</span></span>
<span data-ttu-id="b3426-129">Określa klauzulę filtru OData.</span><span class="sxs-lookup"><span data-stu-id="b3426-129">Specifies an OData filter clause.</span></span>
<span data-ttu-id="b3426-130">To polecenie cmdlet zwraca węzły obliczeniowe, które pasują do filtru, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b3426-130">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="b3426-131">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie węzły COMPUTE dla puli.</span><span class="sxs-lookup"><span data-stu-id="b3426-131">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3426-132">-ID</span><span class="sxs-lookup"><span data-stu-id="b3426-132">-Id</span></span>
<span data-ttu-id="b3426-133">Określa identyfikator węzła obliczeniowego, który ten polecenie cmdlet pobiera z puli.</span><span class="sxs-lookup"><span data-stu-id="b3426-133">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="b3426-134">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="b3426-134">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3426-135">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b3426-135">-MaxCount</span></span>
<span data-ttu-id="b3426-136">Określa maksymalną liczbę węzłów obliczeniowych, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="b3426-136">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="b3426-137">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="b3426-137">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="b3426-138">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="b3426-138">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3426-139">-Pool</span><span class="sxs-lookup"><span data-stu-id="b3426-139">-Pool</span></span>
<span data-ttu-id="b3426-140">Określa pulę jako obiekt **PSCloudPool** , który zawiera węzły obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="b3426-140">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="b3426-141">Aby uzyskać obiekt **PSCloudPool** , użyj polecenia cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="b3426-141">To obtain a **PSCloudPool** object, use the Get-AzureBatchPool cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3426-142">-PoolId</span><span class="sxs-lookup"><span data-stu-id="b3426-142">-PoolId</span></span>
<span data-ttu-id="b3426-143">Określa identyfikator puli zawierającej węzły obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="b3426-143">Specifies the ID of the pool that contains the compute nodes.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3426-144">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="b3426-144">-Select</span></span>
<span data-ttu-id="b3426-145">Określa klauzulę SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="b3426-145">Specifies an OData select clause.</span></span>
<span data-ttu-id="b3426-146">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="b3426-146">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3426-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3426-147">-DefaultProfile</span></span>
<span data-ttu-id="b3426-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3426-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3426-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3426-149">CommonParameters</span></span>
<span data-ttu-id="b3426-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3426-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3426-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3426-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3426-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3426-152">INPUTS</span></span>

### <span data-ttu-id="b3426-153">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b3426-153">BatchAccountContext</span></span>
<span data-ttu-id="b3426-154">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="b3426-154">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b3426-155">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="b3426-155">PSCloudPool</span></span>
<span data-ttu-id="b3426-156">Parametr "Pool" przyjmuje wartość typu "PSCloudPool" z procesu</span><span class="sxs-lookup"><span data-stu-id="b3426-156">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="b3426-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3426-157">OUTPUTS</span></span>

### <span data-ttu-id="b3426-158">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="b3426-158">PSComputeNode</span></span>

## <span data-ttu-id="b3426-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3426-159">NOTES</span></span>

## <span data-ttu-id="b3426-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3426-160">RELATED LINKS</span></span>

[<span data-ttu-id="b3426-161">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b3426-161">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="b3426-162">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="b3426-162">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="b3426-163">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="b3426-163">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="b3426-164">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b3426-164">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="b3426-165">Resetowanie — AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b3426-165">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="b3426-166">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b3426-166">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="b3426-167">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="b3426-167">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


