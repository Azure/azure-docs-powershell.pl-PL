---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: b312a94a971a5ff17a153a8a9b0112e14886fe12
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966737"
---
# <span data-ttu-id="2925d-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="2925d-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="2925d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2925d-102">SYNOPSIS</span></span>
<span data-ttu-id="2925d-103">Zaczyna zmieniać rozmiar puli.</span><span class="sxs-lookup"><span data-stu-id="2925d-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="2925d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2925d-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2925d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2925d-105">DESCRIPTION</span></span>
<span data-ttu-id="2925d-106">Polecenie **cmdlet Start-AzBatchPoolResize** uruchamia operację zmiany rozmiaru partii platformy Azure w puli.</span><span class="sxs-lookup"><span data-stu-id="2925d-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="2925d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2925d-107">EXAMPLES</span></span>

### <span data-ttu-id="2925d-108">Przykład 1. Zmienianie rozmiaru puli na 12 węzłów</span><span class="sxs-lookup"><span data-stu-id="2925d-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="2925d-109">To polecenie uruchamia operację zmiany rozmiaru w puli o identyfikatorze ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="2925d-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="2925d-110">Obiektem docelowym operacji jest 12 dedykowanych węzłów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="2925d-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="2925d-111">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="2925d-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="2925d-112">Przykład 2. Zmienianie rozmiaru puli przy użyciu opcji deallocation</span><span class="sxs-lookup"><span data-stu-id="2925d-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="2925d-113">To polecenie cmdlet zmienia rozmiar puli na pięć dedykowanych węzłów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="2925d-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="2925d-114">Polecenie pobiera pulę o identyfikatorze ContosoPool06 przy użyciu Get-AzBatchPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2925d-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="2925d-115">Polecenie przekazuje ten obiekt puli do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="2925d-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2925d-116">Polecenie uruchamia operację zmiany rozmiaru w puli.</span><span class="sxs-lookup"><span data-stu-id="2925d-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="2925d-117">Celem jest pięć dedykowanych węzłów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="2925d-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="2925d-118">Polecenie określa czas, przez który został uchyliony czas jednej godziny.</span><span class="sxs-lookup"><span data-stu-id="2925d-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="2925d-119">To polecenie określa opcję deallocation (Zakończ).</span><span class="sxs-lookup"><span data-stu-id="2925d-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="2925d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2925d-120">PARAMETERS</span></span>

### <span data-ttu-id="2925d-121">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="2925d-121">-BatchContext</span></span>
<span data-ttu-id="2925d-122">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="2925d-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2925d-123">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2925d-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2925d-124">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="2925d-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2925d-125">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="2925d-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2925d-126">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2925d-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2925d-127">-ComputeNodeallocationOption</span><span class="sxs-lookup"><span data-stu-id="2925d-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="2925d-128">Określa opcję lokalizacji transakcji dla operacji zmiany rozmiaru, która zostanie uruchamiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2925d-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="2925d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2925d-129">-DefaultProfile</span></span>
<span data-ttu-id="2925d-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2925d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2925d-131">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="2925d-131">-Id</span></span>
<span data-ttu-id="2925d-132">Określa identyfikator puli, których rozmiar zostanie zmieniony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2925d-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="2925d-133">- ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="2925d-133">-ResizeTimeout</span></span>
<span data-ttu-id="2925d-134">Określa przeożenie czasu dla operacji zmiany rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="2925d-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="2925d-135">Jeśli pula nie osiągnie rozmiaru docelowego do tego czasu, operacja zmiany rozmiaru zostanie zatrzymana.</span><span class="sxs-lookup"><span data-stu-id="2925d-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="2925d-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="2925d-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="2925d-137">Liczba docelowych dedykowanych węzłów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="2925d-137">The number of target dedicated compute nodes.</span></span>

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

### <span data-ttu-id="2925d-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="2925d-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="2925d-139">Liczba docelowych węzłów obliczeniowych o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="2925d-139">The number of target low-priority compute nodes.</span></span>

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

### <span data-ttu-id="2925d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2925d-140">CommonParameters</span></span>
<span data-ttu-id="2925d-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2925d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2925d-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2925d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2925d-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2925d-143">INPUTS</span></span>

### <span data-ttu-id="2925d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="2925d-144">System.String</span></span>

### <span data-ttu-id="2925d-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2925d-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2925d-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2925d-146">OUTPUTS</span></span>

### <span data-ttu-id="2925d-147">System.Void</span><span class="sxs-lookup"><span data-stu-id="2925d-147">System.Void</span></span>

## <span data-ttu-id="2925d-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2925d-148">NOTES</span></span>

## <span data-ttu-id="2925d-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2925d-149">RELATED LINKS</span></span>

[<span data-ttu-id="2925d-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="2925d-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2925d-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="2925d-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="2925d-152">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="2925d-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="2925d-153">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2925d-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
