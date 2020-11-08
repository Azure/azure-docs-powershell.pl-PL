---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc074d17ea73bf54f623ea3e8ec72567ef2bcffe
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055612"
---
# <span data-ttu-id="fcd27-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="fcd27-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="fcd27-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fcd27-102">SYNOPSIS</span></span>
<span data-ttu-id="fcd27-103">Zwraca listę wszystkich lokalizacji sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="fcd27-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="fcd27-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fcd27-104">SYNTAX</span></span>

### <span data-ttu-id="fcd27-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="fcd27-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="fcd27-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="fcd27-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="fcd27-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="fcd27-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="fcd27-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fcd27-108">DESCRIPTION</span></span>
<span data-ttu-id="fcd27-109">Zwraca listę wszystkich lokalizacji sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="fcd27-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="fcd27-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fcd27-110">EXAMPLES</span></span>

### <span data-ttu-id="fcd27-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="fcd27-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="fcd27-112">Zwracanie listy wszystkich lokalizacji sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="fcd27-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="fcd27-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="fcd27-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="fcd27-114">Zwraca lokalizację na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="fcd27-114">Return a location based on the name.</span></span>

## <span data-ttu-id="fcd27-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fcd27-115">PARAMETERS</span></span>

### <span data-ttu-id="fcd27-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fcd27-116">-Location</span></span>
<span data-ttu-id="fcd27-117">Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="fcd27-117">Fabric location.</span></span>

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

### <span data-ttu-id="fcd27-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcd27-118">-ResourceGroupName</span></span>
<span data-ttu-id="fcd27-119">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="fcd27-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="fcd27-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcd27-120">-ResourceId</span></span>
<span data-ttu-id="fcd27-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="fcd27-121">The resource id.</span></span>

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

### <span data-ttu-id="fcd27-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="fcd27-122">-Filter</span></span>
<span data-ttu-id="fcd27-123">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="fcd27-123">OData filter parameter.</span></span>

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

### <span data-ttu-id="fcd27-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="fcd27-124">-Skip</span></span>
<span data-ttu-id="fcd27-125">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="fcd27-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="fcd27-126">-Początek</span><span class="sxs-lookup"><span data-stu-id="fcd27-126">-Top</span></span>
<span data-ttu-id="fcd27-127">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="fcd27-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="fcd27-128">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="fcd27-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="fcd27-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd27-129">CommonParameters</span></span>
<span data-ttu-id="fcd27-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcd27-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd27-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcd27-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd27-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcd27-132">INPUTS</span></span>

## <span data-ttu-id="fcd27-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fcd27-133">OUTPUTS</span></span>

### <span data-ttu-id="fcd27-134">Microsoft. AzureStack. Management. Fabric. admin. models. FabricLocation</span><span class="sxs-lookup"><span data-stu-id="fcd27-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="fcd27-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fcd27-135">NOTES</span></span>

## <span data-ttu-id="fcd27-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcd27-136">RELATED LINKS</span></span>
