---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07cb5e675003eccc9fad54e723e80a0ddb73ff9a
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889961"
---
# <span data-ttu-id="1b30d-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="1b30d-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="1b30d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b30d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b30d-103">Zwraca listę wszystkich węzłów jednostek skali w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="1b30d-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="1b30d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b30d-104">SYNTAX</span></span>

### <span data-ttu-id="1b30d-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="1b30d-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1b30d-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="1b30d-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1b30d-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="1b30d-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1b30d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1b30d-108">DESCRIPTION</span></span>
<span data-ttu-id="1b30d-109">Zwraca listę wszystkich węzłów jednostek skali w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="1b30d-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="1b30d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b30d-110">EXAMPLES</span></span>

### <span data-ttu-id="1b30d-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="1b30d-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="1b30d-112">Pobierz wszystkie węzły jednostki skalowania w miejscu.</span><span class="sxs-lookup"><span data-stu-id="1b30d-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="1b30d-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="1b30d-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="1b30d-114">Uzyskiwanie określonego węzła jednostki skali w lokalizacji o nazwie.</span><span class="sxs-lookup"><span data-stu-id="1b30d-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="1b30d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b30d-115">PARAMETERS</span></span>

### <span data-ttu-id="1b30d-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b30d-116">-Name</span></span>
<span data-ttu-id="1b30d-117">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="1b30d-117">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="1b30d-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1b30d-118">-Location</span></span>
<span data-ttu-id="1b30d-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="1b30d-119">Location of the resource.</span></span>

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

### <span data-ttu-id="1b30d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b30d-120">-ResourceGroupName</span></span>
<span data-ttu-id="1b30d-121">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="1b30d-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1b30d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b30d-122">-ResourceId</span></span>
<span data-ttu-id="1b30d-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="1b30d-123">The resource id.</span></span>

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

### <span data-ttu-id="1b30d-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="1b30d-124">-Filter</span></span>
<span data-ttu-id="1b30d-125">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="1b30d-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="1b30d-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="1b30d-126">-Skip</span></span>
<span data-ttu-id="1b30d-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="1b30d-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1b30d-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="1b30d-128">-Top</span></span>
<span data-ttu-id="1b30d-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="1b30d-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1b30d-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="1b30d-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1b30d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b30d-131">CommonParameters</span></span>
<span data-ttu-id="1b30d-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b30d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b30d-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b30d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b30d-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b30d-134">INPUTS</span></span>

## <span data-ttu-id="1b30d-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b30d-135">OUTPUTS</span></span>

### <span data-ttu-id="1b30d-136">Microsoft. AzureStack. Management. Fabric. admin. models. ScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="1b30d-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="1b30d-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b30d-137">NOTES</span></span>

## <span data-ttu-id="1b30d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b30d-138">RELATED LINKS</span></span>
