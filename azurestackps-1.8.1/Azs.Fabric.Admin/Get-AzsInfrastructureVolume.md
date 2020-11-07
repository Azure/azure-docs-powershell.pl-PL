---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: deaefa8e98e27572fb3faa9443c296e5a15accb0
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889650"
---
# <span data-ttu-id="9f47e-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="9f47e-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="9f47e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9f47e-102">SYNOPSIS</span></span>
<span data-ttu-id="9f47e-103">Zwraca listę wszystkich woluminów magazynu w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9f47e-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="9f47e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9f47e-104">SYNTAX</span></span>

### <span data-ttu-id="9f47e-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="9f47e-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9f47e-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="9f47e-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9f47e-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="9f47e-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9f47e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9f47e-108">DESCRIPTION</span></span>
<span data-ttu-id="9f47e-109">Zwraca listę wszystkich woluminów magazynu w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9f47e-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="9f47e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9f47e-110">EXAMPLES</span></span>

### <span data-ttu-id="9f47e-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="9f47e-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="9f47e-112">Zapoznaj się z listą wszystkich woluminów magazynu w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9f47e-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="9f47e-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="9f47e-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="9f47e-114">Pobierz wolumin magazynu według nazwy w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9f47e-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="9f47e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f47e-115">PARAMETERS</span></span>

### <span data-ttu-id="9f47e-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9f47e-116">-Name</span></span>
<span data-ttu-id="9f47e-117">Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="9f47e-117">Name of the storage volume.</span></span>

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

### <span data-ttu-id="9f47e-118">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="9f47e-118">-StoragePool</span></span>
<span data-ttu-id="9f47e-119">Nazwa puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="9f47e-119">Storage pool name.</span></span>

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

### <span data-ttu-id="9f47e-120">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="9f47e-120">-StorageSystem</span></span>
<span data-ttu-id="9f47e-121">Reprezentacja zasobu systemu magazynowania.</span><span class="sxs-lookup"><span data-stu-id="9f47e-121">Representation of a storage system resource.</span></span>

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

### <span data-ttu-id="9f47e-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9f47e-122">-Location</span></span>
<span data-ttu-id="9f47e-123">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="9f47e-123">Location of the resource.</span></span>

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

### <span data-ttu-id="9f47e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f47e-124">-ResourceGroupName</span></span>
<span data-ttu-id="9f47e-125">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="9f47e-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="9f47e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f47e-126">-ResourceId</span></span>
<span data-ttu-id="9f47e-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="9f47e-127">The resource id.</span></span>

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

### <span data-ttu-id="9f47e-128">-Filter</span><span class="sxs-lookup"><span data-stu-id="9f47e-128">-Filter</span></span>
<span data-ttu-id="9f47e-129">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="9f47e-129">OData filter parameter.</span></span>

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

### <span data-ttu-id="9f47e-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="9f47e-130">-Skip</span></span>
<span data-ttu-id="9f47e-131">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="9f47e-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9f47e-132">-Początek</span><span class="sxs-lookup"><span data-stu-id="9f47e-132">-Top</span></span>
<span data-ttu-id="9f47e-133">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="9f47e-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9f47e-134">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="9f47e-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9f47e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f47e-135">CommonParameters</span></span>
<span data-ttu-id="9f47e-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f47e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f47e-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f47e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f47e-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f47e-138">INPUTS</span></span>

## <span data-ttu-id="9f47e-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9f47e-139">OUTPUTS</span></span>

### <span data-ttu-id="9f47e-140">Microsoft. AzureStack. Management. Fabric. admin. models. Volume</span><span class="sxs-lookup"><span data-stu-id="9f47e-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="9f47e-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9f47e-141">NOTES</span></span>

## <span data-ttu-id="9f47e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f47e-142">RELATED LINKS</span></span>
