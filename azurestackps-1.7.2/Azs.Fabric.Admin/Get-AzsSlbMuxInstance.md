---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42d6233a99979687b7031ab58a620319fa675a28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887937"
---
# <span data-ttu-id="5af93-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="5af93-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="5af93-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5af93-102">SYNOPSIS</span></span>
<span data-ttu-id="5af93-103">Zwraca listę wszystkich wystąpień programowego modułu równoważenia obciążenia w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="5af93-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="5af93-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5af93-104">SYNTAX</span></span>

### <span data-ttu-id="5af93-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="5af93-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5af93-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="5af93-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5af93-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="5af93-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5af93-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5af93-108">DESCRIPTION</span></span>
<span data-ttu-id="5af93-109">Zwraca listę wszystkich wystąpień programowego modułu równoważenia obciążenia w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="5af93-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="5af93-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5af93-110">EXAMPLES</span></span>

### <span data-ttu-id="5af93-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5af93-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="5af93-112">Pobierz wszystkie wystąpienia multipleksera programowego modułu równoważenia obciążenia w miejscu.</span><span class="sxs-lookup"><span data-stu-id="5af93-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="5af93-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="5af93-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="5af93-114">Uzyskiwanie określonego wystąpienia multipleksera programowego modułu równoważenia obciążenia w lokalizacji o nazwie.</span><span class="sxs-lookup"><span data-stu-id="5af93-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="5af93-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5af93-115">PARAMETERS</span></span>

### <span data-ttu-id="5af93-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="5af93-116">-Filter</span></span>
<span data-ttu-id="5af93-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="5af93-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="5af93-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5af93-118">-Location</span></span>
<span data-ttu-id="5af93-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="5af93-119">Location of the resource.</span></span>

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

### <span data-ttu-id="5af93-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5af93-120">-Name</span></span>
<span data-ttu-id="5af93-121">Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5af93-121">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="5af93-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af93-122">-ResourceGroupName</span></span>
<span data-ttu-id="5af93-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="5af93-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5af93-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5af93-124">-ResourceId</span></span>
<span data-ttu-id="5af93-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="5af93-125">The resource id.</span></span>

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

### <span data-ttu-id="5af93-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="5af93-126">-Skip</span></span>
<span data-ttu-id="5af93-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="5af93-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5af93-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="5af93-128">-Top</span></span>
<span data-ttu-id="5af93-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="5af93-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5af93-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="5af93-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5af93-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af93-131">CommonParameters</span></span>
<span data-ttu-id="5af93-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5af93-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af93-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5af93-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af93-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5af93-134">INPUTS</span></span>

## <span data-ttu-id="5af93-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5af93-135">OUTPUTS</span></span>

### <span data-ttu-id="5af93-136">Microsoft. AzureStack. Management. Fabric. admin. models. SlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="5af93-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="5af93-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5af93-137">NOTES</span></span>

## <span data-ttu-id="5af93-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5af93-138">RELATED LINKS</span></span>

