---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: aabc7b9d6001bf2efd02d2bb03735af312edfd88
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "94061779"
---
# <span data-ttu-id="03e7d-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="03e7d-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="03e7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="03e7d-103">Pobiera węzły obliczeniowe partii z puli.</span><span class="sxs-lookup"><span data-stu-id="03e7d-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="03e7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03e7d-104">SYNTAX</span></span>

### <span data-ttu-id="03e7d-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="03e7d-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03e7d-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="03e7d-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03e7d-107">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="03e7d-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03e7d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="03e7d-108">DESCRIPTION</span></span>
<span data-ttu-id="03e7d-109">Polecenie cmdlet **Get-AzBatchComputeNode** pobiera węzły obliczeniowe usługi Azure Batch z puli.</span><span class="sxs-lookup"><span data-stu-id="03e7d-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="03e7d-110">Określ parametr *PoolID* lub *Pool (Pula* ).</span><span class="sxs-lookup"><span data-stu-id="03e7d-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="03e7d-111">Określ parametr *ID* , aby uzyskać jeden węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="03e7d-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="03e7d-112">Określ parametr *Filter* , aby uzyskać węzły obliczeniowe, które pasują do filtru protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="03e7d-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="03e7d-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03e7d-113">EXAMPLES</span></span>

### <span data-ttu-id="03e7d-114">Przykład 1: uzyskiwanie węzła obliczeniowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="03e7d-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="03e7d-115">To polecenie uzyskuje węzeł obliczeniowy mający identyfikator TVM-2316545714_1-20150725t213220z z puli zawierającej identyfikator Pool06.</span><span class="sxs-lookup"><span data-stu-id="03e7d-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="03e7d-116">Użyj polecenia cmdlet Get-AzBatchAccountKey, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="03e7d-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="03e7d-117">Przykład 2: uzyskiwanie wszystkich węzłów obliczeń bezczynnych z puli</span><span class="sxs-lookup"><span data-stu-id="03e7d-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
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
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="03e7d-118">To polecenie pobiera wszystkie węzły obliczeniowe, które są zawarte w puli o IDENTYFIKATORze Pool06.</span><span class="sxs-lookup"><span data-stu-id="03e7d-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="03e7d-119">To polecenie określa stan bezczynności za pomocą parametru *Filter* .</span><span class="sxs-lookup"><span data-stu-id="03e7d-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="03e7d-120">Przykład 3: uzyskiwanie wszystkich węzłów obliczeniowych w określonej puli</span><span class="sxs-lookup"><span data-stu-id="03e7d-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzBatchPool -Id "Pool07" -BatchContext $Context | Get-AzBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
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
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="03e7d-121">To polecenie pobiera pulę o IDENTYFIKATORze Pool07 przy użyciu polecenia cmdlet Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="03e7d-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="03e7d-122">Polecenie przekazuje tę pulę do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="03e7d-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="03e7d-123">To polecenie cmdlet pobiera wszystkie węzły COMPUTE z tej puli.</span><span class="sxs-lookup"><span data-stu-id="03e7d-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="03e7d-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03e7d-124">PARAMETERS</span></span>

### <span data-ttu-id="03e7d-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="03e7d-125">-BatchContext</span></span>
<span data-ttu-id="03e7d-126">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="03e7d-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="03e7d-127">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="03e7d-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="03e7d-128">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="03e7d-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="03e7d-129">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="03e7d-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="03e7d-130">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="03e7d-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="03e7d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e7d-131">-DefaultProfile</span></span>
<span data-ttu-id="03e7d-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03e7d-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03e7d-133">-Filter</span><span class="sxs-lookup"><span data-stu-id="03e7d-133">-Filter</span></span>
<span data-ttu-id="03e7d-134">Określa klauzulę filtru OData.</span><span class="sxs-lookup"><span data-stu-id="03e7d-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="03e7d-135">To polecenie cmdlet zwraca węzły obliczeniowe, które pasują do filtru, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="03e7d-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="03e7d-136">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie węzły COMPUTE dla puli.</span><span class="sxs-lookup"><span data-stu-id="03e7d-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

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

### <span data-ttu-id="03e7d-137">-ID</span><span class="sxs-lookup"><span data-stu-id="03e7d-137">-Id</span></span>
<span data-ttu-id="03e7d-138">Określa identyfikator węzła obliczeniowego, który ten polecenie cmdlet pobiera z puli.</span><span class="sxs-lookup"><span data-stu-id="03e7d-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="03e7d-139">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="03e7d-139">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="03e7d-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="03e7d-140">-MaxCount</span></span>
<span data-ttu-id="03e7d-141">Określa maksymalną liczbę węzłów obliczeniowych, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="03e7d-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="03e7d-142">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="03e7d-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="03e7d-143">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="03e7d-143">The default value is 1000.</span></span>

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

### <span data-ttu-id="03e7d-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="03e7d-144">-Pool</span></span>
<span data-ttu-id="03e7d-145">Określa pulę jako obiekt **PSCloudPool** , który zawiera węzły obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="03e7d-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="03e7d-146">Aby uzyskać obiekt **PSCloudPool** , użyj polecenia cmdlet Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="03e7d-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

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

### <span data-ttu-id="03e7d-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="03e7d-147">-PoolId</span></span>
<span data-ttu-id="03e7d-148">Określa identyfikator puli zawierającej węzły obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="03e7d-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

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

### <span data-ttu-id="03e7d-149">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="03e7d-149">-Select</span></span>
<span data-ttu-id="03e7d-150">Określa klauzulę SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="03e7d-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="03e7d-151">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="03e7d-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="03e7d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e7d-152">CommonParameters</span></span>
<span data-ttu-id="03e7d-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03e7d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e7d-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03e7d-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e7d-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03e7d-155">INPUTS</span></span>

### <span data-ttu-id="03e7d-156">System. String</span><span class="sxs-lookup"><span data-stu-id="03e7d-156">System.String</span></span>

### <span data-ttu-id="03e7d-157">Microsoft.Azure.Commands.Batch. Modele. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="03e7d-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="03e7d-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="03e7d-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="03e7d-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03e7d-159">OUTPUTS</span></span>

### <span data-ttu-id="03e7d-160">Microsoft.Azure.Commands.Batch. Modele. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="03e7d-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="03e7d-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03e7d-161">NOTES</span></span>

## <span data-ttu-id="03e7d-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03e7d-162">RELATED LINKS</span></span>

[<span data-ttu-id="03e7d-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="03e7d-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="03e7d-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="03e7d-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="03e7d-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="03e7d-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="03e7d-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="03e7d-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="03e7d-167">Resetowanie — AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="03e7d-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="03e7d-168">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="03e7d-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="03e7d-169">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="03e7d-169">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


