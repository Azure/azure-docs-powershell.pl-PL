---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4277ee88af840674d6fc8e4e2d5f614e745ace
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887722"
---
# <span data-ttu-id="03ea1-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="03ea1-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="03ea1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="03ea1-103">Zwraca listę przydziałów magazynowania w podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="03ea1-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="03ea1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03ea1-104">SYNTAX</span></span>

### <span data-ttu-id="03ea1-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="03ea1-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="03ea1-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="03ea1-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="03ea1-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="03ea1-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="03ea1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="03ea1-108">DESCRIPTION</span></span>
<span data-ttu-id="03ea1-109">Zwraca listę przydziałów magazynowania w podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="03ea1-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="03ea1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03ea1-110">EXAMPLES</span></span>

### <span data-ttu-id="03ea1-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="03ea1-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="03ea1-112">Uzyskaj listę przydziałów magazynowania.</span><span class="sxs-lookup"><span data-stu-id="03ea1-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="03ea1-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="03ea1-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="03ea1-114">Uzyskaj szczegółowe informacje o określonym przydziale magazynowania według nazwy.</span><span class="sxs-lookup"><span data-stu-id="03ea1-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="03ea1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03ea1-115">PARAMETERS</span></span>

### <span data-ttu-id="03ea1-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="03ea1-116">-Location</span></span>
<span data-ttu-id="03ea1-117">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="03ea1-117">Resource location.</span></span>

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

### <span data-ttu-id="03ea1-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03ea1-118">-Name</span></span>
<span data-ttu-id="03ea1-119">Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="03ea1-119">The name of the storage quota.</span></span>

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

### <span data-ttu-id="03ea1-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03ea1-120">-ResourceId</span></span>
<span data-ttu-id="03ea1-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="03ea1-121">The resource id.</span></span>

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

### <span data-ttu-id="03ea1-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="03ea1-122">-Skip</span></span>
<span data-ttu-id="03ea1-123">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="03ea1-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="03ea1-124">-Początek</span><span class="sxs-lookup"><span data-stu-id="03ea1-124">-Top</span></span>
<span data-ttu-id="03ea1-125">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="03ea1-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="03ea1-126">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="03ea1-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="03ea1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ea1-127">CommonParameters</span></span>
<span data-ttu-id="03ea1-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03ea1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ea1-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03ea1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ea1-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03ea1-130">INPUTS</span></span>

## <span data-ttu-id="03ea1-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03ea1-131">OUTPUTS</span></span>

### <span data-ttu-id="03ea1-132">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="03ea1-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="03ea1-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03ea1-133">NOTES</span></span>

## <span data-ttu-id="03ea1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03ea1-134">RELATED LINKS</span></span>

