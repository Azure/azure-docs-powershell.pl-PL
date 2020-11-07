---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: deaefa8e98e27572fb3faa9443c296e5a15accb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888974"
---
# <span data-ttu-id="dcddb-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="dcddb-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="dcddb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dcddb-102">SYNOPSIS</span></span>
<span data-ttu-id="dcddb-103">Zwraca listę wszystkich woluminów magazynu w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="dcddb-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="dcddb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dcddb-104">SYNTAX</span></span>

### <span data-ttu-id="dcddb-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="dcddb-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="dcddb-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="dcddb-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="dcddb-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="dcddb-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="dcddb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dcddb-108">DESCRIPTION</span></span>
<span data-ttu-id="dcddb-109">Zwraca listę wszystkich woluminów magazynu w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="dcddb-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="dcddb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dcddb-110">EXAMPLES</span></span>

### <span data-ttu-id="dcddb-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="dcddb-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="dcddb-112">Zapoznaj się z listą wszystkich woluminów magazynu w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="dcddb-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="dcddb-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="dcddb-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="dcddb-114">Pobierz wolumin magazynu według nazwy w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="dcddb-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="dcddb-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dcddb-115">PARAMETERS</span></span>

### <span data-ttu-id="dcddb-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dcddb-116">-Name</span></span>
<span data-ttu-id="dcddb-117">Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="dcddb-117">Name of the storage volume.</span></span>

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

### <span data-ttu-id="dcddb-118">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="dcddb-118">-StoragePool</span></span>
<span data-ttu-id="dcddb-119">Nazwa puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="dcddb-119">Storage pool name.</span></span>

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

### <span data-ttu-id="dcddb-120">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="dcddb-120">-StorageSystem</span></span>
<span data-ttu-id="dcddb-121">Reprezentacja zasobu systemu magazynowania.</span><span class="sxs-lookup"><span data-stu-id="dcddb-121">Representation of a storage system resource.</span></span>

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

### <span data-ttu-id="dcddb-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dcddb-122">-Location</span></span>
<span data-ttu-id="dcddb-123">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="dcddb-123">Location of the resource.</span></span>

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

### <span data-ttu-id="dcddb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcddb-124">-ResourceGroupName</span></span>
<span data-ttu-id="dcddb-125">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="dcddb-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="dcddb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcddb-126">-ResourceId</span></span>
<span data-ttu-id="dcddb-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="dcddb-127">The resource id.</span></span>

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

### <span data-ttu-id="dcddb-128">-Filter</span><span class="sxs-lookup"><span data-stu-id="dcddb-128">-Filter</span></span>
<span data-ttu-id="dcddb-129">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="dcddb-129">OData filter parameter.</span></span>

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

### <span data-ttu-id="dcddb-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="dcddb-130">-Skip</span></span>
<span data-ttu-id="dcddb-131">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="dcddb-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="dcddb-132">-Początek</span><span class="sxs-lookup"><span data-stu-id="dcddb-132">-Top</span></span>
<span data-ttu-id="dcddb-133">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="dcddb-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="dcddb-134">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="dcddb-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="dcddb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcddb-135">CommonParameters</span></span>
<span data-ttu-id="dcddb-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcddb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcddb-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcddb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcddb-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcddb-138">INPUTS</span></span>

## <span data-ttu-id="dcddb-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dcddb-139">OUTPUTS</span></span>

### <span data-ttu-id="dcddb-140">Microsoft. AzureStack. Management. Fabric. admin. models. Volume</span><span class="sxs-lookup"><span data-stu-id="dcddb-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="dcddb-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dcddb-141">NOTES</span></span>

## <span data-ttu-id="dcddb-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcddb-142">RELATED LINKS</span></span>
