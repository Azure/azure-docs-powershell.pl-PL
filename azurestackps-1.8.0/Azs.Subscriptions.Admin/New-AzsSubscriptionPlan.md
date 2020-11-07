---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a4c99f48087dcbac17dc10da3c647525670fe90
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889217"
---
# <span data-ttu-id="e39e2-101">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="e39e2-101">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="e39e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e39e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e39e2-103">Tworzy plan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e39e2-103">Creates a subscription plan.</span></span>

## <span data-ttu-id="e39e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e39e2-104">SYNTAX</span></span>

```
New-AzsSubscriptionPlan [[-AcquisitionId] <Guid>] [-PlanId] <String> [-TargetSubscriptionId] <Guid> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e39e2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e39e2-105">DESCRIPTION</span></span>
<span data-ttu-id="e39e2-106">Tworzy plan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e39e2-106">Creates a subscription plan.</span></span>

## <span data-ttu-id="e39e2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e39e2-107">EXAMPLES</span></span>

### <span data-ttu-id="e39e2-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e39e2-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscriptionPlan -PlanId "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1" -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="e39e2-109">Tworzenie planu abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e39e2-109">Create an subscription plan.</span></span>

## <span data-ttu-id="e39e2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e39e2-110">PARAMETERS</span></span>

### <span data-ttu-id="e39e2-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="e39e2-111">-AcquisitionId</span></span>
<span data-ttu-id="e39e2-112">Identyfikator nabycia.</span><span class="sxs-lookup"><span data-stu-id="e39e2-112">Acquisition identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: $([Guid]::NewGuid())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39e2-113">-PlanId</span><span class="sxs-lookup"><span data-stu-id="e39e2-113">-PlanId</span></span>
<span data-ttu-id="e39e2-114">Identyfikator planu w kontekście subskrypcji dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e39e2-114">Plan identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39e2-115">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e39e2-115">-TargetSubscriptionId</span></span>
<span data-ttu-id="e39e2-116">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e39e2-116">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39e2-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e39e2-117">-Confirm</span></span>
<span data-ttu-id="e39e2-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e39e2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e39e2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e39e2-119">-WhatIf</span></span>
<span data-ttu-id="e39e2-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e39e2-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e39e2-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e39e2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e39e2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e39e2-122">CommonParameters</span></span>
<span data-ttu-id="e39e2-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e39e2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e39e2-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e39e2-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e39e2-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e39e2-125">INPUTS</span></span>

## <span data-ttu-id="e39e2-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e39e2-126">OUTPUTS</span></span>

### <span data-ttu-id="e39e2-127">Microsoft. AzureStack. Management. Subscriptions. admin. models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="e39e2-127">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="e39e2-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e39e2-128">NOTES</span></span>

## <span data-ttu-id="e39e2-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e39e2-129">RELATED LINKS</span></span>

