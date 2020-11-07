---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25bd0c892c8c5978493d855246be994bc96158db
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889789"
---
# <span data-ttu-id="f52fd-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="f52fd-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="f52fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f52fd-102">SYNOPSIS</span></span>
<span data-ttu-id="f52fd-103">Tworzenie lub aktualizowanie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f52fd-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="f52fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f52fd-104">SYNTAX</span></span>

### <span data-ttu-id="f52fd-105">Set (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f52fd-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f52fd-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="f52fd-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f52fd-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="f52fd-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f52fd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f52fd-108">DESCRIPTION</span></span>
<span data-ttu-id="f52fd-109">Tworzenie lub aktualizowanie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f52fd-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="f52fd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f52fd-110">EXAMPLES</span></span>

### <span data-ttu-id="f52fd-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="f52fd-111">EXAMPLE 1</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="f52fd-112">Tworzenie lub aktualizowanie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f52fd-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="f52fd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f52fd-113">PARAMETERS</span></span>

### <span data-ttu-id="f52fd-114">-OfferId</span><span class="sxs-lookup"><span data-stu-id="f52fd-114">-OfferId</span></span>
<span data-ttu-id="f52fd-115">Identyfikator oferty w ramach zakresu dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="f52fd-115">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="f52fd-116">-Type</span><span class="sxs-lookup"><span data-stu-id="f52fd-116">-Type</span></span>
<span data-ttu-id="f52fd-117">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="f52fd-117">Type of resource.</span></span>

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

### <span data-ttu-id="f52fd-118">-Tagi</span><span class="sxs-lookup"><span data-stu-id="f52fd-118">-Tags</span></span>
<span data-ttu-id="f52fd-119">Lista par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="f52fd-119">List of key-value pairs.</span></span>

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

### <span data-ttu-id="f52fd-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f52fd-120">-SubscriptionId</span></span>
<span data-ttu-id="f52fd-121">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f52fd-121">Subscription identifier.</span></span>

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

### <span data-ttu-id="f52fd-122">-State</span><span class="sxs-lookup"><span data-stu-id="f52fd-122">-State</span></span>
<span data-ttu-id="f52fd-123">Stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="f52fd-123">Subscription state.</span></span>

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

### <span data-ttu-id="f52fd-124">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="f52fd-124">-TenantId</span></span>
<span data-ttu-id="f52fd-125">Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="f52fd-125">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="f52fd-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f52fd-126">-DisplayName</span></span>
<span data-ttu-id="f52fd-127">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f52fd-127">Subscription name.</span></span>

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

### <span data-ttu-id="f52fd-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f52fd-128">-Location</span></span>
<span data-ttu-id="f52fd-129">Lokalizacja, w której zasób jest lokalizacją.</span><span class="sxs-lookup"><span data-stu-id="f52fd-129">Location where resource is location.</span></span>

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

### <span data-ttu-id="f52fd-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f52fd-130">-ResourceId</span></span>
<span data-ttu-id="f52fd-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f52fd-131">The resource ID.</span></span>

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

### <span data-ttu-id="f52fd-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f52fd-132">-InputObject</span></span>
<span data-ttu-id="f52fd-133">Posbbily zmodyfikowano przydział sieciowy zwrócony przez Get-AzsNetworkQuota.</span><span class="sxs-lookup"><span data-stu-id="f52fd-133">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

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

### <span data-ttu-id="f52fd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f52fd-134">-WhatIf</span></span>
<span data-ttu-id="f52fd-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f52fd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f52fd-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f52fd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f52fd-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f52fd-137">-Confirm</span></span>
<span data-ttu-id="f52fd-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f52fd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f52fd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f52fd-139">CommonParameters</span></span>
<span data-ttu-id="f52fd-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f52fd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f52fd-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f52fd-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f52fd-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f52fd-142">INPUTS</span></span>

## <span data-ttu-id="f52fd-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f52fd-143">OUTPUTS</span></span>

### <span data-ttu-id="f52fd-144">Microsoft. AzureStack. Management. Subscription. MODELES. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="f52fd-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="f52fd-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f52fd-145">NOTES</span></span>

## <span data-ttu-id="f52fd-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f52fd-146">RELATED LINKS</span></span>
