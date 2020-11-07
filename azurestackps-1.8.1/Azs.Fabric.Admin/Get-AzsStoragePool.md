---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcc4dbfdd4634c53835c588947a77c4c2e773af4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889618"
---
# <span data-ttu-id="abd8c-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="abd8c-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="abd8c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="abd8c-102">SYNOPSIS</span></span>
<span data-ttu-id="abd8c-103">Zwraca listę wszystkich pul magazynu dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="abd8c-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="abd8c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="abd8c-104">SYNTAX</span></span>

### <span data-ttu-id="abd8c-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="abd8c-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="abd8c-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="abd8c-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="abd8c-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="abd8c-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="abd8c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="abd8c-108">DESCRIPTION</span></span>
<span data-ttu-id="abd8c-109">Zwraca listę wszystkich pul magazynu dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="abd8c-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="abd8c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="abd8c-110">EXAMPLES</span></span>

### <span data-ttu-id="abd8c-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="abd8c-111">EXAMPLE 1</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="abd8c-112">Pobierz wszystkie pule magazynów w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="abd8c-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="abd8c-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="abd8c-113">EXAMPLE 2</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="abd8c-114">Uzyskaj Pule magazynów w określonej lokalizacji, używając nazwy puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="abd8c-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="abd8c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="abd8c-115">PARAMETERS</span></span>

### <span data-ttu-id="abd8c-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="abd8c-116">-Name</span></span>
<span data-ttu-id="abd8c-117">Nazwa puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="abd8c-117">Storage pool name.</span></span>

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

### <span data-ttu-id="abd8c-118">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="abd8c-118">-StorageSystem</span></span>
<span data-ttu-id="abd8c-119">Nazwa podsystemu magazynowania.</span><span class="sxs-lookup"><span data-stu-id="abd8c-119">Name of the Storage Sub System.</span></span>

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

### <span data-ttu-id="abd8c-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="abd8c-120">-Location</span></span>
<span data-ttu-id="abd8c-121">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="abd8c-121">Location of the resource.</span></span>

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

### <span data-ttu-id="abd8c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abd8c-122">-ResourceGroupName</span></span>
<span data-ttu-id="abd8c-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="abd8c-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="abd8c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abd8c-124">-ResourceId</span></span>
<span data-ttu-id="abd8c-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="abd8c-125">The resource id.</span></span>

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

### <span data-ttu-id="abd8c-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="abd8c-126">-Filter</span></span>
<span data-ttu-id="abd8c-127">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="abd8c-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="abd8c-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="abd8c-128">-Skip</span></span>
<span data-ttu-id="abd8c-129">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="abd8c-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="abd8c-130">-Początek</span><span class="sxs-lookup"><span data-stu-id="abd8c-130">-Top</span></span>
<span data-ttu-id="abd8c-131">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="abd8c-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="abd8c-132">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="abd8c-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="abd8c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd8c-133">CommonParameters</span></span>
<span data-ttu-id="abd8c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abd8c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd8c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abd8c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd8c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abd8c-136">INPUTS</span></span>

## <span data-ttu-id="abd8c-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="abd8c-137">OUTPUTS</span></span>

### <span data-ttu-id="abd8c-138">Microsoft. AzureStack. Management. Fabric. admin. models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="abd8c-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="abd8c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="abd8c-139">NOTES</span></span>

## <span data-ttu-id="abd8c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="abd8c-140">RELATED LINKS</span></span>
