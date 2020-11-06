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
ms.locfileid: "93523573"
---
# <span data-ttu-id="52261-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="52261-101">New-AzsSubscription</span></span>

## <span data-ttu-id="52261-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52261-102">SYNOPSIS</span></span>
<span data-ttu-id="52261-103">Tworzenie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="52261-103">Create a subscription.</span></span>

## <span data-ttu-id="52261-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52261-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52261-105">Opis</span><span class="sxs-lookup"><span data-stu-id="52261-105">DESCRIPTION</span></span>
<span data-ttu-id="52261-106">Tworzenie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="52261-106">Create a subscription.</span></span>

## <span data-ttu-id="52261-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52261-107">EXAMPLES</span></span>

### <span data-ttu-id="52261-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="52261-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="52261-109">Tworzenie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="52261-109">Create a subscription.</span></span>

## <span data-ttu-id="52261-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52261-110">PARAMETERS</span></span>

### <span data-ttu-id="52261-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="52261-111">-DisplayName</span></span>
<span data-ttu-id="52261-112">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="52261-112">Subscription name.</span></span>

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

### <span data-ttu-id="52261-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="52261-113">-Location</span></span>
<span data-ttu-id="52261-114">Lokalizacja, w której zasób jest lokalizacją.</span><span class="sxs-lookup"><span data-stu-id="52261-114">Location where resource is location.</span></span>

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

### <span data-ttu-id="52261-115">-OfferId</span><span class="sxs-lookup"><span data-stu-id="52261-115">-OfferId</span></span>
<span data-ttu-id="52261-116">Identyfikator oferty w ramach zakresu dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="52261-116">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="52261-117">-State</span><span class="sxs-lookup"><span data-stu-id="52261-117">-State</span></span>
<span data-ttu-id="52261-118">Stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="52261-118">Subscription state.</span></span>

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

### <span data-ttu-id="52261-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="52261-119">-SubscriptionId</span></span>
<span data-ttu-id="52261-120">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="52261-120">Subscription identifier.</span></span>

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

### <span data-ttu-id="52261-121">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="52261-121">-TenantId</span></span>
<span data-ttu-id="52261-122">Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="52261-122">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="52261-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="52261-123">-Confirm</span></span>
<span data-ttu-id="52261-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52261-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52261-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52261-125">-WhatIf</span></span>
<span data-ttu-id="52261-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52261-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52261-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="52261-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52261-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52261-128">CommonParameters</span></span>
<span data-ttu-id="52261-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52261-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52261-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52261-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52261-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52261-131">INPUTS</span></span>

## <span data-ttu-id="52261-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52261-132">OUTPUTS</span></span>

### <span data-ttu-id="52261-133">Microsoft. AzureStack. Management. Subscription. MODELES. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="52261-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="52261-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52261-134">NOTES</span></span>

## <span data-ttu-id="52261-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52261-135">RELATED LINKS</span></span>

