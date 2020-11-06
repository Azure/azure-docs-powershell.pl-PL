---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb23765090b0edfd14fa355b9809a2385900396e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524157"
---
# <span data-ttu-id="0450c-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="0450c-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="0450c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0450c-102">SYNOPSIS</span></span>
<span data-ttu-id="0450c-103">Tworzenie lub aktualizowanie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0450c-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="0450c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0450c-104">SYNTAX</span></span>

### <span data-ttu-id="0450c-105">Set (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="0450c-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0450c-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="0450c-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0450c-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="0450c-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0450c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0450c-108">DESCRIPTION</span></span>
<span data-ttu-id="0450c-109">Tworzenie lub aktualizowanie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0450c-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="0450c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0450c-110">EXAMPLES</span></span>

### <span data-ttu-id="0450c-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0450c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="0450c-112">Tworzenie lub aktualizowanie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0450c-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="0450c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0450c-113">PARAMETERS</span></span>

### <span data-ttu-id="0450c-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0450c-114">-DisplayName</span></span>
<span data-ttu-id="0450c-115">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0450c-115">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0450c-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0450c-116">-InputObject</span></span>
<span data-ttu-id="0450c-117">Posbbily zmodyfikowano przydział sieciowy zwrócony przez Get-AzsNetworkQuota.</span><span class="sxs-lookup"><span data-stu-id="0450c-117">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

```yaml
Type: SubscriptionModel
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0450c-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0450c-118">-Location</span></span>
<span data-ttu-id="0450c-119">Lokalizacja, w której zasób jest lokalizacją.</span><span class="sxs-lookup"><span data-stu-id="0450c-119">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0450c-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="0450c-120">-OfferId</span></span>
<span data-ttu-id="0450c-121">Identyfikator oferty w ramach zakresu dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="0450c-121">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0450c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0450c-122">-ResourceId</span></span>
<span data-ttu-id="0450c-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="0450c-123">The resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0450c-124">-State</span><span class="sxs-lookup"><span data-stu-id="0450c-124">-State</span></span>
<span data-ttu-id="0450c-125">Stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="0450c-125">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0450c-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0450c-126">-SubscriptionId</span></span>
<span data-ttu-id="0450c-127">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0450c-127">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0450c-128">-Tagi</span><span class="sxs-lookup"><span data-stu-id="0450c-128">-Tags</span></span>
<span data-ttu-id="0450c-129">Lista par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="0450c-129">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0450c-130">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="0450c-130">-TenantId</span></span>
<span data-ttu-id="0450c-131">Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="0450c-131">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0450c-132">-Type</span><span class="sxs-lookup"><span data-stu-id="0450c-132">-Type</span></span>
<span data-ttu-id="0450c-133">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="0450c-133">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0450c-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0450c-134">-Confirm</span></span>
<span data-ttu-id="0450c-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0450c-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0450c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0450c-136">-WhatIf</span></span>
<span data-ttu-id="0450c-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0450c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0450c-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0450c-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0450c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0450c-139">CommonParameters</span></span>
<span data-ttu-id="0450c-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0450c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0450c-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0450c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0450c-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0450c-142">INPUTS</span></span>

## <span data-ttu-id="0450c-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0450c-143">OUTPUTS</span></span>

### <span data-ttu-id="0450c-144">Microsoft. AzureStack. Management. Subscription. MODELES. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="0450c-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="0450c-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0450c-145">NOTES</span></span>

## <span data-ttu-id="0450c-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0450c-146">RELATED LINKS</span></span>

