---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 403f980af6b00272ca67b3ba180808ba8c82ebce
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061592"
---
# <span data-ttu-id="90755-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="90755-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="90755-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90755-102">SYNOPSIS</span></span>
<span data-ttu-id="90755-103">Zwraca obrazy maszyny wirtualnej załadowane do repozytorium obrazów platformy.</span><span class="sxs-lookup"><span data-stu-id="90755-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="90755-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90755-104">SYNTAX</span></span>

### <span data-ttu-id="90755-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="90755-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="90755-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="90755-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="90755-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="90755-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="90755-108">Opis</span><span class="sxs-lookup"><span data-stu-id="90755-108">DESCRIPTION</span></span>
<span data-ttu-id="90755-109">Zwraca obrazy platformy.</span><span class="sxs-lookup"><span data-stu-id="90755-109">Returns platform images.</span></span>

## <span data-ttu-id="90755-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90755-110">EXAMPLES</span></span>

### <span data-ttu-id="90755-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="90755-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="90755-112">Zwraca obrazy maszyny wirtualnej załadowane do repozytorium obrazów platformy w lokalizacji lokalnej.</span><span class="sxs-lookup"><span data-stu-id="90755-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="90755-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="90755-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="90755-114">Uzyskiwanie określonego obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="90755-114">Get a specific platform image.</span></span>

## <span data-ttu-id="90755-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90755-115">PARAMETERS</span></span>

### <span data-ttu-id="90755-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="90755-116">-Location</span></span>
<span data-ttu-id="90755-117">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="90755-117">Location of the resource.</span></span>

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

### <span data-ttu-id="90755-118">-Offer</span><span class="sxs-lookup"><span data-stu-id="90755-118">-Offer</span></span>
<span data-ttu-id="90755-119">Imię i nazwisko oferty.</span><span class="sxs-lookup"><span data-stu-id="90755-119">Name of the offer.</span></span>

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

### <span data-ttu-id="90755-120">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="90755-120">-Publisher</span></span>
<span data-ttu-id="90755-121">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="90755-121">Name of the publisher.</span></span>

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

### <span data-ttu-id="90755-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90755-122">-ResourceId</span></span>
<span data-ttu-id="90755-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="90755-123">The resource id.</span></span>

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

### <span data-ttu-id="90755-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="90755-124">-Sku</span></span>
<span data-ttu-id="90755-125">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="90755-125">Name of the SKU.</span></span>

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

### <span data-ttu-id="90755-126">-Version</span><span class="sxs-lookup"><span data-stu-id="90755-126">-Version</span></span>
<span data-ttu-id="90755-127">Wersja obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="90755-127">The version of the platform image.</span></span>

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

### <span data-ttu-id="90755-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90755-128">CommonParameters</span></span>
<span data-ttu-id="90755-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90755-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90755-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90755-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90755-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90755-131">INPUTS</span></span>

## <span data-ttu-id="90755-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90755-132">OUTPUTS</span></span>

### <span data-ttu-id="90755-133">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="90755-133">PlatformImageObject</span></span>

## <span data-ttu-id="90755-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90755-134">NOTES</span></span>

## <span data-ttu-id="90755-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90755-135">RELATED LINKS</span></span>

