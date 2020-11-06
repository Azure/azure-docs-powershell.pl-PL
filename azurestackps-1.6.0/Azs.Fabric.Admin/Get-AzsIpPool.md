---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2528d9b4f9443d8857006b6fc1e94100b0b477ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523142"
---
# <span data-ttu-id="c08f3-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="c08f3-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="c08f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c08f3-102">SYNOPSIS</span></span>
<span data-ttu-id="c08f3-103">Zwraca listę wszystkich pul adresów IP w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c08f3-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="c08f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c08f3-104">SYNTAX</span></span>

### <span data-ttu-id="c08f3-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c08f3-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c08f3-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c08f3-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c08f3-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="c08f3-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c08f3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c08f3-108">DESCRIPTION</span></span>
<span data-ttu-id="c08f3-109">Zwraca listę wszystkich pul adresów IP w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c08f3-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="c08f3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c08f3-110">EXAMPLES</span></span>

### <span data-ttu-id="c08f3-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c08f3-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="c08f3-112">Pobierz wszystkie pule adresów IP infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="c08f3-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="c08f3-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c08f3-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="c08f3-114">Uzyskiwanie puli adresów IP infrastruktury na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="c08f3-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="c08f3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c08f3-115">PARAMETERS</span></span>

### <span data-ttu-id="c08f3-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="c08f3-116">-Filter</span></span>
<span data-ttu-id="c08f3-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="c08f3-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="c08f3-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c08f3-118">-Location</span></span>
<span data-ttu-id="c08f3-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="c08f3-119">Location of the resource.</span></span>

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

### <span data-ttu-id="c08f3-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c08f3-120">-Name</span></span>
<span data-ttu-id="c08f3-121">Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="c08f3-121">IP pool name.</span></span>

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

### <span data-ttu-id="c08f3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c08f3-122">-ResourceGroupName</span></span>
<span data-ttu-id="c08f3-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="c08f3-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c08f3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c08f3-124">-ResourceId</span></span>
<span data-ttu-id="c08f3-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="c08f3-125">The resource id.</span></span>

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

### <span data-ttu-id="c08f3-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="c08f3-126">-Skip</span></span>
<span data-ttu-id="c08f3-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="c08f3-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c08f3-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="c08f3-128">-Top</span></span>
<span data-ttu-id="c08f3-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="c08f3-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c08f3-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="c08f3-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c08f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c08f3-131">CommonParameters</span></span>
<span data-ttu-id="c08f3-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c08f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c08f3-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c08f3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c08f3-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c08f3-134">INPUTS</span></span>

## <span data-ttu-id="c08f3-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c08f3-135">OUTPUTS</span></span>

### <span data-ttu-id="c08f3-136">Microsoft. AzureStack. Management. Fabric. admin. models. IpPool</span><span class="sxs-lookup"><span data-stu-id="c08f3-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="c08f3-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c08f3-137">NOTES</span></span>

## <span data-ttu-id="c08f3-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c08f3-138">RELATED LINKS</span></span>

