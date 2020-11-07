---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 947bb6b453d92897f7901a00ed5a43efa4ac640e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888725"
---
# <span data-ttu-id="141fa-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="141fa-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="141fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="141fa-102">SYNOPSIS</span></span>
<span data-ttu-id="141fa-103">Usuwanie obrazu maszyny wirtualnej z repozytorium obrazów platformy.</span><span class="sxs-lookup"><span data-stu-id="141fa-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="141fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="141fa-104">SYNTAX</span></span>

### <span data-ttu-id="141fa-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="141fa-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="141fa-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="141fa-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="141fa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="141fa-107">DESCRIPTION</span></span>
<span data-ttu-id="141fa-108">Usuwanie obrazu platformy</span><span class="sxs-lookup"><span data-stu-id="141fa-108">Delete a platform image</span></span>

## <span data-ttu-id="141fa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="141fa-109">EXAMPLES</span></span>

### <span data-ttu-id="141fa-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="141fa-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="141fa-111">Usuwanie istniejącego obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="141fa-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="141fa-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="141fa-112">PARAMETERS</span></span>

### <span data-ttu-id="141fa-113">-Force</span><span class="sxs-lookup"><span data-stu-id="141fa-113">-Force</span></span>
<span data-ttu-id="141fa-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="141fa-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141fa-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="141fa-115">-Location</span></span>
<span data-ttu-id="141fa-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="141fa-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141fa-117">-Offer</span><span class="sxs-lookup"><span data-stu-id="141fa-117">-Offer</span></span>
<span data-ttu-id="141fa-118">Imię i nazwisko oferty.</span><span class="sxs-lookup"><span data-stu-id="141fa-118">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141fa-119">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="141fa-119">-Publisher</span></span>
<span data-ttu-id="141fa-120">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="141fa-120">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141fa-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="141fa-121">-ResourceId</span></span>
<span data-ttu-id="141fa-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="141fa-122">The resource id.</span></span>

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

### <span data-ttu-id="141fa-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="141fa-123">-Sku</span></span>
<span data-ttu-id="141fa-124">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="141fa-124">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141fa-125">-Version</span><span class="sxs-lookup"><span data-stu-id="141fa-125">-Version</span></span>
<span data-ttu-id="141fa-126">Wersja obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="141fa-126">The version of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141fa-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="141fa-127">-Confirm</span></span>
<span data-ttu-id="141fa-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="141fa-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141fa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="141fa-129">-WhatIf</span></span>
<span data-ttu-id="141fa-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="141fa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="141fa-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="141fa-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141fa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="141fa-132">CommonParameters</span></span>
<span data-ttu-id="141fa-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="141fa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="141fa-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="141fa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="141fa-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="141fa-135">INPUTS</span></span>

## <span data-ttu-id="141fa-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="141fa-136">OUTPUTS</span></span>

## <span data-ttu-id="141fa-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="141fa-137">NOTES</span></span>

## <span data-ttu-id="141fa-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="141fa-138">RELATED LINKS</span></span>

