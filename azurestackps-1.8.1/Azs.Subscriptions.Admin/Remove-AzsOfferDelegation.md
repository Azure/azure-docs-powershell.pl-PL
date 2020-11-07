---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e9fc37b5f99a9ad38e92ce1efc730718882b533d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889477"
---
# <span data-ttu-id="64d9f-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="64d9f-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="64d9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="64d9f-103">Usuwa delegowanie oferty</span><span class="sxs-lookup"><span data-stu-id="64d9f-103">Removes the offer delegation</span></span>

## <span data-ttu-id="64d9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64d9f-104">SYNTAX</span></span>

### <span data-ttu-id="64d9f-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="64d9f-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64d9f-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="64d9f-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64d9f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="64d9f-107">DESCRIPTION</span></span>
<span data-ttu-id="64d9f-108">Usuwa delegowanie oferty</span><span class="sxs-lookup"><span data-stu-id="64d9f-108">Removes the offer delegation</span></span>

## <span data-ttu-id="64d9f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64d9f-109">EXAMPLES</span></span>

### <span data-ttu-id="64d9f-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="64d9f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="64d9f-111">Usuwa delegowanie oferty</span><span class="sxs-lookup"><span data-stu-id="64d9f-111">Removes the offer delegation</span></span>

## <span data-ttu-id="64d9f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64d9f-112">PARAMETERS</span></span>

### <span data-ttu-id="64d9f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="64d9f-113">-Force</span></span>
<span data-ttu-id="64d9f-114">Flaga usunięcia elementu bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="64d9f-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="64d9f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="64d9f-115">-Name</span></span>
<span data-ttu-id="64d9f-116">Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="64d9f-116">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="64d9f-117">-Offername</span><span class="sxs-lookup"><span data-stu-id="64d9f-117">-OfferName</span></span>
<span data-ttu-id="64d9f-118">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="64d9f-118">Name of an offer.</span></span>

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

### <span data-ttu-id="64d9f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64d9f-119">-ResourceGroupName</span></span>
<span data-ttu-id="64d9f-120">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="64d9f-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="64d9f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64d9f-121">-ResourceId</span></span>
<span data-ttu-id="64d9f-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="64d9f-122">The resource id.</span></span>

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

### <span data-ttu-id="64d9f-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64d9f-123">-Confirm</span></span>
<span data-ttu-id="64d9f-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64d9f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64d9f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64d9f-125">-WhatIf</span></span>
<span data-ttu-id="64d9f-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64d9f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64d9f-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="64d9f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64d9f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d9f-128">CommonParameters</span></span>
<span data-ttu-id="64d9f-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64d9f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d9f-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64d9f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d9f-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64d9f-131">INPUTS</span></span>

## <span data-ttu-id="64d9f-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64d9f-132">OUTPUTS</span></span>

## <span data-ttu-id="64d9f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64d9f-133">NOTES</span></span>

## <span data-ttu-id="64d9f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64d9f-134">RELATED LINKS</span></span>

