---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66d8deb8551dfee98c15fcc5524c993c741bca0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523761"
---
# <span data-ttu-id="2228b-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="2228b-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="2228b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2228b-102">SYNOPSIS</span></span>
<span data-ttu-id="2228b-103">Zapoznaj się z listą ofert jako operatora.</span><span class="sxs-lookup"><span data-stu-id="2228b-103">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="2228b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2228b-104">SYNTAX</span></span>

### <span data-ttu-id="2228b-105">ListAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2228b-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2228b-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="2228b-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="2228b-107">Lista</span><span class="sxs-lookup"><span data-stu-id="2228b-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2228b-108">Zasobów</span><span class="sxs-lookup"><span data-stu-id="2228b-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2228b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2228b-109">DESCRIPTION</span></span>
<span data-ttu-id="2228b-110">Zapoznaj się z listą ofert.</span><span class="sxs-lookup"><span data-stu-id="2228b-110">Get the list of offers.</span></span>

## <span data-ttu-id="2228b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2228b-111">EXAMPLES</span></span>

### <span data-ttu-id="2228b-112">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2228b-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="2228b-113">Zapoznaj się z listą ofert jako operatora.</span><span class="sxs-lookup"><span data-stu-id="2228b-113">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="2228b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2228b-114">PARAMETERS</span></span>

### <span data-ttu-id="2228b-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2228b-115">-Name</span></span>
<span data-ttu-id="2228b-116">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="2228b-116">Name of an offer.</span></span>

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

### <span data-ttu-id="2228b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2228b-117">-ResourceGroupName</span></span>
<span data-ttu-id="2228b-118">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="2228b-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="2228b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2228b-119">-ResourceId</span></span>
<span data-ttu-id="2228b-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="2228b-120">The resource id.</span></span>

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

### <span data-ttu-id="2228b-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="2228b-121">-Skip</span></span>
<span data-ttu-id="2228b-122">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="2228b-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2228b-123">-Początek</span><span class="sxs-lookup"><span data-stu-id="2228b-123">-Top</span></span>
<span data-ttu-id="2228b-124">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="2228b-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2228b-125">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="2228b-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2228b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2228b-126">CommonParameters</span></span>
<span data-ttu-id="2228b-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2228b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2228b-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2228b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2228b-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2228b-129">INPUTS</span></span>

## <span data-ttu-id="2228b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2228b-130">OUTPUTS</span></span>

### <span data-ttu-id="2228b-131">Microsoft. AzureStack. Management. Subscriptions. admin. models. Offer</span><span class="sxs-lookup"><span data-stu-id="2228b-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="2228b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2228b-132">NOTES</span></span>

## <span data-ttu-id="2228b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2228b-133">RELATED LINKS</span></span>

