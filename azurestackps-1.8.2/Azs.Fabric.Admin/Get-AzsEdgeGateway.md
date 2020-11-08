---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 793bf4a4b5b9dfb448c5b2a1baf9d74af592a23e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055613"
---
# <span data-ttu-id="547a8-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="547a8-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="547a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="547a8-102">SYNOPSIS</span></span>
<span data-ttu-id="547a8-103">Zwraca listę wszystkich bram do brzegu w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="547a8-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="547a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="547a8-104">SYNTAX</span></span>

### <span data-ttu-id="547a8-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="547a8-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="547a8-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="547a8-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="547a8-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="547a8-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="547a8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="547a8-108">DESCRIPTION</span></span>
<span data-ttu-id="547a8-109">Zwraca listę wszystkich bram do brzegu w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="547a8-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="547a8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="547a8-110">EXAMPLES</span></span>

### <span data-ttu-id="547a8-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="547a8-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="547a8-112">Zapoznaj się z listą wszystkich bram do brzegu.</span><span class="sxs-lookup"><span data-stu-id="547a8-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="547a8-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="547a8-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="547a8-114">Uzyskaj określoną bramę Edge.</span><span class="sxs-lookup"><span data-stu-id="547a8-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="547a8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="547a8-115">PARAMETERS</span></span>

### <span data-ttu-id="547a8-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="547a8-116">-Name</span></span>
<span data-ttu-id="547a8-117">Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="547a8-117">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="547a8-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="547a8-118">-Location</span></span>
<span data-ttu-id="547a8-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="547a8-119">Location of the resource.</span></span>

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

### <span data-ttu-id="547a8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="547a8-120">-ResourceGroupName</span></span>
<span data-ttu-id="547a8-121">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="547a8-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="547a8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="547a8-122">-ResourceId</span></span>
<span data-ttu-id="547a8-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="547a8-123">The resource id.</span></span>

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

### <span data-ttu-id="547a8-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="547a8-124">-Filter</span></span>
<span data-ttu-id="547a8-125">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="547a8-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="547a8-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="547a8-126">-Skip</span></span>
<span data-ttu-id="547a8-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="547a8-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="547a8-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="547a8-128">-Top</span></span>
<span data-ttu-id="547a8-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="547a8-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="547a8-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="547a8-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="547a8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547a8-131">CommonParameters</span></span>
<span data-ttu-id="547a8-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="547a8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547a8-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="547a8-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547a8-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="547a8-134">INPUTS</span></span>

## <span data-ttu-id="547a8-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="547a8-135">OUTPUTS</span></span>

### <span data-ttu-id="547a8-136">Microsoft. AzureStack. Management. Fabric. admin. models. EdgeGateway</span><span class="sxs-lookup"><span data-stu-id="547a8-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="547a8-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="547a8-137">NOTES</span></span>

## <span data-ttu-id="547a8-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="547a8-138">RELATED LINKS</span></span>
