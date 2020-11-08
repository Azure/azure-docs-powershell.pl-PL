---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b08aed00a4c16bd2031608ff795a4dde8491859
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061541"
---
# <span data-ttu-id="794b6-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="794b6-101">Set-AzsOffer</span></span>

## <span data-ttu-id="794b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="794b6-102">SYNOPSIS</span></span>
<span data-ttu-id="794b6-103">Zaktualizuj ofertę.</span><span class="sxs-lookup"><span data-stu-id="794b6-103">Update the offer.</span></span>

## <span data-ttu-id="794b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="794b6-104">SYNTAX</span></span>

### <span data-ttu-id="794b6-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="794b6-105">Update (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-BasePlanIds <String[]>]
 [-Description <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-MaxSubscriptionsPerAccount <Int64>]
 [-AddonPlanDefinition <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="794b6-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="794b6-106">InputObject</span></span>
```
Set-AzsOffer [-ResourceGroupName <String>] -InputObject <Offer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="794b6-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="794b6-107">ResourceId</span></span>
```
Set-AzsOffer -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="794b6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="794b6-108">DESCRIPTION</span></span>
<span data-ttu-id="794b6-109">Zaktualizuj ofertę.</span><span class="sxs-lookup"><span data-stu-id="794b6-109">Update the offer.</span></span>

## <span data-ttu-id="794b6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="794b6-110">EXAMPLES</span></span>

### <span data-ttu-id="794b6-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="794b6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Private
```

<span data-ttu-id="794b6-112">Zaktualizuj ofertę.</span><span class="sxs-lookup"><span data-stu-id="794b6-112">Update the offer.</span></span>

## <span data-ttu-id="794b6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="794b6-113">PARAMETERS</span></span>

### <span data-ttu-id="794b6-114">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="794b6-114">-AddonPlanDefinition</span></span>
<span data-ttu-id="794b6-115">Odwołania do planów dodatków, które dzierżawa mogą opcjonalnie nabyć jako część oferty.</span><span class="sxs-lookup"><span data-stu-id="794b6-115">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

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

### <span data-ttu-id="794b6-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="794b6-116">-BasePlanIds</span></span>
<span data-ttu-id="794b6-117">Identyfikatory planów podstawowych, które są dostępne dla dzierżawy natychmiast po zasubskrybowaniu oferty przez dzierżawcę.</span><span class="sxs-lookup"><span data-stu-id="794b6-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

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

### <span data-ttu-id="794b6-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="794b6-118">-Description</span></span>
<span data-ttu-id="794b6-119">Opis oferty.</span><span class="sxs-lookup"><span data-stu-id="794b6-119">Description of offer.</span></span>

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

### <span data-ttu-id="794b6-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="794b6-120">-DisplayName</span></span>
<span data-ttu-id="794b6-121">Nazwa wyświetlana oferty.</span><span class="sxs-lookup"><span data-stu-id="794b6-121">Display name of offer.</span></span>

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

### <span data-ttu-id="794b6-122">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="794b6-122">-ExternalReferenceId</span></span>
<span data-ttu-id="794b6-123">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="794b6-123">External reference identifier.</span></span>

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

### <span data-ttu-id="794b6-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="794b6-124">-InputObject</span></span>
<span data-ttu-id="794b6-125">Obiekt wejściowy typu Microsoft. AzureStack. Management. Subscriptions. admin. models. offer.</span><span class="sxs-lookup"><span data-stu-id="794b6-125">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer.</span></span>

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

### <span data-ttu-id="794b6-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="794b6-126">-Location</span></span>
<span data-ttu-id="794b6-127">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="794b6-127">Location of the resource.</span></span>

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

### <span data-ttu-id="794b6-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="794b6-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="794b6-129">Maksymalna liczba abonamentów na konto.</span><span class="sxs-lookup"><span data-stu-id="794b6-129">Maximum subscriptions per account.</span></span>

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

### <span data-ttu-id="794b6-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="794b6-130">-Name</span></span>
<span data-ttu-id="794b6-131">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="794b6-131">Name of an offer.</span></span>

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

### <span data-ttu-id="794b6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="794b6-132">-ResourceGroupName</span></span>
<span data-ttu-id="794b6-133">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="794b6-133">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="794b6-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="794b6-134">-ResourceId</span></span>
<span data-ttu-id="794b6-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="794b6-135">The resource id.</span></span>

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

### <span data-ttu-id="794b6-136">-State</span><span class="sxs-lookup"><span data-stu-id="794b6-136">-State</span></span>
<span data-ttu-id="794b6-137">Stan ułatwień dostępu w ofercie.</span><span class="sxs-lookup"><span data-stu-id="794b6-137">Offer accessibility state.</span></span>

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

### <span data-ttu-id="794b6-138">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="794b6-138">-SubscriptionCount</span></span>
<span data-ttu-id="794b6-139">Bieżąca liczba abonamentów.</span><span class="sxs-lookup"><span data-stu-id="794b6-139">Current subscription count.</span></span>

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

### <span data-ttu-id="794b6-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="794b6-140">-Confirm</span></span>
<span data-ttu-id="794b6-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="794b6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="794b6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="794b6-142">-WhatIf</span></span>
<span data-ttu-id="794b6-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="794b6-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="794b6-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="794b6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="794b6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="794b6-145">CommonParameters</span></span>
<span data-ttu-id="794b6-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="794b6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="794b6-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="794b6-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="794b6-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="794b6-148">INPUTS</span></span>

## <span data-ttu-id="794b6-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="794b6-149">OUTPUTS</span></span>

### <span data-ttu-id="794b6-150">Microsoft. AzureStack. Management. Subscriptions. admin. models. Offer</span><span class="sxs-lookup"><span data-stu-id="794b6-150">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="794b6-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="794b6-151">NOTES</span></span>

## <span data-ttu-id="794b6-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="794b6-152">RELATED LINKS</span></span>

