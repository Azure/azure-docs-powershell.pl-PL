---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a4c99f48087dcbac17dc10da3c647525670fe90
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055877"
---
# <span data-ttu-id="a8366-101">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="a8366-101">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="a8366-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8366-102">SYNOPSIS</span></span>
<span data-ttu-id="a8366-103">Tworzy plan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a8366-103">Creates a subscription plan.</span></span>

## <span data-ttu-id="a8366-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8366-104">SYNTAX</span></span>

```
New-AzsSubscriptionPlan [[-AcquisitionId] <Guid>] [-PlanId] <String> [-TargetSubscriptionId] <Guid> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8366-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a8366-105">DESCRIPTION</span></span>
<span data-ttu-id="a8366-106">Tworzy plan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a8366-106">Creates a subscription plan.</span></span>

## <span data-ttu-id="a8366-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8366-107">EXAMPLES</span></span>

### <span data-ttu-id="a8366-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a8366-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscriptionPlan -PlanId "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1" -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="a8366-109">Tworzenie planu abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a8366-109">Create an subscription plan.</span></span>

## <span data-ttu-id="a8366-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8366-110">PARAMETERS</span></span>

### <span data-ttu-id="a8366-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="a8366-111">-AcquisitionId</span></span>
<span data-ttu-id="a8366-112">Identyfikator nabycia.</span><span class="sxs-lookup"><span data-stu-id="a8366-112">Acquisition identifier.</span></span>

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

### <span data-ttu-id="a8366-113">-PlanId</span><span class="sxs-lookup"><span data-stu-id="a8366-113">-PlanId</span></span>
<span data-ttu-id="a8366-114">Identyfikator planu w kontekście subskrypcji dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="a8366-114">Plan identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="a8366-115">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8366-115">-TargetSubscriptionId</span></span>
<span data-ttu-id="a8366-116">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a8366-116">The target subscription ID.</span></span>

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

### <span data-ttu-id="a8366-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8366-117">-Confirm</span></span>
<span data-ttu-id="a8366-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8366-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8366-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8366-119">-WhatIf</span></span>
<span data-ttu-id="a8366-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8366-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8366-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a8366-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8366-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8366-122">CommonParameters</span></span>
<span data-ttu-id="a8366-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8366-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8366-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8366-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8366-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8366-125">INPUTS</span></span>

## <span data-ttu-id="a8366-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8366-126">OUTPUTS</span></span>

### <span data-ttu-id="a8366-127">Microsoft. AzureStack. Management. Subscriptions. admin. models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="a8366-127">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="a8366-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8366-128">NOTES</span></span>

## <span data-ttu-id="a8366-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8366-129">RELATED LINKS</span></span>

