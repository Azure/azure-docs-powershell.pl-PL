---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: fdceee36319d1c9ea950dbf5573b4ba0e3c614ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523869"
---
# <span data-ttu-id="1f068-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="1f068-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="1f068-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f068-102">SYNOPSIS</span></span>
<span data-ttu-id="1f068-103">Usuwanie określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1f068-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="1f068-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f068-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f068-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1f068-105">DESCRIPTION</span></span>
<span data-ttu-id="1f068-106">Usuwanie określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1f068-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="1f068-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f068-107">EXAMPLES</span></span>

### <span data-ttu-id="1f068-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1f068-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="1f068-109">Usuwanie określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1f068-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="1f068-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f068-110">PARAMETERS</span></span>

### <span data-ttu-id="1f068-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1f068-111">-Force</span></span>
<span data-ttu-id="1f068-112">Usuń abonament bez monitowania</span><span class="sxs-lookup"><span data-stu-id="1f068-112">Remove subscription without prompting</span></span>

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

### <span data-ttu-id="1f068-113">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1f068-113">-SubscriptionId</span></span>
<span data-ttu-id="1f068-114">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1f068-114">Id of the subscription.</span></span>

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

### <span data-ttu-id="1f068-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f068-115">-Confirm</span></span>
<span data-ttu-id="1f068-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f068-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f068-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f068-117">-WhatIf</span></span>
<span data-ttu-id="1f068-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f068-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f068-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1f068-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f068-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f068-120">CommonParameters</span></span>
<span data-ttu-id="1f068-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f068-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f068-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f068-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f068-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f068-123">INPUTS</span></span>

## <span data-ttu-id="1f068-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f068-124">OUTPUTS</span></span>

## <span data-ttu-id="1f068-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f068-125">NOTES</span></span>

## <span data-ttu-id="1f068-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f068-126">RELATED LINKS</span></span>

