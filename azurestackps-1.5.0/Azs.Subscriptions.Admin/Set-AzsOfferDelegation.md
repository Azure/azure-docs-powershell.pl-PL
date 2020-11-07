---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e0c752c3ffd266a3615fdd5a1f5193e0202b29a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523253"
---
# <span data-ttu-id="f3946-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="f3946-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="f3946-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3946-102">SYNOPSIS</span></span>
<span data-ttu-id="f3946-103">Umożliwia zaktualizowanie delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="f3946-103">Updates the offer delegation.</span></span>

## <span data-ttu-id="f3946-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3946-104">SYNTAX</span></span>

### <span data-ttu-id="f3946-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f3946-105">Update (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3946-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="f3946-106">InputObject</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] [-Location <String>] -InputObject <OfferDelegation> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3946-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="f3946-107">ResourceId</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] -ResourceId <String> [-Location <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3946-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f3946-108">DESCRIPTION</span></span>
<span data-ttu-id="f3946-109">Umożliwia zaktualizowanie delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="f3946-109">Updates the offer delegation.</span></span>

## <span data-ttu-id="f3946-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3946-110">EXAMPLES</span></span>

### <span data-ttu-id="f3946-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3946-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"
```

<span data-ttu-id="f3946-112">Umożliwia zaktualizowanie delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="f3946-112">Updates the offer delegation.</span></span>

## <span data-ttu-id="f3946-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3946-113">PARAMETERS</span></span>

### <span data-ttu-id="f3946-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f3946-114">-InputObject</span></span>
<span data-ttu-id="f3946-115">Obiekt wejściowy typu Microsoft. AzureStack. Management. Subscriptions. admin. models. OfferDelegation.</span><span class="sxs-lookup"><span data-stu-id="f3946-115">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation.</span></span>

```yaml
Type: OfferDelegation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3946-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f3946-116">-Location</span></span>
<span data-ttu-id="f3946-117">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="f3946-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3946-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3946-118">-Name</span></span>
<span data-ttu-id="f3946-119">Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="f3946-119">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3946-120">-Offername</span><span class="sxs-lookup"><span data-stu-id="f3946-120">-OfferName</span></span>
<span data-ttu-id="f3946-121">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="f3946-121">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3946-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3946-122">-ResourceGroupName</span></span>
<span data-ttu-id="f3946-123">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="f3946-123">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3946-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3946-124">-ResourceId</span></span>
<span data-ttu-id="f3946-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f3946-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3946-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f3946-126">-SubscriptionId</span></span>
<span data-ttu-id="f3946-127">Identyfikator subskrypcji otrzymującej ofertę delegowaną.</span><span class="sxs-lookup"><span data-stu-id="f3946-127">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3946-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3946-128">-Confirm</span></span>
<span data-ttu-id="f3946-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3946-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3946-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3946-130">-WhatIf</span></span>
<span data-ttu-id="f3946-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3946-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3946-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f3946-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3946-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3946-133">CommonParameters</span></span>
<span data-ttu-id="f3946-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3946-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3946-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3946-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3946-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3946-136">INPUTS</span></span>

## <span data-ttu-id="f3946-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3946-137">OUTPUTS</span></span>

### <span data-ttu-id="f3946-138">Microsoft. AzureStack. Management. Subscriptions. admin. models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="f3946-138">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="f3946-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3946-139">NOTES</span></span>

## <span data-ttu-id="f3946-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3946-140">RELATED LINKS</span></span>
