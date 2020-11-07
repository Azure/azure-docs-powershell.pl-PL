---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d07aad989b08909228aebca7538b007f36bfcab
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889101"
---
# <span data-ttu-id="ea17f-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="ea17f-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="ea17f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea17f-102">SYNOPSIS</span></span>
<span data-ttu-id="ea17f-103">Zwraca listę stanów kondycji regionu.</span><span class="sxs-lookup"><span data-stu-id="ea17f-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="ea17f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea17f-104">SYNTAX</span></span>

### <span data-ttu-id="ea17f-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ea17f-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea17f-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ea17f-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ea17f-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="ea17f-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ea17f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ea17f-108">DESCRIPTION</span></span>
<span data-ttu-id="ea17f-109">Zwraca listę stanów kondycji regionu.</span><span class="sxs-lookup"><span data-stu-id="ea17f-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="ea17f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea17f-110">EXAMPLES</span></span>

### <span data-ttu-id="ea17f-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="ea17f-111">EXAMPLE 1</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="ea17f-112">Zwraca listę stanów kondycji regionu.</span><span class="sxs-lookup"><span data-stu-id="ea17f-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="ea17f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea17f-113">PARAMETERS</span></span>

### <span data-ttu-id="ea17f-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ea17f-114">-Location</span></span>
<span data-ttu-id="ea17f-115">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="ea17f-115">Name of the region</span></span>

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

### <span data-ttu-id="ea17f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea17f-116">-ResourceGroupName</span></span>
<span data-ttu-id="ea17f-117">Nazwa grupy zasobów, opcjonalna.</span><span class="sxs-lookup"><span data-stu-id="ea17f-117">Resource group name, optional.</span></span>

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

### <span data-ttu-id="ea17f-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea17f-118">-ResourceId</span></span>
<span data-ttu-id="ea17f-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="ea17f-119">The resource id.</span></span>

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

### <span data-ttu-id="ea17f-120">-Filter</span><span class="sxs-lookup"><span data-stu-id="ea17f-120">-Filter</span></span>
<span data-ttu-id="ea17f-121">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="ea17f-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="ea17f-122">-Początek</span><span class="sxs-lookup"><span data-stu-id="ea17f-122">-Top</span></span>
<span data-ttu-id="ea17f-123">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="ea17f-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ea17f-124">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="ea17f-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ea17f-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="ea17f-125">-Skip</span></span>
<span data-ttu-id="ea17f-126">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="ea17f-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ea17f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea17f-127">CommonParameters</span></span>
<span data-ttu-id="ea17f-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea17f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea17f-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea17f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea17f-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea17f-130">INPUTS</span></span>

## <span data-ttu-id="ea17f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea17f-131">OUTPUTS</span></span>

### <span data-ttu-id="ea17f-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="ea17f-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="ea17f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea17f-133">NOTES</span></span>

## <span data-ttu-id="ea17f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea17f-134">RELATED LINKS</span></span>
