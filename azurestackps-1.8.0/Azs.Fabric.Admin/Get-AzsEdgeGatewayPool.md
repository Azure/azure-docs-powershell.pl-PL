---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1f1be36f51aab748ec790c56aea7092f1d3d877
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888997"
---
# <span data-ttu-id="254ff-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="254ff-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="254ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="254ff-102">SYNOPSIS</span></span>
<span data-ttu-id="254ff-103">Zwraca obiekty puli bramy w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="254ff-103">Returns gateway pool objects at a location.</span></span>

## <span data-ttu-id="254ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="254ff-104">SYNTAX</span></span>

### <span data-ttu-id="254ff-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="254ff-105">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="254ff-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="254ff-106">Get</span></span>
```
Get-AzsEdgeGatewayPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="254ff-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="254ff-107">ResourceId</span></span>
```
Get-AzsEdgeGatewayPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="254ff-108">Opis</span><span class="sxs-lookup"><span data-stu-id="254ff-108">DESCRIPTION</span></span>
<span data-ttu-id="254ff-109">Zwraca obiekty puli bramy Edge w miejscu.</span><span class="sxs-lookup"><span data-stu-id="254ff-109">Returns edge gateway pool objects at a location.</span></span>

## <span data-ttu-id="254ff-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="254ff-110">EXAMPLES</span></span>

### <span data-ttu-id="254ff-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="254ff-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGatewayPool
```

<span data-ttu-id="254ff-112">Wyświetlanie listy wszystkich pul z systemem Edge.</span><span class="sxs-lookup"><span data-stu-id="254ff-112">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="254ff-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="254ff-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGatewayPool -Name "AzS-Gwy01"
```

<span data-ttu-id="254ff-114">Pobierz określoną pulę bram brzegowych.</span><span class="sxs-lookup"><span data-stu-id="254ff-114">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="254ff-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="254ff-115">PARAMETERS</span></span>

### <span data-ttu-id="254ff-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="254ff-116">-Name</span></span>
<span data-ttu-id="254ff-117">Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="254ff-117">Name of the edge gateway pool.</span></span>

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

### <span data-ttu-id="254ff-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="254ff-118">-Location</span></span>
<span data-ttu-id="254ff-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="254ff-119">Location of the resource.</span></span>

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

### <span data-ttu-id="254ff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="254ff-120">-ResourceGroupName</span></span>
<span data-ttu-id="254ff-121">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="254ff-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="254ff-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="254ff-122">-ResourceId</span></span>
<span data-ttu-id="254ff-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="254ff-123">The resource id.</span></span>

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

### <span data-ttu-id="254ff-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="254ff-124">-Filter</span></span>
<span data-ttu-id="254ff-125">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="254ff-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="254ff-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="254ff-126">-Skip</span></span>
<span data-ttu-id="254ff-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="254ff-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="254ff-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="254ff-128">-Top</span></span>
<span data-ttu-id="254ff-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="254ff-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="254ff-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="254ff-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="254ff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="254ff-131">CommonParameters</span></span>
<span data-ttu-id="254ff-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="254ff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="254ff-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="254ff-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="254ff-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="254ff-134">INPUTS</span></span>

## <span data-ttu-id="254ff-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="254ff-135">OUTPUTS</span></span>

### <span data-ttu-id="254ff-136">Microsoft. AzureStack. Management. Fabric. admin. models. EdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="254ff-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGatewayPool</span></span>

## <span data-ttu-id="254ff-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="254ff-137">NOTES</span></span>

## <span data-ttu-id="254ff-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="254ff-138">RELATED LINKS</span></span>
