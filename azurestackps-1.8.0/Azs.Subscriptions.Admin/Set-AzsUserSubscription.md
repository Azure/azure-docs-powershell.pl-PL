---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ef53ac2d32d71a68b7fe342f5d2d0cafc2a193f8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888842"
---
# <span data-ttu-id="f093a-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="f093a-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="f093a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f093a-102">SYNOPSIS</span></span>
<span data-ttu-id="f093a-103">Aktualizuje określoną subskrypcję użytkownika</span><span class="sxs-lookup"><span data-stu-id="f093a-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="f093a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f093a-104">SYNTAX</span></span>

### <span data-ttu-id="f093a-105">Set (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f093a-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f093a-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="f093a-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f093a-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="f093a-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f093a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f093a-108">DESCRIPTION</span></span>
<span data-ttu-id="f093a-109">Aktualizuje określoną subskrypcję użytkownika</span><span class="sxs-lookup"><span data-stu-id="f093a-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="f093a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f093a-110">EXAMPLES</span></span>

### <span data-ttu-id="f093a-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f093a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="f093a-112">Aktualizuje subskrypcję</span><span class="sxs-lookup"><span data-stu-id="f093a-112">Updates a subscription</span></span>

## <span data-ttu-id="f093a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f093a-113">PARAMETERS</span></span>

### <span data-ttu-id="f093a-114">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f093a-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="f093a-115">Identyfikator subskrypcji DelegatedProvider nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="f093a-115">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f093a-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f093a-116">-DisplayName</span></span>
<span data-ttu-id="f093a-117">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f093a-117">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f093a-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="f093a-118">-ExternalReferenceId</span></span>
<span data-ttu-id="f093a-119">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="f093a-119">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f093a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f093a-120">-InputObject</span></span>
<span data-ttu-id="f093a-121">Obiekt wejściowy typu Microsoft. AzureStack. Management. Network. admin. modele. przydział.</span><span class="sxs-lookup"><span data-stu-id="f093a-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

```yaml
Type: Subscription
Parameter Sets: InputObject
Aliases: Subscription

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f093a-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f093a-122">-Location</span></span>
<span data-ttu-id="f093a-123">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="f093a-123">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f093a-124">-OfferId</span><span class="sxs-lookup"><span data-stu-id="f093a-124">-OfferId</span></span>
<span data-ttu-id="f093a-125">Identyfikator oferty w ramach zakresu dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="f093a-125">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f093a-126">-Właściciel</span><span class="sxs-lookup"><span data-stu-id="f093a-126">-Owner</span></span>
<span data-ttu-id="f093a-127">Właściciel subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f093a-127">Subscription owner.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f093a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f093a-128">-ResourceId</span></span>
<span data-ttu-id="f093a-129">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f093a-129">The resource ID.</span></span>

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

### <span data-ttu-id="f093a-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="f093a-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="f093a-131">Typ Menedżera zasobów routingu.</span><span class="sxs-lookup"><span data-stu-id="f093a-131">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f093a-132">-State</span><span class="sxs-lookup"><span data-stu-id="f093a-132">-State</span></span>
<span data-ttu-id="f093a-133">Stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="f093a-133">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f093a-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f093a-134">-SubscriptionId</span></span>
<span data-ttu-id="f093a-135">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f093a-135">Subscription identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: Set
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f093a-136">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="f093a-136">-TenantId</span></span>
<span data-ttu-id="f093a-137">Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="f093a-137">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f093a-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f093a-138">-Confirm</span></span>
<span data-ttu-id="f093a-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f093a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f093a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f093a-140">-WhatIf</span></span>
<span data-ttu-id="f093a-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f093a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f093a-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f093a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f093a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f093a-143">CommonParameters</span></span>
<span data-ttu-id="f093a-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f093a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f093a-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f093a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f093a-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f093a-146">INPUTS</span></span>

## <span data-ttu-id="f093a-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f093a-147">OUTPUTS</span></span>

### <span data-ttu-id="f093a-148">Microsoft. AzureStack. Management. Subscriptions. admin. modele. Subscription</span><span class="sxs-lookup"><span data-stu-id="f093a-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="f093a-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f093a-149">NOTES</span></span>

## <span data-ttu-id="f093a-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f093a-150">RELATED LINKS</span></span>

