---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b08aed00a4c16bd2031608ff795a4dde8491859
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889205"
---
# <span data-ttu-id="0ebb5-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="0ebb5-101">Set-AzsOffer</span></span>

## <span data-ttu-id="0ebb5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ebb5-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebb5-103">Zaktualizuj ofertę.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-103">Update the offer.</span></span>

## <span data-ttu-id="0ebb5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ebb5-104">SYNTAX</span></span>

### <span data-ttu-id="0ebb5-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0ebb5-105">Update (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-BasePlanIds <String[]>]
 [-Description <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-MaxSubscriptionsPerAccount <Int64>]
 [-AddonPlanDefinition <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ebb5-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="0ebb5-106">InputObject</span></span>
```
Set-AzsOffer [-ResourceGroupName <String>] -InputObject <Offer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ebb5-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="0ebb5-107">ResourceId</span></span>
```
Set-AzsOffer -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ebb5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0ebb5-108">DESCRIPTION</span></span>
<span data-ttu-id="0ebb5-109">Zaktualizuj ofertę.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-109">Update the offer.</span></span>

## <span data-ttu-id="0ebb5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ebb5-110">EXAMPLES</span></span>

### <span data-ttu-id="0ebb5-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0ebb5-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Private
```

<span data-ttu-id="0ebb5-112">Zaktualizuj ofertę.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-112">Update the offer.</span></span>

## <span data-ttu-id="0ebb5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ebb5-113">PARAMETERS</span></span>

### <span data-ttu-id="0ebb5-114">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="0ebb5-114">-AddonPlanDefinition</span></span>
<span data-ttu-id="0ebb5-115">Odwołania do planów dodatków, które dzierżawa mogą opcjonalnie nabyć jako część oferty.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-115">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebb5-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="0ebb5-116">-BasePlanIds</span></span>
<span data-ttu-id="0ebb5-117">Identyfikatory planów podstawowych, które są dostępne dla dzierżawy natychmiast po zasubskrybowaniu oferty przez dzierżawcę.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebb5-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="0ebb5-118">-Description</span></span>
<span data-ttu-id="0ebb5-119">Opis oferty.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-119">Description of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebb5-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0ebb5-120">-DisplayName</span></span>
<span data-ttu-id="0ebb5-121">Nazwa wyświetlana oferty.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-121">Display name of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebb5-122">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="0ebb5-122">-ExternalReferenceId</span></span>
<span data-ttu-id="0ebb5-123">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-123">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebb5-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0ebb5-124">-InputObject</span></span>
<span data-ttu-id="0ebb5-125">Obiekt wejściowy typu Microsoft. AzureStack. Management. Subscriptions. admin. models. offer.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-125">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer.</span></span>

```yaml
Type: Offer
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ebb5-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0ebb5-126">-Location</span></span>
<span data-ttu-id="0ebb5-127">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-127">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebb5-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="0ebb5-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="0ebb5-129">Maksymalna liczba abonamentów na konto.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-129">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebb5-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0ebb5-130">-Name</span></span>
<span data-ttu-id="0ebb5-131">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-131">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebb5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ebb5-132">-ResourceGroupName</span></span>
<span data-ttu-id="0ebb5-133">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-133">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebb5-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ebb5-134">-ResourceId</span></span>
<span data-ttu-id="0ebb5-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ebb5-136">-State</span><span class="sxs-lookup"><span data-stu-id="0ebb5-136">-State</span></span>
<span data-ttu-id="0ebb5-137">Stan ułatwień dostępu w ofercie.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-137">Offer accessibility state.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebb5-138">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="0ebb5-138">-SubscriptionCount</span></span>
<span data-ttu-id="0ebb5-139">Bieżąca liczba abonamentów.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-139">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebb5-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0ebb5-140">-Confirm</span></span>
<span data-ttu-id="0ebb5-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ebb5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ebb5-142">-WhatIf</span></span>
<span data-ttu-id="0ebb5-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ebb5-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ebb5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebb5-145">CommonParameters</span></span>
<span data-ttu-id="0ebb5-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebb5-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ebb5-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebb5-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ebb5-148">INPUTS</span></span>

## <span data-ttu-id="0ebb5-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ebb5-149">OUTPUTS</span></span>

### <span data-ttu-id="0ebb5-150">Microsoft. AzureStack. Management. Subscriptions. admin. models. Offer</span><span class="sxs-lookup"><span data-stu-id="0ebb5-150">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="0ebb5-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ebb5-151">NOTES</span></span>

## <span data-ttu-id="0ebb5-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ebb5-152">RELATED LINKS</span></span>

