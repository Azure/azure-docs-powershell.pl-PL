---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
ms.openlocfilehash: 73e7e9e0e4020f284b26e720e0f34ec7f11fd04f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224947"
---
# <span data-ttu-id="a532c-101">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="a532c-101">Enable-AzBatchAutoScale</span></span>

## <span data-ttu-id="a532c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a532c-102">SYNOPSIS</span></span>
<span data-ttu-id="a532c-103">Umożliwia automatyczne skalowanie puli.</span><span class="sxs-lookup"><span data-stu-id="a532c-103">Enables automatic scaling of a pool.</span></span>

## <span data-ttu-id="a532c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a532c-104">SYNTAX</span></span>

```
Enable-AzBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a532c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a532c-105">DESCRIPTION</span></span>
<span data-ttu-id="a532c-106">Polecenie cmdlet **enable-AzBatchAutoScale** umożliwia automatyczne skalowanie określonej puli.</span><span class="sxs-lookup"><span data-stu-id="a532c-106">The **Enable-AzBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="a532c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a532c-107">EXAMPLES</span></span>

### <span data-ttu-id="a532c-108">Przykład 1: Włączanie automatycznego skalowania puli</span><span class="sxs-lookup"><span data-stu-id="a532c-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="a532c-109">Pierwsze polecenie definiuje formułę, a następnie zapisuje ją w zmiennej $Formula.</span><span class="sxs-lookup"><span data-stu-id="a532c-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="a532c-110">Drugie polecenie umożliwia automatyczne skalowanie puli o nazwie Moja Pula przy użyciu formuły w $Formula.</span><span class="sxs-lookup"><span data-stu-id="a532c-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="a532c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a532c-111">PARAMETERS</span></span>

### <span data-ttu-id="a532c-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="a532c-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="a532c-113">Określa czas (w minutach), jaki upływa przed automatycznym dopasowaniem rozmiaru puli zgodnie z formułą skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="a532c-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="a532c-114">Wartość domyślna to 15 minut, a wartość minimalna to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="a532c-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="a532c-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="a532c-115">-AutoScaleFormula</span></span>
<span data-ttu-id="a532c-116">Określa formułę żądanej liczby węzłów obliczeniowych w puli.</span><span class="sxs-lookup"><span data-stu-id="a532c-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="a532c-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a532c-117">-BatchContext</span></span>
<span data-ttu-id="a532c-118">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a532c-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a532c-119">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a532c-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a532c-120">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="a532c-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a532c-121">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="a532c-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a532c-122">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a532c-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a532c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a532c-123">-DefaultProfile</span></span>
<span data-ttu-id="a532c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a532c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a532c-125">-ID</span><span class="sxs-lookup"><span data-stu-id="a532c-125">-Id</span></span>
<span data-ttu-id="a532c-126">Określa identyfikator obiektu puli, dla którego ma zostać włączone Skalowanie automatyczne.</span><span class="sxs-lookup"><span data-stu-id="a532c-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="a532c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a532c-127">CommonParameters</span></span>
<span data-ttu-id="a532c-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a532c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a532c-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a532c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a532c-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a532c-130">INPUTS</span></span>

### <span data-ttu-id="a532c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a532c-131">System.String</span></span>

### <span data-ttu-id="a532c-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a532c-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a532c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a532c-133">OUTPUTS</span></span>

### <span data-ttu-id="a532c-134">System. void</span><span class="sxs-lookup"><span data-stu-id="a532c-134">System.Void</span></span>

## <span data-ttu-id="a532c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a532c-135">NOTES</span></span>

## <span data-ttu-id="a532c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a532c-136">RELATED LINKS</span></span>

[<span data-ttu-id="a532c-137">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="a532c-137">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="a532c-138">Test — AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="a532c-138">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="a532c-139">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="a532c-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
