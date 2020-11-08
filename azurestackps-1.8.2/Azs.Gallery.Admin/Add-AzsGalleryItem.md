---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0eadd6f0561ca5b44a588397f46d6ad3d7a1c3c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055843"
---
# <span data-ttu-id="2179e-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="2179e-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="2179e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2179e-102">SYNOPSIS</span></span>
<span data-ttu-id="2179e-103">Umożliwia przekazanie elementu galerii dostawców do magazynu.</span><span class="sxs-lookup"><span data-stu-id="2179e-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="2179e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2179e-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2179e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2179e-105">DESCRIPTION</span></span>
<span data-ttu-id="2179e-106">Umożliwia przekazanie elementu galerii dostawców do magazynu.</span><span class="sxs-lookup"><span data-stu-id="2179e-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="2179e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2179e-107">EXAMPLES</span></span>

### <span data-ttu-id="2179e-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="2179e-108">EXAMPLE 1</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="2179e-109">Tworzenie nowego elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="2179e-109">Create a new gallery item.</span></span>

## <span data-ttu-id="2179e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2179e-110">PARAMETERS</span></span>

### <span data-ttu-id="2179e-111">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="2179e-111">-GalleryItemUri</span></span>
<span data-ttu-id="2179e-112">Identyfikator URI pliku JSON elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="2179e-112">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="2179e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2179e-113">-Force</span></span>
<span data-ttu-id="2179e-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2179e-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2179e-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2179e-115">-WhatIf</span></span>
<span data-ttu-id="2179e-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2179e-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2179e-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2179e-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2179e-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2179e-118">-Confirm</span></span>
<span data-ttu-id="2179e-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2179e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2179e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2179e-120">CommonParameters</span></span>
<span data-ttu-id="2179e-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2179e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2179e-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2179e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2179e-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2179e-123">INPUTS</span></span>

## <span data-ttu-id="2179e-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2179e-124">OUTPUTS</span></span>

### <span data-ttu-id="2179e-125">Microsoft. AzureStack. Management. Gallery. admin. models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="2179e-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="2179e-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2179e-126">NOTES</span></span>

## <span data-ttu-id="2179e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2179e-127">RELATED LINKS</span></span>
