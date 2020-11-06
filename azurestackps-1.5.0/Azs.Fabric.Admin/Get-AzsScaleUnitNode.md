---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d5870624b6d39b3e821ed6a7fb76d87c8422ab2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523058"
---
# <span data-ttu-id="1751b-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="1751b-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="1751b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1751b-102">SYNOPSIS</span></span>
<span data-ttu-id="1751b-103">Zwraca listę wszystkich węzłów jednostek skali w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="1751b-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="1751b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1751b-104">SYNTAX</span></span>

### <span data-ttu-id="1751b-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="1751b-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1751b-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="1751b-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1751b-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="1751b-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1751b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1751b-108">DESCRIPTION</span></span>
<span data-ttu-id="1751b-109">Zwraca listę wszystkich węzłów jednostek skali w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="1751b-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="1751b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1751b-110">EXAMPLES</span></span>

### <span data-ttu-id="1751b-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1751b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="1751b-112">Pobierz wszystkie węzły jednostki skalowania w miejscu.</span><span class="sxs-lookup"><span data-stu-id="1751b-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="1751b-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1751b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="1751b-114">Uzyskiwanie określonego węzła jednostki skali w lokalizacji o nazwie.</span><span class="sxs-lookup"><span data-stu-id="1751b-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="1751b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1751b-115">PARAMETERS</span></span>

### <span data-ttu-id="1751b-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="1751b-116">-Filter</span></span>
<span data-ttu-id="1751b-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="1751b-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="1751b-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1751b-118">-Location</span></span>
<span data-ttu-id="1751b-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="1751b-119">Location of the resource.</span></span>

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

### <span data-ttu-id="1751b-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1751b-120">-Name</span></span>
<span data-ttu-id="1751b-121">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="1751b-121">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="1751b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1751b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1751b-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="1751b-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1751b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1751b-124">-ResourceId</span></span>
<span data-ttu-id="1751b-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="1751b-125">The resource id.</span></span>

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

### <span data-ttu-id="1751b-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="1751b-126">-Skip</span></span>
<span data-ttu-id="1751b-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="1751b-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1751b-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="1751b-128">-Top</span></span>
<span data-ttu-id="1751b-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="1751b-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1751b-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="1751b-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1751b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1751b-131">CommonParameters</span></span>
<span data-ttu-id="1751b-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1751b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1751b-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1751b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1751b-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1751b-134">INPUTS</span></span>

## <span data-ttu-id="1751b-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1751b-135">OUTPUTS</span></span>

### <span data-ttu-id="1751b-136">Microsoft. AzureStack. Management. Fabric. admin. models. ScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="1751b-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="1751b-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1751b-137">NOTES</span></span>

## <span data-ttu-id="1751b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1751b-138">RELATED LINKS</span></span>

