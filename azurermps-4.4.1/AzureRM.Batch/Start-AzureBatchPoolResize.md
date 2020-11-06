---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: 558f8c062e60f6e9f7c18c05be8f1ccb2eafa9fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548355"
---
# <span data-ttu-id="f4476-101">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="f4476-101">Start-AzureBatchPoolResize</span></span>

## <span data-ttu-id="f4476-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4476-102">SYNOPSIS</span></span>
<span data-ttu-id="f4476-103">Rozpoczynanie zmieniania rozmiaru puli.</span><span class="sxs-lookup"><span data-stu-id="f4476-103">Starts to resize a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4476-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4476-104">SYNTAX</span></span>

```
Start-AzureBatchPoolResize [-Id] <String> -TargetDedicated <Int32> [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4476-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f4476-105">DESCRIPTION</span></span>
<span data-ttu-id="f4476-106">Polecenie cmdlet **Start-AzureBatchPoolResize** rozpoczyna operację zmiany rozmiaru wsadu Azure Part na puli.</span><span class="sxs-lookup"><span data-stu-id="f4476-106">The **Start-AzureBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="f4476-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4476-107">EXAMPLES</span></span>

### <span data-ttu-id="f4476-108">Przykład 1: Zmienianie rozmiaru puli na 12 węzłów</span><span class="sxs-lookup"><span data-stu-id="f4476-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicated 12 -BatchContext $Context
```

<span data-ttu-id="f4476-109">To polecenie rozpoczyna operację zmiany rozmiaru puli o IDENTYFIKATORze ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="f4476-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="f4476-110">Elementem docelowym tej operacji jest 12 dedykowanych węzłów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="f4476-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="f4476-111">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="f4476-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f4476-112">Przykład 2: Zmienianie rozmiaru puli przy użyciu opcji dealokacji</span><span class="sxs-lookup"><span data-stu-id="f4476-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicated 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="f4476-113">To polecenie cmdlet umożliwia zmienianie rozmiaru puli na pięć dedykowanych węzłów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="f4476-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="f4476-114">Polecenie pobiera pulę o IDENTYFIKATORze ContosoPool06 przy użyciu polecenia cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="f4476-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="f4476-115">Polecenie przekazuje ten obiekt puli do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="f4476-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f4476-116">Polecenie rozpoczyna operację zmiany rozmiaru w puli.</span><span class="sxs-lookup"><span data-stu-id="f4476-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="f4476-117">Celem jest pięć dedykowanych węzłów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="f4476-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="f4476-118">To polecenie określa czas trwania jednej godziny.</span><span class="sxs-lookup"><span data-stu-id="f4476-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="f4476-119">Polecenie określa opcję rozdzielania, którą można zakończyć.</span><span class="sxs-lookup"><span data-stu-id="f4476-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="f4476-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4476-120">PARAMETERS</span></span>

### <span data-ttu-id="f4476-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f4476-121">-BatchContext</span></span>
<span data-ttu-id="f4476-122">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="f4476-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f4476-123">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="f4476-123">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="f4476-124">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="f4476-124">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="f4476-125">Określa opcję dealokacji dla operacji zmiany rozmiaru, która zostanie uruchomiona przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4476-125">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="f4476-126">-ID</span><span class="sxs-lookup"><span data-stu-id="f4476-126">-Id</span></span>
<span data-ttu-id="f4476-127">Określa identyfikator puli, której rozmiar tego polecenia cmdlet zmienia.</span><span class="sxs-lookup"><span data-stu-id="f4476-127">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="f4476-128">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="f4476-128">-ResizeTimeout</span></span>
<span data-ttu-id="f4476-129">Określa okres limitu czasu dla operacji zmiany rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="f4476-129">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="f4476-130">Jeśli pula nie dociera do rozmiaru docelowego, operacja zmiany rozmiaru zostaje zatrzymana.</span><span class="sxs-lookup"><span data-stu-id="f4476-130">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="f4476-131">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="f4476-131">-TargetDedicated</span></span>
<span data-ttu-id="f4476-132">Określa liczbę docelową dedykowanych węzłów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="f4476-132">Specifies the target number of dedicated compute nodes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4476-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4476-133">-DefaultProfile</span></span>
<span data-ttu-id="f4476-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4476-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4476-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4476-135">CommonParameters</span></span>
<span data-ttu-id="f4476-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4476-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4476-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4476-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4476-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4476-138">INPUTS</span></span>

### <span data-ttu-id="f4476-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f4476-139">BatchAccountContext</span></span>
<span data-ttu-id="f4476-140">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="f4476-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="f4476-141">Ciąg</span><span class="sxs-lookup"><span data-stu-id="f4476-141">String</span></span>
<span data-ttu-id="f4476-142">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="f4476-142">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f4476-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4476-143">OUTPUTS</span></span>

## <span data-ttu-id="f4476-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4476-144">NOTES</span></span>

## <span data-ttu-id="f4476-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4476-145">RELATED LINKS</span></span>

[<span data-ttu-id="f4476-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f4476-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f4476-147">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="f4476-147">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="f4476-148">Zatrzymaj — AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="f4476-148">Stop-AzureBatchPoolResize</span></span>](./Stop-AzureBatchPoolResize.md)

[<span data-ttu-id="f4476-149">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="f4476-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


