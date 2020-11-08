---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsoffer
schema: 2.0.0
ms.openlocfilehash: 10fbcaf6a8286bf0d7bdeb801ff8797418c91f0f
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/22/2020
ms.locfileid: "94054055"
---
# <span data-ttu-id="2a34f-101">New-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="2a34f-101">New-AzsOffer</span></span>

## <span data-ttu-id="2a34f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a34f-102">SYNOPSIS</span></span>
<span data-ttu-id="2a34f-103">Utwórz lub zaktualizuj ofertę.</span><span class="sxs-lookup"><span data-stu-id="2a34f-103">Create or update the offer.</span></span>

## <span data-ttu-id="2a34f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a34f-104">SYNTAX</span></span>

### <span data-ttu-id="2a34f-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="2a34f-105">CreateExpanded (Default)</span></span>
```
New-AzsOffer -Name <String> -ResourceGroupName <String> -BasePlanIds <String[]> [-SubscriptionId <String>]
 [-AddonPlanDefinition <IAddonPlanDefinition[]>] [-Description <String>] [-DisplayName <String>]
 [-ExternalReferenceId <String>] [-Location <String>] [-MaxSubscriptionsPerAccount <Int32>]
 [-PropertiesName <String>] [-State <AccessibilityState>] [-SubscriptionCount <Int32>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2a34f-106">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="2a34f-106">Create</span></span>
```
New-AzsOffer -OfferDefinition <IOffer> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2a34f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2a34f-107">DESCRIPTION</span></span>
<span data-ttu-id="2a34f-108">Utwórz lub zaktualizuj ofertę.</span><span class="sxs-lookup"><span data-stu-id="2a34f-108">Create or update the offer.</span></span>

## <span data-ttu-id="2a34f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a34f-109">EXAMPLES</span></span>

### <span data-ttu-id="2a34f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2a34f-110">Example 1</span></span>
```powershell
PS C:\> New-AzsOffer -Name "testoffer" -ResourceGroupName "testrg" -BasePlanIds "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan"

AddonPlans                 : {}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan}
Description                : 
DisplayName                : testoffer
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer
Location                   : redmond
MaxSubscriptionsPerAccount : 0
Name                       : testoffer
PropertiesName             : testoffer
State                      : Private
SubscriptionCount          : 0
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="2a34f-111">Tworzy nową ofertę.</span><span class="sxs-lookup"><span data-stu-id="2a34f-111">Creates a new offer.</span></span>

## <span data-ttu-id="2a34f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a34f-112">PARAMETERS</span></span>

### <span data-ttu-id="2a34f-113">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="2a34f-113">-AddonPlanDefinition</span></span>
<span data-ttu-id="2a34f-114">Odwołania do planów dodatków, które dzierżawa mogą opcjonalnie nabyć jako część oferty.</span><span class="sxs-lookup"><span data-stu-id="2a34f-114">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
<span data-ttu-id="2a34f-115">Aby skonstruować, zobacz sekcję notatki dla właściwości ADDONPLANDEFINITION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="2a34f-115">To construct, see NOTES section for ADDONPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IAddonPlanDefinition[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="2a34f-116">-BasePlanIds</span></span>
<span data-ttu-id="2a34f-117">Identyfikatory planów podstawowych, które są dostępne dla dzierżawy natychmiast po zasubskrybowaniu oferty przez dzierżawcę.</span><span class="sxs-lookup"><span data-stu-id="2a34f-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a34f-118">-DefaultProfile</span></span>
<span data-ttu-id="2a34f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a34f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="2a34f-120">-Description</span></span>
<span data-ttu-id="2a34f-121">Opis oferty.</span><span class="sxs-lookup"><span data-stu-id="2a34f-121">Description of offer.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2a34f-122">-DisplayName</span></span>
<span data-ttu-id="2a34f-123">Nazwa wyświetlana oferty.</span><span class="sxs-lookup"><span data-stu-id="2a34f-123">Display name of offer.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-124">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="2a34f-124">-ExternalReferenceId</span></span>
<span data-ttu-id="2a34f-125">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="2a34f-125">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2a34f-126">-Location</span></span>
<span data-ttu-id="2a34f-127">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="2a34f-127">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="2a34f-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="2a34f-129">Maksymalna liczba abonamentów na konto.</span><span class="sxs-lookup"><span data-stu-id="2a34f-129">Maximum subscriptions per account.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a34f-130">-Name</span></span>
<span data-ttu-id="2a34f-131">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="2a34f-131">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-132">-OfferDefinition</span><span class="sxs-lookup"><span data-stu-id="2a34f-132">-OfferDefinition</span></span>
<span data-ttu-id="2a34f-133">Przedstawia oferowanie usług, za które można utworzyć abonament.</span><span class="sxs-lookup"><span data-stu-id="2a34f-133">Represents an offering of services against which a subscription can be created.</span></span>
<span data-ttu-id="2a34f-134">Aby skonstruować, zobacz sekcję notatki dla właściwości OFFERDEFINITION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="2a34f-134">To construct, see NOTES section for OFFERDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-135">-Propertiesname</span><span class="sxs-lookup"><span data-stu-id="2a34f-135">-PropertiesName</span></span>
<span data-ttu-id="2a34f-136">Imię i nazwisko oferty.</span><span class="sxs-lookup"><span data-stu-id="2a34f-136">Name of the Offer.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a34f-137">-ResourceGroupName</span></span>
<span data-ttu-id="2a34f-138">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="2a34f-138">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-139">-State</span><span class="sxs-lookup"><span data-stu-id="2a34f-139">-State</span></span>
<span data-ttu-id="2a34f-140">Stan ułatwień dostępu w ofercie.</span><span class="sxs-lookup"><span data-stu-id="2a34f-140">Offer accessibility state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.AccessibilityState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Private"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-141">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="2a34f-141">-SubscriptionCount</span></span>
<span data-ttu-id="2a34f-142">Bieżąca liczba abonamentów.</span><span class="sxs-lookup"><span data-stu-id="2a34f-142">Current subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-143">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2a34f-143">-SubscriptionId</span></span>
<span data-ttu-id="2a34f-144">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="2a34f-144">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a34f-145">-Confirm</span></span>
<span data-ttu-id="2a34f-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a34f-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a34f-147">-WhatIf</span></span>
<span data-ttu-id="2a34f-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a34f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a34f-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a34f-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2a34f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a34f-150">CommonParameters</span></span>
<span data-ttu-id="2a34f-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a34f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a34f-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a34f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a34f-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a34f-153">INPUTS</span></span>

### <span data-ttu-id="2a34f-154">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="2a34f-154">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

## <span data-ttu-id="2a34f-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a34f-155">OUTPUTS</span></span>

### <span data-ttu-id="2a34f-156">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="2a34f-156">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="2a34f-157">PISUJE</span><span class="sxs-lookup"><span data-stu-id="2a34f-157">ALIASES</span></span>

## <span data-ttu-id="2a34f-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a34f-158">NOTES</span></span>

<span data-ttu-id="2a34f-159">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2a34f-159">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2a34f-160">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2a34f-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2a34f-161">ADDONPLANDEFINITION <IAddonPlanDefinition [] >: odwołania do planów dodatków, które dzierżawa mogą opcjonalnie nabyć jako część oferty.</span><span class="sxs-lookup"><span data-stu-id="2a34f-161">ADDONPLANDEFINITION <IAddonPlanDefinition[]>: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
  - <span data-ttu-id="2a34f-162">`[MaxAcquisitionCount <Int32?>]`: Maksymalna liczba wystąpień, które można nabyć w ramach pojedynczego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="2a34f-162">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="2a34f-163">Jeśli argument nie zostanie określony, przyjmowana jest wartość 1.</span><span class="sxs-lookup"><span data-stu-id="2a34f-163">If not specified, the assumed value is 1.</span></span>
  - <span data-ttu-id="2a34f-164">`[PlanId <String>]`: Identyfikator planu.</span><span class="sxs-lookup"><span data-stu-id="2a34f-164">`[PlanId <String>]`: Plan identifier.</span></span>

<span data-ttu-id="2a34f-165">OFFERDEFINITION <IOffer> : przedstawia oferowanie usług, za które można utworzyć abonament.</span><span class="sxs-lookup"><span data-stu-id="2a34f-165">OFFERDEFINITION <IOffer>: Represents an offering of services against which a subscription can be created.</span></span>
  - <span data-ttu-id="2a34f-166">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="2a34f-166">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="2a34f-167">`[AddonPlans <IAddonPlanDefinition[]>]`: Odwołania do planów dodatków, które dzierżawa mogą opcjonalnie nabyć jako część oferty.</span><span class="sxs-lookup"><span data-stu-id="2a34f-167">`[AddonPlans <IAddonPlanDefinition[]>]`: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
    - <span data-ttu-id="2a34f-168">`[MaxAcquisitionCount <Int32?>]`: Maksymalna liczba wystąpień, które można nabyć w ramach pojedynczego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="2a34f-168">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="2a34f-169">Jeśli argument nie zostanie określony, przyjmowana jest wartość 1.</span><span class="sxs-lookup"><span data-stu-id="2a34f-169">If not specified, the assumed value is 1.</span></span>
    - <span data-ttu-id="2a34f-170">`[PlanId <String>]`: Identyfikator planu.</span><span class="sxs-lookup"><span data-stu-id="2a34f-170">`[PlanId <String>]`: Plan identifier.</span></span>
  - <span data-ttu-id="2a34f-171">`[BasePlanIds <String[]>]`: Identyfikatory planów podstawowych, które są dostępne dla dzierżawy natychmiast po zasubskrybowaniu oferty przez dzierżawcę.</span><span class="sxs-lookup"><span data-stu-id="2a34f-171">`[BasePlanIds <String[]>]`: Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>
  - <span data-ttu-id="2a34f-172">`[Description <String>]`: Opis oferty.</span><span class="sxs-lookup"><span data-stu-id="2a34f-172">`[Description <String>]`: Description of offer.</span></span>
  - <span data-ttu-id="2a34f-173">`[DisplayName <String>]`: Wyświetlana nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="2a34f-173">`[DisplayName <String>]`: Display name of offer.</span></span>
  - <span data-ttu-id="2a34f-174">`[ExternalReferenceId <String>]`: Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="2a34f-174">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="2a34f-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Maksymalna liczba abonamentów na konto.</span><span class="sxs-lookup"><span data-stu-id="2a34f-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Maximum subscriptions per account.</span></span>
  - <span data-ttu-id="2a34f-176">`[PropertiesName <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="2a34f-176">`[PropertiesName <String>]`: Name of the Offer.</span></span>
  - <span data-ttu-id="2a34f-177">`[State <AccessibilityState?>]`: Stan ułatwień dostępu oferowanie.</span><span class="sxs-lookup"><span data-stu-id="2a34f-177">`[State <AccessibilityState?>]`: Offer accessibility state.</span></span>
  - <span data-ttu-id="2a34f-178">`[SubscriptionCount <Int32?>]`: Liczba bieżących abonamentów.</span><span class="sxs-lookup"><span data-stu-id="2a34f-178">`[SubscriptionCount <Int32?>]`: Current subscription count.</span></span>

## <span data-ttu-id="2a34f-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a34f-179">RELATED LINKS</span></span>

