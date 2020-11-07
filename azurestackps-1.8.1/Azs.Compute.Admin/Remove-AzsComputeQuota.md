---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ebc1ebae40d6d1726ee6c23def6f82ff1efc8517
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889713"
---
# <span data-ttu-id="3e05e-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="3e05e-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="3e05e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e05e-102">SYNOPSIS</span></span>
<span data-ttu-id="3e05e-103">Usuwa określony przydział obliczania.</span><span class="sxs-lookup"><span data-stu-id="3e05e-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="3e05e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e05e-104">SYNTAX</span></span>

### <span data-ttu-id="3e05e-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3e05e-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e05e-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="3e05e-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e05e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3e05e-107">DESCRIPTION</span></span>
<span data-ttu-id="3e05e-108">Usuwanie istniejącego przydziału.</span><span class="sxs-lookup"><span data-stu-id="3e05e-108">Delete an existing quota.</span></span>

## <span data-ttu-id="3e05e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e05e-109">EXAMPLES</span></span>

### <span data-ttu-id="3e05e-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3e05e-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="3e05e-111">Usuń przydział obliczeń, używając wszystkich parametrów.</span><span class="sxs-lookup"><span data-stu-id="3e05e-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="3e05e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e05e-112">PARAMETERS</span></span>

### <span data-ttu-id="3e05e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3e05e-113">-Force</span></span>
<span data-ttu-id="3e05e-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3e05e-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3e05e-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3e05e-115">-Location</span></span>
<span data-ttu-id="3e05e-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="3e05e-116">Location of the resource.</span></span> <span data-ttu-id="3e05e-117">Jeśli nie przydzielono jej domyślnie do lokalizacji powiązanej z subskrypcją usługi tenat.</span><span class="sxs-lookup"><span data-stu-id="3e05e-117">If not given we default to the location bound to the tenat's subscription.</span></span>

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

### <span data-ttu-id="3e05e-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e05e-118">-Name</span></span>
<span data-ttu-id="3e05e-119">Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="3e05e-119">Name of the quota.</span></span>

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

### <span data-ttu-id="3e05e-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e05e-120">-ResourceId</span></span>
<span data-ttu-id="3e05e-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="3e05e-121">The resource id.</span></span>

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

### <span data-ttu-id="3e05e-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e05e-122">-Confirm</span></span>
<span data-ttu-id="3e05e-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e05e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e05e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e05e-124">-WhatIf</span></span>
<span data-ttu-id="3e05e-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e05e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e05e-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3e05e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e05e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e05e-127">CommonParameters</span></span>
<span data-ttu-id="3e05e-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e05e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e05e-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e05e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e05e-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e05e-130">INPUTS</span></span>

## <span data-ttu-id="3e05e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e05e-131">OUTPUTS</span></span>

## <span data-ttu-id="3e05e-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e05e-132">NOTES</span></span>

## <span data-ttu-id="3e05e-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e05e-133">RELATED LINKS</span></span>

