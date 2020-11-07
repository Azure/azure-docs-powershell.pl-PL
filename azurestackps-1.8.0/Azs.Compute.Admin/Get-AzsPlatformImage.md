---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 403f980af6b00272ca67b3ba180808ba8c82ebce
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889053"
---
# <span data-ttu-id="1dd9c-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="1dd9c-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="1dd9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1dd9c-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd9c-103">Zwraca obrazy maszyny wirtualnej załadowane do repozytorium obrazów platformy.</span><span class="sxs-lookup"><span data-stu-id="1dd9c-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="1dd9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1dd9c-104">SYNTAX</span></span>

### <span data-ttu-id="1dd9c-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="1dd9c-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1dd9c-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="1dd9c-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1dd9c-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="1dd9c-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1dd9c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1dd9c-108">DESCRIPTION</span></span>
<span data-ttu-id="1dd9c-109">Zwraca obrazy platformy.</span><span class="sxs-lookup"><span data-stu-id="1dd9c-109">Returns platform images.</span></span>

## <span data-ttu-id="1dd9c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1dd9c-110">EXAMPLES</span></span>

### <span data-ttu-id="1dd9c-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1dd9c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="1dd9c-112">Zwraca obrazy maszyny wirtualnej załadowane do repozytorium obrazów platformy w lokalizacji lokalnej.</span><span class="sxs-lookup"><span data-stu-id="1dd9c-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="1dd9c-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1dd9c-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="1dd9c-114">Uzyskiwanie określonego obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="1dd9c-114">Get a specific platform image.</span></span>

## <span data-ttu-id="1dd9c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1dd9c-115">PARAMETERS</span></span>

### <span data-ttu-id="1dd9c-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1dd9c-116">-Location</span></span>
<span data-ttu-id="1dd9c-117">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="1dd9c-117">Location of the resource.</span></span>

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

### <span data-ttu-id="1dd9c-118">-Offer</span><span class="sxs-lookup"><span data-stu-id="1dd9c-118">-Offer</span></span>
<span data-ttu-id="1dd9c-119">Imię i nazwisko oferty.</span><span class="sxs-lookup"><span data-stu-id="1dd9c-119">Name of the offer.</span></span>

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

### <span data-ttu-id="1dd9c-120">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="1dd9c-120">-Publisher</span></span>
<span data-ttu-id="1dd9c-121">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="1dd9c-121">Name of the publisher.</span></span>

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

### <span data-ttu-id="1dd9c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dd9c-122">-ResourceId</span></span>
<span data-ttu-id="1dd9c-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="1dd9c-123">The resource id.</span></span>

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

### <span data-ttu-id="1dd9c-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="1dd9c-124">-Sku</span></span>
<span data-ttu-id="1dd9c-125">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="1dd9c-125">Name of the SKU.</span></span>

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

### <span data-ttu-id="1dd9c-126">-Version</span><span class="sxs-lookup"><span data-stu-id="1dd9c-126">-Version</span></span>
<span data-ttu-id="1dd9c-127">Wersja obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="1dd9c-127">The version of the platform image.</span></span>

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

### <span data-ttu-id="1dd9c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd9c-128">CommonParameters</span></span>
<span data-ttu-id="1dd9c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dd9c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd9c-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dd9c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd9c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1dd9c-131">INPUTS</span></span>

## <span data-ttu-id="1dd9c-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1dd9c-132">OUTPUTS</span></span>

### <span data-ttu-id="1dd9c-133">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="1dd9c-133">PlatformImageObject</span></span>

## <span data-ttu-id="1dd9c-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1dd9c-134">NOTES</span></span>

## <span data-ttu-id="1dd9c-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1dd9c-135">RELATED LINKS</span></span>

