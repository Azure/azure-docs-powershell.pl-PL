---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: feae2282f6b989b8d595b2a51cd147975e689174
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969409"
---
# <span data-ttu-id="1b947-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="1b947-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="1b947-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b947-102">SYNOPSIS</span></span>
<span data-ttu-id="1b947-103">Eksportowanie dzienników, w których są wyświetlane żądania interfejsu Api wykonane przez tę subskrypcję w danym oknie czasowym w celu pokazania działań ograniczania.</span><span class="sxs-lookup"><span data-stu-id="1b947-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="1b947-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1b947-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b947-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1b947-105">DESCRIPTION</span></span>
<span data-ttu-id="1b947-106">Eksportuje dane statystyczne dotyczące połączeń subskrypcji do interfejsu API Microsoft.Compute na podstawie stanu "Sukces", "Niepowodzenie" lub "Ograniczone" we wstępnie zdefiniowanych interwałach czasowych.</span><span class="sxs-lookup"><span data-stu-id="1b947-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="1b947-107">Dzienniki można dalej grupować według pięciu parametrów: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent lub GroupByApplicationId.</span><span class="sxs-lookup"><span data-stu-id="1b947-107">The logs can be further grouped by five parameters: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent, or GroupByApplicationId.</span></span>
<span data-ttu-id="1b947-108">To polecenie cmdlet gromadzi tylko dzienniki dostawcy zasobów obliczeniowych. Ponadto dane o typach zasobów Dysk i Migawka nie są jeszcze dostępne.</span><span class="sxs-lookup"><span data-stu-id="1b947-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="1b947-109">Aby uzyskać omówienie ograniczania interfejsu API dostawcy zasobów obliczeniowych, zobacz https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="1b947-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="1b947-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1b947-110">EXAMPLES</span></span>

### <span data-ttu-id="1b947-111">Przykład 1. Eksportowanie rekordów zagregowanych według nazwy operacji</span><span class="sxs-lookup"><span data-stu-id="1b947-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             operationName   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <operationName> 10            10                 0
2/21/2018  7:30:00 PM <operationName> 8             8                  0
2/21/2018  9:00:00 PM <operationName> 9             9                  0

```

<span data-ttu-id="1b947-112">To polecenie przechowuje zagregowane liczby wywołań interfejsu API Microsoft.Compute rozdzielone sukcesem, niepowodzeniem lub ograniczeniem między 2018-02-20T17:54:14 i 2018-02-22T17:54:17 w danym URI SAS, zagregowanym według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="1b947-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="1b947-113">Przykład 2. Eksportowanie rekordów zagregowanych według identyfikatora aplikacji</span><span class="sxs-lookup"><span data-stu-id="1b947-113">Example 2: Export records aggregated by application id</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByApplicationId

This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             clientApplicationId   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <clientApplicationId> 10            10                 0
2/21/2018  7:30:00 PM <clientApplicationId> 8             8                  0
2/21/2018  9:00:00 PM <clientApplicationId> 9             9                  0

```

<span data-ttu-id="1b947-114">To polecenie przechowuje zagregowane liczby wywołań interfejsu API Microsoft.Compute rozdzielone sukcesem, niepowodzeniem lub ograniczeniem między 2018-02-20T17:54:14 i 2018-02-22T17:54:17 w danym identyfikatorze SAS, zagregowanym według identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1b947-114">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by application id.</span></span> 

### <span data-ttu-id="1b947-115">Przykład 3. Eksportowanie rekordów zagregowanych przez agenta użytkownika</span><span class="sxs-lookup"><span data-stu-id="1b947-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByUserAgent
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             userAgent   TotalRequests SuccessfulRequests ThrottledRequests
---------             ---------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <userAgent> 10            10                 0
2/21/2018  7:30:00 PM <userAgent> 8             8                  0
2/21/2018  9:00:00 PM <userAgent> 9             9                  0

```

<span data-ttu-id="1b947-116">To polecenie przechowuje zagregowane liczby wywołań interfejsu API Microsoft.Compute rozdzielone sukcesem, niepowodzeniem lub ograniczeniem między 2018-02-20T17:54:14 i 2018-02-22T17:54:17 w danym identyfikatorze URI SAS zagregowanym przez agenta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1b947-116">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span> 

## <span data-ttu-id="1b947-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b947-117">PARAMETERS</span></span>

### <span data-ttu-id="1b947-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1b947-118">-AsJob</span></span>
<span data-ttu-id="1b947-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1b947-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b947-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="1b947-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="1b947-121">Uri SAS kontenera obiektów blob rejestrowania, w którym interfejs API LogAnalytics zapisuje dzienniki wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="1b947-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="1b947-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b947-122">-DefaultProfile</span></span>
<span data-ttu-id="1b947-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b947-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b947-124">— FromTime</span><span class="sxs-lookup"><span data-stu-id="1b947-124">-FromTime</span></span>
<span data-ttu-id="1b947-125">Czas kwerendy</span><span class="sxs-lookup"><span data-stu-id="1b947-125">From time of the query</span></span>

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

### <span data-ttu-id="1b947-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="1b947-126">-GroupByApplicationId</span></span>
<span data-ttu-id="1b947-127">Wynik zapytania grupowania według identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1b947-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="1b947-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="1b947-128">-GroupByOperationName</span></span>
<span data-ttu-id="1b947-129">Wynik zapytania grupowania według nazwy operacji.</span><span class="sxs-lookup"><span data-stu-id="1b947-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="1b947-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="1b947-130">-GroupByResourceName</span></span>
<span data-ttu-id="1b947-131">Wynik zapytania grupowania według nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="1b947-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="1b947-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="1b947-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="1b947-133">Wynik zapytania grupowego według zastosowanych zasad ograniczania.</span><span class="sxs-lookup"><span data-stu-id="1b947-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="1b947-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="1b947-134">-GroupByUserAgent</span></span>
<span data-ttu-id="1b947-135">Wynik zapytania grupowania według Agenta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1b947-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="1b947-136">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="1b947-136">-IntervalLength</span></span>
<span data-ttu-id="1b947-137">Wartość interwału w minutach używana do tworzenia dzienników stawek połączeń usługi LogAnalytics.</span><span class="sxs-lookup"><span data-stu-id="1b947-137">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b947-138">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1b947-138">-Location</span></span>
<span data-ttu-id="1b947-139">Lokalizacja, w której jest wyszukiwana kwerenda analityczna dziennika.</span><span class="sxs-lookup"><span data-stu-id="1b947-139">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="1b947-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1b947-140">-NoWait</span></span>
<span data-ttu-id="1b947-141">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="1b947-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="1b947-142">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="1b947-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="1b947-143">— ToTime</span><span class="sxs-lookup"><span data-stu-id="1b947-143">-ToTime</span></span>
<span data-ttu-id="1b947-144">Czas kwerendy</span><span class="sxs-lookup"><span data-stu-id="1b947-144">To time of the query</span></span>

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

### <span data-ttu-id="1b947-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b947-145">-Confirm</span></span>
<span data-ttu-id="1b947-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1b947-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b947-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b947-147">-WhatIf</span></span>
<span data-ttu-id="1b947-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b947-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b947-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1b947-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b947-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b947-150">CommonParameters</span></span>
<span data-ttu-id="1b947-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b947-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b947-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b947-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b947-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b947-153">INPUTS</span></span>

### <span data-ttu-id="1b947-154">System.String</span><span class="sxs-lookup"><span data-stu-id="1b947-154">System.String</span></span>

## <span data-ttu-id="1b947-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b947-155">OUTPUTS</span></span>

### <span data-ttu-id="1b947-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="1b947-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="1b947-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1b947-157">NOTES</span></span>

## <span data-ttu-id="1b947-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b947-158">RELATED LINKS</span></span>
