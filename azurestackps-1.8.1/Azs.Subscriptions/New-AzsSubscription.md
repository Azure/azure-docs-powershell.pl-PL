---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: d905159ca62f34584f045a699621f6672507ffe1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889805"
---
# <span data-ttu-id="dfb38-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="dfb38-101">New-AzsSubscription</span></span>

## <span data-ttu-id="dfb38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dfb38-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb38-103">Tworzenie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="dfb38-103">Create a subscription.</span></span>

## <span data-ttu-id="dfb38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dfb38-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfb38-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dfb38-105">DESCRIPTION</span></span>
<span data-ttu-id="dfb38-106">Tworzenie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="dfb38-106">Create a subscription.</span></span>

## <span data-ttu-id="dfb38-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dfb38-107">EXAMPLES</span></span>

### <span data-ttu-id="dfb38-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="dfb38-108">EXAMPLE 1</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="dfb38-109">Tworzenie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="dfb38-109">Create a subscription.</span></span>

## <span data-ttu-id="dfb38-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dfb38-110">PARAMETERS</span></span>

### <span data-ttu-id="dfb38-111">-OfferId</span><span class="sxs-lookup"><span data-stu-id="dfb38-111">-OfferId</span></span>
<span data-ttu-id="dfb38-112">Identyfikator oferty w ramach zakresu dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="dfb38-112">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="dfb38-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dfb38-113">-DisplayName</span></span>
<span data-ttu-id="dfb38-114">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dfb38-114">Subscription name.</span></span>

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

### <span data-ttu-id="dfb38-115">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="dfb38-115">-TenantId</span></span>
<span data-ttu-id="dfb38-116">Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="dfb38-116">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="dfb38-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="dfb38-117">-SubscriptionId</span></span>
<span data-ttu-id="dfb38-118">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dfb38-118">Subscription identifier.</span></span>

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

### <span data-ttu-id="dfb38-119">-State</span><span class="sxs-lookup"><span data-stu-id="dfb38-119">-State</span></span>
<span data-ttu-id="dfb38-120">Stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="dfb38-120">Subscription state.</span></span>

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

### <span data-ttu-id="dfb38-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dfb38-121">-Location</span></span>
<span data-ttu-id="dfb38-122">Lokalizacja, w której zasób jest lokalizacją.</span><span class="sxs-lookup"><span data-stu-id="dfb38-122">Location where resource is location.</span></span>

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

### <span data-ttu-id="dfb38-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfb38-123">-WhatIf</span></span>
<span data-ttu-id="dfb38-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfb38-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfb38-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dfb38-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfb38-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dfb38-126">-Confirm</span></span>
<span data-ttu-id="dfb38-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfb38-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfb38-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb38-128">CommonParameters</span></span>
<span data-ttu-id="dfb38-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfb38-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb38-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfb38-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb38-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dfb38-131">INPUTS</span></span>

## <span data-ttu-id="dfb38-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dfb38-132">OUTPUTS</span></span>

### <span data-ttu-id="dfb38-133">Microsoft. AzureStack. Management. Subscription. MODELES. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="dfb38-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="dfb38-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dfb38-134">NOTES</span></span>

## <span data-ttu-id="dfb38-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dfb38-135">RELATED LINKS</span></span>
