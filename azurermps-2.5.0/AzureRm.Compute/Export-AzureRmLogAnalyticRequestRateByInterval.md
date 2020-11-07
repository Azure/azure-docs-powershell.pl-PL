---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticrequestratebyinterval
schema: 2.0.0
ms.openlocfilehash: 4e55da6a5f0fbacab9b7af834c2729a2f79c1995
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898082"
---
# <span data-ttu-id="39eec-101">Export-AzureRmLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="39eec-101">Export-AzureRmLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="39eec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39eec-102">SYNOPSIS</span></span>
<span data-ttu-id="39eec-103">Eksportuj dzienniki pokazujące żądania API wprowadzone przez tę subskrypcję w danym oknie czasu, aby pokazać działania ograniczające.</span><span class="sxs-lookup"><span data-stu-id="39eec-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39eec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39eec-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticRequestRateByInterval  [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins>
 [-GroupByOperationName] [-GroupByThrottlePolicy] [-GroupByResourceName] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39eec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="39eec-105">DESCRIPTION</span></span>
<span data-ttu-id="39eec-106">Spowoduje to wyeksportowanie zagregowanych liczb z funkcji Microsoft. obliczeniowych wywołań API, rozdzielonych sukcesem, niepowodzeniem lub ograniczeniem wyświetlanym w odstępach czasu.</span><span class="sxs-lookup"><span data-stu-id="39eec-106">This exports aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled displayed in time intervals.</span></span>
<span data-ttu-id="39eec-107">Dzienniki mogą być pogrupowane według trzech parametrów: GroupByOperationName, GroupByThrottlePolicy lub GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="39eec-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="39eec-108">Pamiętaj, że to polecenie cmdlet zbiera tylko dzienniki CRP.</span><span class="sxs-lookup"><span data-stu-id="39eec-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="39eec-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39eec-109">EXAMPLES</span></span>

### <span data-ttu-id="39eec-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="39eec-110">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="39eec-111">To polecenie przechowuje zagregowane liczby funkcji Microsoft. COMPUTE API, rozdzielone sukcesem, niepowodzeniem lub ograniczeniem między 2018-02-20T17:54:14 i 2018-02-22T17:54:17 w danym IDENTYFIKATORze SAS, zagregowanym według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="39eec-111">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="39eec-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39eec-112">PARAMETERS</span></span>

### <span data-ttu-id="39eec-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39eec-113">-AsJob</span></span>
<span data-ttu-id="39eec-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="39eec-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39eec-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="39eec-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="39eec-116">Identyfikator URI SAS kontenera obiektu BLOB rejestrowania, do którego LogAnalytics API zapisuje dzienniki wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="39eec-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39eec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39eec-117">-DefaultProfile</span></span>
<span data-ttu-id="39eec-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="39eec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39eec-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="39eec-119">-FromTime</span></span>
<span data-ttu-id="39eec-120">Od czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="39eec-120">From time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39eec-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="39eec-121">-GroupByOperationName</span></span>
<span data-ttu-id="39eec-122">Grupa wyniki zapytania grupy według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="39eec-122">Group query result by Operation Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39eec-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="39eec-123">-GroupByResourceName</span></span>
<span data-ttu-id="39eec-124">Grupa wynik kwerendy według nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="39eec-124">Group query result by Resource Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39eec-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="39eec-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="39eec-126">Grupa wyników zapytania grupy według zastosowanych zasad dławienia.</span><span class="sxs-lookup"><span data-stu-id="39eec-126">Group query result by Throttle Policy applied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39eec-127">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="39eec-127">-IntervalLength</span></span>
<span data-ttu-id="39eec-128">Wartość interwału wyrażona w minutach używana do tworzenia dzienników stawek rozmów LogAnalytics.</span><span class="sxs-lookup"><span data-stu-id="39eec-128">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: IntervalInMins
Parameter Sets: (All)
Aliases: 
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39eec-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="39eec-129">-Location</span></span>
<span data-ttu-id="39eec-130">Lokalizacja, w której jest wysyłana kwerenda w dzienniku analitycznym.</span><span class="sxs-lookup"><span data-stu-id="39eec-130">The location upon which log analytic is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39eec-131">-ToTime</span><span class="sxs-lookup"><span data-stu-id="39eec-131">-ToTime</span></span>
<span data-ttu-id="39eec-132">Do czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="39eec-132">To time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39eec-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39eec-133">-Confirm</span></span>
<span data-ttu-id="39eec-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39eec-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39eec-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39eec-135">-WhatIf</span></span>
<span data-ttu-id="39eec-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39eec-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39eec-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="39eec-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39eec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39eec-138">CommonParameters</span></span>
<span data-ttu-id="39eec-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39eec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39eec-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39eec-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39eec-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39eec-141">INPUTS</span></span>

### <span data-ttu-id="39eec-142">System. String</span><span class="sxs-lookup"><span data-stu-id="39eec-142">System.String</span></span>

## <span data-ttu-id="39eec-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39eec-143">OUTPUTS</span></span>

### <span data-ttu-id="39eec-144">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="39eec-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="39eec-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39eec-145">NOTES</span></span>

## <span data-ttu-id="39eec-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39eec-146">RELATED LINKS</span></span>

