---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: dcac72f8ca362ea87d464e024d6e77b2b3b61425
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710783"
---
# <span data-ttu-id="6ffcb-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="6ffcb-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="6ffcb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ffcb-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffcb-103">Pobiera wynik automatycznej formuły skalowania w puli.</span><span class="sxs-lookup"><span data-stu-id="6ffcb-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="6ffcb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ffcb-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ffcb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ffcb-105">DESCRIPTION</span></span>
<span data-ttu-id="6ffcb-106">Polecenie cmdlet **test-AzBatchAutoScale** pobiera wynik automatycznego skalowania formuły w określonej puli.</span><span class="sxs-lookup"><span data-stu-id="6ffcb-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="6ffcb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ffcb-107">EXAMPLES</span></span>

### <span data-ttu-id="6ffcb-108">Przykład 1. Ocena formuły autoskalowania w puli</span><span class="sxs-lookup"><span data-stu-id="6ffcb-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="6ffcb-109">Pierwsze polecenie zapisuje formułę w zmiennej $Formula w celu użycia w przykładzie.</span><span class="sxs-lookup"><span data-stu-id="6ffcb-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="6ffcb-110">Drugie polecenie szacuje formułę autoskalowania w puli o IDENTYFIKATORze ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="6ffcb-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="6ffcb-111">W poleceniu ostatnie są wyświetlane **wyniki** przy użyciu standardowej składni z kropką.</span><span class="sxs-lookup"><span data-stu-id="6ffcb-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="6ffcb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ffcb-112">PARAMETERS</span></span>

### <span data-ttu-id="6ffcb-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="6ffcb-113">-AutoScaleFormula</span></span>
<span data-ttu-id="6ffcb-114">Określa formułę żądanej liczby węzłów obliczeniowych w puli.</span><span class="sxs-lookup"><span data-stu-id="6ffcb-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="6ffcb-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6ffcb-115">-BatchContext</span></span>
<span data-ttu-id="6ffcb-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="6ffcb-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6ffcb-117">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="6ffcb-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6ffcb-118">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="6ffcb-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6ffcb-119">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="6ffcb-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6ffcb-120">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6ffcb-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6ffcb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ffcb-121">-DefaultProfile</span></span>
<span data-ttu-id="6ffcb-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ffcb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ffcb-123">-ID</span><span class="sxs-lookup"><span data-stu-id="6ffcb-123">-Id</span></span>
<span data-ttu-id="6ffcb-124">Określa identyfikator obiektu puli, dla którego ma zostać przetestowane automatyczne skalowanie.</span><span class="sxs-lookup"><span data-stu-id="6ffcb-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="6ffcb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffcb-125">CommonParameters</span></span>
<span data-ttu-id="6ffcb-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ffcb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffcb-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ffcb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffcb-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ffcb-128">INPUTS</span></span>

### <span data-ttu-id="6ffcb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6ffcb-129">System.String</span></span>

### <span data-ttu-id="6ffcb-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6ffcb-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6ffcb-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ffcb-131">OUTPUTS</span></span>

### <span data-ttu-id="6ffcb-132">Microsoft.Azure.Commands.Batch. Modele. PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="6ffcb-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="6ffcb-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ffcb-133">NOTES</span></span>

## <span data-ttu-id="6ffcb-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ffcb-134">RELATED LINKS</span></span>

[<span data-ttu-id="6ffcb-135">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="6ffcb-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="6ffcb-136">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="6ffcb-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="6ffcb-137">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6ffcb-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6ffcb-138">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="6ffcb-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


