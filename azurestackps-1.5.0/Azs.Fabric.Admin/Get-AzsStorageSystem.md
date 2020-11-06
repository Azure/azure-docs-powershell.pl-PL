---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 362eb6a8d688aab2276fa1166f65474dab488952
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523133"
---
# <span data-ttu-id="d37a7-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="d37a7-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="d37a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d37a7-102">SYNOPSIS</span></span>
<span data-ttu-id="d37a7-103">Zwraca listę wszystkich podsystemów magazynowania dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d37a7-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="d37a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d37a7-104">SYNTAX</span></span>

### <span data-ttu-id="d37a7-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d37a7-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d37a7-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="d37a7-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="d37a7-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="d37a7-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d37a7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d37a7-108">DESCRIPTION</span></span>
<span data-ttu-id="d37a7-109">Zwraca listę wszystkich podsystemów magazynowania dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d37a7-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="d37a7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d37a7-110">EXAMPLES</span></span>

### <span data-ttu-id="d37a7-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d37a7-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="d37a7-112">Pobieranie wszystkich podsystemów magazynowania z lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d37a7-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="d37a7-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d37a7-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="d37a7-114">Uzyskaj podsystem magazynowania pod nazwą lokalizacji i nazwy.</span><span class="sxs-lookup"><span data-stu-id="d37a7-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="d37a7-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d37a7-115">PARAMETERS</span></span>

### <span data-ttu-id="d37a7-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="d37a7-116">-Filter</span></span>
<span data-ttu-id="d37a7-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="d37a7-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="d37a7-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d37a7-118">-Location</span></span>
<span data-ttu-id="d37a7-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="d37a7-119">Location of the resource.</span></span>

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

### <span data-ttu-id="d37a7-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d37a7-120">-Name</span></span>
<span data-ttu-id="d37a7-121">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="d37a7-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d37a7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d37a7-122">-ResourceGroupName</span></span>
<span data-ttu-id="d37a7-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="d37a7-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d37a7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d37a7-124">-ResourceId</span></span>
<span data-ttu-id="d37a7-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d37a7-125">The resource id.</span></span>

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

### <span data-ttu-id="d37a7-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="d37a7-126">-Skip</span></span>
<span data-ttu-id="d37a7-127">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="d37a7-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d37a7-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="d37a7-128">-Top</span></span>
<span data-ttu-id="d37a7-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="d37a7-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d37a7-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="d37a7-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d37a7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37a7-131">CommonParameters</span></span>
<span data-ttu-id="d37a7-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d37a7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37a7-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d37a7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37a7-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d37a7-134">INPUTS</span></span>

## <span data-ttu-id="d37a7-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d37a7-135">OUTPUTS</span></span>

### <span data-ttu-id="d37a7-136">Microsoft. AzureStack. Management. Fabric. admin. models. StorageSystem</span><span class="sxs-lookup"><span data-stu-id="d37a7-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="d37a7-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d37a7-137">NOTES</span></span>

## <span data-ttu-id="d37a7-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d37a7-138">RELATED LINKS</span></span>

