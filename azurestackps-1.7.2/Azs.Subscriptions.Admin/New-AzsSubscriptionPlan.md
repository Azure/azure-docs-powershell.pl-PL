---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: aee9eab2ce04c1b9454fcf133edc290e887caf50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888397"
---
# <span data-ttu-id="34195-101">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="34195-101">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="34195-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34195-102">SYNOPSIS</span></span>
<span data-ttu-id="34195-103">Tworzy plan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="34195-103">Creates a subscription plan.</span></span>

## <span data-ttu-id="34195-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34195-104">SYNTAX</span></span>

```
New-AzsSubscriptionPlan [[-AcquisitionId] <Guid>] [-PlanId] <String> [-TargetSubscriptionId] <Guid> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34195-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34195-105">DESCRIPTION</span></span>
<span data-ttu-id="34195-106">Tworzy plan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="34195-106">Creates a subscription plan.</span></span>

## <span data-ttu-id="34195-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34195-107">EXAMPLES</span></span>

### <span data-ttu-id="34195-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="34195-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscriptionPlan -PlanId "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1" -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="34195-109">Tworzenie planu abonamentu.</span><span class="sxs-lookup"><span data-stu-id="34195-109">Create an subscription plan.</span></span>

## <span data-ttu-id="34195-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34195-110">PARAMETERS</span></span>

### <span data-ttu-id="34195-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="34195-111">-AcquisitionId</span></span>
<span data-ttu-id="34195-112">Identyfikator nabycia.</span><span class="sxs-lookup"><span data-stu-id="34195-112">Acquisition identifier.</span></span>

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

### <span data-ttu-id="34195-113">-PlanId</span><span class="sxs-lookup"><span data-stu-id="34195-113">-PlanId</span></span>
<span data-ttu-id="34195-114">Identyfikator planu w kontekście subskrypcji dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="34195-114">Plan identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="34195-115">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34195-115">-TargetSubscriptionId</span></span>
<span data-ttu-id="34195-116">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="34195-116">The target subscription ID.</span></span>

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

### <span data-ttu-id="34195-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34195-117">-Confirm</span></span>
<span data-ttu-id="34195-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34195-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34195-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34195-119">-WhatIf</span></span>
<span data-ttu-id="34195-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34195-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34195-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="34195-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34195-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34195-122">CommonParameters</span></span>
<span data-ttu-id="34195-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34195-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34195-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34195-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34195-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34195-125">INPUTS</span></span>

## <span data-ttu-id="34195-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34195-126">OUTPUTS</span></span>

### <span data-ttu-id="34195-127">Microsoft. AzureStack. Management. Subscriptions. admin. models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="34195-127">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="34195-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34195-128">NOTES</span></span>

## <span data-ttu-id="34195-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34195-129">RELATED LINKS</span></span>

