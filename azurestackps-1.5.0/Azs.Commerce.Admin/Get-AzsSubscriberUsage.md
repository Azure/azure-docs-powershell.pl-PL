---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 12b98727cdb8e6d31fb1aaf1a2215b79a6b982e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523718"
---
# <span data-ttu-id="80405-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="80405-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="80405-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80405-102">SYNOPSIS</span></span>
<span data-ttu-id="80405-103">Pobierz dane dotyczące użycia podczas określonego czasu.</span><span class="sxs-lookup"><span data-stu-id="80405-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="80405-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80405-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="80405-105">Opis</span><span class="sxs-lookup"><span data-stu-id="80405-105">DESCRIPTION</span></span>
<span data-ttu-id="80405-106">Pobierz dane dotyczące użycia podczas określonego czasu.</span><span class="sxs-lookup"><span data-stu-id="80405-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="80405-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80405-107">EXAMPLES</span></span>

### <span data-ttu-id="80405-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="80405-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="80405-109">Pobierz dane użycia z ostatnich 24 godzin.</span><span class="sxs-lookup"><span data-stu-id="80405-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="80405-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80405-110">PARAMETERS</span></span>

### <span data-ttu-id="80405-111">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="80405-111">-AggregationGranularity</span></span>
<span data-ttu-id="80405-112">Stopień szczegółowości agregacji.</span><span class="sxs-lookup"><span data-stu-id="80405-112">The aggregation granularity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80405-113">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="80405-113">-ContinuationToken</span></span>
<span data-ttu-id="80405-114">Token kontynuacji.</span><span class="sxs-lookup"><span data-stu-id="80405-114">The continuation token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80405-115">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="80405-115">-ReportedEndTime</span></span>
<span data-ttu-id="80405-116">Zgłoszona godzina zakończenia (z wyłączeniem).</span><span class="sxs-lookup"><span data-stu-id="80405-116">The reported end time (exclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80405-117">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="80405-117">-ReportedStartTime</span></span>
<span data-ttu-id="80405-118">Zgłoszona godzina rozpoczęcia (włącznie).</span><span class="sxs-lookup"><span data-stu-id="80405-118">The reported start time (inclusive).</span></span>

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

### <span data-ttu-id="80405-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="80405-119">-Skip</span></span>
<span data-ttu-id="80405-120">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="80405-120">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80405-121">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="80405-121">-SubscriberId</span></span>
<span data-ttu-id="80405-122">Identyfikator subskrypcji dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="80405-122">The tenant subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80405-123">-Początek</span><span class="sxs-lookup"><span data-stu-id="80405-123">-Top</span></span>
<span data-ttu-id="80405-124">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="80405-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="80405-125">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="80405-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80405-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80405-126">CommonParameters</span></span>
<span data-ttu-id="80405-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80405-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80405-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80405-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80405-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80405-129">INPUTS</span></span>

## <span data-ttu-id="80405-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80405-130">OUTPUTS</span></span>

### <span data-ttu-id="80405-131">Microsoft. AzureStack. Management. Commerce. admin. models. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="80405-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="80405-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80405-132">NOTES</span></span>

## <span data-ttu-id="80405-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80405-133">RELATED LINKS</span></span>

