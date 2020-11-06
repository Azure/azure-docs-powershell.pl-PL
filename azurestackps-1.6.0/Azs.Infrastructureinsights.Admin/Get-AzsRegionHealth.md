---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6713b912f962a7a85627ca2280d6195cc5c5d88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523605"
---
# <span data-ttu-id="5ccd1-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="5ccd1-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="5ccd1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ccd1-102">SYNOPSIS</span></span>
<span data-ttu-id="5ccd1-103">Zwraca listę stanów kondycji regionu.</span><span class="sxs-lookup"><span data-stu-id="5ccd1-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="5ccd1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ccd1-104">SYNTAX</span></span>

### <span data-ttu-id="5ccd1-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="5ccd1-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ccd1-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="5ccd1-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5ccd1-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="5ccd1-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5ccd1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5ccd1-108">DESCRIPTION</span></span>
<span data-ttu-id="5ccd1-109">Zwraca listę stanów kondycji regionu.</span><span class="sxs-lookup"><span data-stu-id="5ccd1-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="5ccd1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ccd1-110">EXAMPLES</span></span>

### <span data-ttu-id="5ccd1-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5ccd1-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="5ccd1-112">Zwraca listę stanów kondycji regionu.</span><span class="sxs-lookup"><span data-stu-id="5ccd1-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="5ccd1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ccd1-113">PARAMETERS</span></span>

### <span data-ttu-id="5ccd1-114">-Filter</span><span class="sxs-lookup"><span data-stu-id="5ccd1-114">-Filter</span></span>
<span data-ttu-id="5ccd1-115">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="5ccd1-115">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ccd1-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5ccd1-116">-Location</span></span>
<span data-ttu-id="5ccd1-117">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="5ccd1-117">Name of the region</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ccd1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ccd1-118">-ResourceGroupName</span></span>
<span data-ttu-id="5ccd1-119">Nazwa grupy zasobów, w której znajduje się dany zasób.</span><span class="sxs-lookup"><span data-stu-id="5ccd1-119">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ccd1-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ccd1-120">-ResourceId</span></span>
<span data-ttu-id="5ccd1-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="5ccd1-121">The resource id.</span></span>

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

### <span data-ttu-id="5ccd1-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="5ccd1-122">-Skip</span></span>
<span data-ttu-id="5ccd1-123">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="5ccd1-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5ccd1-124">-Początek</span><span class="sxs-lookup"><span data-stu-id="5ccd1-124">-Top</span></span>
<span data-ttu-id="5ccd1-125">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="5ccd1-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5ccd1-126">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="5ccd1-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5ccd1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ccd1-127">CommonParameters</span></span>
<span data-ttu-id="5ccd1-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ccd1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ccd1-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ccd1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ccd1-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ccd1-130">INPUTS</span></span>

## <span data-ttu-id="5ccd1-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ccd1-131">OUTPUTS</span></span>

### <span data-ttu-id="5ccd1-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="5ccd1-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="5ccd1-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ccd1-133">NOTES</span></span>

## <span data-ttu-id="5ccd1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ccd1-134">RELATED LINKS</span></span>

