---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: a048e7bd2a013bd5d8526feead3b38483a1f61b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959802"
---
# <span data-ttu-id="9e0e5-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="9e0e5-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="9e0e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e0e5-102">SYNOPSIS</span></span>
<span data-ttu-id="9e0e5-103">Uzyskuje wynik formuły skalowania automatycznego w puli.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="9e0e5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9e0e5-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e0e5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9e0e5-105">DESCRIPTION</span></span>
<span data-ttu-id="9e0e5-106">Polecenie **cmdlet Test-AzBatchAutoScale** uzyskuje wynik formuły skalowania automatycznego w określonej puli.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="9e0e5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9e0e5-107">EXAMPLES</span></span>

### <span data-ttu-id="9e0e5-108">Przykład 1. Szacowanie formuły automatycznego skalowania w puli</span><span class="sxs-lookup"><span data-stu-id="9e0e5-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="9e0e5-109">Pierwsze polecenie przechowuje formułę w $Formula zmienną do użycia w tym przykładzie.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="9e0e5-110">Drugie polecenie oblicza formułę automatycznego skalowania w puli o identyfikatorze ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="9e0e5-111">Końcowe polecenie wyświetla wyniki **przy** użyciu standardowej składni kropki.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="9e0e5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e0e5-112">PARAMETERS</span></span>

### <span data-ttu-id="9e0e5-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="9e0e5-113">-AutoScaleFormula</span></span>
<span data-ttu-id="9e0e5-114">Określa formułę dla żądanej liczby węzłów obliczeniowych w puli.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e0e5-115">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="9e0e5-115">-BatchContext</span></span>
<span data-ttu-id="9e0e5-116">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9e0e5-117">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9e0e5-118">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9e0e5-119">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9e0e5-120">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9e0e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e0e5-121">-DefaultProfile</span></span>
<span data-ttu-id="9e0e5-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e0e5-123">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="9e0e5-123">-Id</span></span>
<span data-ttu-id="9e0e5-124">Określa identyfikator obiektu puli, dla której ma być testowe automatyczne skalowanie.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="9e0e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e0e5-125">CommonParameters</span></span>
<span data-ttu-id="9e0e5-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e0e5-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e0e5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e0e5-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e0e5-128">INPUTS</span></span>

### <span data-ttu-id="9e0e5-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9e0e5-129">System.String</span></span>

### <span data-ttu-id="9e0e5-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9e0e5-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9e0e5-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e0e5-131">OUTPUTS</span></span>

### <span data-ttu-id="9e0e5-132">Microsoft.Azure.Commands.Batch. Models.PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="9e0e5-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="9e0e5-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9e0e5-133">NOTES</span></span>

## <span data-ttu-id="9e0e5-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e0e5-134">RELATED LINKS</span></span>

[<span data-ttu-id="9e0e5-135">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="9e0e5-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="9e0e5-136">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="9e0e5-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="9e0e5-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9e0e5-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9e0e5-138">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="9e0e5-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
