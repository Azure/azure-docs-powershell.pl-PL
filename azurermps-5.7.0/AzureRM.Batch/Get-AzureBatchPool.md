---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 2bd84d8e5d0f48c5b9a3af65944ece99369270c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527110"
---
# <span data-ttu-id="b2f20-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b2f20-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="b2f20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2f20-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f20-103">Pobiera pule partii na podstawie określonego konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="b2f20-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2f20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2f20-104">SYNTAX</span></span>

### <span data-ttu-id="b2f20-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b2f20-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2f20-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="b2f20-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2f20-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b2f20-107">DESCRIPTION</span></span>
<span data-ttu-id="b2f20-108">Polecenie cmdlet **Get-AzureBatchPool** pobiera pule usługi Azure Batch w ramach konta wsadowego określonego za pomocą parametru *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="b2f20-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="b2f20-109">Za pomocą parametru *ID* można uzyskać pojedynczą pulę lub można użyć parametru *Filter* w celu uzyskania pul zgodnych z filtrem Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="b2f20-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="b2f20-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2f20-110">EXAMPLES</span></span>

### <span data-ttu-id="b2f20-111">Przykład 1: uzyskiwanie puli według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="b2f20-111">Example 1: Get a pool by ID</span></span>
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

<span data-ttu-id="b2f20-112">To polecenie pobiera pulę o IDENTYFIKATORze moja Pula.</span><span class="sxs-lookup"><span data-stu-id="b2f20-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="b2f20-113">Przykład 2: pobieranie wszystkich pul przy użyciu filtru OData</span><span class="sxs-lookup"><span data-stu-id="b2f20-113">Example 2: Get all pools using an OData filter</span></span>
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

<span data-ttu-id="b2f20-114">To polecenie pobiera pule, których identyfikatory rozpoczynają się od mojej, przy użyciu parametru *Filter* .</span><span class="sxs-lookup"><span data-stu-id="b2f20-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="b2f20-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2f20-115">PARAMETERS</span></span>

### <span data-ttu-id="b2f20-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b2f20-116">-BatchContext</span></span>
<span data-ttu-id="b2f20-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="b2f20-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b2f20-118">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="b2f20-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b2f20-119">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="b2f20-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b2f20-120">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="b2f20-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b2f20-121">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b2f20-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b2f20-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f20-122">-DefaultProfile</span></span>
<span data-ttu-id="b2f20-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2f20-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2f20-124">-Expand</span><span class="sxs-lookup"><span data-stu-id="b2f20-124">-Expand</span></span>
<span data-ttu-id="b2f20-125">Określa klauzulę expanda Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="b2f20-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="b2f20-126">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej jednostki.</span><span class="sxs-lookup"><span data-stu-id="b2f20-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="b2f20-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="b2f20-127">-Filter</span></span>
<span data-ttu-id="b2f20-128">Określa klauzulę filtru OData do użycia podczas wysyłania zapytań dotyczących pul.</span><span class="sxs-lookup"><span data-stu-id="b2f20-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="b2f20-129">Jeśli nie określisz filtru, zostaną zwrócone wszystkie pule na koncie wsadowym określonym za pomocą parametru *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="b2f20-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f20-130">-ID</span><span class="sxs-lookup"><span data-stu-id="b2f20-130">-Id</span></span>
<span data-ttu-id="b2f20-131">Określa identyfikator puli, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="b2f20-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="b2f20-132">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="b2f20-132">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2f20-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b2f20-133">-MaxCount</span></span>
<span data-ttu-id="b2f20-134">Określa maksymalną liczbę zestawów, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="b2f20-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="b2f20-135">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="b2f20-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="b2f20-136">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="b2f20-136">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f20-137">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="b2f20-137">-Select</span></span>
<span data-ttu-id="b2f20-138">Określa klauzulę SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="b2f20-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="b2f20-139">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="b2f20-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="b2f20-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f20-140">CommonParameters</span></span>
<span data-ttu-id="b2f20-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2f20-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f20-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f20-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f20-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2f20-143">INPUTS</span></span>

### <span data-ttu-id="b2f20-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b2f20-144">BatchAccountContext</span></span>
<span data-ttu-id="b2f20-145">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="b2f20-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b2f20-146">Ciąg</span><span class="sxs-lookup"><span data-stu-id="b2f20-146">String</span></span>
<span data-ttu-id="b2f20-147">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="b2f20-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b2f20-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2f20-148">OUTPUTS</span></span>

### <span data-ttu-id="b2f20-149">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="b2f20-149">PSCloudPool</span></span>

## <span data-ttu-id="b2f20-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2f20-150">NOTES</span></span>

## <span data-ttu-id="b2f20-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2f20-151">RELATED LINKS</span></span>

[<span data-ttu-id="b2f20-152">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b2f20-152">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b2f20-153">Nowe — AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b2f20-153">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="b2f20-154">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b2f20-154">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="b2f20-155">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="b2f20-155">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


