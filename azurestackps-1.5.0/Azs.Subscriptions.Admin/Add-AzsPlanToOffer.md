---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e501feeea3509725b53c85007934c8e682de48a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710648"
---
# <span data-ttu-id="0ff43-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="0ff43-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="0ff43-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ff43-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff43-103">Łączy plan z ofertą.</span><span class="sxs-lookup"><span data-stu-id="0ff43-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="0ff43-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ff43-104">SYNTAX</span></span>

```
Add-AzsPlanToOffer [-PlanName] <String> [-OfferName] <String> [-ResourceGroupName] <String>
 [[-PlanLinkType] <String>] [[-MaxAcquisitionCount] <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ff43-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0ff43-105">DESCRIPTION</span></span>
<span data-ttu-id="0ff43-106">Łączy plan z ofertą.</span><span class="sxs-lookup"><span data-stu-id="0ff43-106">Links a plan to an offer.</span></span>

## <span data-ttu-id="0ff43-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ff43-107">EXAMPLES</span></span>

### <span data-ttu-id="0ff43-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0ff43-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlanToOffer -PlanLinkType Addon -Offer offer1 -PlanName plan1 -ResourceGroupName rg1 -MaxAcquisitionCount 2
```

## <span data-ttu-id="0ff43-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ff43-109">PARAMETERS</span></span>

### <span data-ttu-id="0ff43-110">-Force</span><span class="sxs-lookup"><span data-stu-id="0ff43-110">-Force</span></span>
<span data-ttu-id="0ff43-111">Flaga usunięcia elementu bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="0ff43-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="0ff43-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="0ff43-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="0ff43-113">Maksymalna liczba nabyć przez abonentów</span><span class="sxs-lookup"><span data-stu-id="0ff43-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff43-114">-Offername</span><span class="sxs-lookup"><span data-stu-id="0ff43-114">-OfferName</span></span>
<span data-ttu-id="0ff43-115">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="0ff43-115">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff43-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="0ff43-116">-PlanLinkType</span></span>
<span data-ttu-id="0ff43-117">Typ linku planu.</span><span class="sxs-lookup"><span data-stu-id="0ff43-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="0ff43-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="0ff43-118">-PlanName</span></span>
<span data-ttu-id="0ff43-119">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="0ff43-119">Name of the plan.</span></span>

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

### <span data-ttu-id="0ff43-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ff43-120">-ResourceGroupName</span></span>
<span data-ttu-id="0ff43-121">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="0ff43-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff43-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0ff43-122">-Confirm</span></span>
<span data-ttu-id="0ff43-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ff43-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ff43-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ff43-124">-WhatIf</span></span>
<span data-ttu-id="0ff43-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ff43-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ff43-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0ff43-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ff43-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff43-127">CommonParameters</span></span>
<span data-ttu-id="0ff43-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ff43-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff43-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ff43-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff43-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ff43-130">INPUTS</span></span>

## <span data-ttu-id="0ff43-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ff43-131">OUTPUTS</span></span>

## <span data-ttu-id="0ff43-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ff43-132">NOTES</span></span>

## <span data-ttu-id="0ff43-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ff43-133">RELATED LINKS</span></span>
