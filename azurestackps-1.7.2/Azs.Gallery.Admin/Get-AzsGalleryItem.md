---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2020caba1d7cac4ed1830fbc1b6a3ccdb4c71f27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888614"
---
# <span data-ttu-id="0af80-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="0af80-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="0af80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0af80-102">SYNOPSIS</span></span>
<span data-ttu-id="0af80-103">Wyświetla elementy galerii.</span><span class="sxs-lookup"><span data-stu-id="0af80-103">Lists gallery items.</span></span>

## <span data-ttu-id="0af80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0af80-104">SYNTAX</span></span>

### <span data-ttu-id="0af80-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="0af80-105">List (Default)</span></span>
```
Get-AzsGalleryItem [<CommonParameters>]
```

### <span data-ttu-id="0af80-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="0af80-106">Get</span></span>
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="0af80-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0af80-107">DESCRIPTION</span></span>
<span data-ttu-id="0af80-108">Uzyskiwanie listy elementów galerii dostępnych w witrynie Azure Stack platform</span><span class="sxs-lookup"><span data-stu-id="0af80-108">Get a list of gallery items available in Azure Stack Marketplace</span></span>

## <span data-ttu-id="0af80-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0af80-109">EXAMPLES</span></span>

### <span data-ttu-id="0af80-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0af80-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsGalleryItem
```

<span data-ttu-id="0af80-111">Elementy galerii list.</span><span class="sxs-lookup"><span data-stu-id="0af80-111">List gallery items.</span></span>

### <span data-ttu-id="0af80-112">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0af80-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

<span data-ttu-id="0af80-113">Uzyskaj element galerii według nazwy.</span><span class="sxs-lookup"><span data-stu-id="0af80-113">Get a gallery item by name.</span></span>

## <span data-ttu-id="0af80-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0af80-114">PARAMETERS</span></span>

### <span data-ttu-id="0af80-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0af80-115">-Name</span></span>
<span data-ttu-id="0af80-116">Tożsamość elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="0af80-116">Identity of the gallery item.</span></span>
<span data-ttu-id="0af80-117">Zawiera nazwę wydawcy, nazwę elementu i może zawierać wersję rozdzieloną znakiem kropki.</span><span class="sxs-lookup"><span data-stu-id="0af80-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="0af80-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af80-118">CommonParameters</span></span>
<span data-ttu-id="0af80-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0af80-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af80-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0af80-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af80-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0af80-121">INPUTS</span></span>

## <span data-ttu-id="0af80-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0af80-122">OUTPUTS</span></span>

### <span data-ttu-id="0af80-123">Microsoft. AzureStack. Management. Gallery. admin. models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="0af80-123">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="0af80-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0af80-124">NOTES</span></span>

## <span data-ttu-id="0af80-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0af80-125">RELATED LINKS</span></span>

