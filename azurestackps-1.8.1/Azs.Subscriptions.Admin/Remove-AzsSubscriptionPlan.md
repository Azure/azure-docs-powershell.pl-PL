---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b2f5117224318eae53b8b11f4af58c736ac800b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889462"
---
# <span data-ttu-id="a2afe-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="a2afe-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="a2afe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2afe-102">SYNOPSIS</span></span>
<span data-ttu-id="a2afe-103">Usuwa plan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a2afe-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="a2afe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2afe-104">SYNTAX</span></span>

### <span data-ttu-id="a2afe-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a2afe-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2afe-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="a2afe-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2afe-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a2afe-107">DESCRIPTION</span></span>
<span data-ttu-id="a2afe-108">Usuwa plan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a2afe-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="a2afe-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2afe-109">EXAMPLES</span></span>

### <span data-ttu-id="a2afe-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a2afe-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="a2afe-111">Usuwanie planu abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a2afe-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="a2afe-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2afe-112">PARAMETERS</span></span>

### <span data-ttu-id="a2afe-113">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="a2afe-113">-AcquisitionId</span></span>
<span data-ttu-id="a2afe-114">Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="a2afe-114">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="a2afe-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a2afe-115">-Force</span></span>
<span data-ttu-id="a2afe-116">Flaga usunięcia elementu bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="a2afe-116">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="a2afe-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2afe-117">-ResourceId</span></span>
<span data-ttu-id="a2afe-118">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a2afe-118">The resource id.</span></span>

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

### <span data-ttu-id="a2afe-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2afe-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="a2afe-120">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a2afe-120">The target subscription ID.</span></span>

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

### <span data-ttu-id="a2afe-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a2afe-121">-Confirm</span></span>
<span data-ttu-id="a2afe-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2afe-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2afe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2afe-123">-WhatIf</span></span>
<span data-ttu-id="a2afe-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2afe-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2afe-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a2afe-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2afe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2afe-126">CommonParameters</span></span>
<span data-ttu-id="a2afe-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2afe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2afe-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2afe-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2afe-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2afe-129">INPUTS</span></span>

## <span data-ttu-id="a2afe-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2afe-130">OUTPUTS</span></span>

## <span data-ttu-id="a2afe-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2afe-131">NOTES</span></span>

## <span data-ttu-id="a2afe-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2afe-132">RELATED LINKS</span></span>

