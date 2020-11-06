---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/test-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 4258c5d83b15c2cecb6e2cd4e3edc216efec7a97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525346"
---
# <span data-ttu-id="47ffc-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="47ffc-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="47ffc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="47ffc-103">Pobiera wynik automatycznej formuły skalowania w puli.</span><span class="sxs-lookup"><span data-stu-id="47ffc-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47ffc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47ffc-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47ffc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="47ffc-105">DESCRIPTION</span></span>
<span data-ttu-id="47ffc-106">Polecenie cmdlet **test-AzureBatchAutoScale** pobiera wynik automatycznego skalowania formuły w określonej puli.</span><span class="sxs-lookup"><span data-stu-id="47ffc-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="47ffc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47ffc-107">EXAMPLES</span></span>

### <span data-ttu-id="47ffc-108">Przykład 1. Ocena formuły autoskalowania w puli</span><span class="sxs-lookup"><span data-stu-id="47ffc-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="47ffc-109">Pierwsze polecenie zapisuje formułę w zmiennej $Formula w celu użycia w przykładzie.</span><span class="sxs-lookup"><span data-stu-id="47ffc-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>

<span data-ttu-id="47ffc-110">Drugie polecenie szacuje formułę autoskalowania w puli o IDENTYFIKATORze ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="47ffc-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>

<span data-ttu-id="47ffc-111">W poleceniu ostatnie są wyświetlane **wyniki** przy użyciu standardowej składni z kropką.</span><span class="sxs-lookup"><span data-stu-id="47ffc-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="47ffc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47ffc-112">PARAMETERS</span></span>

### <span data-ttu-id="47ffc-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="47ffc-113">-AutoScaleFormula</span></span>
<span data-ttu-id="47ffc-114">Określa formułę żądanej liczby węzłów obliczeniowych w puli.</span><span class="sxs-lookup"><span data-stu-id="47ffc-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ffc-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="47ffc-115">-BatchContext</span></span>
<span data-ttu-id="47ffc-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="47ffc-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="47ffc-117">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="47ffc-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="47ffc-118">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="47ffc-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="47ffc-119">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="47ffc-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="47ffc-120">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="47ffc-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="47ffc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ffc-121">-DefaultProfile</span></span>
<span data-ttu-id="47ffc-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47ffc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47ffc-123">-ID</span><span class="sxs-lookup"><span data-stu-id="47ffc-123">-Id</span></span>
<span data-ttu-id="47ffc-124">Określa identyfikator obiektu puli, dla którego ma zostać przetestowane automatyczne skalowanie.</span><span class="sxs-lookup"><span data-stu-id="47ffc-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47ffc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ffc-125">CommonParameters</span></span>
<span data-ttu-id="47ffc-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47ffc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ffc-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47ffc-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ffc-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47ffc-128">INPUTS</span></span>

### <span data-ttu-id="47ffc-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="47ffc-129">BatchAccountContext</span></span>
<span data-ttu-id="47ffc-130">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="47ffc-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="47ffc-131">Ciąg</span><span class="sxs-lookup"><span data-stu-id="47ffc-131">String</span></span>
<span data-ttu-id="47ffc-132">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="47ffc-132">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="47ffc-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47ffc-133">OUTPUTS</span></span>

### <span data-ttu-id="47ffc-134">PSAutoScaleEvaluation</span><span class="sxs-lookup"><span data-stu-id="47ffc-134">PSAutoScaleEvaluation</span></span>

## <span data-ttu-id="47ffc-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47ffc-135">NOTES</span></span>

## <span data-ttu-id="47ffc-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47ffc-136">RELATED LINKS</span></span>

[<span data-ttu-id="47ffc-137">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="47ffc-137">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="47ffc-138">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="47ffc-138">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="47ffc-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="47ffc-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="47ffc-140">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="47ffc-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


