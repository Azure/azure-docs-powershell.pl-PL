---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: 7d23774085bb467ca091aa500cf67ee43fa2aa46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981249"
---
# <span data-ttu-id="857c2-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="857c2-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="857c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="857c2-102">SYNOPSIS</span></span>
<span data-ttu-id="857c2-103">Pobiera metryk użycia puli dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="857c2-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="857c2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="857c2-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="857c2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="857c2-105">DESCRIPTION</span></span>
<span data-ttu-id="857c2-106">Polecenie **cmdlet Get-AzBatchPoolUsageMetric** pobiera metryki użycia, agregowane według puli w poszczególnych interwałach czasowych dla określonego konta.</span><span class="sxs-lookup"><span data-stu-id="857c2-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="857c2-107">Możesz uzyskać statystykę dla konkretnej puli i przedziału czasu.</span><span class="sxs-lookup"><span data-stu-id="857c2-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="857c2-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="857c2-108">EXAMPLES</span></span>

### <span data-ttu-id="857c2-109">Przykład 1. Uzyskiwanie metryk użycia puli dla przedziału czasu</span><span class="sxs-lookup"><span data-stu-id="857c2-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzBatchPoolUsageMetric -StartTime $StartTime -EndTime $EndTime -BatchContext $context
DataEgressGiB      : 6.68875873088837E-06
DataIngressGiB     : 1.9485130906105E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 8
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.61587512493134E-06
DataIngressGiB     : 1.76150351762772E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4

DataEgressGiB      : 7.36676156520844E-06
DataIngressGiB     : 2.10804864764214E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 7.99999999955555
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.80586493015289E-06
DataIngressGiB     : 1.80602073669434E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 11.9999999993333
VirtualMachineSize : standard_d4
```

<span data-ttu-id="857c2-110">Pierwsze polecenie tworzy odwołanie do obiektu do kluczy konta dla konta partii o nazwie ContosoBatchAccount przy użyciu polecenia **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="857c2-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="857c2-111">Polecenie przechowuje to odwołanie do obiektu w $Context zmienną.</span><span class="sxs-lookup"><span data-stu-id="857c2-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="857c2-112">Następne dwa polecenia tworzą obiekty **DateTime** przy użyciu Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="857c2-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="857c2-113">Polecenia przechowują te wartości w $StartTime i $EndTime zmiennych do użycia z końcowym poleceniem.</span><span class="sxs-lookup"><span data-stu-id="857c2-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="857c2-114">Ostatnie polecenie zwraca wszystkie metryki użycia puli, zagregowane według puli, w interwale czasu między określonym czasem rozpoczęcia i zakończenia.</span><span class="sxs-lookup"><span data-stu-id="857c2-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="857c2-115">Przykład 2. Uzyskiwanie metryk użycia puli przy użyciu filtru</span><span class="sxs-lookup"><span data-stu-id="857c2-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzBatchPoolUsageMetric -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="857c2-116">To polecenie zwraca metryki użycia dla puli o nazwie ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="857c2-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="857c2-117">To polecenie określa ciąg filtru określający tę pulę i używa tej samej $Context wartości, co w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="857c2-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="857c2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="857c2-118">PARAMETERS</span></span>

### <span data-ttu-id="857c2-119">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="857c2-119">-BatchContext</span></span>
<span data-ttu-id="857c2-120">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="857c2-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="857c2-121">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="857c2-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="857c2-122">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="857c2-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="857c2-123">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="857c2-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="857c2-124">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="857c2-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="857c2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857c2-125">-DefaultProfile</span></span>
<span data-ttu-id="857c2-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="857c2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="857c2-127">- EndTime</span><span class="sxs-lookup"><span data-stu-id="857c2-127">-EndTime</span></span>
<span data-ttu-id="857c2-128">Określa koniec zakresu czasu, dla którego to polecenie cmdlet pobiera metryki użycia.</span><span class="sxs-lookup"><span data-stu-id="857c2-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="857c2-129">Określ czas o co najmniej dwie godziny wcześniej.</span><span class="sxs-lookup"><span data-stu-id="857c2-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="857c2-130">Jeśli nie określisz czasu zakończenia, to polecenie cmdlet użyje ostatniego dostępnego interwału agregacji.</span><span class="sxs-lookup"><span data-stu-id="857c2-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857c2-131">— Filtr</span><span class="sxs-lookup"><span data-stu-id="857c2-131">-Filter</span></span>
<span data-ttu-id="857c2-132">Określa klauzulę filtru OData, która ma być filtrowana w celu filtrowania metryk zwracanych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="857c2-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet returns.</span></span>
<span data-ttu-id="857c2-133">Jedyną prawidłową właściwością **jest poolId** z wartością ciągu.</span><span class="sxs-lookup"><span data-stu-id="857c2-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="857c2-134">Możliwe operacje to: eq, ge, gt, le, lt, startswith.</span><span class="sxs-lookup"><span data-stu-id="857c2-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="857c2-135">— StartTime</span><span class="sxs-lookup"><span data-stu-id="857c2-135">-StartTime</span></span>
<span data-ttu-id="857c2-136">Określa początek zakresu czasu, dla którego to polecenie cmdlet pobiera metryki użycia.</span><span class="sxs-lookup"><span data-stu-id="857c2-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="857c2-137">Określ czas co najmniej dwie i pół godziny wcześniej.</span><span class="sxs-lookup"><span data-stu-id="857c2-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="857c2-138">Jeśli nie określisz czasu rozpoczęcia, to polecenie cmdlet użyje ostatniego dostępnego interwału agregacji.</span><span class="sxs-lookup"><span data-stu-id="857c2-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857c2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857c2-139">CommonParameters</span></span>
<span data-ttu-id="857c2-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="857c2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857c2-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="857c2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857c2-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="857c2-142">INPUTS</span></span>

### <span data-ttu-id="857c2-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="857c2-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="857c2-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="857c2-144">OUTPUTS</span></span>

### <span data-ttu-id="857c2-145">Microsoft.Azure.Commands.Batch. Models.PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="857c2-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="857c2-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="857c2-146">NOTES</span></span>

## <span data-ttu-id="857c2-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="857c2-147">RELATED LINKS</span></span>

[<span data-ttu-id="857c2-148">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="857c2-148">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="857c2-149">Get-AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="857c2-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="857c2-150">Get-AzBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="857c2-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)
