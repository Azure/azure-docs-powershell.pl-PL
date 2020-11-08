---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1f1be36f51aab748ec790c56aea7092f1d3d877
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055611"
---
# <span data-ttu-id="2f0f3-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="2f0f3-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="2f0f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f0f3-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0f3-103">Zwraca obiekty puli bramy w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="2f0f3-103">Returns gateway pool objects at a location.</span></span>

## <span data-ttu-id="2f0f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f0f3-104">SYNTAX</span></span>

### <span data-ttu-id="2f0f3-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2f0f3-105">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2f0f3-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="2f0f3-106">Get</span></span>
```
Get-AzsEdgeGatewayPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="2f0f3-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="2f0f3-107">ResourceId</span></span>
```
Get-AzsEdgeGatewayPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2f0f3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2f0f3-108">DESCRIPTION</span></span>
<span data-ttu-id="2f0f3-109">Zwraca obiekty puli bramy Edge w miejscu.</span><span class="sxs-lookup"><span data-stu-id="2f0f3-109">Returns edge gateway pool objects at a location.</span></span>

## <span data-ttu-id="2f0f3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f0f3-110">EXAMPLES</span></span>

### <span data-ttu-id="2f0f3-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="2f0f3-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGatewayPool
```

<span data-ttu-id="2f0f3-112">Wyświetlanie listy wszystkich pul z systemem Edge.</span><span class="sxs-lookup"><span data-stu-id="2f0f3-112">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="2f0f3-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="2f0f3-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGatewayPool -Name "AzS-Gwy01"
```

<span data-ttu-id="2f0f3-114">Pobierz określoną pulę bram brzegowych.</span><span class="sxs-lookup"><span data-stu-id="2f0f3-114">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="2f0f3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f0f3-115">PARAMETERS</span></span>

### <span data-ttu-id="2f0f3-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2f0f3-116">-Name</span></span>
<span data-ttu-id="2f0f3-117">Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="2f0f3-117">Name of the edge gateway pool.</span></span>

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

### <span data-ttu-id="2f0f3-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2f0f3-118">-Location</span></span>
<span data-ttu-id="2f0f3-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="2f0f3-119">Location of the resource.</span></span>

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

### <span data-ttu-id="2f0f3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f0f3-120">-ResourceGroupName</span></span>
<span data-ttu-id="2f0f3-121">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="2f0f3-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="2f0f3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f0f3-122">-ResourceId</span></span>
<span data-ttu-id="2f0f3-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="2f0f3-123">The resource id.</span></span>

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

### <span data-ttu-id="2f0f3-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="2f0f3-124">-Filter</span></span>
<span data-ttu-id="2f0f3-125">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="2f0f3-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="2f0f3-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="2f0f3-126">-Skip</span></span>
<span data-ttu-id="2f0f3-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="2f0f3-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2f0f3-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="2f0f3-128">-Top</span></span>
<span data-ttu-id="2f0f3-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="2f0f3-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2f0f3-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="2f0f3-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2f0f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0f3-131">CommonParameters</span></span>
<span data-ttu-id="2f0f3-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f0f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0f3-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f0f3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0f3-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f0f3-134">INPUTS</span></span>

## <span data-ttu-id="2f0f3-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f0f3-135">OUTPUTS</span></span>

### <span data-ttu-id="2f0f3-136">Microsoft. AzureStack. Management. Fabric. admin. models. EdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="2f0f3-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGatewayPool</span></span>

## <span data-ttu-id="2f0f3-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f0f3-137">NOTES</span></span>

## <span data-ttu-id="2f0f3-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f0f3-138">RELATED LINKS</span></span>
