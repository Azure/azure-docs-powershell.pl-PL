---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticthrottledrequests
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
ms.openlocfilehash: a8deadf4760950eebbec22626bca475439ab0b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545795"
---
# <span data-ttu-id="13f5a-101">Export-AzureRmLogAnalyticThrottledRequests</span><span class="sxs-lookup"><span data-stu-id="13f5a-101">Export-AzureRmLogAnalyticThrottledRequests</span></span>

## <span data-ttu-id="13f5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="13f5a-103">Dzienniki eksportu, które pokazują całkowite ograniczone żądania API dla tej subskrypcji w danym oknie czasu.</span><span class="sxs-lookup"><span data-stu-id="13f5a-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13f5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13f5a-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticThrottledRequests [-GroupByOperationName] [-FromTime] <DateTime>
 [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String> [-GroupByResourceName] [-ToTime] <DateTime>
 [-Location] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13f5a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="13f5a-105">DESCRIPTION</span></span>
<span data-ttu-id="13f5a-106">Spowoduje to wyeksportowanie całkowitej liczby przeprowadzonych połączeń API Microsoft. COMPUTE API.</span><span class="sxs-lookup"><span data-stu-id="13f5a-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="13f5a-107">Dzienniki można dodatkowo agregować, korzystając z trzech opcji: GroupByOperationName, GroupByThrottlePolicy lub GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="13f5a-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="13f5a-108">Pamiętaj, że to polecenie cmdlet zbiera tylko dzienniki CRP.</span><span class="sxs-lookup"><span data-stu-id="13f5a-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="13f5a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13f5a-109">EXAMPLES</span></span>

### <span data-ttu-id="13f5a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13f5a-110">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticThrottledRequests -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="13f5a-111">To polecenie przechowuje łączną liczbę nawiązywania połączeń API obliczeniowych Microsoft. COMPUTE (2018-02-20T17:54:14 i 2018-02-22T17:54:17 w danym identyfikatorze URI SAS, zagregowanym według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="13f5a-111">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="13f5a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13f5a-112">PARAMETERS</span></span>

### <span data-ttu-id="13f5a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13f5a-113">-AsJob</span></span>
<span data-ttu-id="13f5a-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="13f5a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13f5a-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="13f5a-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="13f5a-116">Identyfikator URI SAS kontenera obiektu BLOB rejestrowania, do którego LogAnalytics API zapisuje dzienniki wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="13f5a-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="13f5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f5a-117">-DefaultProfile</span></span>
<span data-ttu-id="13f5a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13f5a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13f5a-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="13f5a-119">-FromTime</span></span>
<span data-ttu-id="13f5a-120">Od czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="13f5a-120">From time of the query</span></span>

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

### <span data-ttu-id="13f5a-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="13f5a-121">-GroupByOperationName</span></span>
<span data-ttu-id="13f5a-122">Grupa wyniki zapytania grupy według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="13f5a-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="13f5a-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="13f5a-123">-GroupByResourceName</span></span>
<span data-ttu-id="13f5a-124">Grupa wynik kwerendy według nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="13f5a-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="13f5a-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="13f5a-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="13f5a-126">Grupa wyników zapytania grupy według zastosowanych zasad dławienia.</span><span class="sxs-lookup"><span data-stu-id="13f5a-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="13f5a-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="13f5a-127">-Location</span></span>
<span data-ttu-id="13f5a-128">Lokalizacja, w której jest wysyłana kwerenda w dzienniku analitycznym.</span><span class="sxs-lookup"><span data-stu-id="13f5a-128">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="13f5a-129">-ToTime</span><span class="sxs-lookup"><span data-stu-id="13f5a-129">-ToTime</span></span>
<span data-ttu-id="13f5a-130">Do czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="13f5a-130">To time of the query</span></span>

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

### <span data-ttu-id="13f5a-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13f5a-131">-Confirm</span></span>
<span data-ttu-id="13f5a-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13f5a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13f5a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13f5a-133">-WhatIf</span></span>
<span data-ttu-id="13f5a-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13f5a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13f5a-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13f5a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13f5a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f5a-136">CommonParameters</span></span>
<span data-ttu-id="13f5a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13f5a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f5a-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13f5a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f5a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13f5a-139">INPUTS</span></span>

### <span data-ttu-id="13f5a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="13f5a-140">System.String</span></span>

## <span data-ttu-id="13f5a-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13f5a-141">OUTPUTS</span></span>

### <span data-ttu-id="13f5a-142">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="13f5a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="13f5a-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13f5a-143">NOTES</span></span>

## <span data-ttu-id="13f5a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13f5a-144">RELATED LINKS</span></span>
