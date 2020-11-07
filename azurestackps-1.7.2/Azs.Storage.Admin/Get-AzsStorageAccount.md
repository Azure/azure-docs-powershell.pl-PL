---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: be2198103338a3df56f924e28b497095e21bf1de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888546"
---
# <span data-ttu-id="a835b-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a835b-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="a835b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a835b-102">SYNOPSIS</span></span>
<span data-ttu-id="a835b-103">Zwraca żądane konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="a835b-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="a835b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a835b-104">SYNTAX</span></span>

### <span data-ttu-id="a835b-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a835b-105">List (Default)</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-ResourceGroupName <String>] [-Summary] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a835b-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="a835b-106">Get</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="a835b-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="a835b-107">ResourceId</span></span>
```
Get-AzsStorageAccount [-ResourceId <String>] [<CommonParameters>]
```

## <span data-ttu-id="a835b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a835b-108">DESCRIPTION</span></span>
<span data-ttu-id="a835b-109">Zwraca żądane konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="a835b-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="a835b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a835b-110">EXAMPLES</span></span>

### <span data-ttu-id="a835b-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a835b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Summary
```

<span data-ttu-id="a835b-112">Uzyskaj listę kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="a835b-112">Get a list of storage accounts.</span></span>

### <span data-ttu-id="a835b-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a835b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName 431e8245-9e38-43e9-bf73-5f9cb2fbbdb6 -Name f8f7ff7335cb4ba284fb855547e48f34
```

<span data-ttu-id="a835b-114">Uzyskiwanie szczegółowych informacji dotyczących określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a835b-114">Get details of the specified storage account.</span></span>

## <span data-ttu-id="a835b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a835b-115">PARAMETERS</span></span>

### <span data-ttu-id="a835b-116">-Farmname</span><span class="sxs-lookup"><span data-stu-id="a835b-116">-FarmName</span></span>
<span data-ttu-id="a835b-117">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="a835b-117">Farm Id.</span></span>

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

### <span data-ttu-id="a835b-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a835b-118">-Name</span></span>
<span data-ttu-id="a835b-119">Identyfikator konta magazynu wewnętrznego, który nie jest widoczny dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="a835b-119">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a835b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a835b-120">-ResourceGroupName</span></span>
<span data-ttu-id="a835b-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a835b-121">Resource group name.</span></span>

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

### <span data-ttu-id="a835b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a835b-122">-ResourceId</span></span>
<span data-ttu-id="a835b-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a835b-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a835b-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="a835b-124">-Skip</span></span>
<span data-ttu-id="a835b-125">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="a835b-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a835b-126">— Podsumowanie</span><span class="sxs-lookup"><span data-stu-id="a835b-126">-Summary</span></span>
<span data-ttu-id="a835b-127">Zostanie zwrócony przełącznik dla podsumowania wheter lub szczegółowe informacje.</span><span class="sxs-lookup"><span data-stu-id="a835b-127">Switch for wheter summary or detailed information is returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a835b-128">-Początek</span><span class="sxs-lookup"><span data-stu-id="a835b-128">-Top</span></span>
<span data-ttu-id="a835b-129">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="a835b-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a835b-130">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="a835b-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a835b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a835b-131">CommonParameters</span></span>
<span data-ttu-id="a835b-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a835b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a835b-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a835b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a835b-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a835b-134">INPUTS</span></span>

## <span data-ttu-id="a835b-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a835b-135">OUTPUTS</span></span>

### <span data-ttu-id="a835b-136">Microsoft. AzureStack. Management. Storage. admin. models. StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a835b-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageAccount</span></span>

## <span data-ttu-id="a835b-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a835b-137">NOTES</span></span>

## <span data-ttu-id="a835b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a835b-138">RELATED LINKS</span></span>

