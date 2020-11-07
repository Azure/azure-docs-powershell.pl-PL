---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b82dadf9a9e26b0023872378d41e4978e18436ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710762"
---
# <span data-ttu-id="e91c3-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="e91c3-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="e91c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e91c3-102">SYNOPSIS</span></span>
<span data-ttu-id="e91c3-103">Usuwa plan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e91c3-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="e91c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e91c3-104">SYNTAX</span></span>

### <span data-ttu-id="e91c3-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e91c3-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e91c3-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="e91c3-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e91c3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e91c3-107">DESCRIPTION</span></span>
<span data-ttu-id="e91c3-108">Usuwa plan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e91c3-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="e91c3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e91c3-109">EXAMPLES</span></span>

### <span data-ttu-id="e91c3-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e91c3-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="e91c3-111">Usuwanie planu abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e91c3-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="e91c3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e91c3-112">PARAMETERS</span></span>

### <span data-ttu-id="e91c3-113">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="e91c3-113">-AcquisitionId</span></span>
<span data-ttu-id="e91c3-114">Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="e91c3-114">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="e91c3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e91c3-115">-Force</span></span>
<span data-ttu-id="e91c3-116">Flaga usunięcia elementu bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="e91c3-116">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="e91c3-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e91c3-117">-ResourceId</span></span>
<span data-ttu-id="e91c3-118">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e91c3-118">The resource id.</span></span>

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

### <span data-ttu-id="e91c3-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e91c3-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="e91c3-120">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e91c3-120">The target subscription ID.</span></span>

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

### <span data-ttu-id="e91c3-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e91c3-121">-Confirm</span></span>
<span data-ttu-id="e91c3-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e91c3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e91c3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e91c3-123">-WhatIf</span></span>
<span data-ttu-id="e91c3-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e91c3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e91c3-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e91c3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e91c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e91c3-126">CommonParameters</span></span>
<span data-ttu-id="e91c3-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e91c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e91c3-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e91c3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e91c3-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e91c3-129">INPUTS</span></span>

## <span data-ttu-id="e91c3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e91c3-130">OUTPUTS</span></span>

## <span data-ttu-id="e91c3-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e91c3-131">NOTES</span></span>

## <span data-ttu-id="e91c3-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e91c3-132">RELATED LINKS</span></span>

