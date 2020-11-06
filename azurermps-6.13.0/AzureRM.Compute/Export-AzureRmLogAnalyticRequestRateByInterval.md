---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: c4008e9b6587e0b6c5b8ed56057490b0aad8764f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550323"
---
# <span data-ttu-id="f57dd-101">Export-AzureRmLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="f57dd-101">Export-AzureRmLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="f57dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f57dd-102">SYNOPSIS</span></span>
<span data-ttu-id="f57dd-103">Eksportuj dzienniki pokazujące żądania API wprowadzone przez tę subskrypcję w danym oknie czasu, aby pokazać działania ograniczające.</span><span class="sxs-lookup"><span data-stu-id="f57dd-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f57dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f57dd-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticRequestRateByInterval [-FromTime] <DateTime> [-GroupByOperationName]
 [-IntervalLength] <IntervalInMins> [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String>
 [-GroupByResourceName] [-ToTime] <DateTime> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f57dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f57dd-105">DESCRIPTION</span></span>
<span data-ttu-id="f57dd-106">Umożliwia eksportowanie danych statystycznych dotyczących rozmów subskrypcji do usługi Microsoft. COMPUTE API według stanu powodzenia, awarii lub ograniczenia, w wstępnie zdefiniowanych interwałach.</span><span class="sxs-lookup"><span data-stu-id="f57dd-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="f57dd-107">Dzienniki mogą być pogrupowane według trzech parametrów: GroupByOperationName, GroupByThrottlePolicy lub GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="f57dd-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="f57dd-108">Należy pamiętać, że w tym poleceniu cmdlet są zbierane tylko dzienniki dostawcy zasobów. Ponadto dane dotyczące typów zasobów dysk i migawka nie są jeszcze dostępne.</span><span class="sxs-lookup"><span data-stu-id="f57dd-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="f57dd-109">Aby zapoznać się z omówieniem ograniczania interfejsu API dostawcy zasobów obliczeniowych, zobacz https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="f57dd-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="f57dd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f57dd-110">EXAMPLES</span></span>

### <span data-ttu-id="f57dd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f57dd-111">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="f57dd-112">To polecenie przechowuje zagregowane liczby funkcji Microsoft. COMPUTE API, rozdzielone sukcesem, niepowodzeniem lub ograniczeniem między 2018-02-20T17:54:14 i 2018-02-22T17:54:17 w danym IDENTYFIKATORze SAS, zagregowanym według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="f57dd-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="f57dd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f57dd-113">PARAMETERS</span></span>

### <span data-ttu-id="f57dd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f57dd-114">-AsJob</span></span>
<span data-ttu-id="f57dd-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f57dd-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f57dd-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="f57dd-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="f57dd-117">Identyfikator URI SAS kontenera obiektu BLOB rejestrowania, do którego LogAnalytics API zapisuje dzienniki wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="f57dd-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f57dd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f57dd-118">-DefaultProfile</span></span>
<span data-ttu-id="f57dd-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f57dd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f57dd-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="f57dd-120">-FromTime</span></span>
<span data-ttu-id="f57dd-121">Od czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="f57dd-121">From time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f57dd-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="f57dd-122">-GroupByOperationName</span></span>
<span data-ttu-id="f57dd-123">Grupa wyniki zapytania grupy według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="f57dd-123">Group query result by Operation Name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f57dd-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="f57dd-124">-GroupByResourceName</span></span>
<span data-ttu-id="f57dd-125">Grupa wynik kwerendy według nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="f57dd-125">Group query result by Resource Name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f57dd-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="f57dd-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="f57dd-127">Grupa wyników zapytania grupy według zastosowanych zasad dławienia.</span><span class="sxs-lookup"><span data-stu-id="f57dd-127">Group query result by Throttle Policy applied.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f57dd-128">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="f57dd-128">-IntervalLength</span></span>
<span data-ttu-id="f57dd-129">Wartość interwału wyrażona w minutach używana do tworzenia dzienników stawek rozmów LogAnalytics.</span><span class="sxs-lookup"><span data-stu-id="f57dd-129">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f57dd-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f57dd-130">-Location</span></span>
<span data-ttu-id="f57dd-131">Lokalizacja, w której jest wysyłana kwerenda w dzienniku analitycznym.</span><span class="sxs-lookup"><span data-stu-id="f57dd-131">The location upon which log analytic is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f57dd-132">-ToTime</span><span class="sxs-lookup"><span data-stu-id="f57dd-132">-ToTime</span></span>
<span data-ttu-id="f57dd-133">Do czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="f57dd-133">To time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f57dd-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f57dd-134">-Confirm</span></span>
<span data-ttu-id="f57dd-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f57dd-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f57dd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f57dd-136">-WhatIf</span></span>
<span data-ttu-id="f57dd-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f57dd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f57dd-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f57dd-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f57dd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f57dd-139">CommonParameters</span></span>
<span data-ttu-id="f57dd-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f57dd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f57dd-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f57dd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f57dd-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f57dd-142">INPUTS</span></span>

### <span data-ttu-id="f57dd-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f57dd-143">System.String</span></span>

## <span data-ttu-id="f57dd-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f57dd-144">OUTPUTS</span></span>

### <span data-ttu-id="f57dd-145">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="f57dd-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="f57dd-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f57dd-146">NOTES</span></span>

## <span data-ttu-id="f57dd-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f57dd-147">RELATED LINKS</span></span>
