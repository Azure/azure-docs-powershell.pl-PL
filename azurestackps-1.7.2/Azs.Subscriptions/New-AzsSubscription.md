---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 617a7ac7d949eb54ab08b0d0cb06c0fca3ba79bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888770"
---
# <span data-ttu-id="a1c9d-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="a1c9d-101">New-AzsSubscription</span></span>

## <span data-ttu-id="a1c9d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c9d-103">Tworzenie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-103">Create a subscription.</span></span>

## <span data-ttu-id="a1c9d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1c9d-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1c9d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a1c9d-105">DESCRIPTION</span></span>
<span data-ttu-id="a1c9d-106">Tworzenie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-106">Create a subscription.</span></span>

## <span data-ttu-id="a1c9d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1c9d-107">EXAMPLES</span></span>

### <span data-ttu-id="a1c9d-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a1c9d-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="a1c9d-109">Tworzenie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-109">Create a subscription.</span></span>

## <span data-ttu-id="a1c9d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1c9d-110">PARAMETERS</span></span>

### <span data-ttu-id="a1c9d-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a1c9d-111">-DisplayName</span></span>
<span data-ttu-id="a1c9d-112">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-112">Subscription name.</span></span>

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

### <span data-ttu-id="a1c9d-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a1c9d-113">-Location</span></span>
<span data-ttu-id="a1c9d-114">Lokalizacja, w której zasób jest lokalizacją.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-114">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c9d-115">-OfferId</span><span class="sxs-lookup"><span data-stu-id="a1c9d-115">-OfferId</span></span>
<span data-ttu-id="a1c9d-116">Identyfikator oferty w ramach zakresu dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-116">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c9d-117">-State</span><span class="sxs-lookup"><span data-stu-id="a1c9d-117">-State</span></span>
<span data-ttu-id="a1c9d-118">Stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-118">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c9d-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a1c9d-119">-SubscriptionId</span></span>
<span data-ttu-id="a1c9d-120">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-120">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c9d-121">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="a1c9d-121">-TenantId</span></span>
<span data-ttu-id="a1c9d-122">Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-122">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="a1c9d-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1c9d-123">-Confirm</span></span>
<span data-ttu-id="a1c9d-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1c9d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1c9d-125">-WhatIf</span></span>
<span data-ttu-id="a1c9d-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1c9d-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1c9d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c9d-128">CommonParameters</span></span>
<span data-ttu-id="a1c9d-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c9d-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c9d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c9d-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1c9d-131">INPUTS</span></span>

## <span data-ttu-id="a1c9d-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1c9d-132">OUTPUTS</span></span>

### <span data-ttu-id="a1c9d-133">Microsoft. AzureStack. Management. Subscription. MODELES. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="a1c9d-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="a1c9d-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1c9d-134">NOTES</span></span>

## <span data-ttu-id="a1c9d-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1c9d-135">RELATED LINKS</span></span>

