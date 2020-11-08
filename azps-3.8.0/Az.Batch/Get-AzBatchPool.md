---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
ms.openlocfilehash: adfaf42b6c4ce210ce2356e09d347e7a126d24d9
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "94061769"
---
# <span data-ttu-id="8a1c7-101">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="8a1c7-101">Get-AzBatchPool</span></span>

## <span data-ttu-id="8a1c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a1c7-102">SYNOPSIS</span></span>
<span data-ttu-id="8a1c7-103">Pobiera pule partii na podstawie określonego konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-103">Gets Batch pools under the specified Batch account.</span></span>

## <span data-ttu-id="8a1c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a1c7-104">SYNTAX</span></span>

### <span data-ttu-id="8a1c7-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8a1c7-105">ODataFilter (Default)</span></span>
```
Get-AzBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a1c7-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="8a1c7-106">Id</span></span>
```
Get-AzBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a1c7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8a1c7-107">DESCRIPTION</span></span>
<span data-ttu-id="8a1c7-108">Polecenie cmdlet **Get-AzBatchPool** pobiera pule usługi Azure Batch w ramach konta wsadowego określonego za pomocą parametru *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="8a1c7-108">The **Get-AzBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="8a1c7-109">Za pomocą parametru *ID* można uzyskać pojedynczą pulę lub można użyć parametru *Filter* w celu uzyskania pul zgodnych z filtrem Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="8a1c7-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="8a1c7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a1c7-110">EXAMPLES</span></span>

### <span data-ttu-id="8a1c7-111">Przykład 1: uzyskiwanie puli według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="8a1c7-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzBatchPool -Id "MyPool" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : standard_d1_v2
```

<span data-ttu-id="8a1c7-112">To polecenie pobiera pulę o IDENTYFIKATORze moja Pula.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="8a1c7-113">Przykład 2: pobieranie wszystkich pul przy użyciu filtru OData</span><span class="sxs-lookup"><span data-stu-id="8a1c7-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : standard_d1_v2
```

<span data-ttu-id="8a1c7-114">To polecenie pobiera pule, których identyfikatory rozpoczynają się od mojej, przy użyciu parametru *Filter* .</span><span class="sxs-lookup"><span data-stu-id="8a1c7-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="8a1c7-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a1c7-115">PARAMETERS</span></span>

### <span data-ttu-id="8a1c7-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8a1c7-116">-BatchContext</span></span>
<span data-ttu-id="8a1c7-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8a1c7-118">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8a1c7-119">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8a1c7-120">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8a1c7-121">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8a1c7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a1c7-122">-DefaultProfile</span></span>
<span data-ttu-id="8a1c7-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a1c7-124">-Expand</span><span class="sxs-lookup"><span data-stu-id="8a1c7-124">-Expand</span></span>
<span data-ttu-id="8a1c7-125">Określa klauzulę expanda Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="8a1c7-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="8a1c7-126">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej jednostki.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="8a1c7-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="8a1c7-127">-Filter</span></span>
<span data-ttu-id="8a1c7-128">Określa klauzulę filtru OData do użycia podczas wysyłania zapytań dotyczących pul.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="8a1c7-129">Jeśli nie określisz filtru, zostaną zwrócone wszystkie pule na koncie wsadowym określonym za pomocą parametru *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="8a1c7-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1c7-130">-ID</span><span class="sxs-lookup"><span data-stu-id="8a1c7-130">-Id</span></span>
<span data-ttu-id="8a1c7-131">Określa identyfikator puli, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="8a1c7-132">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-132">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a1c7-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8a1c7-133">-MaxCount</span></span>
<span data-ttu-id="8a1c7-134">Określa maksymalną liczbę zestawów, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="8a1c7-135">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="8a1c7-136">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-136">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1c7-137">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="8a1c7-137">-Select</span></span>
<span data-ttu-id="8a1c7-138">Określa klauzulę SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="8a1c7-139">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="8a1c7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a1c7-140">CommonParameters</span></span>
<span data-ttu-id="8a1c7-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a1c7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a1c7-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a1c7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a1c7-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a1c7-143">INPUTS</span></span>

### <span data-ttu-id="8a1c7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8a1c7-144">System.String</span></span>

### <span data-ttu-id="8a1c7-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8a1c7-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8a1c7-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a1c7-146">OUTPUTS</span></span>

### <span data-ttu-id="8a1c7-147">Microsoft.Azure.Commands.Batch. Modele. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="8a1c7-147">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

## <span data-ttu-id="8a1c7-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a1c7-148">NOTES</span></span>

## <span data-ttu-id="8a1c7-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a1c7-149">RELATED LINKS</span></span>

[<span data-ttu-id="8a1c7-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8a1c7-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8a1c7-151">Nowe — AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="8a1c7-151">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="8a1c7-152">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="8a1c7-152">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="8a1c7-153">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="8a1c7-153">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


