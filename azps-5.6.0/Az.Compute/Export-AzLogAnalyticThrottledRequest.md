---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 02d78a36bcd2afc6eef037a0b043c5db89d37f0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969402"
---
# <span data-ttu-id="068b3-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="068b3-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="068b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="068b3-102">SYNOPSIS</span></span>
<span data-ttu-id="068b3-103">Eksportowanie dzienników, w których jest pokazywana całkowita liczba ograniczanych żądań api dla tej subskrypcji w danym oknie czasowym.</span><span class="sxs-lookup"><span data-stu-id="068b3-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="068b3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="068b3-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] 
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="068b3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="068b3-105">DESCRIPTION</span></span>
<span data-ttu-id="068b3-106">Eksportuje całkowitą liczbę ograniczanych wywołań interfejsu API Microsoft.Compute.</span><span class="sxs-lookup"><span data-stu-id="068b3-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="068b3-107">Dzienniki można dodatkowo zagregować za pomocą pięciu opcji: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent lub GroupByApplicationId.</span><span class="sxs-lookup"><span data-stu-id="068b3-107">The logs can be further aggregated by five options: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent, or GroupByApplicationId.</span></span>
<span data-ttu-id="068b3-108">To polecenie cmdlet gromadzi tylko dzienniki CRP.</span><span class="sxs-lookup"><span data-stu-id="068b3-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="068b3-109">Aby uzyskać omówienie ograniczania interfejsu API dostawcy zasobów obliczeniowych, zobacz https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="068b3-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="068b3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="068b3-110">EXAMPLES</span></span>

### <span data-ttu-id="068b3-111">Przykład 1. Eksportowanie rekordów zagregowanych według nazwy operacji</span><span class="sxs-lookup"><span data-stu-id="068b3-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="068b3-112">To polecenie przechowuje łącznie ograniczone wywołania interfejsu API Microsoft.Compute między 2018-02-20T17:54:14 a 2018-02-22T17:54:17 w danym URI SAS, zagregowany według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="068b3-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="068b3-113">Przykład 2. Eksportowanie rekordów zagregowanych według identyfikatora aplikacji</span><span class="sxs-lookup"><span data-stu-id="068b3-113">Example 2: Export records aggregated by applicaiton id</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByApplicationId
```

<span data-ttu-id="068b3-114">To polecenie przechowuje wszystkie ograniczone wywołania interfejsu API Microsoft.Compute między 2018-02-20T17:54:14 a 2018-02-22T17:54:17 w danym identyfikatorze URI SAS, zagregowany według identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="068b3-114">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by appliction id.</span></span>

### <span data-ttu-id="068b3-115">Przykład 3. Eksportowanie rekordów zagregowanych przez agenta użytkownika</span><span class="sxs-lookup"><span data-stu-id="068b3-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByUserAgent
```

<span data-ttu-id="068b3-116">To polecenie przechowuje łącznie ograniczone wywołania interfejsu API Microsoft.Compute między 2018-02-20T17:54:14 a 2018-02-22T17:54:17 w danym identyfikatorze URI SAS zagregowany przez agenta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="068b3-116">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span>

## <span data-ttu-id="068b3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="068b3-117">PARAMETERS</span></span>

### <span data-ttu-id="068b3-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="068b3-118">-AsJob</span></span>
<span data-ttu-id="068b3-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="068b3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="068b3-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="068b3-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="068b3-121">Uri SAS kontenera obiektów blob rejestrowania, w którym interfejs API LogAnalytics zapisuje dzienniki wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="068b3-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="068b3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="068b3-122">-DefaultProfile</span></span>
<span data-ttu-id="068b3-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="068b3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="068b3-124">— FromTime</span><span class="sxs-lookup"><span data-stu-id="068b3-124">-FromTime</span></span>
<span data-ttu-id="068b3-125">Czas kwerendy</span><span class="sxs-lookup"><span data-stu-id="068b3-125">From time of the query</span></span>

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

### <span data-ttu-id="068b3-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="068b3-126">-GroupByApplicationId</span></span>
<span data-ttu-id="068b3-127">Wynik zapytania grupowania według identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="068b3-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="068b3-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="068b3-128">-GroupByOperationName</span></span>
<span data-ttu-id="068b3-129">Wynik zapytania grupowania według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="068b3-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="068b3-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="068b3-130">-GroupByResourceName</span></span>
<span data-ttu-id="068b3-131">Wynik zapytania grupowania według nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="068b3-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="068b3-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="068b3-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="068b3-133">Wynik zapytania grupowego według zastosowanych zasad ograniczania.</span><span class="sxs-lookup"><span data-stu-id="068b3-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="068b3-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="068b3-134">-GroupByUserAgent</span></span>
<span data-ttu-id="068b3-135">Wynik zapytania grupowania według Agenta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="068b3-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="068b3-136">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="068b3-136">-Location</span></span>
<span data-ttu-id="068b3-137">Lokalizacja, w której jest wyszukiwana kwerenda analityczna dziennika.</span><span class="sxs-lookup"><span data-stu-id="068b3-137">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="068b3-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="068b3-138">-NoWait</span></span>
<span data-ttu-id="068b3-139">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="068b3-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="068b3-140">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="068b3-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="068b3-141">— ToTime</span><span class="sxs-lookup"><span data-stu-id="068b3-141">-ToTime</span></span>
<span data-ttu-id="068b3-142">Czas kwerendy</span><span class="sxs-lookup"><span data-stu-id="068b3-142">To time of the query</span></span>

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

### <span data-ttu-id="068b3-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="068b3-143">-Confirm</span></span>
<span data-ttu-id="068b3-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="068b3-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="068b3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="068b3-145">-WhatIf</span></span>
<span data-ttu-id="068b3-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="068b3-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="068b3-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="068b3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="068b3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="068b3-148">CommonParameters</span></span>
<span data-ttu-id="068b3-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="068b3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="068b3-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="068b3-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="068b3-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="068b3-151">INPUTS</span></span>

### <span data-ttu-id="068b3-152">System.String</span><span class="sxs-lookup"><span data-stu-id="068b3-152">System.String</span></span>

## <span data-ttu-id="068b3-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="068b3-153">OUTPUTS</span></span>

### <span data-ttu-id="068b3-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="068b3-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="068b3-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="068b3-155">NOTES</span></span>

## <span data-ttu-id="068b3-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="068b3-156">RELATED LINKS</span></span>
