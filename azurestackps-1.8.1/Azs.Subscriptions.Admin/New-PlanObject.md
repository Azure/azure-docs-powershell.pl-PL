---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04c79f659f2dcf1d4100151ff0506722482aaad5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889517"
---
# <span data-ttu-id="8b432-101">New-PlanObject</span><span class="sxs-lookup"><span data-stu-id="8b432-101">New-PlanObject</span></span>

## <span data-ttu-id="8b432-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b432-102">SYNOPSIS</span></span>
<span data-ttu-id="8b432-103">Plan przedstawia pakiet przydziałów i możliwości oferowanych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="8b432-103">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="8b432-104">Dzierżawa może uzyskać ten plan za pośrednictwem oferty uaktualnienia jej dostępu do podstawowych usług w chmurze.</span><span class="sxs-lookup"><span data-stu-id="8b432-104">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="8b432-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b432-105">SYNTAX</span></span>

```
New-PlanObject [[-Description] <String>] [[-Id] <String>] [[-Type] <String>] [[-SkuIds] <String[]>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-ExternalReferenceId] <String>] [[-Name] <String>] [[-DisplayName] <String>] [[-Location] <String>]
 [[-QuotaIds] <String[]>] [[-SubscriptionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="8b432-106">Opis</span><span class="sxs-lookup"><span data-stu-id="8b432-106">DESCRIPTION</span></span>
<span data-ttu-id="8b432-107">Plan przedstawia pakiet przydziałów i możliwości oferowanych dzierżaw.</span><span class="sxs-lookup"><span data-stu-id="8b432-107">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="8b432-108">Dzierżawa może uzyskać ten plan za pośrednictwem oferty uaktualnienia jej dostępu do podstawowych usług w chmurze.</span><span class="sxs-lookup"><span data-stu-id="8b432-108">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="8b432-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b432-109">EXAMPLES</span></span>

### <span data-ttu-id="8b432-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b432-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="8b432-111">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="8b432-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="8b432-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b432-112">PARAMETERS</span></span>

### <span data-ttu-id="8b432-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="8b432-113">-Description</span></span>
<span data-ttu-id="8b432-114">Opis planu.</span><span class="sxs-lookup"><span data-stu-id="8b432-114">Description of the plan.</span></span>

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

### <span data-ttu-id="8b432-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8b432-115">-DisplayName</span></span>
<span data-ttu-id="8b432-116">Nazwa wyświetlana.</span><span class="sxs-lookup"><span data-stu-id="8b432-116">Display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b432-117">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="8b432-117">-ExternalReferenceId</span></span>
<span data-ttu-id="8b432-118">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="8b432-118">External reference identifier.</span></span>

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

### <span data-ttu-id="8b432-119">-ID</span><span class="sxs-lookup"><span data-stu-id="8b432-119">-Id</span></span>
<span data-ttu-id="8b432-120">Identyfikator URI zasobu.</span><span class="sxs-lookup"><span data-stu-id="8b432-120">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b432-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8b432-121">-Location</span></span>
<span data-ttu-id="8b432-122">Lokalizacja, w której zasób jest lokalizacją.</span><span class="sxs-lookup"><span data-stu-id="8b432-122">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b432-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8b432-123">-Name</span></span>
<span data-ttu-id="8b432-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8b432-124">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b432-125">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="8b432-125">-QuotaIds</span></span>
<span data-ttu-id="8b432-126">Identyfikatory przydziałów w ramach planu.</span><span class="sxs-lookup"><span data-stu-id="8b432-126">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b432-127">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="8b432-127">-SkuIds</span></span>
<span data-ttu-id="8b432-128">Identyfikatory wersji SKU.</span><span class="sxs-lookup"><span data-stu-id="8b432-128">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b432-129">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="8b432-129">-SubscriptionCount</span></span>
<span data-ttu-id="8b432-130">Liczba abonamentów.</span><span class="sxs-lookup"><span data-stu-id="8b432-130">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b432-131">-Tagi</span><span class="sxs-lookup"><span data-stu-id="8b432-131">-Tags</span></span>
<span data-ttu-id="8b432-132">Lista par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="8b432-132">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b432-133">-Type</span><span class="sxs-lookup"><span data-stu-id="8b432-133">-Type</span></span>
<span data-ttu-id="8b432-134">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="8b432-134">Type of resource.</span></span>

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

### <span data-ttu-id="8b432-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b432-135">CommonParameters</span></span>
<span data-ttu-id="8b432-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b432-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b432-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b432-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b432-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b432-138">INPUTS</span></span>

## <span data-ttu-id="8b432-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b432-139">OUTPUTS</span></span>

## <span data-ttu-id="8b432-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b432-140">NOTES</span></span>

## <span data-ttu-id="8b432-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b432-141">RELATED LINKS</span></span>

