---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db1f78f3adec999cdf8839eb972a71595f6c15b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523377"
---
# <span data-ttu-id="41239-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="41239-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="41239-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41239-102">SYNOPSIS</span></span>
<span data-ttu-id="41239-103">Umożliwia przekazanie elementu galerii dostawców do magazynu.</span><span class="sxs-lookup"><span data-stu-id="41239-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="41239-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41239-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41239-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41239-105">DESCRIPTION</span></span>
<span data-ttu-id="41239-106">Umożliwia przekazanie elementu galerii dostawców do magazynu.</span><span class="sxs-lookup"><span data-stu-id="41239-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="41239-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41239-107">EXAMPLES</span></span>

### <span data-ttu-id="41239-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="41239-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="41239-109">Tworzenie nowego elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="41239-109">Create a new gallery item.</span></span>

## <span data-ttu-id="41239-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41239-110">PARAMETERS</span></span>

### <span data-ttu-id="41239-111">-Force</span><span class="sxs-lookup"><span data-stu-id="41239-111">-Force</span></span>
<span data-ttu-id="41239-112">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="41239-112">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="41239-113">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="41239-113">-GalleryItemUri</span></span>
<span data-ttu-id="41239-114">Identyfikator URI pliku JSON elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="41239-114">The URI to the gallery item JSON file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41239-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41239-115">-Confirm</span></span>
<span data-ttu-id="41239-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41239-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41239-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41239-117">-WhatIf</span></span>
<span data-ttu-id="41239-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41239-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41239-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41239-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41239-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41239-120">CommonParameters</span></span>
<span data-ttu-id="41239-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41239-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41239-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41239-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41239-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41239-123">INPUTS</span></span>

## <span data-ttu-id="41239-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41239-124">OUTPUTS</span></span>

### <span data-ttu-id="41239-125">Microsoft. AzureStack. Management. Gallery. admin. models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="41239-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="41239-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41239-126">NOTES</span></span>

## <span data-ttu-id="41239-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41239-127">RELATED LINKS</span></span>

