---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2ac9f85896c1ae0a8eb7e060600ba5b4eb0e792
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888681"
---
# <span data-ttu-id="24cd4-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="24cd4-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="24cd4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24cd4-102">SYNOPSIS</span></span>
<span data-ttu-id="24cd4-103">Usuwanie określonej oferty.</span><span class="sxs-lookup"><span data-stu-id="24cd4-103">Delete the specified offer.</span></span>

## <span data-ttu-id="24cd4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24cd4-104">SYNTAX</span></span>

### <span data-ttu-id="24cd4-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="24cd4-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24cd4-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="24cd4-106">ResourceId</span></span>
```
Remove-AzsOffer -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24cd4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="24cd4-107">DESCRIPTION</span></span>
<span data-ttu-id="24cd4-108">Usuwanie określonej oferty.</span><span class="sxs-lookup"><span data-stu-id="24cd4-108">Delete the specified offer.</span></span>

## <span data-ttu-id="24cd4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24cd4-109">EXAMPLES</span></span>

### <span data-ttu-id="24cd4-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="24cd4-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOffer -Name offername1 -ResourceGroupName rg1
```

<span data-ttu-id="24cd4-111">Usuwanie określonej oferty.</span><span class="sxs-lookup"><span data-stu-id="24cd4-111">Delete the specified offer.</span></span>

## <span data-ttu-id="24cd4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24cd4-112">PARAMETERS</span></span>

### <span data-ttu-id="24cd4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="24cd4-113">-Force</span></span>
<span data-ttu-id="24cd4-114">Flaga usunięcia elementu bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="24cd4-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="24cd4-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24cd4-115">-Name</span></span>
<span data-ttu-id="24cd4-116">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="24cd4-116">Name of an offer.</span></span>

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

### <span data-ttu-id="24cd4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24cd4-117">-ResourceGroupName</span></span>
<span data-ttu-id="24cd4-118">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="24cd4-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="24cd4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24cd4-119">-ResourceId</span></span>
<span data-ttu-id="24cd4-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="24cd4-120">The resource id.</span></span>

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

### <span data-ttu-id="24cd4-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24cd4-121">-Confirm</span></span>
<span data-ttu-id="24cd4-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24cd4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24cd4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24cd4-123">-WhatIf</span></span>
<span data-ttu-id="24cd4-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24cd4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24cd4-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24cd4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24cd4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24cd4-126">CommonParameters</span></span>
<span data-ttu-id="24cd4-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24cd4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24cd4-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24cd4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24cd4-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24cd4-129">INPUTS</span></span>

## <span data-ttu-id="24cd4-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24cd4-130">OUTPUTS</span></span>

## <span data-ttu-id="24cd4-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24cd4-131">NOTES</span></span>

## <span data-ttu-id="24cd4-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24cd4-132">RELATED LINKS</span></span>

