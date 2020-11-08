---
external help file: ''
Module Name: Azs.Commerce.Admin
online version: https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage
schema: 2.0.0
ms.openlocfilehash: 9eed3f6f2a4d07bd48136c50ec173f801b30c928
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054310"
---
# <span data-ttu-id="657f8-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="657f8-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="657f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="657f8-102">SYNOPSIS</span></span>
<span data-ttu-id="657f8-103">Pobiera kolekcję SubscriberUsageAggregates, które są UsageAggregates od użytkowników.</span><span class="sxs-lookup"><span data-stu-id="657f8-103">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="657f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="657f8-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage -ReportedEndTime <DateTime> -ReportedStartTime <DateTime> [-SubscriptionId <String[]>]
 [-AggregationGranularity <String>] [-ContinuationToken <String>] [-SubscriberId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="657f8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="657f8-105">DESCRIPTION</span></span>
<span data-ttu-id="657f8-106">Pobiera kolekcję SubscriberUsageAggregates, które są UsageAggregates od użytkowników.</span><span class="sxs-lookup"><span data-stu-id="657f8-106">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="657f8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="657f8-107">EXAMPLES</span></span>

### <span data-ttu-id="657f8-108">Przykład 1: pobieranie danych użycia zagregowanych według dni</span><span class="sxs-lookup"><span data-stu-id="657f8-108">Example 1: Get usage data aggregated by day</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-31T00:00:00Z" -AggregationGranularity Daily
```

<span data-ttu-id="657f8-109">Pobierz dane dotyczące użycia dla całego dnia 30 grudnia 2019 (czas UTC) dla wszystkich dzierżawców w ramach dostawcy zagregowanego przez dany dzień.</span><span class="sxs-lookup"><span data-stu-id="657f8-109">Get the usage data for the entire day of 30th Dec 2019 (in UTC) for all tenants under provider aggregated by the day.</span></span>
<span data-ttu-id="657f8-110">ReportedStartTime i ReportedEndTime muszą być zaokrąglone do dni.</span><span class="sxs-lookup"><span data-stu-id="657f8-110">ReportedStartTime and ReportedEndTime must be rounded to days.</span></span>
<span data-ttu-id="657f8-111">Jeśli jest wywoływana jako administrator usługi, w ten sposób przedstawiane są wszystkie dane dotyczące użycia dla każdej dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="657f8-111">If called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

### <span data-ttu-id="657f8-112">Przykład 2: pobieranie danych użycia zagregowanych o godzinie</span><span class="sxs-lookup"><span data-stu-id="657f8-112">Example 2: Get usage data aggregated by the hour</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-30T02:00:00Z" -AggregationGranularity Hourly
```

<span data-ttu-id="657f8-113">Pobierz dane dotyczące użycia między 12am-2AM w 30 Dec 2019 (czas UTC) zagregowanych o godzinie.</span><span class="sxs-lookup"><span data-stu-id="657f8-113">Get the usage data between  12am - 2am on 30th Dec 2019 (in UTC) aggregated by the hour.</span></span>
<span data-ttu-id="657f8-114">ReportedStartTime i ReportedEndTime muszą być zaokrąglane do godzin.</span><span class="sxs-lookup"><span data-stu-id="657f8-114">ReportedStartTime and ReportedEndTime must be rounded to hours.</span></span>
<span data-ttu-id="657f8-115">Podobnie, jeśli jest wywoływana jako administrator usługi, w ten sposób wszystkie dane dotyczące użycia dla każdej dzierżawy są wyświetlane w ten sposób.</span><span class="sxs-lookup"><span data-stu-id="657f8-115">Likewise, if called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

## <span data-ttu-id="657f8-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="657f8-116">PARAMETERS</span></span>

### <span data-ttu-id="657f8-117">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="657f8-117">-AggregationGranularity</span></span>
<span data-ttu-id="657f8-118">Stopień szczegółowości agregacji.</span><span class="sxs-lookup"><span data-stu-id="657f8-118">The aggregation granularity.</span></span>

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

### <span data-ttu-id="657f8-119">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="657f8-119">-ContinuationToken</span></span>
<span data-ttu-id="657f8-120">Token kontynuacji.</span><span class="sxs-lookup"><span data-stu-id="657f8-120">The continuation token.</span></span>

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

### <span data-ttu-id="657f8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="657f8-121">-DefaultProfile</span></span>
<span data-ttu-id="657f8-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="657f8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="657f8-123">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="657f8-123">-ReportedEndTime</span></span>
<span data-ttu-id="657f8-124">Zgłoszona godzina zakończenia (z wyłączeniem).</span><span class="sxs-lookup"><span data-stu-id="657f8-124">The reported end time (exclusive).</span></span>

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

### <span data-ttu-id="657f8-125">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="657f8-125">-ReportedStartTime</span></span>
<span data-ttu-id="657f8-126">Zgłoszona godzina rozpoczęcia (włącznie).</span><span class="sxs-lookup"><span data-stu-id="657f8-126">The reported start time (inclusive).</span></span>

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

### <span data-ttu-id="657f8-127">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="657f8-127">-SubscriberId</span></span>
<span data-ttu-id="657f8-128">Identyfikator subskrypcji dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="657f8-128">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="657f8-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="657f8-129">-SubscriptionId</span></span>
<span data-ttu-id="657f8-130">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="657f8-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="657f8-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="657f8-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="657f8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="657f8-132">CommonParameters</span></span>
<span data-ttu-id="657f8-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="657f8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="657f8-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="657f8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="657f8-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="657f8-135">INPUTS</span></span>

## <span data-ttu-id="657f8-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="657f8-136">OUTPUTS</span></span>

### <span data-ttu-id="657f8-137">Microsoft. Azure. PowerShell. polecenia cmdlet. Commerce. modele. Api20150601Preview. IUsageAggregate</span><span class="sxs-lookup"><span data-stu-id="657f8-137">Microsoft.Azure.PowerShell.Cmdlets.Commerce.Models.Api20150601Preview.IUsageAggregate</span></span>



## <span data-ttu-id="657f8-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="657f8-138">NOTES</span></span>

## <span data-ttu-id="657f8-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="657f8-139">RELATED LINKS</span></span>

