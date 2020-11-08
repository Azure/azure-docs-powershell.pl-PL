---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25411a71a6d8233be55ab25ac99487da0b44bd0b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055826"
---
# <span data-ttu-id="2e4e4-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="2e4e4-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="2e4e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e4e4-102">SYNOPSIS</span></span>
<span data-ttu-id="2e4e4-103">Umożliwia usunięcie określonego abonamentu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="2e4e4-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="2e4e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e4e4-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e4e4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e4e4-105">DESCRIPTION</span></span>
<span data-ttu-id="2e4e4-106">Umożliwia usunięcie określonego abonamentu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="2e4e4-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="2e4e4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e4e4-107">EXAMPLES</span></span>

### <span data-ttu-id="2e4e4-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2e4e4-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="2e4e4-109">Usuwanie określonego abonamentu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="2e4e4-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="2e4e4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e4e4-110">PARAMETERS</span></span>

### <span data-ttu-id="2e4e4-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2e4e4-111">-Force</span></span>
<span data-ttu-id="2e4e4-112">Flaga usunięcia elementu bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="2e4e4-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="2e4e4-113">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2e4e4-113">-SubscriptionId</span></span>
<span data-ttu-id="2e4e4-114">Parametr identyfikatora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2e4e4-114">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e4e4-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e4e4-115">-Confirm</span></span>
<span data-ttu-id="2e4e4-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e4e4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e4e4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e4e4-117">-WhatIf</span></span>
<span data-ttu-id="2e4e4-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e4e4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e4e4-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e4e4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e4e4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e4e4-120">CommonParameters</span></span>
<span data-ttu-id="2e4e4-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e4e4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e4e4-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e4e4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e4e4-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e4e4-123">INPUTS</span></span>

## <span data-ttu-id="2e4e4-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e4e4-124">OUTPUTS</span></span>

## <span data-ttu-id="2e4e4-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e4e4-125">NOTES</span></span>

## <span data-ttu-id="2e4e4-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e4e4-126">RELATED LINKS</span></span>

