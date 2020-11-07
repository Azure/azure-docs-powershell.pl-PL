---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 752bd7f183bf5a5bdad7950e6567024cbe5b8dec
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889914"
---
# <span data-ttu-id="ad77d-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="ad77d-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="ad77d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad77d-102">SYNOPSIS</span></span>
<span data-ttu-id="ad77d-103">Zwraca listę kondycji każdej usługi.</span><span class="sxs-lookup"><span data-stu-id="ad77d-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="ad77d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad77d-104">SYNTAX</span></span>

### <span data-ttu-id="ad77d-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ad77d-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ad77d-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ad77d-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ad77d-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="ad77d-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ad77d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ad77d-108">DESCRIPTION</span></span>
<span data-ttu-id="ad77d-109">Zwraca listę kondycji każdej usługi.</span><span class="sxs-lookup"><span data-stu-id="ad77d-109">Returns a list of each service's health.</span></span> <span data-ttu-id="ad77d-110">Właściwość AlertSummary zawiera szczegóły dotyczące liczników ostrzeżeń/błędów.</span><span class="sxs-lookup"><span data-stu-id="ad77d-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="ad77d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad77d-111">EXAMPLES</span></span>

### <span data-ttu-id="ad77d-112">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="ad77d-112">EXAMPLE 1</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="ad77d-113">Zwraca listę kondycji każdej usługi.</span><span class="sxs-lookup"><span data-stu-id="ad77d-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="ad77d-114">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="ad77d-114">EXAMPLE 2</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="ad77d-115">Zwraca wartość kondycji usługi.</span><span class="sxs-lookup"><span data-stu-id="ad77d-115">Returns a service's health.</span></span>

## <span data-ttu-id="ad77d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad77d-116">PARAMETERS</span></span>

### <span data-ttu-id="ad77d-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad77d-117">-Name</span></span>
<span data-ttu-id="ad77d-118">Nazwa kondycji usługi.</span><span class="sxs-lookup"><span data-stu-id="ad77d-118">Service Health name.</span></span>

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

### <span data-ttu-id="ad77d-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ad77d-119">-Location</span></span>
<span data-ttu-id="ad77d-120">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="ad77d-120">Name of the region</span></span>

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

### <span data-ttu-id="ad77d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad77d-121">-ResourceGroupName</span></span>
<span data-ttu-id="ad77d-122">Nazwa grupy zasobów, opcjonalna.</span><span class="sxs-lookup"><span data-stu-id="ad77d-122">Name of the resource group, optional.</span></span>

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

### <span data-ttu-id="ad77d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad77d-123">-ResourceId</span></span>
<span data-ttu-id="ad77d-124">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="ad77d-124">The resource id.</span></span>

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

### <span data-ttu-id="ad77d-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="ad77d-125">-Filter</span></span>
<span data-ttu-id="ad77d-126">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="ad77d-126">OData filter parameter.</span></span>

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

### <span data-ttu-id="ad77d-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="ad77d-127">-Skip</span></span>
<span data-ttu-id="ad77d-128">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="ad77d-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ad77d-129">-Początek</span><span class="sxs-lookup"><span data-stu-id="ad77d-129">-Top</span></span>
<span data-ttu-id="ad77d-130">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="ad77d-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ad77d-131">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="ad77d-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ad77d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad77d-132">CommonParameters</span></span>
<span data-ttu-id="ad77d-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad77d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad77d-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad77d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad77d-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad77d-135">INPUTS</span></span>

## <span data-ttu-id="ad77d-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad77d-136">OUTPUTS</span></span>

### <span data-ttu-id="ad77d-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. servicehealth</span><span class="sxs-lookup"><span data-stu-id="ad77d-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="ad77d-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad77d-138">NOTES</span></span>

## <span data-ttu-id="ad77d-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad77d-139">RELATED LINKS</span></span>
