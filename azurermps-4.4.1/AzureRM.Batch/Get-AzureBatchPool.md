---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 6f89e7db5d2df2c475be1ac9875fd1e87217db77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719538"
---
# <span data-ttu-id="32d4b-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="32d4b-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="32d4b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="32d4b-103">Pobiera pule partii na podstawie określonego konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="32d4b-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32d4b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32d4b-104">SYNTAX</span></span>

### <span data-ttu-id="32d4b-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="32d4b-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32d4b-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="32d4b-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32d4b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="32d4b-107">DESCRIPTION</span></span>
<span data-ttu-id="32d4b-108">Polecenie cmdlet **Get-AzureBatchPool** pobiera pule usługi Azure Batch w ramach konta wsadowego określonego za pomocą parametru *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="32d4b-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="32d4b-109">Za pomocą parametru *ID* można uzyskać pojedynczą pulę lub można użyć parametru *Filter* w celu uzyskania pul zgodnych z filtrem Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="32d4b-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="32d4b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32d4b-110">EXAMPLES</span></span>

### <span data-ttu-id="32d4b-111">Przykład 1: uzyskiwanie puli według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="32d4b-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzureBatchPool -Id "MyPool" -BatchContext $Context
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
VirtualMachineSize                   : small
```

<span data-ttu-id="32d4b-112">To polecenie pobiera pulę o IDENTYFIKATORze moja Pula.</span><span class="sxs-lookup"><span data-stu-id="32d4b-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="32d4b-113">Przykład 2: pobieranie wszystkich pul przy użyciu filtru OData</span><span class="sxs-lookup"><span data-stu-id="32d4b-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzureBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
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
VirtualMachineSize                   : small
```

<span data-ttu-id="32d4b-114">To polecenie pobiera pule, których identyfikatory rozpoczynają się od mojej, przy użyciu parametru *Filter* .</span><span class="sxs-lookup"><span data-stu-id="32d4b-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="32d4b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32d4b-115">PARAMETERS</span></span>

### <span data-ttu-id="32d4b-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="32d4b-116">-BatchContext</span></span>
<span data-ttu-id="32d4b-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="32d4b-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="32d4b-118">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="32d4b-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="32d4b-119">-Expand</span><span class="sxs-lookup"><span data-stu-id="32d4b-119">-Expand</span></span>
<span data-ttu-id="32d4b-120">Określa klauzulę expanda Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="32d4b-120">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="32d4b-121">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej jednostki.</span><span class="sxs-lookup"><span data-stu-id="32d4b-121">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="32d4b-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="32d4b-122">-Filter</span></span>
<span data-ttu-id="32d4b-123">Określa klauzulę filtru OData do użycia podczas wysyłania zapytań dotyczących pul.</span><span class="sxs-lookup"><span data-stu-id="32d4b-123">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="32d4b-124">Jeśli nie określisz filtru, zostaną zwrócone wszystkie pule na koncie wsadowym określonym za pomocą parametru *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="32d4b-124">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="32d4b-125">-ID</span><span class="sxs-lookup"><span data-stu-id="32d4b-125">-Id</span></span>
<span data-ttu-id="32d4b-126">Określa identyfikator puli, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="32d4b-126">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="32d4b-127">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="32d4b-127">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="32d4b-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="32d4b-128">-MaxCount</span></span>
<span data-ttu-id="32d4b-129">Określa maksymalną liczbę zestawów, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="32d4b-129">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="32d4b-130">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="32d4b-130">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="32d4b-131">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="32d4b-131">The default value is 1000.</span></span>

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

### <span data-ttu-id="32d4b-132">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="32d4b-132">-Select</span></span>
<span data-ttu-id="32d4b-133">Określa klauzulę SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="32d4b-133">Specifies an OData select clause.</span></span>
<span data-ttu-id="32d4b-134">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="32d4b-134">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="32d4b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32d4b-135">-DefaultProfile</span></span>
<span data-ttu-id="32d4b-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="32d4b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32d4b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d4b-137">CommonParameters</span></span>
<span data-ttu-id="32d4b-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32d4b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d4b-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32d4b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d4b-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32d4b-140">INPUTS</span></span>

### <span data-ttu-id="32d4b-141">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="32d4b-141">BatchAccountContext</span></span>
<span data-ttu-id="32d4b-142">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="32d4b-142">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="32d4b-143">Ciąg</span><span class="sxs-lookup"><span data-stu-id="32d4b-143">String</span></span>
<span data-ttu-id="32d4b-144">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="32d4b-144">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="32d4b-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32d4b-145">OUTPUTS</span></span>

### <span data-ttu-id="32d4b-146">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="32d4b-146">PSCloudPool</span></span>

## <span data-ttu-id="32d4b-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32d4b-147">NOTES</span></span>

## <span data-ttu-id="32d4b-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32d4b-148">RELATED LINKS</span></span>

[<span data-ttu-id="32d4b-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="32d4b-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="32d4b-150">Nowe — AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="32d4b-150">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="32d4b-151">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="32d4b-151">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="32d4b-152">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="32d4b-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


