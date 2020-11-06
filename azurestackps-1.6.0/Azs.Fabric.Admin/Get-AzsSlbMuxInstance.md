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
ms.locfileid: "93523822"
---
# <span data-ttu-id="f631a-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="f631a-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="f631a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f631a-102">SYNOPSIS</span></span>
<span data-ttu-id="f631a-103">Zwraca listę wszystkich wystąpień programowego modułu równoważenia obciążenia w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f631a-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="f631a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f631a-104">SYNTAX</span></span>

### <span data-ttu-id="f631a-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f631a-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f631a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f631a-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="f631a-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="f631a-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f631a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f631a-108">DESCRIPTION</span></span>
<span data-ttu-id="f631a-109">Zwraca listę wszystkich wystąpień programowego modułu równoważenia obciążenia w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f631a-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="f631a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f631a-110">EXAMPLES</span></span>

### <span data-ttu-id="f631a-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f631a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="f631a-112">Pobierz wszystkie wystąpienia multipleksera programowego modułu równoważenia obciążenia w miejscu.</span><span class="sxs-lookup"><span data-stu-id="f631a-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="f631a-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f631a-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="f631a-114">Uzyskiwanie określonego wystąpienia multipleksera programowego modułu równoważenia obciążenia w lokalizacji o nazwie.</span><span class="sxs-lookup"><span data-stu-id="f631a-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="f631a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f631a-115">PARAMETERS</span></span>

### <span data-ttu-id="f631a-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="f631a-116">-Filter</span></span>
<span data-ttu-id="f631a-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="f631a-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="f631a-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f631a-118">-Location</span></span>
<span data-ttu-id="f631a-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="f631a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="f631a-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f631a-120">-Name</span></span>
<span data-ttu-id="f631a-121">Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f631a-121">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="f631a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f631a-122">-ResourceGroupName</span></span>
<span data-ttu-id="f631a-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="f631a-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="f631a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f631a-124">-ResourceId</span></span>
<span data-ttu-id="f631a-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f631a-125">The resource id.</span></span>

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

### <span data-ttu-id="f631a-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="f631a-126">-Skip</span></span>
<span data-ttu-id="f631a-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="f631a-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f631a-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="f631a-128">-Top</span></span>
<span data-ttu-id="f631a-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="f631a-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f631a-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="f631a-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f631a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f631a-131">CommonParameters</span></span>
<span data-ttu-id="f631a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f631a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f631a-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f631a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f631a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f631a-134">INPUTS</span></span>

## <span data-ttu-id="f631a-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f631a-135">OUTPUTS</span></span>

### <span data-ttu-id="f631a-136">Microsoft. AzureStack. Management. Fabric. admin. models. SlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="f631a-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="f631a-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f631a-137">NOTES</span></span>

## <span data-ttu-id="f631a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f631a-138">RELATED LINKS</span></span>

