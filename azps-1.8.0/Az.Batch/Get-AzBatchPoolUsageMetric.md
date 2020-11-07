---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: 480a39602f0218ed05122005a657c7e7870f7e88
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710838"
---
# <span data-ttu-id="f2c55-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="f2c55-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="f2c55-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2c55-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c55-103">Pobiera metryki użycia puli dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="f2c55-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="f2c55-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2c55-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2c55-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f2c55-105">DESCRIPTION</span></span>
<span data-ttu-id="f2c55-106">Polecenie cmdlet **Get-AzBatchPoolUsageMetric** pobiera metryki użycia, zagregowane według puli w poszczególnych przedziałach czasu, dla określonego konta.</span><span class="sxs-lookup"><span data-stu-id="f2c55-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="f2c55-107">Można uzyskać statystykę dla określonej puli i dla określonego zakresu czasu.</span><span class="sxs-lookup"><span data-stu-id="f2c55-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="f2c55-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2c55-108">EXAMPLES</span></span>

### <span data-ttu-id="f2c55-109">Przykład 1: pobieranie metryk użycia puli dla zakresu czasu</span><span class="sxs-lookup"><span data-stu-id="f2c55-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
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

<span data-ttu-id="f2c55-110">Pierwsze polecenie tworzy odwołanie obiektu do kluczy konta dla konta wsadowego o nazwie ContosoBatchAccount przy użyciu polecenia **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="f2c55-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="f2c55-111">Polecenie zapisuje to odwołanie do obiektu w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="f2c55-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="f2c55-112">Następne dwa polecenia tworzą obiekty **DateTime** przy użyciu Get-Date polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2c55-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="f2c55-113">Te wartości są przechowywane w poleceniach $StartTime i $EndTime zmiennych do użycia z poleceniem Final.</span><span class="sxs-lookup"><span data-stu-id="f2c55-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="f2c55-114">Ostatnie polecenie zwraca wszystkie metryki użycia puli, zagregowane według puli, w okresie między określonymi godzinami rozpoczęcia i zakończenia.</span><span class="sxs-lookup"><span data-stu-id="f2c55-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="f2c55-115">Przykład 2: uzyskiwanie metryk użycia puli za pomocą filtru</span><span class="sxs-lookup"><span data-stu-id="f2c55-115">Example 2: Get pool usage metrics by using a filter</span></span>
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

<span data-ttu-id="f2c55-116">To polecenie zwraca metryki użycia dla puli o nazwie ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="f2c55-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="f2c55-117">Polecenie określa ciąg filtru umożliwiający określenie tej puli i używa tej samej wartości $Context, co w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="f2c55-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="f2c55-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2c55-118">PARAMETERS</span></span>

### <span data-ttu-id="f2c55-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f2c55-119">-BatchContext</span></span>
<span data-ttu-id="f2c55-120">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="f2c55-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f2c55-121">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="f2c55-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f2c55-122">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="f2c55-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f2c55-123">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="f2c55-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f2c55-124">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f2c55-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f2c55-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2c55-125">-DefaultProfile</span></span>
<span data-ttu-id="f2c55-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2c55-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2c55-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f2c55-127">-EndTime</span></span>
<span data-ttu-id="f2c55-128">Określa koniec zakresu czasu, dla którego to polecenie cmdlet pobiera metryki użycia.</span><span class="sxs-lookup"><span data-stu-id="f2c55-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="f2c55-129">Określ godzinę wcześniejszą niż dwie godziny.</span><span class="sxs-lookup"><span data-stu-id="f2c55-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="f2c55-130">Jeśli nie określisz godziny zakończenia, to polecenie cmdlet będzie korzystać z ostatniego dostępnego interwału agregacji.</span><span class="sxs-lookup"><span data-stu-id="f2c55-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="f2c55-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="f2c55-131">-Filter</span></span>
<span data-ttu-id="f2c55-132">Określa klauzulę filtru OData używaną do filtrowania metryk, które to polecenie cmdlet retruns.</span><span class="sxs-lookup"><span data-stu-id="f2c55-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet retruns.</span></span>
<span data-ttu-id="f2c55-133">Jedyną prawidłową właściwością jest **poolId** z wartością ciągu.</span><span class="sxs-lookup"><span data-stu-id="f2c55-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="f2c55-134">Możliwe są następujące operacje: EQ, GE, gt, Le, lt, StartsWith.</span><span class="sxs-lookup"><span data-stu-id="f2c55-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="f2c55-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f2c55-135">-StartTime</span></span>
<span data-ttu-id="f2c55-136">Określa początek zakresu czasu, dla którego to polecenie cmdlet pobiera metryki użycia.</span><span class="sxs-lookup"><span data-stu-id="f2c55-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="f2c55-137">Określ czas co najmniej dwóch i pół godziny.</span><span class="sxs-lookup"><span data-stu-id="f2c55-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="f2c55-138">Jeśli nie określisz godziny rozpoczęcia, to polecenie cmdlet będzie korzystać z ostatniego dostępnego interwału agregacji.</span><span class="sxs-lookup"><span data-stu-id="f2c55-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="f2c55-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c55-139">CommonParameters</span></span>
<span data-ttu-id="f2c55-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2c55-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c55-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2c55-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c55-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2c55-142">INPUTS</span></span>

### <span data-ttu-id="f2c55-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f2c55-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f2c55-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2c55-144">OUTPUTS</span></span>

### <span data-ttu-id="f2c55-145">Microsoft.Azure.Commands.Batch. Modele. PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="f2c55-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="f2c55-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2c55-146">NOTES</span></span>

## <span data-ttu-id="f2c55-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2c55-147">RELATED LINKS</span></span>

[<span data-ttu-id="f2c55-148">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f2c55-148">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f2c55-149">Get-AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="f2c55-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="f2c55-150">Get-AzBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="f2c55-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)

