---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1ab041d888a43f498e694be9bc2e103422177f7
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889258"
---
# <span data-ttu-id="e4e00-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="e4e00-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="e4e00-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4e00-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e00-103">Pobierz listę delegowanych ofert.</span><span class="sxs-lookup"><span data-stu-id="e4e00-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="e4e00-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4e00-104">SYNTAX</span></span>

### <span data-ttu-id="e4e00-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e4e00-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4e00-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e4e00-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="e4e00-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="e4e00-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e4e00-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e4e00-108">DESCRIPTION</span></span>
<span data-ttu-id="e4e00-109">Pobierz listę delegowanych ofert.</span><span class="sxs-lookup"><span data-stu-id="e4e00-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="e4e00-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4e00-110">EXAMPLES</span></span>

### <span data-ttu-id="e4e00-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e4e00-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="e4e00-112">Pobierz listę delegowanych ofert.</span><span class="sxs-lookup"><span data-stu-id="e4e00-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="e4e00-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4e00-113">PARAMETERS</span></span>

### <span data-ttu-id="e4e00-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4e00-114">-Name</span></span>
<span data-ttu-id="e4e00-115">Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="e4e00-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="e4e00-116">-Offername</span><span class="sxs-lookup"><span data-stu-id="e4e00-116">-OfferName</span></span>
<span data-ttu-id="e4e00-117">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="e4e00-117">Name of an offer.</span></span>

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

### <span data-ttu-id="e4e00-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4e00-118">-ResourceGroupName</span></span>
<span data-ttu-id="e4e00-119">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="e4e00-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="e4e00-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4e00-120">-ResourceId</span></span>
<span data-ttu-id="e4e00-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e4e00-121">The resource id.</span></span>

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

### <span data-ttu-id="e4e00-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="e4e00-122">-Skip</span></span>
<span data-ttu-id="e4e00-123">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="e4e00-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e4e00-124">-Początek</span><span class="sxs-lookup"><span data-stu-id="e4e00-124">-Top</span></span>
<span data-ttu-id="e4e00-125">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="e4e00-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e4e00-126">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="e4e00-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e4e00-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e00-127">CommonParameters</span></span>
<span data-ttu-id="e4e00-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4e00-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e00-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4e00-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e00-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4e00-130">INPUTS</span></span>

## <span data-ttu-id="e4e00-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4e00-131">OUTPUTS</span></span>

### <span data-ttu-id="e4e00-132">Microsoft. AzureStack. Management. Subscriptions. admin. models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="e4e00-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="e4e00-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4e00-133">NOTES</span></span>

## <span data-ttu-id="e4e00-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4e00-134">RELATED LINKS</span></span>

