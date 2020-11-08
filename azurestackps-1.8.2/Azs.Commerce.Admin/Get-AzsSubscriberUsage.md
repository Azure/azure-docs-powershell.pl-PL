---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f45a90d4f8e8c3072393c5dc959885636b64dce
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055767"
---
# <span data-ttu-id="45c4f-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="45c4f-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="45c4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="45c4f-103">Pobierz dane dotyczące użycia podczas określonego czasu.</span><span class="sxs-lookup"><span data-stu-id="45c4f-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="45c4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45c4f-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="45c4f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45c4f-105">DESCRIPTION</span></span>
<span data-ttu-id="45c4f-106">Pobierz dane dotyczące użycia podczas określonego czasu.</span><span class="sxs-lookup"><span data-stu-id="45c4f-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="45c4f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45c4f-107">EXAMPLES</span></span>

### <span data-ttu-id="45c4f-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="45c4f-108">EXAMPLE 1</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="45c4f-109">Pobierz dane użycia z ostatnich 24 godzin.</span><span class="sxs-lookup"><span data-stu-id="45c4f-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="45c4f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45c4f-110">PARAMETERS</span></span>

### <span data-ttu-id="45c4f-111">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="45c4f-111">-SubscriberId</span></span>
<span data-ttu-id="45c4f-112">Identyfikator subskrypcji dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="45c4f-112">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="45c4f-113">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="45c4f-113">-ReportedStartTime</span></span>
<span data-ttu-id="45c4f-114">Zgłoszona godzina rozpoczęcia (włącznie).</span><span class="sxs-lookup"><span data-stu-id="45c4f-114">The reported start time (inclusive).</span></span>

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

### <span data-ttu-id="45c4f-115">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="45c4f-115">-AggregationGranularity</span></span>
<span data-ttu-id="45c4f-116">Stopień szczegółowości agregacji.</span><span class="sxs-lookup"><span data-stu-id="45c4f-116">The aggregation granularity.</span></span>

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

### <span data-ttu-id="45c4f-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="45c4f-117">-Skip</span></span>
<span data-ttu-id="45c4f-118">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="45c4f-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="45c4f-119">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="45c4f-119">-ReportedEndTime</span></span>
<span data-ttu-id="45c4f-120">Zgłoszona godzina zakończenia (z wyłączeniem).</span><span class="sxs-lookup"><span data-stu-id="45c4f-120">The reported end time (exclusive).</span></span>

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

### <span data-ttu-id="45c4f-121">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="45c4f-121">-ContinuationToken</span></span>
<span data-ttu-id="45c4f-122">Token kontynuacji.</span><span class="sxs-lookup"><span data-stu-id="45c4f-122">The continuation token.</span></span>

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

### <span data-ttu-id="45c4f-123">-Początek</span><span class="sxs-lookup"><span data-stu-id="45c4f-123">-Top</span></span>
<span data-ttu-id="45c4f-124">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="45c4f-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="45c4f-125">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="45c4f-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="45c4f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c4f-126">CommonParameters</span></span>
<span data-ttu-id="45c4f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45c4f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c4f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45c4f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c4f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45c4f-129">INPUTS</span></span>

## <span data-ttu-id="45c4f-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45c4f-130">OUTPUTS</span></span>

### <span data-ttu-id="45c4f-131">Microsoft. AzureStack. Management. Commerce. admin. models. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="45c4f-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="45c4f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45c4f-132">NOTES</span></span>

## <span data-ttu-id="45c4f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45c4f-133">RELATED LINKS</span></span>
