---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0aa30655a7fa73b6cb53de12f8906ebb59ea5a17
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889690"
---
# <span data-ttu-id="4531e-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="4531e-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="4531e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4531e-102">SYNOPSIS</span></span>
<span data-ttu-id="4531e-103">Umożliwia usunięcie obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4531e-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="4531e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4531e-104">SYNTAX</span></span>

### <span data-ttu-id="4531e-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="4531e-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4531e-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="4531e-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4531e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4531e-107">DESCRIPTION</span></span>
<span data-ttu-id="4531e-108">Umożliwia usunięcie określonego obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4531e-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="4531e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4531e-109">EXAMPLES</span></span>

### <span data-ttu-id="4531e-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4531e-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="4531e-111">Usuwanie rozszerzenia obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="4531e-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="4531e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4531e-112">PARAMETERS</span></span>

### <span data-ttu-id="4531e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4531e-113">-Force</span></span>
<span data-ttu-id="4531e-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4531e-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4531e-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4531e-115">-Location</span></span>
<span data-ttu-id="4531e-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="4531e-116">Location of the resource.</span></span>

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

### <span data-ttu-id="4531e-117">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="4531e-117">-Publisher</span></span>
<span data-ttu-id="4531e-118">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="4531e-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="4531e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4531e-119">-ResourceId</span></span>
<span data-ttu-id="4531e-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="4531e-120">The resource id.</span></span>

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

### <span data-ttu-id="4531e-121">-Type</span><span class="sxs-lookup"><span data-stu-id="4531e-121">-Type</span></span>
<span data-ttu-id="4531e-122">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="4531e-122">Type of extension.</span></span>

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

### <span data-ttu-id="4531e-123">-Version</span><span class="sxs-lookup"><span data-stu-id="4531e-123">-Version</span></span>
<span data-ttu-id="4531e-124">Wersja obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4531e-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="4531e-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4531e-125">-Confirm</span></span>
<span data-ttu-id="4531e-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4531e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4531e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4531e-127">-WhatIf</span></span>
<span data-ttu-id="4531e-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4531e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4531e-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4531e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4531e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4531e-130">CommonParameters</span></span>
<span data-ttu-id="4531e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4531e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4531e-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4531e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4531e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4531e-133">INPUTS</span></span>

## <span data-ttu-id="4531e-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4531e-134">OUTPUTS</span></span>

## <span data-ttu-id="4531e-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4531e-135">NOTES</span></span>

## <span data-ttu-id="4531e-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4531e-136">RELATED LINKS</span></span>

