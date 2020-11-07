---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fdf0c09e087779e9a08161f2af6f9070f193c31b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888433"
---
# <span data-ttu-id="7d5e9-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="7d5e9-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="7d5e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d5e9-102">SYNOPSIS</span></span>
<span data-ttu-id="7d5e9-103">Zwraca listę wszystkich sieci logicznych w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="7d5e9-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="7d5e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d5e9-104">SYNTAX</span></span>

### <span data-ttu-id="7d5e9-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="7d5e9-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7d5e9-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="7d5e9-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="7d5e9-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="7d5e9-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7d5e9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7d5e9-108">DESCRIPTION</span></span>
<span data-ttu-id="7d5e9-109">Zwraca listę wszystkich sieci logicznych w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="7d5e9-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="7d5e9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d5e9-110">EXAMPLES</span></span>

### <span data-ttu-id="7d5e9-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7d5e9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="7d5e9-112">Pobieranie wszystkich sieci logicznych w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="7d5e9-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="7d5e9-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7d5e9-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="7d5e9-114">Uzyskaj określone sieci logiczne w lokalizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="7d5e9-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="7d5e9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d5e9-115">PARAMETERS</span></span>

### <span data-ttu-id="7d5e9-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="7d5e9-116">-Filter</span></span>
<span data-ttu-id="7d5e9-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="7d5e9-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="7d5e9-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7d5e9-118">-Location</span></span>
<span data-ttu-id="7d5e9-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="7d5e9-119">Location of the resource.</span></span>

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

### <span data-ttu-id="7d5e9-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7d5e9-120">-Name</span></span>
<span data-ttu-id="7d5e9-121">Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="7d5e9-121">Name of the logical network.</span></span>

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

### <span data-ttu-id="7d5e9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d5e9-122">-ResourceGroupName</span></span>
<span data-ttu-id="7d5e9-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="7d5e9-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="7d5e9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d5e9-124">-ResourceId</span></span>
<span data-ttu-id="7d5e9-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="7d5e9-125">The resource id.</span></span>

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

### <span data-ttu-id="7d5e9-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="7d5e9-126">-Skip</span></span>
<span data-ttu-id="7d5e9-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="7d5e9-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7d5e9-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="7d5e9-128">-Top</span></span>
<span data-ttu-id="7d5e9-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="7d5e9-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7d5e9-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="7d5e9-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7d5e9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d5e9-131">CommonParameters</span></span>
<span data-ttu-id="7d5e9-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d5e9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d5e9-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d5e9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d5e9-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d5e9-134">INPUTS</span></span>

## <span data-ttu-id="7d5e9-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d5e9-135">OUTPUTS</span></span>

### <span data-ttu-id="7d5e9-136">Microsoft. AzureStack. Management. Fabric. admin. models. LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="7d5e9-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="7d5e9-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d5e9-137">NOTES</span></span>

## <span data-ttu-id="7d5e9-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d5e9-138">RELATED LINKS</span></span>

