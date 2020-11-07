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
ms.locfileid: "93523301"
---
# <span data-ttu-id="f5ab4-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="f5ab4-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="f5ab4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ab4-103">Zwraca listę przydziałów magazynowania w podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="f5ab4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5ab4-104">SYNTAX</span></span>

### <span data-ttu-id="f5ab4-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f5ab4-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f5ab4-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f5ab4-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="f5ab4-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="f5ab4-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f5ab4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f5ab4-108">DESCRIPTION</span></span>
<span data-ttu-id="f5ab4-109">Zwraca listę przydziałów magazynowania w podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="f5ab4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5ab4-110">EXAMPLES</span></span>

### <span data-ttu-id="f5ab4-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f5ab4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="f5ab4-112">Uzyskaj listę przydziałów magazynowania.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="f5ab4-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f5ab4-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="f5ab4-114">Uzyskaj szczegółowe informacje o określonym przydziale magazynowania według nazwy.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="f5ab4-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5ab4-115">PARAMETERS</span></span>

### <span data-ttu-id="f5ab4-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f5ab4-116">-Location</span></span>
<span data-ttu-id="f5ab4-117">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-117">Resource location.</span></span>

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

### <span data-ttu-id="f5ab4-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f5ab4-118">-Name</span></span>
<span data-ttu-id="f5ab4-119">Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-119">The name of the storage quota.</span></span>

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

### <span data-ttu-id="f5ab4-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5ab4-120">-ResourceId</span></span>
<span data-ttu-id="f5ab4-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-121">The resource id.</span></span>

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

### <span data-ttu-id="f5ab4-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="f5ab4-122">-Skip</span></span>
<span data-ttu-id="f5ab4-123">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f5ab4-124">-Początek</span><span class="sxs-lookup"><span data-stu-id="f5ab4-124">-Top</span></span>
<span data-ttu-id="f5ab4-125">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f5ab4-126">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f5ab4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ab4-127">CommonParameters</span></span>
<span data-ttu-id="f5ab4-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ab4-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5ab4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ab4-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5ab4-130">INPUTS</span></span>

## <span data-ttu-id="f5ab4-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5ab4-131">OUTPUTS</span></span>

### <span data-ttu-id="f5ab4-132">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="f5ab4-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="f5ab4-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5ab4-133">NOTES</span></span>

## <span data-ttu-id="f5ab4-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5ab4-134">RELATED LINKS</span></span>
