---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67835cc0ae5191f50aefb79f76148752c68508bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887922"
---
# <span data-ttu-id="a7396-101">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="a7396-101">Get-AzsVolume</span></span>

## <span data-ttu-id="a7396-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7396-102">SYNOPSIS</span></span>
<span data-ttu-id="a7396-103">Zwraca listę wszystkich woluminów magazynu w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a7396-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="a7396-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7396-104">SYNTAX</span></span>

### <span data-ttu-id="a7396-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a7396-105">List (Default)</span></span>
```
Get-AzsVolume -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a7396-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="a7396-106">Get</span></span>
```
Get-AzsVolume -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="a7396-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="a7396-107">ResourceId</span></span>
```
Get-AzsVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a7396-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a7396-108">DESCRIPTION</span></span>
<span data-ttu-id="a7396-109">Zwraca listę wszystkich woluminów magazynu w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a7396-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="a7396-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7396-110">EXAMPLES</span></span>

### <span data-ttu-id="a7396-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7396-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="a7396-112">Zapoznaj się z listą wszystkich woluminów magazynu w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a7396-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="a7396-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7396-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="a7396-114">Pobierz wolumin magazynu według nazwy w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a7396-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="a7396-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7396-115">PARAMETERS</span></span>

### <span data-ttu-id="a7396-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="a7396-116">-Filter</span></span>
<span data-ttu-id="a7396-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="a7396-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="a7396-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a7396-118">-Location</span></span>
<span data-ttu-id="a7396-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="a7396-119">Location of the resource.</span></span>

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

### <span data-ttu-id="a7396-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a7396-120">-Name</span></span>
<span data-ttu-id="a7396-121">Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="a7396-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="a7396-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7396-122">-ResourceGroupName</span></span>
<span data-ttu-id="a7396-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="a7396-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a7396-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7396-124">-ResourceId</span></span>
<span data-ttu-id="a7396-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a7396-125">The resource id.</span></span>

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

### <span data-ttu-id="a7396-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="a7396-126">-ScaleUnit</span></span>
<span data-ttu-id="a7396-127">Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="a7396-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="a7396-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="a7396-128">-StorageSubSystem</span></span>
<span data-ttu-id="a7396-129">Podsystem magazynowania, w którym znajduje się wolumin.</span><span class="sxs-lookup"><span data-stu-id="a7396-129">Storage subsystem in which the volume is located.</span></span>

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

### <span data-ttu-id="a7396-130">-Początek</span><span class="sxs-lookup"><span data-stu-id="a7396-130">-Top</span></span>
<span data-ttu-id="a7396-131">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="a7396-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a7396-132">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="a7396-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a7396-133">-Skip</span><span class="sxs-lookup"><span data-stu-id="a7396-133">-Skip</span></span>
<span data-ttu-id="a7396-134">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="a7396-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a7396-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7396-135">CommonParameters</span></span>
<span data-ttu-id="a7396-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7396-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7396-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7396-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7396-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7396-138">INPUTS</span></span>

## <span data-ttu-id="a7396-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7396-139">OUTPUTS</span></span>

### <span data-ttu-id="a7396-140">Microsoft. AzureStack. Management. Fabric. admin. models. Volume</span><span class="sxs-lookup"><span data-stu-id="a7396-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>
## <span data-ttu-id="a7396-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7396-141">NOTES</span></span>

## <span data-ttu-id="a7396-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7396-142">RELATED LINKS</span></span>
