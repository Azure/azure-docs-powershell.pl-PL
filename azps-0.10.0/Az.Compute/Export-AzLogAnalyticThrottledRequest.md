---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-AzLogAnalyticThrottledRequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 45f0a75b07d0fae07092ffbe2b23f42cfa6d707a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893834"
---
# <span data-ttu-id="b72d2-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="b72d2-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="b72d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b72d2-102">SYNOPSIS</span></span>
<span data-ttu-id="b72d2-103">Dzienniki eksportu, które pokazują całkowite ograniczone żądania API dla tej subskrypcji w danym oknie czasu.</span><span class="sxs-lookup"><span data-stu-id="b72d2-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="b72d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b72d2-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String>
 [-GroupByOperationName]  [-GroupByThrottlePolicy] [-GroupByResourceName] 
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b72d2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b72d2-105">DESCRIPTION</span></span>
<span data-ttu-id="b72d2-106">Spowoduje to wyeksportowanie całkowitej liczby przeprowadzonych połączeń API Microsoft. COMPUTE API.</span><span class="sxs-lookup"><span data-stu-id="b72d2-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="b72d2-107">Dzienniki można dodatkowo agregować, korzystając z trzech opcji: GroupByOperationName, GroupByThrottlePolicy lub GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="b72d2-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="b72d2-108">Pamiętaj, że to polecenie cmdlet zbiera tylko dzienniki CRP.</span><span class="sxs-lookup"><span data-stu-id="b72d2-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="b72d2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b72d2-109">EXAMPLES</span></span>

### <span data-ttu-id="b72d2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b72d2-110">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="b72d2-111">To polecenie przechowuje łączną liczbę nawiązywania połączeń API obliczeniowych Microsoft. COMPUTE (2018-02-20T17:54:14 i 2018-02-22T17:54:17 w danym identyfikatorze URI SAS, zagregowanym według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="b72d2-111">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="b72d2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b72d2-112">PARAMETERS</span></span>

### <span data-ttu-id="b72d2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b72d2-113">-AsJob</span></span>
<span data-ttu-id="b72d2-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b72d2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b72d2-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="b72d2-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="b72d2-116">Identyfikator URI SAS kontenera obiektu BLOB rejestrowania, do którego LogAnalytics API zapisuje dzienniki wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="b72d2-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="b72d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b72d2-117">-DefaultProfile</span></span>
<span data-ttu-id="b72d2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b72d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b72d2-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="b72d2-119">-FromTime</span></span>
<span data-ttu-id="b72d2-120">Od czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="b72d2-120">From time of the query</span></span>

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

### <span data-ttu-id="b72d2-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="b72d2-121">-GroupByOperationName</span></span>
<span data-ttu-id="b72d2-122">Grupa wyniki zapytania grupy według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="b72d2-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="b72d2-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="b72d2-123">-GroupByResourceName</span></span>
<span data-ttu-id="b72d2-124">Grupa wynik kwerendy według nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="b72d2-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="b72d2-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="b72d2-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="b72d2-126">Grupa wyników zapytania grupy według zastosowanych zasad dławienia.</span><span class="sxs-lookup"><span data-stu-id="b72d2-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="b72d2-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b72d2-127">-Location</span></span>
<span data-ttu-id="b72d2-128">Lokalizacja, w której jest wysyłana kwerenda w dzienniku analitycznym.</span><span class="sxs-lookup"><span data-stu-id="b72d2-128">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="b72d2-129">-ToTime</span><span class="sxs-lookup"><span data-stu-id="b72d2-129">-ToTime</span></span>
<span data-ttu-id="b72d2-130">Do czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="b72d2-130">To time of the query</span></span>

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

### <span data-ttu-id="b72d2-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b72d2-131">-Confirm</span></span>
<span data-ttu-id="b72d2-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b72d2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b72d2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b72d2-133">-WhatIf</span></span>
<span data-ttu-id="b72d2-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b72d2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b72d2-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b72d2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b72d2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b72d2-136">CommonParameters</span></span>
<span data-ttu-id="b72d2-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b72d2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b72d2-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b72d2-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b72d2-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b72d2-139">INPUTS</span></span>

### <span data-ttu-id="b72d2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b72d2-140">System.String</span></span>

## <span data-ttu-id="b72d2-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b72d2-141">OUTPUTS</span></span>

### <span data-ttu-id="b72d2-142">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="b72d2-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="b72d2-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b72d2-143">NOTES</span></span>

## <span data-ttu-id="b72d2-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b72d2-144">RELATED LINKS</span></span>

