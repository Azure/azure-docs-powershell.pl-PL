---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b2f5117224318eae53b8b11f4af58c736ac800b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055776"
---
# <span data-ttu-id="39c0f-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="39c0f-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="39c0f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="39c0f-103">Usuwa plan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="39c0f-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="39c0f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39c0f-104">SYNTAX</span></span>

### <span data-ttu-id="39c0f-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="39c0f-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39c0f-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="39c0f-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39c0f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="39c0f-107">DESCRIPTION</span></span>
<span data-ttu-id="39c0f-108">Usuwa plan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="39c0f-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="39c0f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39c0f-109">EXAMPLES</span></span>

### <span data-ttu-id="39c0f-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="39c0f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="39c0f-111">Usuwanie planu abonamentu.</span><span class="sxs-lookup"><span data-stu-id="39c0f-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="39c0f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39c0f-112">PARAMETERS</span></span>

### <span data-ttu-id="39c0f-113">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="39c0f-113">-AcquisitionId</span></span>
<span data-ttu-id="39c0f-114">Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="39c0f-114">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c0f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="39c0f-115">-Force</span></span>
<span data-ttu-id="39c0f-116">Flaga usunięcia elementu bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="39c0f-116">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="39c0f-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39c0f-117">-ResourceId</span></span>
<span data-ttu-id="39c0f-118">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="39c0f-118">The resource id.</span></span>

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

### <span data-ttu-id="39c0f-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39c0f-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="39c0f-120">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="39c0f-120">The target subscription ID.</span></span>

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

### <span data-ttu-id="39c0f-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39c0f-121">-Confirm</span></span>
<span data-ttu-id="39c0f-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39c0f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39c0f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39c0f-123">-WhatIf</span></span>
<span data-ttu-id="39c0f-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39c0f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39c0f-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="39c0f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39c0f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c0f-126">CommonParameters</span></span>
<span data-ttu-id="39c0f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39c0f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c0f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39c0f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c0f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39c0f-129">INPUTS</span></span>

## <span data-ttu-id="39c0f-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39c0f-130">OUTPUTS</span></span>

## <span data-ttu-id="39c0f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39c0f-131">NOTES</span></span>

## <span data-ttu-id="39c0f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39c0f-132">RELATED LINKS</span></span>

