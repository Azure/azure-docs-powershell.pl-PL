---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 39955a2b99ffd7e3c604b4fc288f117face8205f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710680"
---
# <span data-ttu-id="a241a-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="a241a-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="a241a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a241a-102">SYNOPSIS</span></span>
<span data-ttu-id="a241a-103">Zwraca listę wszystkich wystąpień ról infrastruktury w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a241a-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="a241a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a241a-104">SYNTAX</span></span>

### <span data-ttu-id="a241a-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a241a-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a241a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="a241a-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a241a-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="a241a-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a241a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a241a-108">DESCRIPTION</span></span>
<span data-ttu-id="a241a-109">Zwraca listę wszystkich wystąpień ról infrastruktury w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a241a-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="a241a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a241a-110">EXAMPLES</span></span>

### <span data-ttu-id="a241a-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a241a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="a241a-112">Zwraca listę wszystkich wystąpień ról infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="a241a-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="a241a-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a241a-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="a241a-114">Zwracanie pojedynczego wystąpienia roli infrastruktury na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="a241a-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="a241a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a241a-115">PARAMETERS</span></span>

### <span data-ttu-id="a241a-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="a241a-116">-Filter</span></span>
<span data-ttu-id="a241a-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="a241a-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="a241a-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a241a-118">-Location</span></span>
<span data-ttu-id="a241a-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="a241a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="a241a-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a241a-120">-Name</span></span>
<span data-ttu-id="a241a-121">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="a241a-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="a241a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a241a-122">-ResourceGroupName</span></span>
<span data-ttu-id="a241a-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="a241a-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a241a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a241a-124">-ResourceId</span></span>
<span data-ttu-id="a241a-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a241a-125">The resource id.</span></span>

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

### <span data-ttu-id="a241a-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="a241a-126">-Skip</span></span>
<span data-ttu-id="a241a-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="a241a-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a241a-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="a241a-128">-Top</span></span>
<span data-ttu-id="a241a-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="a241a-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a241a-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="a241a-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a241a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a241a-131">CommonParameters</span></span>
<span data-ttu-id="a241a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a241a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a241a-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a241a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a241a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a241a-134">INPUTS</span></span>

## <span data-ttu-id="a241a-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a241a-135">OUTPUTS</span></span>

### <span data-ttu-id="a241a-136">Microsoft. AzureStack. Management. Fabric. admin. models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="a241a-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="a241a-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a241a-137">NOTES</span></span>

## <span data-ttu-id="a241a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a241a-138">RELATED LINKS</span></span>

