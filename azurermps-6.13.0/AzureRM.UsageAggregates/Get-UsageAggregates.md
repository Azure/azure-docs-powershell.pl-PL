---
external help file: Microsoft.Azure.Commands.UsageAggregates.dll-Help.xml
Module Name: AzureRM.UsageAggregates
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.usageaggregates/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/UsageAggregates/Commands.UsageAggregates/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/UsageAggregates/Commands.UsageAggregates/help/Get-UsageAggregates.md
ms.openlocfilehash: cf7554cc287ff88dbcc2569a41d50c300a43ba75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525909"
---
# <span data-ttu-id="d6073-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="d6073-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="d6073-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6073-102">SYNOPSIS</span></span>
<span data-ttu-id="d6073-103">Pobiera zgłoszone dane dotyczące użycia subskrypcji usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="d6073-103">Gets the reported Azure subscription usage details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6073-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6073-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6073-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d6073-105">DESCRIPTION</span></span>
<span data-ttu-id="d6073-106">Polecenie cmdlet **Get-UsageAggregates** pobiera zagregowane dane użycia subskrypcji platformy Azure według następujących właściwości:</span><span class="sxs-lookup"><span data-stu-id="d6073-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 
- <span data-ttu-id="d6073-107">Godziny rozpoczęcia i zakończenia użytkowania, które zostały zgłoszone.</span><span class="sxs-lookup"><span data-stu-id="d6073-107">Start and end times of when the usage was reported.</span></span>
- <span data-ttu-id="d6073-108">Precyzja agregacji — codziennie lub co godzinę.</span><span class="sxs-lookup"><span data-stu-id="d6073-108">Aggregation precision, either daily or hourly.</span></span>
- <span data-ttu-id="d6073-109">Szczegóły poziomu wystąpienia dla wielu wystąpień tego samego zasobu.</span><span class="sxs-lookup"><span data-stu-id="d6073-109">Instance level detail for multiple instances of the same resource.</span></span>
<span data-ttu-id="d6073-110">W przypadku spójnych wyników zwracanych danych zależy od tego, kiedy dane o użyciu zostały zgłoszone przez zasób platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d6073-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>
<span data-ttu-id="d6073-111">Aby uzyskać więcej informacji, zobacz informacje o interfejsie API usługi zaliczenia Azure https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) w bibliotece Microsoft Developer Network).</span><span class="sxs-lookup"><span data-stu-id="d6073-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="d6073-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6073-112">EXAMPLES</span></span>

### <span data-ttu-id="d6073-113">Przykład 1: pobieranie danych subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d6073-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="d6073-114">To polecenie pobiera zgłoszone dane dotyczące użycia subskrypcji między 5/2/2015 a 5/5/2015.</span><span class="sxs-lookup"><span data-stu-id="d6073-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="d6073-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6073-115">PARAMETERS</span></span>

### <span data-ttu-id="d6073-116">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="d6073-116">-AggregationGranularity</span></span>
<span data-ttu-id="d6073-117">Określa dokładność agregacji danych.</span><span class="sxs-lookup"><span data-stu-id="d6073-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="d6073-118">Prawidłowe wartości to: codziennie i co godzinę.</span><span class="sxs-lookup"><span data-stu-id="d6073-118">Valid values are: Daily and Hourly.</span></span>
<span data-ttu-id="d6073-119">Wartość domyślna to codziennie.</span><span class="sxs-lookup"><span data-stu-id="d6073-119">The default value is Daily.</span></span>

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6073-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="d6073-120">-ContinuationToken</span></span>
<span data-ttu-id="d6073-121">Określa token kontynuacji, który został pobrany z treści odpowiedzi w poprzedniej rozmowie.</span><span class="sxs-lookup"><span data-stu-id="d6073-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="d6073-122">W przypadku dużego zestawu wyników odpowiedzi są stronicowane przy użyciu tokenów kontynuacji.</span><span class="sxs-lookup"><span data-stu-id="d6073-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="d6073-123">Token kontynuacji służy jako Zakładka do postępu.</span><span class="sxs-lookup"><span data-stu-id="d6073-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="d6073-124">Jeśli ten parametr nie jest określony, dane są pobierane od początku dnia lub godziny określonej w *ReportedStartTime*.</span><span class="sxs-lookup"><span data-stu-id="d6073-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="d6073-125">Zalecamy, aby w przypadku tych danych obserwować łącze dalej na stronie Odpowiedz na.</span><span class="sxs-lookup"><span data-stu-id="d6073-125">We recommend that you follow the next link in the response to page though the data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6073-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6073-126">-DefaultProfile</span></span>
<span data-ttu-id="d6073-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6073-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6073-128">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="d6073-128">-ReportedEndTime</span></span>
<span data-ttu-id="d6073-129">Określa raportowaną godzinę zakończenia użycia zasobów w systemie rozliczeń Azure.</span><span class="sxs-lookup"><span data-stu-id="d6073-129">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>
<span data-ttu-id="d6073-130">Platforma Azure jest systemem rozproszonym, obejmującym wiele centrów danych na całym świecie, dlatego istnieje opóźnienie między rzeczywistym użyciem zasobu, czyli czasem użycia zasobów, a kiedy zdarzenie użycia osiągnęło system rozliczeń, czyli czas raportowania użycia zasobów.</span><span class="sxs-lookup"><span data-stu-id="d6073-130">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="d6073-131">W celu uzyskania wszystkich zdarzeń użycia dla subskrypcji zgłaszanych przez okres, zbadasz zapytanie według zgłoszonego czasu.</span><span class="sxs-lookup"><span data-stu-id="d6073-131">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="d6073-132">Mimo że kwerenda została zgłoszona przez zgłoszony czas, polecenie cmdlet agreguje dane odpowiedzi przez czas użycia zasobów.</span><span class="sxs-lookup"><span data-stu-id="d6073-132">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="d6073-133">Dane dotyczące użycia zasobów to przydatny sposób na analizowanie danych.</span><span class="sxs-lookup"><span data-stu-id="d6073-133">The resource usage data is the useful pivot for analyzing the data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6073-134">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="d6073-134">-ReportedStartTime</span></span>
<span data-ttu-id="d6073-135">Określa zgłoszony czas rozpoczęcia, po zapisaniu użycia zasobów w systemie rozliczeń Azure.</span><span class="sxs-lookup"><span data-stu-id="d6073-135">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6073-136">-ShowDetails</span><span class="sxs-lookup"><span data-stu-id="d6073-136">-ShowDetails</span></span>
<span data-ttu-id="d6073-137">Wskazuje, czy to polecenie cmdlet zwraca szczegóły na poziomie wystąpienia przy użyciu danych użycia.</span><span class="sxs-lookup"><span data-stu-id="d6073-137">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>
<span data-ttu-id="d6073-138">Wartość domyślna to $True.</span><span class="sxs-lookup"><span data-stu-id="d6073-138">The default value is $True.</span></span>
<span data-ttu-id="d6073-139">Jeśli $False, usługa agreguje wyniki po stronie serwera i w związku z tym zwraca mniej grup agregacji.</span><span class="sxs-lookup"><span data-stu-id="d6073-139">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="d6073-140">Jeśli na przykład korzystasz z trzech witryn internetowych, domyślnie otrzymasz trzy elementy wiersza, aby można było skorzystać z witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d6073-140">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="d6073-141">Jeśli jednak wartość jest $False, wszystkie dane dla tego samego identyfikatora **subskrypcji** , **meterId** , **usageStartTime** i **usageEndTime** są zwijane w jeden element linii.</span><span class="sxs-lookup"><span data-stu-id="d6073-141">However, when the value is $False, all the data for the same **subscriptionId** , **meterId** , **usageStartTime** , and **usageEndTime** is collapsed into a single line item.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6073-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6073-142">CommonParameters</span></span>
<span data-ttu-id="d6073-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6073-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6073-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6073-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6073-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6073-145">INPUTS</span></span>

### <span data-ttu-id="d6073-146">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d6073-146">None</span></span>

## <span data-ttu-id="d6073-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6073-147">OUTPUTS</span></span>

### <span data-ttu-id="d6073-148">Microsoft. Azure. Commerce. UsageAggregates. MODELES. UsageAggregationGetResponse</span><span class="sxs-lookup"><span data-stu-id="d6073-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="d6073-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6073-149">NOTES</span></span>

## <span data-ttu-id="d6073-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6073-150">RELATED LINKS</span></span>