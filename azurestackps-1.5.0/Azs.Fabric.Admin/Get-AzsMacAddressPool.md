---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5c686faa457d83ab0ddffb932b20ab5fcd168ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523973"
---
# <span data-ttu-id="60f78-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="60f78-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="60f78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60f78-102">SYNOPSIS</span></span>
<span data-ttu-id="60f78-103">Zwraca listę wszystkich pul adresów MAC w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="60f78-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="60f78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60f78-104">SYNTAX</span></span>

### <span data-ttu-id="60f78-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="60f78-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="60f78-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="60f78-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="60f78-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="60f78-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="60f78-108">Opis</span><span class="sxs-lookup"><span data-stu-id="60f78-108">DESCRIPTION</span></span>
<span data-ttu-id="60f78-109">Zwraca listę wszystkich pul adresów MAC w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="60f78-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="60f78-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60f78-110">EXAMPLES</span></span>

### <span data-ttu-id="60f78-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="60f78-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="60f78-112">Pobierz wszystkie pule adresów MAC w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="60f78-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="60f78-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="60f78-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="60f78-114">Uzyskaj określoną pulę adresów MAC w lokalizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="60f78-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="60f78-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60f78-115">PARAMETERS</span></span>

### <span data-ttu-id="60f78-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="60f78-116">-Filter</span></span>
<span data-ttu-id="60f78-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="60f78-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="60f78-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="60f78-118">-Location</span></span>
<span data-ttu-id="60f78-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="60f78-119">Location of the resource.</span></span>

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

### <span data-ttu-id="60f78-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="60f78-120">-Name</span></span>
<span data-ttu-id="60f78-121">Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="60f78-121">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="60f78-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60f78-122">-ResourceGroupName</span></span>
<span data-ttu-id="60f78-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="60f78-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="60f78-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60f78-124">-ResourceId</span></span>
<span data-ttu-id="60f78-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="60f78-125">The resource id.</span></span>

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

### <span data-ttu-id="60f78-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="60f78-126">-Skip</span></span>
<span data-ttu-id="60f78-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="60f78-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="60f78-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="60f78-128">-Top</span></span>
<span data-ttu-id="60f78-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="60f78-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="60f78-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="60f78-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="60f78-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f78-131">CommonParameters</span></span>
<span data-ttu-id="60f78-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60f78-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f78-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60f78-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f78-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60f78-134">INPUTS</span></span>

## <span data-ttu-id="60f78-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60f78-135">OUTPUTS</span></span>

### <span data-ttu-id="60f78-136">Microsoft. AzureStack. Management. Fabric. admin. models. MacAddressPool</span><span class="sxs-lookup"><span data-stu-id="60f78-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="60f78-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60f78-137">NOTES</span></span>

## <span data-ttu-id="60f78-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60f78-138">RELATED LINKS</span></span>

