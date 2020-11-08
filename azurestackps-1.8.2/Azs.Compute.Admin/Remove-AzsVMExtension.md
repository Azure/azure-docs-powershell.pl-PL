---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0aa30655a7fa73b6cb53de12f8906ebb59ea5a17
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055751"
---
# <span data-ttu-id="0c0a0-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="0c0a0-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="0c0a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c0a0-102">SYNOPSIS</span></span>
<span data-ttu-id="0c0a0-103">Umożliwia usunięcie obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="0c0a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c0a0-104">SYNTAX</span></span>

### <span data-ttu-id="0c0a0-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="0c0a0-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c0a0-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="0c0a0-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c0a0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0c0a0-107">DESCRIPTION</span></span>
<span data-ttu-id="0c0a0-108">Umożliwia usunięcie określonego obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="0c0a0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c0a0-109">EXAMPLES</span></span>

### <span data-ttu-id="0c0a0-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0c0a0-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="0c0a0-111">Usuwanie rozszerzenia obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="0c0a0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c0a0-112">PARAMETERS</span></span>

### <span data-ttu-id="0c0a0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0c0a0-113">-Force</span></span>
<span data-ttu-id="0c0a0-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0c0a0-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0c0a0-115">-Location</span></span>
<span data-ttu-id="0c0a0-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-116">Location of the resource.</span></span>

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

### <span data-ttu-id="0c0a0-117">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="0c0a0-117">-Publisher</span></span>
<span data-ttu-id="0c0a0-118">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="0c0a0-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c0a0-119">-ResourceId</span></span>
<span data-ttu-id="0c0a0-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-120">The resource id.</span></span>

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

### <span data-ttu-id="0c0a0-121">-Type</span><span class="sxs-lookup"><span data-stu-id="0c0a0-121">-Type</span></span>
<span data-ttu-id="0c0a0-122">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-122">Type of extension.</span></span>

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

### <span data-ttu-id="0c0a0-123">-Version</span><span class="sxs-lookup"><span data-stu-id="0c0a0-123">-Version</span></span>
<span data-ttu-id="0c0a0-124">Wersja obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="0c0a0-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c0a0-125">-Confirm</span></span>
<span data-ttu-id="0c0a0-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c0a0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c0a0-127">-WhatIf</span></span>
<span data-ttu-id="0c0a0-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c0a0-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c0a0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c0a0-130">CommonParameters</span></span>
<span data-ttu-id="0c0a0-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c0a0-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c0a0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c0a0-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c0a0-133">INPUTS</span></span>

## <span data-ttu-id="0c0a0-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c0a0-134">OUTPUTS</span></span>

## <span data-ttu-id="0c0a0-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c0a0-135">NOTES</span></span>

## <span data-ttu-id="0c0a0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c0a0-136">RELATED LINKS</span></span>

