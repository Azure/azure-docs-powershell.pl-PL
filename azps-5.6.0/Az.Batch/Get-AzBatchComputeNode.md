---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: 2adaebc28f27d2ea785df5a93510375020bcd542
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990487"
---
# <span data-ttu-id="9b9d5-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="9b9d5-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="9b9d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="9b9d5-103">Pobiera węzły obliczeniowe partii z puli.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="9b9d5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9b9d5-104">SYNTAX</span></span>

### <span data-ttu-id="9b9d5-105">FiltrDanych OData (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9b9d5-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b9d5-106">Identyfikator</span><span class="sxs-lookup"><span data-stu-id="9b9d5-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b9d5-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="9b9d5-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b9d5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9b9d5-108">DESCRIPTION</span></span>
<span data-ttu-id="9b9d5-109">Polecenie **cmdlet Get-AzBatchComputeNode** pobiera węzły obliczeniowe usługi Azure Batch z puli.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="9b9d5-110">Określ parametr *PoolID lub* *Pool.*</span><span class="sxs-lookup"><span data-stu-id="9b9d5-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="9b9d5-111">Określ parametr *Id,* aby uzyskać pojedynczy węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="9b9d5-112">Określ parametr *filtru,* aby uzyskać węzły obliczeniowe zgodne z filtrem protokołu Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="9b9d5-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="9b9d5-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9b9d5-113">EXAMPLES</span></span>

### <span data-ttu-id="9b9d5-114">Przykład 1. Uzyskiwanie węzła obliczeniowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="9b9d5-114">Example 1: Get a compute node by ID</span></span>
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

<span data-ttu-id="9b9d5-115">To polecenie pobiera węzeł obliczeniowy o identyfikatorze tvm-2316545714_1-20150725t213220z z puli, która ma pulę identyfikatorów06.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="9b9d5-116">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="9b9d5-117">Przykład 2. Uzyskiwanie wszystkich bezczynnych węzłów obliczeniowych z puli</span><span class="sxs-lookup"><span data-stu-id="9b9d5-117">Example 2: Get all idle compute nodes from a pool</span></span>
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

<span data-ttu-id="9b9d5-118">To polecenie pobiera wszystkie bezczynne węzły obliczeniowe znajdujące się w puli zawierającej pulę identyfikatorów 06.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="9b9d5-119">Polecenie określa stan bezczynności przy użyciu *parametru Filter.*</span><span class="sxs-lookup"><span data-stu-id="9b9d5-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="9b9d5-120">Przykład 3. Uzyskiwanie wszystkich węzłów obliczeniowych w określonej puli</span><span class="sxs-lookup"><span data-stu-id="9b9d5-120">Example 3: Get all compute nodes in a specified pool</span></span>
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

<span data-ttu-id="9b9d5-121">To polecenie pobiera pulę o identyfikatorze Pool07 przy użyciu Get-AzBatchPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="9b9d5-122">Polecenie przekazuje pulę do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9b9d5-123">To polecenie cmdlet pobiera wszystkie węzły obliczeniowe z tej puli.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="9b9d5-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b9d5-124">PARAMETERS</span></span>

### <span data-ttu-id="9b9d5-125">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="9b9d5-125">-BatchContext</span></span>
<span data-ttu-id="9b9d5-126">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9b9d5-127">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9b9d5-128">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9b9d5-129">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9b9d5-130">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9b9d5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b9d5-131">-DefaultProfile</span></span>
<span data-ttu-id="9b9d5-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b9d5-133">— Filtr</span><span class="sxs-lookup"><span data-stu-id="9b9d5-133">-Filter</span></span>
<span data-ttu-id="9b9d5-134">Określa klauzulę filtru OData.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="9b9d5-135">To polecenie cmdlet zwraca węzły obliczeniowe zgodne z filtrem, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="9b9d5-136">Jeśli filtr nie zostanie określony, to polecenie cmdlet zwróci wszystkie węzły obliczeniowe dla puli.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

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

### <span data-ttu-id="9b9d5-137">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="9b9d5-137">-Id</span></span>
<span data-ttu-id="9b9d5-138">Określa identyfikator węzła obliczeniowego, który to polecenie cmdlet pobiera z puli.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="9b9d5-139">Nie można określić symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-139">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="9b9d5-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9b9d5-140">-MaxCount</span></span>
<span data-ttu-id="9b9d5-141">Określa maksymalną liczbę węzłów obliczeniowych do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="9b9d5-142">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie użyje górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="9b9d5-143">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-143">The default value is 1000.</span></span>

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

### <span data-ttu-id="9b9d5-144">— Pula</span><span class="sxs-lookup"><span data-stu-id="9b9d5-144">-Pool</span></span>
<span data-ttu-id="9b9d5-145">Określa pulę, jako **obiekt PSCloudPool,** zawierającą węzły obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="9b9d5-146">Aby uzyskać obiekt **PSCloudPool,** użyj Get-AzBatchPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

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

### <span data-ttu-id="9b9d5-147">- PoolId</span><span class="sxs-lookup"><span data-stu-id="9b9d5-147">-PoolId</span></span>
<span data-ttu-id="9b9d5-148">Określa identyfikator puli zawierającej węzły obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

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

### <span data-ttu-id="9b9d5-149">— Wybierz</span><span class="sxs-lookup"><span data-stu-id="9b9d5-149">-Select</span></span>
<span data-ttu-id="9b9d5-150">Określa klauzulę wybierania danych OData.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="9b9d5-151">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="9b9d5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b9d5-152">CommonParameters</span></span>
<span data-ttu-id="9b9d5-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b9d5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b9d5-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b9d5-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b9d5-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b9d5-155">INPUTS</span></span>

### <span data-ttu-id="9b9d5-156">System.String</span><span class="sxs-lookup"><span data-stu-id="9b9d5-156">System.String</span></span>

### <span data-ttu-id="9b9d5-157">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="9b9d5-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="9b9d5-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9b9d5-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9b9d5-159">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b9d5-159">OUTPUTS</span></span>

### <span data-ttu-id="9b9d5-160">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="9b9d5-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="9b9d5-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9b9d5-161">NOTES</span></span>

## <span data-ttu-id="9b9d5-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b9d5-162">RELATED LINKS</span></span>

[<span data-ttu-id="9b9d5-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="9b9d5-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="9b9d5-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="9b9d5-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="9b9d5-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="9b9d5-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="9b9d5-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="9b9d5-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="9b9d5-167">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="9b9d5-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="9b9d5-168">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="9b9d5-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="9b9d5-169">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="9b9d5-169">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
