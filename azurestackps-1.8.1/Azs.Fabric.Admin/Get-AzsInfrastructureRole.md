---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a20f0fbc5b059e878f0062569ffba2c16794204
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889674"
---
# <span data-ttu-id="feeb7-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="feeb7-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="feeb7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="feeb7-102">SYNOPSIS</span></span>
<span data-ttu-id="feeb7-103">Zwraca listę wszystkich ról infrastruktury w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="feeb7-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="feeb7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="feeb7-104">SYNTAX</span></span>

### <span data-ttu-id="feeb7-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="feeb7-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="feeb7-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="feeb7-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="feeb7-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="feeb7-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="feeb7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="feeb7-108">DESCRIPTION</span></span>
<span data-ttu-id="feeb7-109">Zwraca listę wszystkich ról infrastruktury w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="feeb7-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="feeb7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="feeb7-110">EXAMPLES</span></span>

### <span data-ttu-id="feeb7-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="feeb7-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="feeb7-112">Zapoznaj się z listą wszystkich ról infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="feeb7-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="feeb7-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="feeb7-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="feeb7-114">Uzyskaj rolę infrastruktury na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="feeb7-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="feeb7-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="feeb7-115">PARAMETERS</span></span>

### <span data-ttu-id="feeb7-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="feeb7-116">-Name</span></span>
<span data-ttu-id="feeb7-117">Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="feeb7-117">Infrastructure role name.</span></span>

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

### <span data-ttu-id="feeb7-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="feeb7-118">-Location</span></span>
<span data-ttu-id="feeb7-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="feeb7-119">Location of the resource.</span></span>

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

### <span data-ttu-id="feeb7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feeb7-120">-ResourceGroupName</span></span>
<span data-ttu-id="feeb7-121">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="feeb7-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="feeb7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="feeb7-122">-ResourceId</span></span>
<span data-ttu-id="feeb7-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="feeb7-123">The resource id.</span></span>

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

### <span data-ttu-id="feeb7-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="feeb7-124">-Filter</span></span>
<span data-ttu-id="feeb7-125">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="feeb7-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="feeb7-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="feeb7-126">-Skip</span></span>
<span data-ttu-id="feeb7-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="feeb7-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="feeb7-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="feeb7-128">-Top</span></span>
<span data-ttu-id="feeb7-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="feeb7-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="feeb7-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="feeb7-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="feeb7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feeb7-131">CommonParameters</span></span>
<span data-ttu-id="feeb7-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feeb7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feeb7-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feeb7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feeb7-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="feeb7-134">INPUTS</span></span>

## <span data-ttu-id="feeb7-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="feeb7-135">OUTPUTS</span></span>

### <span data-ttu-id="feeb7-136">Microsoft. AzureStack. Management. Fabric. admin. models. InfraRole</span><span class="sxs-lookup"><span data-stu-id="feeb7-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="feeb7-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="feeb7-137">NOTES</span></span>

## <span data-ttu-id="feeb7-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="feeb7-138">RELATED LINKS</span></span>
