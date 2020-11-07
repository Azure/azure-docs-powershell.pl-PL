---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b3fb659c1d11df734bdc95f554e4c100060e185
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523281"
---
# <span data-ttu-id="04227-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="04227-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="04227-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04227-102">SYNOPSIS</span></span>
<span data-ttu-id="04227-103">Usuwa określony przydział obliczania.</span><span class="sxs-lookup"><span data-stu-id="04227-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="04227-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04227-104">SYNTAX</span></span>

### <span data-ttu-id="04227-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="04227-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04227-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="04227-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04227-107">Opis</span><span class="sxs-lookup"><span data-stu-id="04227-107">DESCRIPTION</span></span>
<span data-ttu-id="04227-108">Usuwanie istniejącego przydziału.</span><span class="sxs-lookup"><span data-stu-id="04227-108">Delete an existing quota.</span></span>

## <span data-ttu-id="04227-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04227-109">EXAMPLES</span></span>

### <span data-ttu-id="04227-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="04227-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="04227-111">Usuń przydział obliczeń, używając wszystkich parametrów.</span><span class="sxs-lookup"><span data-stu-id="04227-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="04227-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04227-112">PARAMETERS</span></span>

### <span data-ttu-id="04227-113">-Force</span><span class="sxs-lookup"><span data-stu-id="04227-113">-Force</span></span>
<span data-ttu-id="04227-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="04227-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="04227-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="04227-115">-Location</span></span>
<span data-ttu-id="04227-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="04227-116">Location of the resource.</span></span> <span data-ttu-id="04227-117">Jeśli nie przydzielono jej domyślnie do lokalizacji powiązanej z subskrypcją usługi tenat.</span><span class="sxs-lookup"><span data-stu-id="04227-117">If not given we default to the location bound to the tenat's subscription.</span></span>

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

### <span data-ttu-id="04227-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="04227-118">-Name</span></span>
<span data-ttu-id="04227-119">Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="04227-119">Name of the quota.</span></span>

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

### <span data-ttu-id="04227-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04227-120">-ResourceId</span></span>
<span data-ttu-id="04227-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="04227-121">The resource id.</span></span>

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

### <span data-ttu-id="04227-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04227-122">-Confirm</span></span>
<span data-ttu-id="04227-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04227-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04227-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04227-124">-WhatIf</span></span>
<span data-ttu-id="04227-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04227-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04227-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="04227-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04227-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04227-127">CommonParameters</span></span>
<span data-ttu-id="04227-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04227-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04227-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04227-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04227-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04227-130">INPUTS</span></span>

## <span data-ttu-id="04227-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04227-131">OUTPUTS</span></span>

## <span data-ttu-id="04227-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04227-132">NOTES</span></span>

## <span data-ttu-id="04227-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04227-133">RELATED LINKS</span></span>
