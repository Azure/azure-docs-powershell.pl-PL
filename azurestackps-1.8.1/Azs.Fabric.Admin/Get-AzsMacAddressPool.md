---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e22024b1b246a60104db0832860ed0aff699ff5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889641"
---
# <span data-ttu-id="c9ce9-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="c9ce9-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="c9ce9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ce9-103">Zwraca listę wszystkich pul adresów MAC w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c9ce9-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="c9ce9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9ce9-104">SYNTAX</span></span>

### <span data-ttu-id="c9ce9-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c9ce9-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c9ce9-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c9ce9-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c9ce9-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="c9ce9-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c9ce9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c9ce9-108">DESCRIPTION</span></span>
<span data-ttu-id="c9ce9-109">Zwraca listę wszystkich pul adresów MAC w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c9ce9-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="c9ce9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9ce9-110">EXAMPLES</span></span>

### <span data-ttu-id="c9ce9-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="c9ce9-111">EXAMPLE 1</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="c9ce9-112">Pobierz wszystkie pule adresów MAC w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c9ce9-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="c9ce9-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="c9ce9-113">EXAMPLE 2</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="c9ce9-114">Uzyskaj określoną pulę adresów MAC w lokalizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="c9ce9-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="c9ce9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9ce9-115">PARAMETERS</span></span>

### <span data-ttu-id="c9ce9-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c9ce9-116">-Name</span></span>
<span data-ttu-id="c9ce9-117">Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="c9ce9-117">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="c9ce9-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c9ce9-118">-Location</span></span>
<span data-ttu-id="c9ce9-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="c9ce9-119">Location of the resource.</span></span>

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

### <span data-ttu-id="c9ce9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9ce9-120">-ResourceGroupName</span></span>
<span data-ttu-id="c9ce9-121">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="c9ce9-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c9ce9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9ce9-122">-ResourceId</span></span>
<span data-ttu-id="c9ce9-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="c9ce9-123">The resource id.</span></span>

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

### <span data-ttu-id="c9ce9-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="c9ce9-124">-Filter</span></span>
<span data-ttu-id="c9ce9-125">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="c9ce9-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="c9ce9-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="c9ce9-126">-Skip</span></span>
<span data-ttu-id="c9ce9-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="c9ce9-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c9ce9-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="c9ce9-128">-Top</span></span>
<span data-ttu-id="c9ce9-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="c9ce9-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c9ce9-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="c9ce9-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c9ce9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ce9-131">CommonParameters</span></span>
<span data-ttu-id="c9ce9-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9ce9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ce9-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9ce9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ce9-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9ce9-134">INPUTS</span></span>

## <span data-ttu-id="c9ce9-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9ce9-135">OUTPUTS</span></span>

### <span data-ttu-id="c9ce9-136">Microsoft. AzureStack. Management. Fabric. admin. models. MacAddressPool</span><span class="sxs-lookup"><span data-stu-id="c9ce9-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="c9ce9-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9ce9-137">NOTES</span></span>

## <span data-ttu-id="c9ce9-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9ce9-138">RELATED LINKS</span></span>
