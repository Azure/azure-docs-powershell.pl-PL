---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef5db457846f6fdf0dcd0a0a32b37cab96a557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888266"
---
# <span data-ttu-id="dcaff-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="dcaff-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="dcaff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dcaff-102">SYNOPSIS</span></span>
<span data-ttu-id="dcaff-103">Zwraca listę wszystkich podsieci logicznych.</span><span class="sxs-lookup"><span data-stu-id="dcaff-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="dcaff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dcaff-104">SYNTAX</span></span>

### <span data-ttu-id="dcaff-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="dcaff-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="dcaff-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="dcaff-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="dcaff-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="dcaff-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="dcaff-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dcaff-108">DESCRIPTION</span></span>
<span data-ttu-id="dcaff-109">Zwraca listę wszystkich podsieci logicznych.</span><span class="sxs-lookup"><span data-stu-id="dcaff-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="dcaff-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dcaff-110">EXAMPLES</span></span>

### <span data-ttu-id="dcaff-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dcaff-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="dcaff-112">Zapoznaj się z listą wszystkich podsieci logicznych dla danej sieci logicznej i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="dcaff-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="dcaff-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="dcaff-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="dcaff-114">Uzyskaj określoną podsieć logiczną dla danej sieci logicznej i lokalizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="dcaff-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="dcaff-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dcaff-115">PARAMETERS</span></span>

### <span data-ttu-id="dcaff-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="dcaff-116">-Filter</span></span>
<span data-ttu-id="dcaff-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="dcaff-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="dcaff-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dcaff-118">-Location</span></span>
<span data-ttu-id="dcaff-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="dcaff-119">Location of the resource.</span></span>

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

### <span data-ttu-id="dcaff-120">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="dcaff-120">-LogicalNetwork</span></span>
<span data-ttu-id="dcaff-121">Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="dcaff-121">Name of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcaff-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dcaff-122">-Name</span></span>
<span data-ttu-id="dcaff-123">Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="dcaff-123">Name of the logical subnet.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcaff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcaff-124">-ResourceGroupName</span></span>
<span data-ttu-id="dcaff-125">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="dcaff-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="dcaff-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcaff-126">-ResourceId</span></span>
<span data-ttu-id="dcaff-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="dcaff-127">The resource id.</span></span>

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

### <span data-ttu-id="dcaff-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="dcaff-128">-Skip</span></span>
<span data-ttu-id="dcaff-129">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="dcaff-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="dcaff-130">-Początek</span><span class="sxs-lookup"><span data-stu-id="dcaff-130">-Top</span></span>
<span data-ttu-id="dcaff-131">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="dcaff-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="dcaff-132">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="dcaff-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="dcaff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcaff-133">CommonParameters</span></span>
<span data-ttu-id="dcaff-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcaff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcaff-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcaff-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcaff-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcaff-136">INPUTS</span></span>

## <span data-ttu-id="dcaff-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dcaff-137">OUTPUTS</span></span>

### <span data-ttu-id="dcaff-138">Microsoft. AzureStack. Management. Fabric. admin. models. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="dcaff-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="dcaff-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dcaff-139">NOTES</span></span>

## <span data-ttu-id="dcaff-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcaff-140">RELATED LINKS</span></span>

