---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: 51c1103b50ef236aeedfd2250d7b67c4f0662bcf
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "94061711"
---
# <span data-ttu-id="ecfbf-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="ecfbf-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="ecfbf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ecfbf-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfbf-103">Rozpoczynanie zmieniania rozmiaru puli.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="ecfbf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ecfbf-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecfbf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ecfbf-105">DESCRIPTION</span></span>
<span data-ttu-id="ecfbf-106">Polecenie cmdlet **Start-AzBatchPoolResize** rozpoczyna operację zmiany rozmiaru wsadu Azure Part na puli.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="ecfbf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ecfbf-107">EXAMPLES</span></span>

### <span data-ttu-id="ecfbf-108">Przykład 1: Zmienianie rozmiaru puli na 12 węzłów</span><span class="sxs-lookup"><span data-stu-id="ecfbf-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="ecfbf-109">To polecenie rozpoczyna operację zmiany rozmiaru puli o IDENTYFIKATORze ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="ecfbf-110">Elementem docelowym tej operacji jest 12 dedykowanych węzłów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="ecfbf-111">Użyj polecenia cmdlet Get-AzBatchAccountKey, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ecfbf-112">Przykład 2: Zmienianie rozmiaru puli przy użyciu opcji dealokacji</span><span class="sxs-lookup"><span data-stu-id="ecfbf-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="ecfbf-113">To polecenie cmdlet umożliwia zmienianie rozmiaru puli na pięć dedykowanych węzłów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="ecfbf-114">Polecenie pobiera pulę o IDENTYFIKATORze ContosoPool06 przy użyciu polecenia cmdlet Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="ecfbf-115">Polecenie przekazuje ten obiekt puli do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ecfbf-116">Polecenie rozpoczyna operację zmiany rozmiaru w puli.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="ecfbf-117">Celem jest pięć dedykowanych węzłów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="ecfbf-118">To polecenie określa czas trwania jednej godziny.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="ecfbf-119">Polecenie określa opcję rozdzielania, którą można zakończyć.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="ecfbf-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ecfbf-120">PARAMETERS</span></span>

### <span data-ttu-id="ecfbf-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ecfbf-121">-BatchContext</span></span>
<span data-ttu-id="ecfbf-122">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ecfbf-123">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ecfbf-124">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ecfbf-125">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ecfbf-126">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ecfbf-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="ecfbf-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="ecfbf-128">Określa opcję dealokacji dla operacji zmiany rozmiaru, która zostanie uruchomiona przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfbf-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfbf-129">-DefaultProfile</span></span>
<span data-ttu-id="ecfbf-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecfbf-131">-ID</span><span class="sxs-lookup"><span data-stu-id="ecfbf-131">-Id</span></span>
<span data-ttu-id="ecfbf-132">Określa identyfikator puli, której rozmiar tego polecenia cmdlet zmienia.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfbf-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="ecfbf-133">-ResizeTimeout</span></span>
<span data-ttu-id="ecfbf-134">Określa okres limitu czasu dla operacji zmiany rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="ecfbf-135">Jeśli pula nie dociera do rozmiaru docelowego, operacja zmiany rozmiaru zostaje zatrzymana.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfbf-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="ecfbf-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="ecfbf-137">Liczba dedykowanych węzłów obliczeniowych docelowych.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-137">The number of target dedicated compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfbf-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="ecfbf-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="ecfbf-139">Liczba docelowych węzłów obliczeniowych o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-139">The number of target low-priority compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfbf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfbf-140">CommonParameters</span></span>
<span data-ttu-id="ecfbf-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfbf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfbf-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecfbf-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfbf-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecfbf-143">INPUTS</span></span>

### <span data-ttu-id="ecfbf-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ecfbf-144">System.String</span></span>

### <span data-ttu-id="ecfbf-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ecfbf-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ecfbf-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ecfbf-146">OUTPUTS</span></span>

### <span data-ttu-id="ecfbf-147">System. void</span><span class="sxs-lookup"><span data-stu-id="ecfbf-147">System.Void</span></span>

## <span data-ttu-id="ecfbf-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ecfbf-148">NOTES</span></span>

## <span data-ttu-id="ecfbf-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ecfbf-149">RELATED LINKS</span></span>

[<span data-ttu-id="ecfbf-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ecfbf-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ecfbf-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="ecfbf-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="ecfbf-152">Zatrzymaj — AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="ecfbf-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="ecfbf-153">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="ecfbf-153">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


