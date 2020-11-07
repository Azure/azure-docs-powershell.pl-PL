---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e6588eed555062aaf6dbb4075dffd9506c05503
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889169"
---
# <span data-ttu-id="b2643-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="b2643-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="b2643-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2643-102">SYNOPSIS</span></span>
<span data-ttu-id="b2643-103">Usuwanie określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b2643-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="b2643-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2643-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2643-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b2643-105">DESCRIPTION</span></span>
<span data-ttu-id="b2643-106">Usuwanie określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b2643-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="b2643-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2643-107">EXAMPLES</span></span>

### <span data-ttu-id="b2643-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="b2643-108">EXAMPLE 1</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="b2643-109">Usuwanie określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b2643-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="b2643-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2643-110">PARAMETERS</span></span>

### <span data-ttu-id="b2643-111">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b2643-111">-SubscriptionId</span></span>
<span data-ttu-id="b2643-112">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b2643-112">Id of the subscription.</span></span>

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

### <span data-ttu-id="b2643-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b2643-113">-Force</span></span>
<span data-ttu-id="b2643-114">Usuń abonament bez monitowania</span><span class="sxs-lookup"><span data-stu-id="b2643-114">Remove subscription without prompting</span></span>

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

### <span data-ttu-id="b2643-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2643-115">-WhatIf</span></span>
<span data-ttu-id="b2643-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2643-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2643-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b2643-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2643-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2643-118">-Confirm</span></span>
<span data-ttu-id="b2643-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2643-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2643-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2643-120">CommonParameters</span></span>
<span data-ttu-id="b2643-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2643-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2643-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2643-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2643-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2643-123">INPUTS</span></span>

## <span data-ttu-id="b2643-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2643-124">OUTPUTS</span></span>

## <span data-ttu-id="b2643-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2643-125">NOTES</span></span>

## <span data-ttu-id="b2643-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2643-126">RELATED LINKS</span></span>
