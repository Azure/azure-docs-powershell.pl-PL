---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821495581589eff356cd0d88fc98311b5f566d61
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888937"
---
# <span data-ttu-id="5786a-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="5786a-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="5786a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5786a-102">SYNOPSIS</span></span>
<span data-ttu-id="5786a-103">Zwraca listę wszystkich wystąpień programowego modułu równoważenia obciążenia w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="5786a-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="5786a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5786a-104">SYNTAX</span></span>

### <span data-ttu-id="5786a-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="5786a-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5786a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="5786a-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5786a-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="5786a-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5786a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5786a-108">DESCRIPTION</span></span>
<span data-ttu-id="5786a-109">Zwraca listę wszystkich wystąpień programowego modułu równoważenia obciążenia w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="5786a-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="5786a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5786a-110">EXAMPLES</span></span>

### <span data-ttu-id="5786a-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="5786a-111">EXAMPLE 1</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="5786a-112">Pobierz wszystkie wystąpienia multipleksera programowego modułu równoważenia obciążenia w miejscu.</span><span class="sxs-lookup"><span data-stu-id="5786a-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="5786a-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="5786a-113">EXAMPLE 2</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="5786a-114">Uzyskiwanie określonego wystąpienia multipleksera programowego modułu równoważenia obciążenia w lokalizacji o nazwie.</span><span class="sxs-lookup"><span data-stu-id="5786a-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="5786a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5786a-115">PARAMETERS</span></span>

### <span data-ttu-id="5786a-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5786a-116">-Name</span></span>
<span data-ttu-id="5786a-117">Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5786a-117">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="5786a-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5786a-118">-Location</span></span>
<span data-ttu-id="5786a-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="5786a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="5786a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5786a-120">-ResourceGroupName</span></span>
<span data-ttu-id="5786a-121">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="5786a-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5786a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5786a-122">-ResourceId</span></span>
<span data-ttu-id="5786a-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="5786a-123">The resource id.</span></span>

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

### <span data-ttu-id="5786a-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="5786a-124">-Filter</span></span>
<span data-ttu-id="5786a-125">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="5786a-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="5786a-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="5786a-126">-Skip</span></span>
<span data-ttu-id="5786a-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="5786a-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5786a-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="5786a-128">-Top</span></span>
<span data-ttu-id="5786a-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="5786a-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5786a-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="5786a-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5786a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5786a-131">CommonParameters</span></span>
<span data-ttu-id="5786a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5786a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5786a-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5786a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5786a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5786a-134">INPUTS</span></span>

## <span data-ttu-id="5786a-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5786a-135">OUTPUTS</span></span>

### <span data-ttu-id="5786a-136">Microsoft. AzureStack. Management. Fabric. admin. models. SlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="5786a-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="5786a-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5786a-137">NOTES</span></span>

## <span data-ttu-id="5786a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5786a-138">RELATED LINKS</span></span>
