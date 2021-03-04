---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
ms.openlocfilehash: 7c3aff3f69ae76765a80c7db1e66ee0a79990c9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956474"
---
# <span data-ttu-id="b4475-101">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="b4475-101">Get-AzBatchPool</span></span>

## <span data-ttu-id="b4475-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4475-102">SYNOPSIS</span></span>
<span data-ttu-id="b4475-103">Pobiera pule wsadowe pod określonym kontem usługi Batch.</span><span class="sxs-lookup"><span data-stu-id="b4475-103">Gets Batch pools under the specified Batch account.</span></span>

## <span data-ttu-id="b4475-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b4475-104">SYNTAX</span></span>

### <span data-ttu-id="b4475-105">FiltrDanych OData (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b4475-105">ODataFilter (Default)</span></span>
```
Get-AzBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4475-106">Identyfikator</span><span class="sxs-lookup"><span data-stu-id="b4475-106">Id</span></span>
```
Get-AzBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4475-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b4475-107">DESCRIPTION</span></span>
<span data-ttu-id="b4475-108">Polecenie **cmdlet Get-AzBatchPool** pobiera pule partii platformy Azure w ramach konta batch określonego za pomocą *parametru BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="b4475-108">The **Get-AzBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="b4475-109">Możesz użyć *parametru Identyfikator,* aby uzyskać jedną pulę, lub użyć parametru *Filter* w celu uzyskania pul, które są zgodne z filtrem protokołu Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="b4475-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="b4475-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b4475-110">EXAMPLES</span></span>

### <span data-ttu-id="b4475-111">Przykład 1. Uzyskiwanie puli według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="b4475-111">Example 1: Get a pool by ID</span></span>
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

<span data-ttu-id="b4475-112">To polecenie pobiera pulę z identyfikatorem MyPool.</span><span class="sxs-lookup"><span data-stu-id="b4475-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="b4475-113">Przykład 2. Uzyskiwanie wszystkich pul przy użyciu filtru OData</span><span class="sxs-lookup"><span data-stu-id="b4475-113">Example 2: Get all pools using an OData filter</span></span>
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

<span data-ttu-id="b4475-114">To polecenie pobiera pule, których identyfikatory zaczynają się od wartości Moje, przy użyciu *parametru Filter.*</span><span class="sxs-lookup"><span data-stu-id="b4475-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="b4475-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4475-115">PARAMETERS</span></span>

### <span data-ttu-id="b4475-116">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="b4475-116">-BatchContext</span></span>
<span data-ttu-id="b4475-117">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="b4475-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b4475-118">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b4475-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b4475-119">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="b4475-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b4475-120">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="b4475-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b4475-121">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b4475-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b4475-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4475-122">-DefaultProfile</span></span>
<span data-ttu-id="b4475-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4475-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4475-124">— Rozwiń</span><span class="sxs-lookup"><span data-stu-id="b4475-124">-Expand</span></span>
<span data-ttu-id="b4475-125">Określa klauzulę rozwijania protokołu Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="b4475-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="b4475-126">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej o otrzymuję.</span><span class="sxs-lookup"><span data-stu-id="b4475-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="b4475-127">— Filtr</span><span class="sxs-lookup"><span data-stu-id="b4475-127">-Filter</span></span>
<span data-ttu-id="b4475-128">Określa klauzulę filtru OData do użycia podczas wykonywania zapytań dotyczących pul.</span><span class="sxs-lookup"><span data-stu-id="b4475-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="b4475-129">Jeśli filtr nie zostanie określony, zostaną zwrócone wszystkie pule pod kontem Batch określonym za pomocą *parametru BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="b4475-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="b4475-130">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="b4475-130">-Id</span></span>
<span data-ttu-id="b4475-131">Określa identyfikator puli do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="b4475-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="b4475-132">Nie można określić symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="b4475-132">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="b4475-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b4475-133">-MaxCount</span></span>
<span data-ttu-id="b4475-134">Określa maksymalną liczbę pul do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="b4475-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="b4475-135">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie użyje górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="b4475-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="b4475-136">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="b4475-136">The default value is 1000.</span></span>

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

### <span data-ttu-id="b4475-137">— Wybierz</span><span class="sxs-lookup"><span data-stu-id="b4475-137">-Select</span></span>
<span data-ttu-id="b4475-138">Określa klauzulę wybierania danych OData.</span><span class="sxs-lookup"><span data-stu-id="b4475-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="b4475-139">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="b4475-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="b4475-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4475-140">CommonParameters</span></span>
<span data-ttu-id="b4475-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4475-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4475-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4475-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4475-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4475-143">INPUTS</span></span>

### <span data-ttu-id="b4475-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b4475-144">System.String</span></span>

### <span data-ttu-id="b4475-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b4475-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b4475-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4475-146">OUTPUTS</span></span>

### <span data-ttu-id="b4475-147">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="b4475-147">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

## <span data-ttu-id="b4475-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b4475-148">NOTES</span></span>

## <span data-ttu-id="b4475-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4475-149">RELATED LINKS</span></span>

[<span data-ttu-id="b4475-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b4475-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b4475-151">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="b4475-151">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="b4475-152">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="b4475-152">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="b4475-153">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b4475-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
