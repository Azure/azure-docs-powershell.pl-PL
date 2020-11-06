---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dac95eced72f70d3471019136d302fcdfe95f86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523117"
---
# <span data-ttu-id="e417d-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="e417d-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="e417d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e417d-102">SYNOPSIS</span></span>
<span data-ttu-id="e417d-103">Zwraca listę wszystkich ról infrastruktury w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="e417d-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="e417d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e417d-104">SYNTAX</span></span>

### <span data-ttu-id="e417d-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e417d-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e417d-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e417d-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e417d-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="e417d-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e417d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e417d-108">DESCRIPTION</span></span>
<span data-ttu-id="e417d-109">Zwraca listę wszystkich ról infrastruktury w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="e417d-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="e417d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e417d-110">EXAMPLES</span></span>

### <span data-ttu-id="e417d-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e417d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="e417d-112">Zapoznaj się z listą wszystkich ról infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="e417d-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="e417d-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e417d-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="e417d-114">Uzyskaj rolę infrastruktury na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="e417d-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="e417d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e417d-115">PARAMETERS</span></span>

### <span data-ttu-id="e417d-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="e417d-116">-Filter</span></span>
<span data-ttu-id="e417d-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="e417d-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="e417d-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e417d-118">-Location</span></span>
<span data-ttu-id="e417d-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="e417d-119">Location of the resource.</span></span>

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

### <span data-ttu-id="e417d-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e417d-120">-Name</span></span>
<span data-ttu-id="e417d-121">Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="e417d-121">Infrastructure role name.</span></span>

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

### <span data-ttu-id="e417d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e417d-122">-ResourceGroupName</span></span>
<span data-ttu-id="e417d-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="e417d-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e417d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e417d-124">-ResourceId</span></span>
<span data-ttu-id="e417d-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e417d-125">The resource id.</span></span>

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

### <span data-ttu-id="e417d-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="e417d-126">-Skip</span></span>
<span data-ttu-id="e417d-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="e417d-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e417d-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="e417d-128">-Top</span></span>
<span data-ttu-id="e417d-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="e417d-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e417d-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="e417d-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e417d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e417d-131">CommonParameters</span></span>
<span data-ttu-id="e417d-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e417d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e417d-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e417d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e417d-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e417d-134">INPUTS</span></span>

## <span data-ttu-id="e417d-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e417d-135">OUTPUTS</span></span>

### <span data-ttu-id="e417d-136">Microsoft. AzureStack. Management. Fabric. admin. models. InfraRole</span><span class="sxs-lookup"><span data-stu-id="e417d-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="e417d-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e417d-137">NOTES</span></span>

## <span data-ttu-id="e417d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e417d-138">RELATED LINKS</span></span>

