---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d4b7abdeb085c7cfee6444c4afeeb6a3e79d99e9
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888890"
---
# <span data-ttu-id="dc5ec-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="dc5ec-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="dc5ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="dc5ec-103">Utwórz nowy abonament.</span><span class="sxs-lookup"><span data-stu-id="dc5ec-103">Create a new subscription.</span></span>

## <span data-ttu-id="dc5ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc5ec-104">SYNTAX</span></span>

```
New-AzsUserSubscription [-Owner] <String> [-OfferId] <String> [[-TenantId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-RoutingResourceManagerType] <String>]
 [[-ExternalReferenceId] <String>] [[-State] <String>] [[-SubscriptionId] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc5ec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dc5ec-105">DESCRIPTION</span></span>
<span data-ttu-id="dc5ec-106">Utwórz nowy abonament.</span><span class="sxs-lookup"><span data-stu-id="dc5ec-106">Create a new subscription.</span></span>

## <span data-ttu-id="dc5ec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc5ec-107">EXAMPLES</span></span>

### <span data-ttu-id="dc5ec-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dc5ec-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsUserSubscription -Owner user@contoso.com -OfferId "/subscriptions/302d0fcd-5263-4f4d-82ba-383ad95a3e53/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/offers/offer1"
```

<span data-ttu-id="dc5ec-109">Tworzy nową subskrypcję użytkownika</span><span class="sxs-lookup"><span data-stu-id="dc5ec-109">Creates a new user subscription</span></span>

## <span data-ttu-id="dc5ec-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc5ec-110">PARAMETERS</span></span>

### <span data-ttu-id="dc5ec-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc5ec-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="dc5ec-112">Identyfikator subskrypcji DelegatedProvider nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="dc5ec-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="dc5ec-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dc5ec-113">-DisplayName</span></span>
<span data-ttu-id="dc5ec-114">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dc5ec-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc5ec-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="dc5ec-115">-ExternalReferenceId</span></span>
<span data-ttu-id="dc5ec-116">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="dc5ec-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc5ec-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="dc5ec-117">-OfferId</span></span>
<span data-ttu-id="dc5ec-118">Identyfikator oferty w ramach zakresu dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="dc5ec-118">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="dc5ec-119">-Właściciel</span><span class="sxs-lookup"><span data-stu-id="dc5ec-119">-Owner</span></span>
<span data-ttu-id="dc5ec-120">Właściciel subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dc5ec-120">Subscription owner.</span></span>

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

### <span data-ttu-id="dc5ec-121">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="dc5ec-121">-RoutingResourceManagerType</span></span>
<span data-ttu-id="dc5ec-122">Typ Menedżera zasobów routingu.</span><span class="sxs-lookup"><span data-stu-id="dc5ec-122">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc5ec-123">-State</span><span class="sxs-lookup"><span data-stu-id="dc5ec-123">-State</span></span>
<span data-ttu-id="dc5ec-124">Stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="dc5ec-124">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc5ec-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="dc5ec-125">-SubscriptionId</span></span>
<span data-ttu-id="dc5ec-126">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dc5ec-126">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc5ec-127">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="dc5ec-127">-TenantId</span></span>
<span data-ttu-id="dc5ec-128">Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="dc5ec-128">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc5ec-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dc5ec-129">-Confirm</span></span>
<span data-ttu-id="dc5ec-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc5ec-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc5ec-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc5ec-131">-WhatIf</span></span>
<span data-ttu-id="dc5ec-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc5ec-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc5ec-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dc5ec-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc5ec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc5ec-134">CommonParameters</span></span>
<span data-ttu-id="dc5ec-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc5ec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc5ec-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc5ec-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc5ec-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc5ec-137">INPUTS</span></span>

## <span data-ttu-id="dc5ec-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc5ec-138">OUTPUTS</span></span>

### <span data-ttu-id="dc5ec-139">Microsoft. AzureStack. Management. Subscriptions. admin. modele. Subscription</span><span class="sxs-lookup"><span data-stu-id="dc5ec-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="dc5ec-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc5ec-140">NOTES</span></span>

## <span data-ttu-id="dc5ec-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc5ec-141">RELATED LINKS</span></span>

