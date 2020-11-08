---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07cb5e675003eccc9fad54e723e80a0ddb73ff9a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061643"
---
# <span data-ttu-id="b1358-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="b1358-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="b1358-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1358-102">SYNOPSIS</span></span>
<span data-ttu-id="b1358-103">Zwraca listę wszystkich węzłów jednostek skali w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b1358-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="b1358-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1358-104">SYNTAX</span></span>

### <span data-ttu-id="b1358-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b1358-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b1358-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="b1358-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b1358-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="b1358-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b1358-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b1358-108">DESCRIPTION</span></span>
<span data-ttu-id="b1358-109">Zwraca listę wszystkich węzłów jednostek skali w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b1358-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="b1358-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1358-110">EXAMPLES</span></span>

### <span data-ttu-id="b1358-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="b1358-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="b1358-112">Pobierz wszystkie węzły jednostki skalowania w miejscu.</span><span class="sxs-lookup"><span data-stu-id="b1358-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="b1358-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="b1358-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="b1358-114">Uzyskiwanie określonego węzła jednostki skali w lokalizacji o nazwie.</span><span class="sxs-lookup"><span data-stu-id="b1358-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="b1358-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1358-115">PARAMETERS</span></span>

### <span data-ttu-id="b1358-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b1358-116">-Name</span></span>
<span data-ttu-id="b1358-117">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="b1358-117">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="b1358-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b1358-118">-Location</span></span>
<span data-ttu-id="b1358-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="b1358-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b1358-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1358-120">-ResourceGroupName</span></span>
<span data-ttu-id="b1358-121">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="b1358-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b1358-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1358-122">-ResourceId</span></span>
<span data-ttu-id="b1358-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="b1358-123">The resource id.</span></span>

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

### <span data-ttu-id="b1358-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="b1358-124">-Filter</span></span>
<span data-ttu-id="b1358-125">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="b1358-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="b1358-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="b1358-126">-Skip</span></span>
<span data-ttu-id="b1358-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="b1358-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b1358-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="b1358-128">-Top</span></span>
<span data-ttu-id="b1358-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="b1358-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b1358-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="b1358-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b1358-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1358-131">CommonParameters</span></span>
<span data-ttu-id="b1358-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1358-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1358-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1358-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1358-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1358-134">INPUTS</span></span>

## <span data-ttu-id="b1358-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1358-135">OUTPUTS</span></span>

### <span data-ttu-id="b1358-136">Microsoft. AzureStack. Management. Fabric. admin. models. ScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="b1358-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="b1358-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1358-137">NOTES</span></span>

## <span data-ttu-id="b1358-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1358-138">RELATED LINKS</span></span>
