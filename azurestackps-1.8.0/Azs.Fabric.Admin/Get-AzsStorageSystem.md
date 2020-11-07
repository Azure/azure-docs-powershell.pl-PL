---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3760ecd9c0bc9fd62e49ee8163dfe24ae190985e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888933"
---
# <span data-ttu-id="b4037-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="b4037-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="b4037-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4037-102">SYNOPSIS</span></span>
<span data-ttu-id="b4037-103">Zwraca listę wszystkich podsystemów magazynowania dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b4037-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="b4037-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4037-104">SYNTAX</span></span>

### <span data-ttu-id="b4037-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b4037-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b4037-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="b4037-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4037-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="b4037-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b4037-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b4037-108">DESCRIPTION</span></span>
<span data-ttu-id="b4037-109">Zwraca listę wszystkich podsystemów magazynowania dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b4037-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="b4037-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4037-110">EXAMPLES</span></span>

### <span data-ttu-id="b4037-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="b4037-111">EXAMPLE 1</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="b4037-112">Pobieranie wszystkich podsystemów magazynowania z lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b4037-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="b4037-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="b4037-113">EXAMPLE 2</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="b4037-114">Uzyskaj podsystem magazynowania pod nazwą lokalizacji i nazwy.</span><span class="sxs-lookup"><span data-stu-id="b4037-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="b4037-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4037-115">PARAMETERS</span></span>

### <span data-ttu-id="b4037-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b4037-116">-Name</span></span>
<span data-ttu-id="b4037-117">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="b4037-117">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b4037-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b4037-118">-Location</span></span>
<span data-ttu-id="b4037-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="b4037-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b4037-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4037-120">-ResourceGroupName</span></span>
<span data-ttu-id="b4037-121">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="b4037-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b4037-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4037-122">-ResourceId</span></span>
<span data-ttu-id="b4037-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="b4037-123">The resource id.</span></span>

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

### <span data-ttu-id="b4037-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="b4037-124">-Filter</span></span>
<span data-ttu-id="b4037-125">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="b4037-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="b4037-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="b4037-126">-Skip</span></span>
<span data-ttu-id="b4037-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="b4037-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b4037-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="b4037-128">-Top</span></span>
<span data-ttu-id="b4037-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="b4037-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b4037-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="b4037-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b4037-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4037-131">CommonParameters</span></span>
<span data-ttu-id="b4037-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4037-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4037-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4037-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4037-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4037-134">INPUTS</span></span>

## <span data-ttu-id="b4037-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4037-135">OUTPUTS</span></span>

### <span data-ttu-id="b4037-136">Microsoft. AzureStack. Management. Fabric. admin. models. StorageSystem</span><span class="sxs-lookup"><span data-stu-id="b4037-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="b4037-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4037-137">NOTES</span></span>

## <span data-ttu-id="b4037-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4037-138">RELATED LINKS</span></span>
