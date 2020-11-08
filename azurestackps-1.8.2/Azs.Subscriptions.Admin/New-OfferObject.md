---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5526ccd8fe050f9aa81974c8ea4ae1872125c087
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055660"
---
# <span data-ttu-id="c16ec-101">New-OfferObject</span><span class="sxs-lookup"><span data-stu-id="c16ec-101">New-OfferObject</span></span>

## <span data-ttu-id="c16ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c16ec-102">SYNOPSIS</span></span>
<span data-ttu-id="c16ec-103">Przedstawia oferowanie usług, za które można utworzyć abonament.</span><span class="sxs-lookup"><span data-stu-id="c16ec-103">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="c16ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c16ec-104">SYNTAX</span></span>

```
New-OfferObject [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Type] <String>] [[-MaxSubscriptionsPerAccount] <Int64>] [[-Name] <String>] [[-BasePlanIds] <String[]>]
 [[-DisplayName] <String>] [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-Location] <String>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [<CommonParameters>]
```

## <span data-ttu-id="c16ec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c16ec-105">DESCRIPTION</span></span>
<span data-ttu-id="c16ec-106">Przedstawia oferowanie usług, za które można utworzyć abonament.</span><span class="sxs-lookup"><span data-stu-id="c16ec-106">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="c16ec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c16ec-107">EXAMPLES</span></span>

### <span data-ttu-id="c16ec-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c16ec-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c16ec-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="c16ec-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c16ec-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c16ec-110">PARAMETERS</span></span>

### <span data-ttu-id="c16ec-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="c16ec-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="c16ec-112">Odwołania do planów dodatków, które dzierżawa mogą opcjonalnie nabyć jako część oferty.</span><span class="sxs-lookup"><span data-stu-id="c16ec-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c16ec-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="c16ec-113">-BasePlanIds</span></span>
<span data-ttu-id="c16ec-114">Identyfikatory planów podstawowych, które są dostępne dla dzierżawy natychmiast po zasubskrybowaniu oferty przez dzierżawcę.</span><span class="sxs-lookup"><span data-stu-id="c16ec-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c16ec-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="c16ec-115">-Description</span></span>
<span data-ttu-id="c16ec-116">Opis oferty.</span><span class="sxs-lookup"><span data-stu-id="c16ec-116">Description of offer.</span></span>

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

### <span data-ttu-id="c16ec-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c16ec-117">-DisplayName</span></span>
<span data-ttu-id="c16ec-118">Nazwa wyświetlana oferty.</span><span class="sxs-lookup"><span data-stu-id="c16ec-118">Display name of offer.</span></span>

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

### <span data-ttu-id="c16ec-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="c16ec-119">-ExternalReferenceId</span></span>
<span data-ttu-id="c16ec-120">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="c16ec-120">External reference identifier.</span></span>

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

### <span data-ttu-id="c16ec-121">-ID</span><span class="sxs-lookup"><span data-stu-id="c16ec-121">-Id</span></span>
<span data-ttu-id="c16ec-122">Identyfikator URI zasobu.</span><span class="sxs-lookup"><span data-stu-id="c16ec-122">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c16ec-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c16ec-123">-Location</span></span>
<span data-ttu-id="c16ec-124">Lokalizacja, w której zasób jest lokalizacją.</span><span class="sxs-lookup"><span data-stu-id="c16ec-124">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c16ec-125">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="c16ec-125">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="c16ec-126">Maksymalna liczba abonamentów na konto.</span><span class="sxs-lookup"><span data-stu-id="c16ec-126">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c16ec-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c16ec-127">-Name</span></span>
<span data-ttu-id="c16ec-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="c16ec-128">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c16ec-129">-State</span><span class="sxs-lookup"><span data-stu-id="c16ec-129">-State</span></span>
<span data-ttu-id="c16ec-130">Stan ułatwień dostępu w ofercie.</span><span class="sxs-lookup"><span data-stu-id="c16ec-130">Offer accessibility state.</span></span>

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

### <span data-ttu-id="c16ec-131">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="c16ec-131">-SubscriptionCount</span></span>
<span data-ttu-id="c16ec-132">Bieżąca liczba abonamentów.</span><span class="sxs-lookup"><span data-stu-id="c16ec-132">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c16ec-133">-Tagi</span><span class="sxs-lookup"><span data-stu-id="c16ec-133">-Tags</span></span>
<span data-ttu-id="c16ec-134">Lista par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="c16ec-134">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c16ec-135">-Type</span><span class="sxs-lookup"><span data-stu-id="c16ec-135">-Type</span></span>
<span data-ttu-id="c16ec-136">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="c16ec-136">Type of resource.</span></span>

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

### <span data-ttu-id="c16ec-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c16ec-137">CommonParameters</span></span>
<span data-ttu-id="c16ec-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c16ec-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c16ec-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c16ec-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c16ec-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c16ec-140">INPUTS</span></span>

## <span data-ttu-id="c16ec-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c16ec-141">OUTPUTS</span></span>

## <span data-ttu-id="c16ec-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c16ec-142">NOTES</span></span>

## <span data-ttu-id="c16ec-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c16ec-143">RELATED LINKS</span></span>

