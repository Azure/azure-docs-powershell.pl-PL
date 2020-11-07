---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c5fe6e28ff87cfd3f365441d0e09f09ef21dc454
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889658"
---
# <span data-ttu-id="cfc32-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="cfc32-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="cfc32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cfc32-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc32-103">Zwraca listę wszystkich wystąpień ról infrastruktury w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="cfc32-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="cfc32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cfc32-104">SYNTAX</span></span>

### <span data-ttu-id="cfc32-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="cfc32-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="cfc32-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="cfc32-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="cfc32-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="cfc32-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="cfc32-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cfc32-108">DESCRIPTION</span></span>
<span data-ttu-id="cfc32-109">Zwraca listę wszystkich wystąpień ról infrastruktury w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="cfc32-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="cfc32-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cfc32-110">EXAMPLES</span></span>

### <span data-ttu-id="cfc32-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="cfc32-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="cfc32-112">Zwraca listę wszystkich wystąpień ról infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="cfc32-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="cfc32-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="cfc32-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="cfc32-114">Zwracanie pojedynczego wystąpienia roli infrastruktury na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="cfc32-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="cfc32-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cfc32-115">PARAMETERS</span></span>

### <span data-ttu-id="cfc32-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cfc32-116">-Name</span></span>
<span data-ttu-id="cfc32-117">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="cfc32-117">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="cfc32-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cfc32-118">-Location</span></span>
<span data-ttu-id="cfc32-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="cfc32-119">Location of the resource.</span></span>

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

### <span data-ttu-id="cfc32-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfc32-120">-ResourceGroupName</span></span>
<span data-ttu-id="cfc32-121">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="cfc32-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="cfc32-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfc32-122">-ResourceId</span></span>
<span data-ttu-id="cfc32-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="cfc32-123">The resource id.</span></span>

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

### <span data-ttu-id="cfc32-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="cfc32-124">-Filter</span></span>
<span data-ttu-id="cfc32-125">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="cfc32-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="cfc32-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="cfc32-126">-Skip</span></span>
<span data-ttu-id="cfc32-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="cfc32-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="cfc32-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="cfc32-128">-Top</span></span>
<span data-ttu-id="cfc32-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="cfc32-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="cfc32-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="cfc32-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="cfc32-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc32-131">CommonParameters</span></span>
<span data-ttu-id="cfc32-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfc32-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc32-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfc32-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc32-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfc32-134">INPUTS</span></span>

## <span data-ttu-id="cfc32-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cfc32-135">OUTPUTS</span></span>

### <span data-ttu-id="cfc32-136">Microsoft. AzureStack. Management. Fabric. admin. models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="cfc32-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="cfc32-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cfc32-137">NOTES</span></span>

## <span data-ttu-id="cfc32-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cfc32-138">RELATED LINKS</span></span>
