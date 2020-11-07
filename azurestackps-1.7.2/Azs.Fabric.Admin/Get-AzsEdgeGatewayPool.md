---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67a49abc82ba1ec8d9411141d456b8f71f75600f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704592"
---
# <span data-ttu-id="50424-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="50424-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="50424-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50424-102">SYNOPSIS</span></span>
<span data-ttu-id="50424-103">Zwraca obiekty puli bramy w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="50424-103">Returns gateway pool objects at a location.</span></span>

## <span data-ttu-id="50424-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50424-104">SYNTAX</span></span>

### <span data-ttu-id="50424-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="50424-105">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="50424-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="50424-106">Get</span></span>
```
Get-AzsEdgeGatewayPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="50424-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="50424-107">ResourceId</span></span>
```
Get-AzsEdgeGatewayPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="50424-108">Opis</span><span class="sxs-lookup"><span data-stu-id="50424-108">DESCRIPTION</span></span>
<span data-ttu-id="50424-109">Zwraca obiekty puli bramy Edge w miejscu.</span><span class="sxs-lookup"><span data-stu-id="50424-109">Returns edge gateway pool objects at a location.</span></span>

## <span data-ttu-id="50424-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50424-110">EXAMPLES</span></span>

### <span data-ttu-id="50424-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="50424-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsEdgeGatewayPool
```

<span data-ttu-id="50424-112">Wyświetlanie listy wszystkich pul z systemem Edge.</span><span class="sxs-lookup"><span data-stu-id="50424-112">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="50424-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="50424-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsEdgeGatewayPool -Name "AzS-Gwy01"
```

<span data-ttu-id="50424-114">Pobierz określoną pulę bram brzegowych.</span><span class="sxs-lookup"><span data-stu-id="50424-114">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="50424-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50424-115">PARAMETERS</span></span>

### <span data-ttu-id="50424-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="50424-116">-Filter</span></span>
<span data-ttu-id="50424-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="50424-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="50424-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="50424-118">-Location</span></span>
<span data-ttu-id="50424-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="50424-119">Location of the resource.</span></span>

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

### <span data-ttu-id="50424-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="50424-120">-Name</span></span>
<span data-ttu-id="50424-121">Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="50424-121">Name of the edge gateway pool.</span></span>

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

### <span data-ttu-id="50424-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50424-122">-ResourceGroupName</span></span>
<span data-ttu-id="50424-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="50424-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="50424-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50424-124">-ResourceId</span></span>
<span data-ttu-id="50424-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="50424-125">The resource id.</span></span>

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

### <span data-ttu-id="50424-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="50424-126">-Skip</span></span>
<span data-ttu-id="50424-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="50424-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="50424-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="50424-128">-Top</span></span>
<span data-ttu-id="50424-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="50424-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="50424-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="50424-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="50424-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50424-131">CommonParameters</span></span>
<span data-ttu-id="50424-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50424-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50424-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50424-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50424-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50424-134">INPUTS</span></span>

## <span data-ttu-id="50424-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50424-135">OUTPUTS</span></span>

### <span data-ttu-id="50424-136">Microsoft. AzureStack. Management. Fabric. admin. models. EdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="50424-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGatewayPool</span></span>

## <span data-ttu-id="50424-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50424-137">NOTES</span></span>

## <span data-ttu-id="50424-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50424-138">RELATED LINKS</span></span>

