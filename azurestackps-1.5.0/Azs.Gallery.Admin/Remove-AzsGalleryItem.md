---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 148cfa9db340b4a10e02b0870fc2edb5efb20a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523366"
---
# <span data-ttu-id="8eaed-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="8eaed-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="8eaed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8eaed-102">SYNOPSIS</span></span>
<span data-ttu-id="8eaed-103">Usuwanie określonego elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="8eaed-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="8eaed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8eaed-104">SYNTAX</span></span>

### <span data-ttu-id="8eaed-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8eaed-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8eaed-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="8eaed-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eaed-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8eaed-107">DESCRIPTION</span></span>
<span data-ttu-id="8eaed-108">Usuwanie określonego elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="8eaed-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="8eaed-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8eaed-109">EXAMPLES</span></span>

### <span data-ttu-id="8eaed-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8eaed-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="8eaed-111">Usuwanie elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="8eaed-111">Delete a gallery item.</span></span>

## <span data-ttu-id="8eaed-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8eaed-112">PARAMETERS</span></span>

### <span data-ttu-id="8eaed-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8eaed-113">-Force</span></span>
<span data-ttu-id="8eaed-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8eaed-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8eaed-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8eaed-115">-Name</span></span>
<span data-ttu-id="8eaed-116">Tożsamość elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="8eaed-116">Identity of the gallery item.</span></span>
<span data-ttu-id="8eaed-117">Zawiera nazwę wydawcy, nazwę elementu i może zawierać wersję rozdzieloną znakiem kropki.</span><span class="sxs-lookup"><span data-stu-id="8eaed-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eaed-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8eaed-118">-ResourceId</span></span>
<span data-ttu-id="8eaed-119">W pełni kwalifikowany identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8eaed-119">Fully qualified Azure resource Id.</span></span>

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

### <span data-ttu-id="8eaed-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8eaed-120">-Confirm</span></span>
<span data-ttu-id="8eaed-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8eaed-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8eaed-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eaed-122">-WhatIf</span></span>
<span data-ttu-id="8eaed-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8eaed-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8eaed-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8eaed-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8eaed-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eaed-125">CommonParameters</span></span>
<span data-ttu-id="8eaed-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eaed-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eaed-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eaed-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eaed-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8eaed-128">INPUTS</span></span>

## <span data-ttu-id="8eaed-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8eaed-129">OUTPUTS</span></span>

## <span data-ttu-id="8eaed-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8eaed-130">NOTES</span></span>

## <span data-ttu-id="8eaed-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8eaed-131">RELATED LINKS</span></span>

