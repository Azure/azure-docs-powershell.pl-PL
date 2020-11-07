---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cab0b994648a414aa164b746a02e3fe1fb848e9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888341"
---
# <span data-ttu-id="56d9d-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="56d9d-101">Get-AzsDrive</span></span>

## <span data-ttu-id="56d9d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="56d9d-103">Zwraca listę wszystkich dysków magazynu dla określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="56d9d-103">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="56d9d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56d9d-104">SYNTAX</span></span>

### <span data-ttu-id="56d9d-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="56d9d-105">List (Default)</span></span>
```
Get-AzsDrive -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="56d9d-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="56d9d-106">Get</span></span>
```
Get-AzsDrive -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="56d9d-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="56d9d-107">ResourceId</span></span>
```
Get-AzsDrive -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="56d9d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="56d9d-108">DESCRIPTION</span></span>
<span data-ttu-id="56d9d-109">Zwraca listę wszystkich dysków magazynu dla określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="56d9d-109">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="56d9d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56d9d-110">EXAMPLES</span></span>

### <span data-ttu-id="56d9d-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="56d9d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="56d9d-112">Uzyskaj listę wszystkich dysków magazynu dla określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="56d9d-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="56d9d-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="56d9d-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a654528c-60bb-18e1-457c-51b7cdb7e14a
```

<span data-ttu-id="56d9d-114">Uzyskaj dysk magazynujący według nazwy dla określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="56d9d-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="56d9d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56d9d-115">PARAMETERS</span></span>

### <span data-ttu-id="56d9d-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="56d9d-116">-Filter</span></span>
<span data-ttu-id="56d9d-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="56d9d-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="56d9d-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="56d9d-118">-Location</span></span>
<span data-ttu-id="56d9d-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="56d9d-119">Location of the resource.</span></span>

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

### <span data-ttu-id="56d9d-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56d9d-120">-Name</span></span>
<span data-ttu-id="56d9d-121">Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="56d9d-121">Name of the storage drive.</span></span>

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

### <span data-ttu-id="56d9d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56d9d-122">-ResourceGroupName</span></span>
<span data-ttu-id="56d9d-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="56d9d-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="56d9d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56d9d-124">-ResourceId</span></span>
<span data-ttu-id="56d9d-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="56d9d-125">The resource id.</span></span>

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

### <span data-ttu-id="56d9d-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="56d9d-126">-ScaleUnit</span></span>
<span data-ttu-id="56d9d-127">Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="56d9d-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="56d9d-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="56d9d-128">-StorageSubSystem</span></span>
<span data-ttu-id="56d9d-129">Podsystem magazynowania, w którym znajduje się dysk.</span><span class="sxs-lookup"><span data-stu-id="56d9d-129">Storage subsystem in which the drive is located.</span></span>

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

### <span data-ttu-id="56d9d-130">-Początek</span><span class="sxs-lookup"><span data-stu-id="56d9d-130">-Top</span></span>
<span data-ttu-id="56d9d-131">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="56d9d-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="56d9d-132">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="56d9d-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="56d9d-133">-Skip</span><span class="sxs-lookup"><span data-stu-id="56d9d-133">-Skip</span></span>
<span data-ttu-id="56d9d-134">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="56d9d-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="56d9d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d9d-135">CommonParameters</span></span>
<span data-ttu-id="56d9d-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d9d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d9d-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56d9d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d9d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56d9d-138">INPUTS</span></span>

## <span data-ttu-id="56d9d-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56d9d-139">OUTPUTS</span></span>

### <span data-ttu-id="56d9d-140">Microsoft. AzureStack. Management. Fabric. admin. models. Drive</span><span class="sxs-lookup"><span data-stu-id="56d9d-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Drive</span></span>
## <span data-ttu-id="56d9d-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56d9d-141">NOTES</span></span>

## <span data-ttu-id="56d9d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56d9d-142">RELATED LINKS</span></span>
