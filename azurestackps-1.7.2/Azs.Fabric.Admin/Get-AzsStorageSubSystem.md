---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2abc9073b9e7bcbcd4644150ada4c19cd351f660
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887925"
---
# <span data-ttu-id="c27af-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="c27af-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="c27af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c27af-102">SYNOPSIS</span></span>
<span data-ttu-id="c27af-103">Zwraca listę wszystkich podsystemów magazynowania dla jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c27af-103">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="c27af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c27af-104">SYNTAX</span></span>

### <span data-ttu-id="c27af-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c27af-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c27af-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c27af-106">Get</span></span>
```
Get-AzsStorageSubSystem [-Name] <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c27af-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="c27af-107">ResourceId</span></span>
```
Get-AzsStorageSubSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c27af-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c27af-108">DESCRIPTION</span></span>
<span data-ttu-id="c27af-109">Zwraca listę wszystkich podsystemów magazynowania dla jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c27af-109">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="c27af-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c27af-110">EXAMPLES</span></span>

### <span data-ttu-id="c27af-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c27af-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster
```

<span data-ttu-id="c27af-112">Pobierz wszystkie Podsystemy magazynowania z jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c27af-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="c27af-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c27af-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster -Name S-Cluster.azurestack.local
```

<span data-ttu-id="c27af-114">Uzyskaj Podsystem pamięci masowej pod nazwą jednostki skali i nazwy.</span><span class="sxs-lookup"><span data-stu-id="c27af-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="c27af-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c27af-115">PARAMETERS</span></span>

### <span data-ttu-id="c27af-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="c27af-116">-Filter</span></span>
<span data-ttu-id="c27af-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="c27af-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="c27af-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c27af-118">-Location</span></span>
<span data-ttu-id="c27af-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="c27af-119">Location of the resource.</span></span>

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

### <span data-ttu-id="c27af-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c27af-120">-Name</span></span>
<span data-ttu-id="c27af-121">Nazwa podsystemu magazynowania.</span><span class="sxs-lookup"><span data-stu-id="c27af-121">Name of the storage subsystem.</span></span>

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

### <span data-ttu-id="c27af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c27af-122">-ResourceGroupName</span></span>
<span data-ttu-id="c27af-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="c27af-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c27af-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c27af-124">-ResourceId</span></span>
<span data-ttu-id="c27af-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="c27af-125">The resource id.</span></span>

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

### <span data-ttu-id="c27af-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c27af-126">-ScaleUnit</span></span>
<span data-ttu-id="c27af-127">Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c27af-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="c27af-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="c27af-128">-Top</span></span>
<span data-ttu-id="c27af-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="c27af-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c27af-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="c27af-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c27af-131">-Skip</span><span class="sxs-lookup"><span data-stu-id="c27af-131">-Skip</span></span>
<span data-ttu-id="c27af-132">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="c27af-132">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c27af-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c27af-133">CommonParameters</span></span>
<span data-ttu-id="c27af-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c27af-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c27af-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c27af-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c27af-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c27af-136">INPUTS</span></span>

## <span data-ttu-id="c27af-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c27af-137">OUTPUTS</span></span>

### <span data-ttu-id="c27af-138">Microsoft. AzureStack. Management. Fabric. admin. models. StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="c27af-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSubSystem</span></span>
## <span data-ttu-id="c27af-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c27af-139">NOTES</span></span>

## <span data-ttu-id="c27af-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c27af-140">RELATED LINKS</span></span>
