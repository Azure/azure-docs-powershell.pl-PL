---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: f4d9f8e6bb9c5592d9558aa03cfba6cd88bd38fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706457"
---
# <span data-ttu-id="6d212-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="6d212-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="6d212-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d212-102">SYNOPSIS</span></span>
<span data-ttu-id="6d212-103">Dzienniki eksportu, które pokazują całkowite ograniczone żądania API dla tej subskrypcji w danym oknie czasu.</span><span class="sxs-lookup"><span data-stu-id="6d212-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="6d212-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d212-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d212-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6d212-105">DESCRIPTION</span></span>
<span data-ttu-id="6d212-106">Spowoduje to wyeksportowanie całkowitej liczby przeprowadzonych połączeń API Microsoft. COMPUTE API.</span><span class="sxs-lookup"><span data-stu-id="6d212-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="6d212-107">Dzienniki można dodatkowo agregować, korzystając z trzech opcji: GroupByOperationName, GroupByThrottlePolicy lub GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="6d212-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="6d212-108">Pamiętaj, że to polecenie cmdlet zbiera tylko dzienniki CRP.</span><span class="sxs-lookup"><span data-stu-id="6d212-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="6d212-109">Aby zapoznać się z omówieniem ograniczania interfejsu API dostawcy zasobów obliczeniowych, zobacz https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="6d212-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="6d212-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d212-110">EXAMPLES</span></span>

### <span data-ttu-id="6d212-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6d212-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="6d212-112">To polecenie przechowuje łączną liczbę nawiązywania połączeń API obliczeniowych Microsoft. COMPUTE (2018-02-20T17:54:14 i 2018-02-22T17:54:17 w danym identyfikatorze URI SAS, zagregowanym według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="6d212-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="6d212-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d212-113">PARAMETERS</span></span>

### <span data-ttu-id="6d212-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d212-114">-AsJob</span></span>
<span data-ttu-id="6d212-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6d212-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d212-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="6d212-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="6d212-117">Identyfikator URI SAS kontenera obiektu BLOB rejestrowania, do którego LogAnalytics API zapisuje dzienniki wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="6d212-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d212-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d212-118">-DefaultProfile</span></span>
<span data-ttu-id="6d212-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d212-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d212-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="6d212-120">-FromTime</span></span>
<span data-ttu-id="6d212-121">Od czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="6d212-121">From time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d212-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="6d212-122">-GroupByOperationName</span></span>
<span data-ttu-id="6d212-123">Grupa wyniki zapytania grupy według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="6d212-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="6d212-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="6d212-124">-GroupByResourceName</span></span>
<span data-ttu-id="6d212-125">Grupa wynik kwerendy według nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="6d212-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="6d212-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="6d212-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="6d212-127">Grupa wyników zapytania grupy według zastosowanych zasad dławienia.</span><span class="sxs-lookup"><span data-stu-id="6d212-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="6d212-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6d212-128">-Location</span></span>
<span data-ttu-id="6d212-129">Lokalizacja, w której jest wysyłana kwerenda w dzienniku analitycznym.</span><span class="sxs-lookup"><span data-stu-id="6d212-129">The location upon which log analytic is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d212-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6d212-130">-NoWait</span></span>
<span data-ttu-id="6d212-131">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="6d212-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="6d212-132">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="6d212-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="6d212-133">-ToTime</span><span class="sxs-lookup"><span data-stu-id="6d212-133">-ToTime</span></span>
<span data-ttu-id="6d212-134">Do czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="6d212-134">To time of the query</span></span>

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

### <span data-ttu-id="6d212-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d212-135">-Confirm</span></span>
<span data-ttu-id="6d212-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d212-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d212-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d212-137">-WhatIf</span></span>
<span data-ttu-id="6d212-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d212-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d212-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6d212-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d212-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d212-140">CommonParameters</span></span>
<span data-ttu-id="6d212-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d212-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d212-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d212-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d212-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d212-143">INPUTS</span></span>

### <span data-ttu-id="6d212-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6d212-144">System.String</span></span>

## <span data-ttu-id="6d212-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d212-145">OUTPUTS</span></span>

### <span data-ttu-id="6d212-146">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="6d212-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="6d212-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d212-147">NOTES</span></span>

## <span data-ttu-id="6d212-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d212-148">RELATED LINKS</span></span>
