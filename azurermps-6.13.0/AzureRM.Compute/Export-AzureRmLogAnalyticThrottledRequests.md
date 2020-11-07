---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticthrottledrequests
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
ms.openlocfilehash: 97f68475ab935df66b67f0cab92466e68732a735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541911"
---
# <span data-ttu-id="81b16-101">Export-AzureRmLogAnalyticThrottledRequests</span><span class="sxs-lookup"><span data-stu-id="81b16-101">Export-AzureRmLogAnalyticThrottledRequests</span></span>

## <span data-ttu-id="81b16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81b16-102">SYNOPSIS</span></span>
<span data-ttu-id="81b16-103">Dzienniki eksportu, które pokazują całkowite ograniczone żądania API dla tej subskrypcji w danym oknie czasu.</span><span class="sxs-lookup"><span data-stu-id="81b16-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81b16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81b16-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticThrottledRequests [-GroupByOperationName] [-FromTime] <DateTime>
 [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String> [-GroupByResourceName] [-ToTime] <DateTime>
 [-Location] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81b16-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81b16-105">DESCRIPTION</span></span>
<span data-ttu-id="81b16-106">Spowoduje to wyeksportowanie całkowitej liczby przeprowadzonych połączeń API Microsoft. COMPUTE API.</span><span class="sxs-lookup"><span data-stu-id="81b16-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="81b16-107">Dzienniki można dodatkowo agregować, korzystając z trzech opcji: GroupByOperationName, GroupByThrottlePolicy lub GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="81b16-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="81b16-108">Pamiętaj, że to polecenie cmdlet zbiera tylko dzienniki CRP.</span><span class="sxs-lookup"><span data-stu-id="81b16-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="81b16-109">Aby zapoznać się z omówieniem ograniczania interfejsu API dostawcy zasobów obliczeniowych, zobacz https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="81b16-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="81b16-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81b16-110">EXAMPLES</span></span>

### <span data-ttu-id="81b16-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="81b16-111">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticThrottledRequests -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="81b16-112">To polecenie przechowuje łączną liczbę nawiązywania połączeń API obliczeniowych Microsoft. COMPUTE (2018-02-20T17:54:14 i 2018-02-22T17:54:17 w danym identyfikatorze URI SAS, zagregowanym według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="81b16-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="81b16-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81b16-113">PARAMETERS</span></span>

### <span data-ttu-id="81b16-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81b16-114">-AsJob</span></span>
<span data-ttu-id="81b16-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="81b16-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81b16-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="81b16-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="81b16-117">Identyfikator URI SAS kontenera obiektu BLOB rejestrowania, do którego LogAnalytics API zapisuje dzienniki wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="81b16-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="81b16-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b16-118">-DefaultProfile</span></span>
<span data-ttu-id="81b16-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81b16-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81b16-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="81b16-120">-FromTime</span></span>
<span data-ttu-id="81b16-121">Od czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="81b16-121">From time of the query</span></span>

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

### <span data-ttu-id="81b16-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="81b16-122">-GroupByOperationName</span></span>
<span data-ttu-id="81b16-123">Grupa wyniki zapytania grupy według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="81b16-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="81b16-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="81b16-124">-GroupByResourceName</span></span>
<span data-ttu-id="81b16-125">Grupa wynik kwerendy według nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="81b16-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="81b16-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="81b16-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="81b16-127">Grupa wyników zapytania grupy według zastosowanych zasad dławienia.</span><span class="sxs-lookup"><span data-stu-id="81b16-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="81b16-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="81b16-128">-Location</span></span>
<span data-ttu-id="81b16-129">Lokalizacja, w której jest wysyłana kwerenda w dzienniku analitycznym.</span><span class="sxs-lookup"><span data-stu-id="81b16-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="81b16-130">-ToTime</span><span class="sxs-lookup"><span data-stu-id="81b16-130">-ToTime</span></span>
<span data-ttu-id="81b16-131">Do czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="81b16-131">To time of the query</span></span>

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

### <span data-ttu-id="81b16-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81b16-132">-Confirm</span></span>
<span data-ttu-id="81b16-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81b16-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81b16-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81b16-134">-WhatIf</span></span>
<span data-ttu-id="81b16-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81b16-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81b16-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81b16-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81b16-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b16-137">CommonParameters</span></span>
<span data-ttu-id="81b16-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81b16-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b16-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81b16-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b16-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81b16-140">INPUTS</span></span>

### <span data-ttu-id="81b16-141">System. String</span><span class="sxs-lookup"><span data-stu-id="81b16-141">System.String</span></span>

## <span data-ttu-id="81b16-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81b16-142">OUTPUTS</span></span>

### <span data-ttu-id="81b16-143">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="81b16-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="81b16-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81b16-144">NOTES</span></span>

## <span data-ttu-id="81b16-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81b16-145">RELATED LINKS</span></span>