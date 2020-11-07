---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e9fc37b5f99a9ad38e92ce1efc730718882b533d
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889209"
---
# <span data-ttu-id="69bae-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="69bae-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="69bae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69bae-102">SYNOPSIS</span></span>
<span data-ttu-id="69bae-103">Usuwa delegowanie oferty</span><span class="sxs-lookup"><span data-stu-id="69bae-103">Removes the offer delegation</span></span>

## <span data-ttu-id="69bae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69bae-104">SYNTAX</span></span>

### <span data-ttu-id="69bae-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="69bae-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69bae-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="69bae-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69bae-107">Opis</span><span class="sxs-lookup"><span data-stu-id="69bae-107">DESCRIPTION</span></span>
<span data-ttu-id="69bae-108">Usuwa delegowanie oferty</span><span class="sxs-lookup"><span data-stu-id="69bae-108">Removes the offer delegation</span></span>

## <span data-ttu-id="69bae-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69bae-109">EXAMPLES</span></span>

### <span data-ttu-id="69bae-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="69bae-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="69bae-111">Usuwa delegowanie oferty</span><span class="sxs-lookup"><span data-stu-id="69bae-111">Removes the offer delegation</span></span>

## <span data-ttu-id="69bae-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69bae-112">PARAMETERS</span></span>

### <span data-ttu-id="69bae-113">-Force</span><span class="sxs-lookup"><span data-stu-id="69bae-113">-Force</span></span>
<span data-ttu-id="69bae-114">Flaga usunięcia elementu bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="69bae-114">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bae-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="69bae-115">-Name</span></span>
<span data-ttu-id="69bae-116">Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="69bae-116">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bae-117">-Offername</span><span class="sxs-lookup"><span data-stu-id="69bae-117">-OfferName</span></span>
<span data-ttu-id="69bae-118">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="69bae-118">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69bae-119">-ResourceGroupName</span></span>
<span data-ttu-id="69bae-120">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="69bae-120">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bae-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69bae-121">-ResourceId</span></span>
<span data-ttu-id="69bae-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="69bae-122">The resource id.</span></span>

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

### <span data-ttu-id="69bae-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69bae-123">-Confirm</span></span>
<span data-ttu-id="69bae-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69bae-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69bae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69bae-125">-WhatIf</span></span>
<span data-ttu-id="69bae-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69bae-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69bae-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69bae-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69bae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69bae-128">CommonParameters</span></span>
<span data-ttu-id="69bae-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69bae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69bae-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69bae-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69bae-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69bae-131">INPUTS</span></span>

## <span data-ttu-id="69bae-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69bae-132">OUTPUTS</span></span>

## <span data-ttu-id="69bae-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69bae-133">NOTES</span></span>

## <span data-ttu-id="69bae-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69bae-134">RELATED LINKS</span></span>

