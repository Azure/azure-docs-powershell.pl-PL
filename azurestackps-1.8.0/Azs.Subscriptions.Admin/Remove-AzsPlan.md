---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75010b9591b4211f32c5665aa969bae28d69aaea
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888862"
---
# <span data-ttu-id="bf754-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="bf754-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="bf754-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf754-102">SYNOPSIS</span></span>
<span data-ttu-id="bf754-103">Usuwa określony plan</span><span class="sxs-lookup"><span data-stu-id="bf754-103">Removes the specified plan</span></span>

## <span data-ttu-id="bf754-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf754-104">SYNTAX</span></span>

### <span data-ttu-id="bf754-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="bf754-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf754-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="bf754-106">ResourceId</span></span>
```
Remove-AzsPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf754-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bf754-107">DESCRIPTION</span></span>
<span data-ttu-id="bf754-108">Usuwa określony plan</span><span class="sxs-lookup"><span data-stu-id="bf754-108">Removes the specified plan</span></span>

## <span data-ttu-id="bf754-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf754-109">EXAMPLES</span></span>

### <span data-ttu-id="bf754-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bf754-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlan -Name plan1 -ResourceGroupName "rg1"
```

<span data-ttu-id="bf754-111">Usuwa określony plan</span><span class="sxs-lookup"><span data-stu-id="bf754-111">Removes the specified plan</span></span>

## <span data-ttu-id="bf754-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf754-112">PARAMETERS</span></span>

### <span data-ttu-id="bf754-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bf754-113">-Force</span></span>
<span data-ttu-id="bf754-114">Flaga usunięcia elementu bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="bf754-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="bf754-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf754-115">-Name</span></span>
<span data-ttu-id="bf754-116">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="bf754-116">Name of the plan.</span></span>

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

### <span data-ttu-id="bf754-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf754-117">-ResourceGroupName</span></span>
<span data-ttu-id="bf754-118">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="bf754-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="bf754-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf754-119">-ResourceId</span></span>
<span data-ttu-id="bf754-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="bf754-120">The resource id.</span></span>

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

### <span data-ttu-id="bf754-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bf754-121">-Confirm</span></span>
<span data-ttu-id="bf754-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf754-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf754-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf754-123">-WhatIf</span></span>
<span data-ttu-id="bf754-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf754-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf754-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bf754-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf754-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf754-126">CommonParameters</span></span>
<span data-ttu-id="bf754-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf754-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf754-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf754-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf754-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf754-129">INPUTS</span></span>

## <span data-ttu-id="bf754-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf754-130">OUTPUTS</span></span>

## <span data-ttu-id="bf754-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf754-131">NOTES</span></span>

## <span data-ttu-id="bf754-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf754-132">RELATED LINKS</span></span>

