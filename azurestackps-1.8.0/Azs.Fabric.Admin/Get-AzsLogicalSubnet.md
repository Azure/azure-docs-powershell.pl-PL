---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb535146787c4c33a57ad406f05544f18ba74eb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888962"
---
# <span data-ttu-id="c5de7-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="c5de7-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="c5de7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5de7-102">SYNOPSIS</span></span>
<span data-ttu-id="c5de7-103">Zwraca listę wszystkich podsieci logicznych.</span><span class="sxs-lookup"><span data-stu-id="c5de7-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="c5de7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5de7-104">SYNTAX</span></span>

### <span data-ttu-id="c5de7-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c5de7-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c5de7-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c5de7-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5de7-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="c5de7-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c5de7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c5de7-108">DESCRIPTION</span></span>
<span data-ttu-id="c5de7-109">Zwraca listę wszystkich podsieci logicznych.</span><span class="sxs-lookup"><span data-stu-id="c5de7-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="c5de7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5de7-110">EXAMPLES</span></span>

### <span data-ttu-id="c5de7-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="c5de7-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="c5de7-112">Zapoznaj się z listą wszystkich podsieci logicznych dla danej sieci logicznej i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c5de7-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="c5de7-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="c5de7-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="c5de7-114">Uzyskaj określoną podsieć logiczną dla danej sieci logicznej i lokalizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="c5de7-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="c5de7-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5de7-115">PARAMETERS</span></span>

### <span data-ttu-id="c5de7-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c5de7-116">-Name</span></span>
<span data-ttu-id="c5de7-117">Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="c5de7-117">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="c5de7-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="c5de7-118">-LogicalNetwork</span></span>
<span data-ttu-id="c5de7-119">Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="c5de7-119">Name of the logical network.</span></span>

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

### <span data-ttu-id="c5de7-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c5de7-120">-Location</span></span>
<span data-ttu-id="c5de7-121">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="c5de7-121">Location of the resource.</span></span>

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

### <span data-ttu-id="c5de7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5de7-122">-ResourceGroupName</span></span>
<span data-ttu-id="c5de7-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="c5de7-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c5de7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5de7-124">-ResourceId</span></span>
<span data-ttu-id="c5de7-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="c5de7-125">The resource id.</span></span>

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

### <span data-ttu-id="c5de7-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="c5de7-126">-Filter</span></span>
<span data-ttu-id="c5de7-127">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="c5de7-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="c5de7-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="c5de7-128">-Skip</span></span>
<span data-ttu-id="c5de7-129">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="c5de7-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c5de7-130">-Początek</span><span class="sxs-lookup"><span data-stu-id="c5de7-130">-Top</span></span>
<span data-ttu-id="c5de7-131">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="c5de7-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c5de7-132">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="c5de7-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c5de7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5de7-133">CommonParameters</span></span>
<span data-ttu-id="c5de7-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5de7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5de7-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5de7-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5de7-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5de7-136">INPUTS</span></span>

## <span data-ttu-id="c5de7-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5de7-137">OUTPUTS</span></span>

### <span data-ttu-id="c5de7-138">Microsoft. AzureStack. Management. Fabric. admin. models. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="c5de7-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="c5de7-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5de7-139">NOTES</span></span>

## <span data-ttu-id="c5de7-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5de7-140">RELATED LINKS</span></span>
