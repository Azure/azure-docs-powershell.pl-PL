---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d07aad989b08909228aebca7538b007f36bfcab
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061580"
---
# <span data-ttu-id="52d22-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="52d22-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="52d22-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52d22-102">SYNOPSIS</span></span>
<span data-ttu-id="52d22-103">Zwraca listę stanów kondycji regionu.</span><span class="sxs-lookup"><span data-stu-id="52d22-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="52d22-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52d22-104">SYNTAX</span></span>

### <span data-ttu-id="52d22-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="52d22-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="52d22-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="52d22-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="52d22-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="52d22-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="52d22-108">Opis</span><span class="sxs-lookup"><span data-stu-id="52d22-108">DESCRIPTION</span></span>
<span data-ttu-id="52d22-109">Zwraca listę stanów kondycji regionu.</span><span class="sxs-lookup"><span data-stu-id="52d22-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="52d22-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52d22-110">EXAMPLES</span></span>

### <span data-ttu-id="52d22-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="52d22-111">EXAMPLE 1</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="52d22-112">Zwraca listę stanów kondycji regionu.</span><span class="sxs-lookup"><span data-stu-id="52d22-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="52d22-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52d22-113">PARAMETERS</span></span>

### <span data-ttu-id="52d22-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="52d22-114">-Location</span></span>
<span data-ttu-id="52d22-115">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="52d22-115">Name of the region</span></span>

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

### <span data-ttu-id="52d22-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52d22-116">-ResourceGroupName</span></span>
<span data-ttu-id="52d22-117">Nazwa grupy zasobów, opcjonalna.</span><span class="sxs-lookup"><span data-stu-id="52d22-117">Resource group name, optional.</span></span>

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

### <span data-ttu-id="52d22-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52d22-118">-ResourceId</span></span>
<span data-ttu-id="52d22-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="52d22-119">The resource id.</span></span>

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

### <span data-ttu-id="52d22-120">-Filter</span><span class="sxs-lookup"><span data-stu-id="52d22-120">-Filter</span></span>
<span data-ttu-id="52d22-121">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="52d22-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="52d22-122">-Początek</span><span class="sxs-lookup"><span data-stu-id="52d22-122">-Top</span></span>
<span data-ttu-id="52d22-123">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="52d22-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="52d22-124">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="52d22-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="52d22-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="52d22-125">-Skip</span></span>
<span data-ttu-id="52d22-126">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="52d22-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="52d22-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d22-127">CommonParameters</span></span>
<span data-ttu-id="52d22-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52d22-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d22-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52d22-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d22-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52d22-130">INPUTS</span></span>

## <span data-ttu-id="52d22-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52d22-131">OUTPUTS</span></span>

### <span data-ttu-id="52d22-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="52d22-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="52d22-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52d22-133">NOTES</span></span>

## <span data-ttu-id="52d22-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52d22-134">RELATED LINKS</span></span>
