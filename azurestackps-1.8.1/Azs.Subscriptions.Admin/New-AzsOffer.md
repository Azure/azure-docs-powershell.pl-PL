---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cce59bbbef69f10f39478d784d688a4f1de312fb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889565"
---
# <span data-ttu-id="a42db-101">New-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="a42db-101">New-AzsOffer</span></span>

## <span data-ttu-id="a42db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a42db-102">SYNOPSIS</span></span>
<span data-ttu-id="a42db-103">Tworzy nową ofertę.</span><span class="sxs-lookup"><span data-stu-id="a42db-103">Creates a new offer.</span></span>

## <span data-ttu-id="a42db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a42db-104">SYNTAX</span></span>

```
New-AzsOffer [-Name] <String> [-DisplayName] <String> [-ResourceGroupName] <String> [[-BasePlanIds] <String[]>]
 [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>] [[-Location] <String>]
 [[-MaxSubscriptionsPerAccount] <Int64>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a42db-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a42db-105">DESCRIPTION</span></span>
<span data-ttu-id="a42db-106">Utwórz lub zaktualizuj ofertę.</span><span class="sxs-lookup"><span data-stu-id="a42db-106">Create or update the offer.</span></span>

## <span data-ttu-id="a42db-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a42db-107">EXAMPLES</span></span>

### <span data-ttu-id="a42db-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a42db-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Public -DisplayName "offer1" -BasePlanIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1"
```

<span data-ttu-id="a42db-109">Tworzy nową ofertę.</span><span class="sxs-lookup"><span data-stu-id="a42db-109">Creates a new offer.</span></span>

## <span data-ttu-id="a42db-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a42db-110">PARAMETERS</span></span>

### <span data-ttu-id="a42db-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="a42db-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="a42db-112">Odwołania do planów dodatków, które dzierżawa mogą opcjonalnie nabyć jako część oferty.</span><span class="sxs-lookup"><span data-stu-id="a42db-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a42db-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="a42db-113">-BasePlanIds</span></span>
<span data-ttu-id="a42db-114">Identyfikatory planów podstawowych, które są dostępne dla dzierżawy natychmiast po zasubskrybowaniu oferty przez dzierżawcę.</span><span class="sxs-lookup"><span data-stu-id="a42db-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a42db-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="a42db-115">-Description</span></span>
<span data-ttu-id="a42db-116">Opis oferty.</span><span class="sxs-lookup"><span data-stu-id="a42db-116">Description of offer.</span></span>

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

### <span data-ttu-id="a42db-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a42db-117">-DisplayName</span></span>
<span data-ttu-id="a42db-118">Nazwa wyświetlana oferty.</span><span class="sxs-lookup"><span data-stu-id="a42db-118">Display name of offer.</span></span>

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

### <span data-ttu-id="a42db-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="a42db-119">-ExternalReferenceId</span></span>
<span data-ttu-id="a42db-120">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="a42db-120">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a42db-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a42db-121">-Location</span></span>
<span data-ttu-id="a42db-122">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="a42db-122">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a42db-123">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="a42db-123">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="a42db-124">Maksymalna liczba abonamentów na konto.</span><span class="sxs-lookup"><span data-stu-id="a42db-124">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a42db-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a42db-125">-Name</span></span>
<span data-ttu-id="a42db-126">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="a42db-126">Name of an offer.</span></span>

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

### <span data-ttu-id="a42db-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a42db-127">-ResourceGroupName</span></span>
<span data-ttu-id="a42db-128">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="a42db-128">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="a42db-129">-State</span><span class="sxs-lookup"><span data-stu-id="a42db-129">-State</span></span>
<span data-ttu-id="a42db-130">Stan ułatwień dostępu w ofercie.</span><span class="sxs-lookup"><span data-stu-id="a42db-130">Offer accessibility state.</span></span>
<span data-ttu-id="a42db-131">Wartość domyślna to Private.</span><span class="sxs-lookup"><span data-stu-id="a42db-131">Default value is Private.</span></span>
<span data-ttu-id="a42db-132">Ten parametr będzie przestarzały w przyszłej wersji</span><span class="sxs-lookup"><span data-stu-id="a42db-132">This parameter will be deprecated in a future release</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: Private
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a42db-133">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="a42db-133">-SubscriptionCount</span></span>
<span data-ttu-id="a42db-134">Bieżąca liczba abonamentów.</span><span class="sxs-lookup"><span data-stu-id="a42db-134">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a42db-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a42db-135">-Confirm</span></span>
<span data-ttu-id="a42db-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a42db-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a42db-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a42db-137">-WhatIf</span></span>
<span data-ttu-id="a42db-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a42db-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a42db-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a42db-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a42db-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a42db-140">CommonParameters</span></span>
<span data-ttu-id="a42db-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a42db-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a42db-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a42db-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a42db-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a42db-143">INPUTS</span></span>

## <span data-ttu-id="a42db-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a42db-144">OUTPUTS</span></span>

### <span data-ttu-id="a42db-145">Microsoft. AzureStack. Management. Subscriptions. admin. models. Offer</span><span class="sxs-lookup"><span data-stu-id="a42db-145">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="a42db-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a42db-146">NOTES</span></span>

## <span data-ttu-id="a42db-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a42db-147">RELATED LINKS</span></span>

