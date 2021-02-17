---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
ms.openlocfilehash: 73e7e9e0e4020f284b26e720e0f34ec7f11fd04f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239451"
---
# <span data-ttu-id="5ca15-101">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="5ca15-101">Enable-AzBatchAutoScale</span></span>

## <span data-ttu-id="5ca15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ca15-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca15-103">Umożliwia automatyczne skalowanie puli.</span><span class="sxs-lookup"><span data-stu-id="5ca15-103">Enables automatic scaling of a pool.</span></span>

## <span data-ttu-id="5ca15-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5ca15-104">SYNTAX</span></span>

```
Enable-AzBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ca15-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5ca15-105">DESCRIPTION</span></span>
<span data-ttu-id="5ca15-106">Polecenie **cmdlet Enable-AzBatchAutoScale** umożliwia automatyczne skalowanie określonej puli.</span><span class="sxs-lookup"><span data-stu-id="5ca15-106">The **Enable-AzBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="5ca15-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5ca15-107">EXAMPLES</span></span>

### <span data-ttu-id="5ca15-108">Przykład 1. Włączanie automatycznego skalowania puli</span><span class="sxs-lookup"><span data-stu-id="5ca15-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="5ca15-109">Pierwsze polecenie definiuje formułę, a następnie zapisuje ją w $Formula zmienną.</span><span class="sxs-lookup"><span data-stu-id="5ca15-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="5ca15-110">Drugie polecenie umożliwia automatyczne skalowanie puli o nazwie MyPool przy użyciu formuły $Formula.</span><span class="sxs-lookup"><span data-stu-id="5ca15-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="5ca15-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ca15-111">PARAMETERS</span></span>

### <span data-ttu-id="5ca15-112">-AutoScaleEvaluationIntervalation</span><span class="sxs-lookup"><span data-stu-id="5ca15-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="5ca15-113">Określa czas (w minutach), który upływa przed automatycznym dostosowaniem rozmiaru puli zgodnie z formułą Autoskalowanie.</span><span class="sxs-lookup"><span data-stu-id="5ca15-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="5ca15-114">Wartość domyślna to 15 minut, a wartość minimalna to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="5ca15-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca15-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="5ca15-115">-AutoScaleFormula</span></span>
<span data-ttu-id="5ca15-116">Określa formułę dla żądanej liczby węzłów obliczeniowych w puli.</span><span class="sxs-lookup"><span data-stu-id="5ca15-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca15-117">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="5ca15-117">-BatchContext</span></span>
<span data-ttu-id="5ca15-118">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="5ca15-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5ca15-119">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5ca15-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5ca15-120">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="5ca15-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5ca15-121">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="5ca15-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5ca15-122">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5ca15-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5ca15-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca15-123">-DefaultProfile</span></span>
<span data-ttu-id="5ca15-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ca15-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ca15-125">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="5ca15-125">-Id</span></span>
<span data-ttu-id="5ca15-126">Określa identyfikator obiektu puli, dla której zostanie włączyć automatyczne skalowanie.</span><span class="sxs-lookup"><span data-stu-id="5ca15-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="5ca15-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca15-127">CommonParameters</span></span>
<span data-ttu-id="5ca15-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ca15-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca15-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ca15-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca15-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ca15-130">INPUTS</span></span>

### <span data-ttu-id="5ca15-131">System.String</span><span class="sxs-lookup"><span data-stu-id="5ca15-131">System.String</span></span>

### <span data-ttu-id="5ca15-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5ca15-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5ca15-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ca15-133">OUTPUTS</span></span>

### <span data-ttu-id="5ca15-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="5ca15-134">System.Void</span></span>

## <span data-ttu-id="5ca15-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5ca15-135">NOTES</span></span>

## <span data-ttu-id="5ca15-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ca15-136">RELATED LINKS</span></span>

[<span data-ttu-id="5ca15-137">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="5ca15-137">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="5ca15-138">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="5ca15-138">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="5ca15-139">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5ca15-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
