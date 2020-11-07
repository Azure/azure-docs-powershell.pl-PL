---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9212655ecb5f67dbf459548c48ff6d25420a8537
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710682"
---
# <span data-ttu-id="22385-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="22385-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="22385-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22385-102">SYNOPSIS</span></span>
<span data-ttu-id="22385-103">Odłączanie planu od oferty.</span><span class="sxs-lookup"><span data-stu-id="22385-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="22385-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22385-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22385-105">Opis</span><span class="sxs-lookup"><span data-stu-id="22385-105">DESCRIPTION</span></span>
<span data-ttu-id="22385-106">Odłączanie planu od oferty.</span><span class="sxs-lookup"><span data-stu-id="22385-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="22385-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22385-107">EXAMPLES</span></span>

### <span data-ttu-id="22385-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="22385-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="22385-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22385-109">PARAMETERS</span></span>

### <span data-ttu-id="22385-110">-Force</span><span class="sxs-lookup"><span data-stu-id="22385-110">-Force</span></span>
<span data-ttu-id="22385-111">Flaga usunięcia elementu bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="22385-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="22385-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="22385-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="22385-113">Maksymalna liczba nabyć przez abonentów</span><span class="sxs-lookup"><span data-stu-id="22385-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22385-114">-Offername</span><span class="sxs-lookup"><span data-stu-id="22385-114">-OfferName</span></span>
<span data-ttu-id="22385-115">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="22385-115">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22385-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="22385-116">-PlanLinkType</span></span>
<span data-ttu-id="22385-117">Typ linku planu.</span><span class="sxs-lookup"><span data-stu-id="22385-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="22385-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="22385-118">-PlanName</span></span>
<span data-ttu-id="22385-119">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="22385-119">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22385-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22385-120">-ResourceGroupName</span></span>
<span data-ttu-id="22385-121">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="22385-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22385-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="22385-122">-Confirm</span></span>
<span data-ttu-id="22385-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22385-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22385-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22385-124">-WhatIf</span></span>
<span data-ttu-id="22385-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22385-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22385-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="22385-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22385-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22385-127">CommonParameters</span></span>
<span data-ttu-id="22385-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22385-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22385-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22385-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22385-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22385-130">INPUTS</span></span>

## <span data-ttu-id="22385-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22385-131">OUTPUTS</span></span>

## <span data-ttu-id="22385-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22385-132">NOTES</span></span>

## <span data-ttu-id="22385-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22385-133">RELATED LINKS</span></span>

