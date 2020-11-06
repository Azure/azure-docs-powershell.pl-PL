---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c58e8dedf4f55a9e1fb6451bf7f774b766b6d71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523758"
---
# <span data-ttu-id="75eef-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="75eef-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="75eef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75eef-102">SYNOPSIS</span></span>
<span data-ttu-id="75eef-103">Pobierz listę delegowanych ofert.</span><span class="sxs-lookup"><span data-stu-id="75eef-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="75eef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75eef-104">SYNTAX</span></span>

### <span data-ttu-id="75eef-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="75eef-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="75eef-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="75eef-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="75eef-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="75eef-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="75eef-108">Opis</span><span class="sxs-lookup"><span data-stu-id="75eef-108">DESCRIPTION</span></span>
<span data-ttu-id="75eef-109">Pobierz listę delegowanych ofert.</span><span class="sxs-lookup"><span data-stu-id="75eef-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="75eef-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75eef-110">EXAMPLES</span></span>

### <span data-ttu-id="75eef-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="75eef-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="75eef-112">Pobierz listę delegowanych ofert.</span><span class="sxs-lookup"><span data-stu-id="75eef-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="75eef-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75eef-113">PARAMETERS</span></span>

### <span data-ttu-id="75eef-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="75eef-114">-Name</span></span>
<span data-ttu-id="75eef-115">Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="75eef-115">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75eef-116">-Offername</span><span class="sxs-lookup"><span data-stu-id="75eef-116">-OfferName</span></span>
<span data-ttu-id="75eef-117">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="75eef-117">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75eef-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75eef-118">-ResourceGroupName</span></span>
<span data-ttu-id="75eef-119">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="75eef-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75eef-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75eef-120">-ResourceId</span></span>
<span data-ttu-id="75eef-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="75eef-121">The resource id.</span></span>

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

### <span data-ttu-id="75eef-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="75eef-122">-Skip</span></span>
<span data-ttu-id="75eef-123">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="75eef-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75eef-124">-Początek</span><span class="sxs-lookup"><span data-stu-id="75eef-124">-Top</span></span>
<span data-ttu-id="75eef-125">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="75eef-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="75eef-126">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="75eef-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75eef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75eef-127">CommonParameters</span></span>
<span data-ttu-id="75eef-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75eef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75eef-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75eef-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75eef-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75eef-130">INPUTS</span></span>

## <span data-ttu-id="75eef-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75eef-131">OUTPUTS</span></span>

### <span data-ttu-id="75eef-132">Microsoft. AzureStack. Management. Subscriptions. admin. models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="75eef-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="75eef-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75eef-133">NOTES</span></span>

## <span data-ttu-id="75eef-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75eef-134">RELATED LINKS</span></span>

