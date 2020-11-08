---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e30a1501cb5df34dc8f8b2ab51041f867a5ee6c1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055792"
---
# <span data-ttu-id="5685f-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="5685f-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="5685f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5685f-102">SYNOPSIS</span></span>
<span data-ttu-id="5685f-103">Zapoznaj się z listą ofert jako administrator.</span><span class="sxs-lookup"><span data-stu-id="5685f-103">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="5685f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5685f-104">SYNTAX</span></span>

### <span data-ttu-id="5685f-105">ListAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5685f-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5685f-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="5685f-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="5685f-107">Lista</span><span class="sxs-lookup"><span data-stu-id="5685f-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5685f-108">Zasobów</span><span class="sxs-lookup"><span data-stu-id="5685f-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5685f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5685f-109">DESCRIPTION</span></span>
<span data-ttu-id="5685f-110">Zapoznaj się z listą ofert.</span><span class="sxs-lookup"><span data-stu-id="5685f-110">Get the list of offers.</span></span>

## <span data-ttu-id="5685f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5685f-111">EXAMPLES</span></span>

### <span data-ttu-id="5685f-112">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5685f-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="5685f-113">Zapoznaj się z listą ofert jako administrator.</span><span class="sxs-lookup"><span data-stu-id="5685f-113">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="5685f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5685f-114">PARAMETERS</span></span>

### <span data-ttu-id="5685f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5685f-115">-Name</span></span>
<span data-ttu-id="5685f-116">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="5685f-116">Name of an offer.</span></span>

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

### <span data-ttu-id="5685f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5685f-117">-ResourceGroupName</span></span>
<span data-ttu-id="5685f-118">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="5685f-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5685f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5685f-119">-ResourceId</span></span>
<span data-ttu-id="5685f-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="5685f-120">The resource id.</span></span>

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

### <span data-ttu-id="5685f-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="5685f-121">-Skip</span></span>
<span data-ttu-id="5685f-122">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="5685f-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5685f-123">-Początek</span><span class="sxs-lookup"><span data-stu-id="5685f-123">-Top</span></span>
<span data-ttu-id="5685f-124">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="5685f-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5685f-125">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="5685f-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5685f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5685f-126">CommonParameters</span></span>
<span data-ttu-id="5685f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5685f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5685f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5685f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5685f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5685f-129">INPUTS</span></span>

## <span data-ttu-id="5685f-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5685f-130">OUTPUTS</span></span>

### <span data-ttu-id="5685f-131">Microsoft. AzureStack. Management. Subscriptions. admin. models. Offer</span><span class="sxs-lookup"><span data-stu-id="5685f-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="5685f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5685f-132">NOTES</span></span>

## <span data-ttu-id="5685f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5685f-133">RELATED LINKS</span></span>

