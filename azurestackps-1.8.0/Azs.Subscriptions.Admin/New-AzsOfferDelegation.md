---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78c0e9d2796cd6edf1a2d094cc6dd3b37614e3aa
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889221"
---
# <span data-ttu-id="de97b-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="de97b-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="de97b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de97b-102">SYNOPSIS</span></span>
<span data-ttu-id="de97b-103">Utwórz nową delegację oferty.</span><span class="sxs-lookup"><span data-stu-id="de97b-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="de97b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de97b-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de97b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="de97b-105">DESCRIPTION</span></span>
<span data-ttu-id="de97b-106">Utwórz nową delegację oferty.</span><span class="sxs-lookup"><span data-stu-id="de97b-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="de97b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de97b-107">EXAMPLES</span></span>

### <span data-ttu-id="de97b-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="de97b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="de97b-109">Utwórz nową delegację oferty.</span><span class="sxs-lookup"><span data-stu-id="de97b-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="de97b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de97b-110">PARAMETERS</span></span>

### <span data-ttu-id="de97b-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="de97b-111">-Location</span></span>
<span data-ttu-id="de97b-112">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="de97b-112">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de97b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de97b-113">-Name</span></span>
<span data-ttu-id="de97b-114">Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="de97b-114">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de97b-115">-Offername</span><span class="sxs-lookup"><span data-stu-id="de97b-115">-OfferName</span></span>
<span data-ttu-id="de97b-116">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="de97b-116">Name of an offer.</span></span>

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

### <span data-ttu-id="de97b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de97b-117">-ResourceGroupName</span></span>
<span data-ttu-id="de97b-118">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="de97b-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de97b-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="de97b-119">-SubscriptionId</span></span>
<span data-ttu-id="de97b-120">Identyfikator subskrypcji otrzymującej ofertę delegowaną.</span><span class="sxs-lookup"><span data-stu-id="de97b-120">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de97b-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de97b-121">-Confirm</span></span>
<span data-ttu-id="de97b-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de97b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de97b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de97b-123">-WhatIf</span></span>
<span data-ttu-id="de97b-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de97b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de97b-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="de97b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de97b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de97b-126">CommonParameters</span></span>
<span data-ttu-id="de97b-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de97b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de97b-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de97b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de97b-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de97b-129">INPUTS</span></span>

## <span data-ttu-id="de97b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de97b-130">OUTPUTS</span></span>

### <span data-ttu-id="de97b-131">Microsoft. AzureStack. Management. Subscriptions. admin. models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="de97b-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="de97b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de97b-132">NOTES</span></span>

## <span data-ttu-id="de97b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de97b-133">RELATED LINKS</span></span>

