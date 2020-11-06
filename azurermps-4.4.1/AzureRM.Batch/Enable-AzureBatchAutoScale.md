---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
ms.openlocfilehash: 1a85ac52622bb752b2e3437eb096f229c4d8e762
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554026"
---
# <span data-ttu-id="03e73-101">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="03e73-101">Enable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="03e73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03e73-102">SYNOPSIS</span></span>
<span data-ttu-id="03e73-103">Umożliwia automatyczne skalowanie puli.</span><span class="sxs-lookup"><span data-stu-id="03e73-103">Enables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03e73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03e73-104">SYNTAX</span></span>

```
Enable-AzureBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03e73-105">Opis</span><span class="sxs-lookup"><span data-stu-id="03e73-105">DESCRIPTION</span></span>
<span data-ttu-id="03e73-106">Polecenie cmdlet **enable-AzureBatchAutoScale** umożliwia automatyczne skalowanie określonej puli.</span><span class="sxs-lookup"><span data-stu-id="03e73-106">The **Enable-AzureBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="03e73-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03e73-107">EXAMPLES</span></span>

### <span data-ttu-id="03e73-108">Przykład 1: Włączanie automatycznego skalowania puli</span><span class="sxs-lookup"><span data-stu-id="03e73-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzureBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="03e73-109">Pierwsze polecenie definiuje formułę, a następnie zapisuje ją w zmiennej $Formula.</span><span class="sxs-lookup"><span data-stu-id="03e73-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>

<span data-ttu-id="03e73-110">Drugie polecenie umożliwia automatyczne skalowanie puli o nazwie Moja Pula przy użyciu formuły w $Formula.</span><span class="sxs-lookup"><span data-stu-id="03e73-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="03e73-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03e73-111">PARAMETERS</span></span>

### <span data-ttu-id="03e73-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="03e73-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="03e73-113">Określa czas (w minutach), jaki upływa przed automatycznym dopasowaniem rozmiaru puli zgodnie z formułą skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="03e73-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="03e73-114">Wartość domyślna to 15 minut, a wartość minimalna to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="03e73-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="03e73-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="03e73-115">-AutoScaleFormula</span></span>
<span data-ttu-id="03e73-116">Określa formułę żądanej liczby węzłów obliczeniowych w puli.</span><span class="sxs-lookup"><span data-stu-id="03e73-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="03e73-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="03e73-117">-BatchContext</span></span>
<span data-ttu-id="03e73-118">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="03e73-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="03e73-119">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="03e73-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="03e73-120">-ID</span><span class="sxs-lookup"><span data-stu-id="03e73-120">-Id</span></span>
<span data-ttu-id="03e73-121">Określa identyfikator obiektu puli, dla którego ma zostać włączone Skalowanie automatyczne.</span><span class="sxs-lookup"><span data-stu-id="03e73-121">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="03e73-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e73-122">-DefaultProfile</span></span>
<span data-ttu-id="03e73-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03e73-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03e73-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e73-124">CommonParameters</span></span>
<span data-ttu-id="03e73-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03e73-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e73-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03e73-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e73-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03e73-127">INPUTS</span></span>

### <span data-ttu-id="03e73-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="03e73-128">BatchAccountContext</span></span>
<span data-ttu-id="03e73-129">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="03e73-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="03e73-130">Ciąg</span><span class="sxs-lookup"><span data-stu-id="03e73-130">String</span></span>
<span data-ttu-id="03e73-131">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="03e73-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="03e73-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03e73-132">OUTPUTS</span></span>

## <span data-ttu-id="03e73-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03e73-133">NOTES</span></span>

## <span data-ttu-id="03e73-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03e73-134">RELATED LINKS</span></span>

[<span data-ttu-id="03e73-135">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="03e73-135">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="03e73-136">Test — AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="03e73-136">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="03e73-137">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="03e73-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


