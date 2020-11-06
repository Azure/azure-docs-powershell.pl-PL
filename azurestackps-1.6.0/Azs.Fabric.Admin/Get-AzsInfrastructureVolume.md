---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdb6542f9e7bfd594130374d5d72fed8b26596e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523781"
---
# <span data-ttu-id="03eb9-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="03eb9-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="03eb9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="03eb9-103">Zwraca listę wszystkich woluminów magazynu w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="03eb9-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="03eb9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03eb9-104">SYNTAX</span></span>

### <span data-ttu-id="03eb9-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="03eb9-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="03eb9-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="03eb9-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="03eb9-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="03eb9-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="03eb9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="03eb9-108">DESCRIPTION</span></span>
<span data-ttu-id="03eb9-109">Zwraca listę wszystkich woluminów magazynu w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="03eb9-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="03eb9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03eb9-110">EXAMPLES</span></span>

### <span data-ttu-id="03eb9-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="03eb9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="03eb9-112">Zapoznaj się z listą wszystkich woluminów magazynu w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="03eb9-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="03eb9-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="03eb9-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="03eb9-114">Pobierz wolumin magazynu według nazwy w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="03eb9-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="03eb9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03eb9-115">PARAMETERS</span></span>

### <span data-ttu-id="03eb9-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="03eb9-116">-Filter</span></span>
<span data-ttu-id="03eb9-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="03eb9-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="03eb9-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="03eb9-118">-Location</span></span>
<span data-ttu-id="03eb9-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="03eb9-119">Location of the resource.</span></span>

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

### <span data-ttu-id="03eb9-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03eb9-120">-Name</span></span>
<span data-ttu-id="03eb9-121">Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="03eb9-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="03eb9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03eb9-122">-ResourceGroupName</span></span>
<span data-ttu-id="03eb9-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="03eb9-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="03eb9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03eb9-124">-ResourceId</span></span>
<span data-ttu-id="03eb9-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="03eb9-125">The resource id.</span></span>

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

### <span data-ttu-id="03eb9-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="03eb9-126">-Skip</span></span>
<span data-ttu-id="03eb9-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="03eb9-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="03eb9-128">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="03eb9-128">-StoragePool</span></span>
<span data-ttu-id="03eb9-129">Nazwa puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="03eb9-129">Storage pool name.</span></span>

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

### <span data-ttu-id="03eb9-130">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="03eb9-130">-StorageSystem</span></span>
<span data-ttu-id="03eb9-131">System magazynowania, w którym znajduje się wolumin infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="03eb9-131">Storage system in which the infrastructure volume is located.</span></span>

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

### <span data-ttu-id="03eb9-132">-Początek</span><span class="sxs-lookup"><span data-stu-id="03eb9-132">-Top</span></span>
<span data-ttu-id="03eb9-133">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="03eb9-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="03eb9-134">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="03eb9-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="03eb9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03eb9-135">CommonParameters</span></span>
<span data-ttu-id="03eb9-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03eb9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03eb9-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03eb9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03eb9-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03eb9-138">INPUTS</span></span>

## <span data-ttu-id="03eb9-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03eb9-139">OUTPUTS</span></span>

### <span data-ttu-id="03eb9-140">Microsoft. AzureStack. Management. Fabric. admin. models. Volume</span><span class="sxs-lookup"><span data-stu-id="03eb9-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="03eb9-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03eb9-141">NOTES</span></span>

## <span data-ttu-id="03eb9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03eb9-142">RELATED LINKS</span></span>

