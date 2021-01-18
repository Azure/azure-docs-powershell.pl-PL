---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 79bf599b22796181c2f433f186e0e4bde8094773
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501936"
---
# <span data-ttu-id="f03e7-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="f03e7-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="f03e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f03e7-102">SYNOPSIS</span></span>
<span data-ttu-id="f03e7-103">Dzienniki eksportu, które pokazują całkowite ograniczone żądania API dla tej subskrypcji w danym oknie czasu.</span><span class="sxs-lookup"><span data-stu-id="f03e7-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="f03e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f03e7-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f03e7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f03e7-105">DESCRIPTION</span></span>
<span data-ttu-id="f03e7-106">Spowoduje to wyeksportowanie całkowitej liczby przeprowadzonych połączeń API Microsoft. COMPUTE API.</span><span class="sxs-lookup"><span data-stu-id="f03e7-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="f03e7-107">Dzienniki można dodatkowo agregować, korzystając z trzech opcji: GroupByOperationName, GroupByThrottlePolicy lub GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="f03e7-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="f03e7-108">Pamiętaj, że to polecenie cmdlet zbiera tylko dzienniki CRP.</span><span class="sxs-lookup"><span data-stu-id="f03e7-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="f03e7-109">Aby zapoznać się z omówieniem ograniczania interfejsu API dostawcy zasobów obliczeniowych, zobacz https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="f03e7-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="f03e7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f03e7-110">EXAMPLES</span></span>

### <span data-ttu-id="f03e7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f03e7-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="f03e7-112">To polecenie przechowuje łączną liczbę nawiązywania połączeń API obliczeniowych Microsoft. COMPUTE (2018-02-20T17:54:14 i 2018-02-22T17:54:17 w danym identyfikatorze URI SAS, zagregowanym według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="f03e7-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="f03e7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f03e7-113">PARAMETERS</span></span>

### <span data-ttu-id="f03e7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f03e7-114">-AsJob</span></span>
<span data-ttu-id="f03e7-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f03e7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f03e7-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="f03e7-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="f03e7-117">Identyfikator URI SAS kontenera obiektu BLOB rejestrowania, do którego LogAnalytics API zapisuje dzienniki wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="f03e7-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="f03e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f03e7-118">-DefaultProfile</span></span>
<span data-ttu-id="f03e7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f03e7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f03e7-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="f03e7-120">-FromTime</span></span>
<span data-ttu-id="f03e7-121">Od czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="f03e7-121">From time of the query</span></span>

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

### <span data-ttu-id="f03e7-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="f03e7-122">-GroupByOperationName</span></span>
<span data-ttu-id="f03e7-123">Grupa wyniki zapytania grupy według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="f03e7-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="f03e7-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="f03e7-124">-GroupByResourceName</span></span>
<span data-ttu-id="f03e7-125">Grupa wynik kwerendy według nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="f03e7-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="f03e7-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="f03e7-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="f03e7-127">Grupa wyników zapytania grupy według zastosowanych zasad dławienia.</span><span class="sxs-lookup"><span data-stu-id="f03e7-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="f03e7-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f03e7-128">-Location</span></span>
<span data-ttu-id="f03e7-129">Lokalizacja, w której jest wysyłana kwerenda w dzienniku analitycznym.</span><span class="sxs-lookup"><span data-stu-id="f03e7-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="f03e7-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f03e7-130">-NoWait</span></span>
<span data-ttu-id="f03e7-131">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="f03e7-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f03e7-132">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="f03e7-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f03e7-133">-ToTime</span><span class="sxs-lookup"><span data-stu-id="f03e7-133">-ToTime</span></span>
<span data-ttu-id="f03e7-134">Do czasu zapytania</span><span class="sxs-lookup"><span data-stu-id="f03e7-134">To time of the query</span></span>

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

### <span data-ttu-id="f03e7-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f03e7-135">-Confirm</span></span>
<span data-ttu-id="f03e7-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f03e7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f03e7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f03e7-137">-WhatIf</span></span>
<span data-ttu-id="f03e7-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f03e7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f03e7-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f03e7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f03e7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03e7-140">CommonParameters</span></span>
<span data-ttu-id="f03e7-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f03e7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03e7-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f03e7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03e7-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f03e7-143">INPUTS</span></span>

### <span data-ttu-id="f03e7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f03e7-144">System.String</span></span>

## <span data-ttu-id="f03e7-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f03e7-145">OUTPUTS</span></span>

### <span data-ttu-id="f03e7-146">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="f03e7-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="f03e7-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f03e7-147">NOTES</span></span>

## <span data-ttu-id="f03e7-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f03e7-148">RELATED LINKS</span></span>
