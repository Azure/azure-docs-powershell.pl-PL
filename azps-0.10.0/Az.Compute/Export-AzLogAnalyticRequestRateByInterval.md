---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: bbf275b08421265130da898b670b46c95b15c34c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893833"
---
# <span data-ttu-id="b4ef8-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="b4ef8-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="b4ef8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4ef8-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ef8-103">Eksportuj dzienniki pokazujące żądania API wprowadzone przez tę subskrypcję w danym oknie czasu, aby pokazać działania ograniczające.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="b4ef8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4ef8-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval  [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins>
 [-GroupByOperationName] [-GroupByThrottlePolicy] [-GroupByResourceName] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4ef8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b4ef8-105">DESCRIPTION</span></span>
<span data-ttu-id="b4ef8-106">Spowoduje to wyeksportowanie zagregowanych liczb z funkcji Microsoft. obliczeniowych wywołań API, rozdzielonych sukcesem, niepowodzeniem lub ograniczeniem wyświetlanym w odstępach czasu.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-106">This exports aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled displayed in time intervals.</span></span>
<span data-ttu-id="b4ef8-107">Dzienniki mogą być pogrupowane według trzech parametrów: GroupByOperationName, GroupByThrottlePolicy lub GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="b4ef8-108">Pamiętaj, że to polecenie cmdlet zbiera tylko dzienniki CRP.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="b4ef8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4ef8-109">EXAMPLES</span></span>

### <span data-ttu-id="b4ef8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b4ef8-110">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="b4ef8-111">To polecenie przechowuje zagregowane liczby funkcji Microsoft. COMPUTE API, rozdzielone sukcesem, niepowodzeniem lub ograniczeniem między 2018-02-20T17:54:14 i 2018-02-22T17:54:17 w danym IDENTYFIKATORze SAS, zagregowanym według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-111">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="b4ef8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4ef8-112">PARAMETERS</span></span>

### <span data-ttu-id="b4ef8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4ef8-113">-AsJob</span></span>
<span data-ttu-id="b4ef8-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b4ef8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4ef8-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="b4ef8-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="b4ef8-116">Identyfikator URI SAS kontenera obiektu BLOB rejestrowania, do którego LogAnalytics API zapisuje dzienniki wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="b4ef8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ef8-117">-DefaultProfile</span></span>
<span data-ttu-id="b4ef8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4ef8-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="b4ef8-119">-FromTime</span></span>
<span data-ttu-id="b4ef8-120">Od czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="b4ef8-120">From time of the query</span></span>

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

### <span data-ttu-id="b4ef8-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="b4ef8-121">-GroupByOperationName</span></span>
<span data-ttu-id="b4ef8-122">Grupa wyniki zapytania grupy według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="b4ef8-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="b4ef8-123">-GroupByResourceName</span></span>
<span data-ttu-id="b4ef8-124">Grupa wynik kwerendy według nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="b4ef8-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="b4ef8-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="b4ef8-126">Grupa wyników zapytania grupy według zastosowanych zasad dławienia.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="b4ef8-127">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="b4ef8-127">-IntervalLength</span></span>
<span data-ttu-id="b4ef8-128">Wartość interwału wyrażona w minutach używana do tworzenia dzienników stawek rozmów LogAnalytics.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-128">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

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

### <span data-ttu-id="b4ef8-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b4ef8-129">-Location</span></span>
<span data-ttu-id="b4ef8-130">Lokalizacja, w której jest wysyłana kwerenda w dzienniku analitycznym.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-130">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="b4ef8-131">-ToTime</span><span class="sxs-lookup"><span data-stu-id="b4ef8-131">-ToTime</span></span>
<span data-ttu-id="b4ef8-132">Do czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="b4ef8-132">To time of the query</span></span>

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

### <span data-ttu-id="b4ef8-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4ef8-133">-Confirm</span></span>
<span data-ttu-id="b4ef8-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4ef8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4ef8-135">-WhatIf</span></span>
<span data-ttu-id="b4ef8-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4ef8-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4ef8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ef8-138">CommonParameters</span></span>
<span data-ttu-id="b4ef8-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4ef8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ef8-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4ef8-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ef8-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4ef8-141">INPUTS</span></span>

### <span data-ttu-id="b4ef8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b4ef8-142">System.String</span></span>

## <span data-ttu-id="b4ef8-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4ef8-143">OUTPUTS</span></span>

### <span data-ttu-id="b4ef8-144">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="b4ef8-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="b4ef8-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4ef8-145">NOTES</span></span>

## <span data-ttu-id="b4ef8-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4ef8-146">RELATED LINKS</span></span>

