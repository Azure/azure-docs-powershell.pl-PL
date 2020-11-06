---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e42278eb4ed402d561399dbd1077f819ef3d2cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523357"
---
# <span data-ttu-id="aecef-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="aecef-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="aecef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aecef-102">SYNOPSIS</span></span>
<span data-ttu-id="aecef-103">Zwraca listę kondycji każdej usługi.</span><span class="sxs-lookup"><span data-stu-id="aecef-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="aecef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aecef-104">SYNTAX</span></span>

### <span data-ttu-id="aecef-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="aecef-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="aecef-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="aecef-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="aecef-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="aecef-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="aecef-108">Opis</span><span class="sxs-lookup"><span data-stu-id="aecef-108">DESCRIPTION</span></span>
<span data-ttu-id="aecef-109">Zwraca listę kondycji każdej usługi.</span><span class="sxs-lookup"><span data-stu-id="aecef-109">Returns a list of each service's health.</span></span> <span data-ttu-id="aecef-110">Właściwość AlertSummary zawiera szczegóły dotyczące liczników ostrzeżeń/błędów.</span><span class="sxs-lookup"><span data-stu-id="aecef-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="aecef-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aecef-111">EXAMPLES</span></span>

### <span data-ttu-id="aecef-112">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="aecef-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="aecef-113">Zwraca listę kondycji każdej usługi.</span><span class="sxs-lookup"><span data-stu-id="aecef-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="aecef-114">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="aecef-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="aecef-115">Zwraca wartość kondycji usługi.</span><span class="sxs-lookup"><span data-stu-id="aecef-115">Returns a service's health.</span></span>

## <span data-ttu-id="aecef-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aecef-116">PARAMETERS</span></span>

### <span data-ttu-id="aecef-117">-Filter</span><span class="sxs-lookup"><span data-stu-id="aecef-117">-Filter</span></span>
<span data-ttu-id="aecef-118">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="aecef-118">OData filter parameter.</span></span>

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

### <span data-ttu-id="aecef-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="aecef-119">-Location</span></span>
<span data-ttu-id="aecef-120">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="aecef-120">Name of the region</span></span>

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

### <span data-ttu-id="aecef-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aecef-121">-Name</span></span>
<span data-ttu-id="aecef-122">Nazwa kondycji usługi.</span><span class="sxs-lookup"><span data-stu-id="aecef-122">Service Health name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ServiceHealth

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aecef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aecef-123">-ResourceGroupName</span></span>
<span data-ttu-id="aecef-124">Nazwa grupy zasobów, w której znajduje się dany zasób.</span><span class="sxs-lookup"><span data-stu-id="aecef-124">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="aecef-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aecef-125">-ResourceId</span></span>
<span data-ttu-id="aecef-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="aecef-126">The resource id.</span></span>

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

### <span data-ttu-id="aecef-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="aecef-127">-Skip</span></span>
<span data-ttu-id="aecef-128">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="aecef-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="aecef-129">-Początek</span><span class="sxs-lookup"><span data-stu-id="aecef-129">-Top</span></span>
<span data-ttu-id="aecef-130">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="aecef-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="aecef-131">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="aecef-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="aecef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aecef-132">CommonParameters</span></span>
<span data-ttu-id="aecef-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aecef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aecef-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aecef-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aecef-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aecef-135">INPUTS</span></span>

## <span data-ttu-id="aecef-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aecef-136">OUTPUTS</span></span>

### <span data-ttu-id="aecef-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. servicehealth</span><span class="sxs-lookup"><span data-stu-id="aecef-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="aecef-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aecef-138">NOTES</span></span>

## <span data-ttu-id="aecef-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aecef-139">RELATED LINKS</span></span>

