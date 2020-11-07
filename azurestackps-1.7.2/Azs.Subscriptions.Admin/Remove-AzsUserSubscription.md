---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d76356e99419ff345e2eccc025c91637417de1a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888369"
---
# <span data-ttu-id="46295-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="46295-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="46295-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46295-102">SYNOPSIS</span></span>
<span data-ttu-id="46295-103">Umożliwia usunięcie określonego abonamentu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="46295-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="46295-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46295-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46295-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46295-105">DESCRIPTION</span></span>
<span data-ttu-id="46295-106">Umożliwia usunięcie określonego abonamentu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="46295-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="46295-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46295-107">EXAMPLES</span></span>

### <span data-ttu-id="46295-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="46295-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="46295-109">Usuwanie określonego abonamentu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="46295-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="46295-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46295-110">PARAMETERS</span></span>

### <span data-ttu-id="46295-111">-Force</span><span class="sxs-lookup"><span data-stu-id="46295-111">-Force</span></span>
<span data-ttu-id="46295-112">Flaga usunięcia elementu bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="46295-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="46295-113">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="46295-113">-SubscriptionId</span></span>
<span data-ttu-id="46295-114">Parametr identyfikatora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="46295-114">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="46295-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46295-115">-Confirm</span></span>
<span data-ttu-id="46295-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46295-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46295-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46295-117">-WhatIf</span></span>
<span data-ttu-id="46295-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46295-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46295-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="46295-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46295-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46295-120">CommonParameters</span></span>
<span data-ttu-id="46295-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46295-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46295-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46295-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46295-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46295-123">INPUTS</span></span>

## <span data-ttu-id="46295-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46295-124">OUTPUTS</span></span>

## <span data-ttu-id="46295-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46295-125">NOTES</span></span>

## <span data-ttu-id="46295-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46295-126">RELATED LINKS</span></span>

