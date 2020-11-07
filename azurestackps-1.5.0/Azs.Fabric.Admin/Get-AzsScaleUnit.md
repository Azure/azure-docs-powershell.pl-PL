---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 869cd48507ba9384026f8e58b9cd7853179b844f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710664"
---
# <span data-ttu-id="3423a-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="3423a-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="3423a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3423a-102">SYNOPSIS</span></span>
<span data-ttu-id="3423a-103">Zwraca listę wszystkich jednostek skali w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="3423a-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="3423a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3423a-104">SYNTAX</span></span>

### <span data-ttu-id="3423a-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="3423a-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3423a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3423a-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3423a-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="3423a-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3423a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3423a-108">DESCRIPTION</span></span>
<span data-ttu-id="3423a-109">Zwraca listę wszystkich jednostek skali w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="3423a-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="3423a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3423a-110">EXAMPLES</span></span>

### <span data-ttu-id="3423a-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3423a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="3423a-112">Zwracanie listy informacji o jednostkach skali.</span><span class="sxs-lookup"><span data-stu-id="3423a-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="3423a-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3423a-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="3423a-114">Zwracają informacje o określonej jednostce skali.</span><span class="sxs-lookup"><span data-stu-id="3423a-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="3423a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3423a-115">PARAMETERS</span></span>

### <span data-ttu-id="3423a-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="3423a-116">-Filter</span></span>
<span data-ttu-id="3423a-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="3423a-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="3423a-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3423a-118">-Location</span></span>
<span data-ttu-id="3423a-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="3423a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="3423a-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3423a-120">-Name</span></span>
<span data-ttu-id="3423a-121">Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="3423a-121">Name of the scale units.</span></span>

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

### <span data-ttu-id="3423a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3423a-122">-ResourceGroupName</span></span>
<span data-ttu-id="3423a-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="3423a-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="3423a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3423a-124">-ResourceId</span></span>
<span data-ttu-id="3423a-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="3423a-125">The resource id.</span></span>

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

### <span data-ttu-id="3423a-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="3423a-126">-Skip</span></span>
<span data-ttu-id="3423a-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="3423a-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3423a-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="3423a-128">-Top</span></span>
<span data-ttu-id="3423a-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="3423a-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3423a-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="3423a-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3423a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3423a-131">CommonParameters</span></span>
<span data-ttu-id="3423a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3423a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3423a-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3423a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3423a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3423a-134">INPUTS</span></span>

## <span data-ttu-id="3423a-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3423a-135">OUTPUTS</span></span>

### <span data-ttu-id="3423a-136">Microsoft. AzureStack. Management. Fabric. admin. models. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="3423a-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="3423a-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3423a-137">NOTES</span></span>

## <span data-ttu-id="3423a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3423a-138">RELATED LINKS</span></span>

