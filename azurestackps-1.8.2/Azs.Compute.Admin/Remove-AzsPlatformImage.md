---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28d807ebcd1ae61844b0316492b3d9d10437f1d3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055749"
---
# <span data-ttu-id="0cedd-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="0cedd-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="0cedd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0cedd-102">SYNOPSIS</span></span>
<span data-ttu-id="0cedd-103">Usuwanie obrazu maszyny wirtualnej z repozytorium obrazów platformy.</span><span class="sxs-lookup"><span data-stu-id="0cedd-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="0cedd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0cedd-104">SYNTAX</span></span>

### <span data-ttu-id="0cedd-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="0cedd-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cedd-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="0cedd-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cedd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0cedd-107">DESCRIPTION</span></span>
<span data-ttu-id="0cedd-108">Usuwanie obrazu platformy</span><span class="sxs-lookup"><span data-stu-id="0cedd-108">Delete a platform image</span></span>

## <span data-ttu-id="0cedd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0cedd-109">EXAMPLES</span></span>

### <span data-ttu-id="0cedd-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0cedd-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="0cedd-111">Usuwanie istniejącego obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="0cedd-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="0cedd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0cedd-112">PARAMETERS</span></span>

### <span data-ttu-id="0cedd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0cedd-113">-Force</span></span>
<span data-ttu-id="0cedd-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0cedd-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0cedd-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0cedd-115">-Location</span></span>
<span data-ttu-id="0cedd-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="0cedd-116">Location of the resource.</span></span>

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

### <span data-ttu-id="0cedd-117">-Offer</span><span class="sxs-lookup"><span data-stu-id="0cedd-117">-Offer</span></span>
<span data-ttu-id="0cedd-118">Imię i nazwisko oferty.</span><span class="sxs-lookup"><span data-stu-id="0cedd-118">Name of the offer.</span></span>

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

### <span data-ttu-id="0cedd-119">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="0cedd-119">-Publisher</span></span>
<span data-ttu-id="0cedd-120">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="0cedd-120">Name of the publisher.</span></span>

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

### <span data-ttu-id="0cedd-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cedd-121">-ResourceId</span></span>
<span data-ttu-id="0cedd-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="0cedd-122">The resource id.</span></span>

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

### <span data-ttu-id="0cedd-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="0cedd-123">-Sku</span></span>
<span data-ttu-id="0cedd-124">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="0cedd-124">Name of the SKU.</span></span>

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

### <span data-ttu-id="0cedd-125">-Version</span><span class="sxs-lookup"><span data-stu-id="0cedd-125">-Version</span></span>
<span data-ttu-id="0cedd-126">Wersja obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0cedd-126">The version of the virtual machine image.</span></span>

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

### <span data-ttu-id="0cedd-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0cedd-127">-Confirm</span></span>
<span data-ttu-id="0cedd-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cedd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cedd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cedd-129">-WhatIf</span></span>
<span data-ttu-id="0cedd-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cedd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cedd-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0cedd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cedd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cedd-132">CommonParameters</span></span>
<span data-ttu-id="0cedd-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cedd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cedd-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cedd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cedd-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cedd-135">INPUTS</span></span>

## <span data-ttu-id="0cedd-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0cedd-136">OUTPUTS</span></span>

## <span data-ttu-id="0cedd-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0cedd-137">NOTES</span></span>

## <span data-ttu-id="0cedd-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0cedd-138">RELATED LINKS</span></span>

